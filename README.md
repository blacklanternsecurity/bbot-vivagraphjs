# BBOT Graph Visualization (VivaGraphJS)

![bbot_graph6](https://user-images.githubusercontent.com/20261699/225952607-ddae05fa-f4c9-46ba-90b3-60467b0735a6.gif)

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
