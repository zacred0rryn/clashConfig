# DEPRECATED
This Clash-related repo is no longer maintained since I've switched to [SagerNet/sing-box](https://github.com/SagerNet/sing-box).

---

## ~How to use~
* ~Clone this repo~
* ~Paste clash subscription link in `config.yml`~
* ~Check if the `Proxy Providers` and `Proxy Groups` are compatible with the proxies in the subscription~
  * ~If not, annotate the unnecessary part or unannotate the useful part~
* ~Import the config file in CFW~

## ~Mixin~
* ~Use mixin to activate TUN mode since the DNS settings are written in `config.yml`~
* ~Mixin config is as follow:~
<details>

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
        auto-detect-interface: true # conflict with `interface-name`
# interface-name: eth0 # conflict with `tun.auto-detect-interface`
```

</details>
