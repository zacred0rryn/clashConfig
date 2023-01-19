## How to use
* Clone this repo
* Paste clash subscription link at column 200 in `config.yml`
* Check if the `Proxy Providers` and `Proxy Groups` are compatible with the proxies in the subscription
  * If not, annotate the unnecessary part or unannotate the useful part
* Import the config file in CFW

## Mixin
* Use mixin to activate TUN mode since the DNS settings are written in `config.yml`
* Mixin config is as follow: 
```yml
mixin:
  tun: 
    enable: true
    stack: system
    dns-hijack:
      - udp://any:53
      - tcp://any:53
    auto-redir: true
    auto-route: true
    auto-detect-interface: true
```
