# mitmproxy alternate-server-replay

Basic useful feature list:

 * Unmatched requests return a 404 instead of killing the connection
 * When the request path matches, we use best-match fitting of the params/form for better replay

## Usage

Make a recording as normal:

    mitmdump -w ~/record-server-responses.md --socks

To serve a replay:

    mitmdump -s "~/mitmdump-alternate-server-replay/alternate-server-replay.py ~/record-server-responses.md" --socks
