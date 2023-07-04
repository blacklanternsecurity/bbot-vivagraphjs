# BBOT Graph Visualization ([VivaGraphJS](https://github.com/anvaka/VivaGraphJS))

<video controls="" autoplay="" name="media"><source src="https://github-production-user-asset-6210df.s3.amazonaws.com/20261699/245941416-ebf2a81e-7530-4a9e-922d-4e62eb949f35.mp4" type="video/mp4"></video>

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
