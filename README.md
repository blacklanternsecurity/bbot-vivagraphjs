# BBOT Graph Visualization (VivaGraphJS)

## Setup

- Spin up a websocat listener (allows connections between two clients)
~~~bash
websocat -v -E -t ws-l:127.0.0.1:1234 broadcast:mirror:
~~~
- Open `visualize.html` in a web browser
- Execute bbot with the `websocket` output module:
~~~bash
bbot -t tesla.com microsoft.com disney.com -om websocket -c scope_dns_search_distance=10 scope_report_distance=10 output_modules.websocket.url=ws://127.0.0.1:1234
~~~
