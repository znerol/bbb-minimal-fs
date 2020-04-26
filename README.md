Minimal FreeSWITCH config for BigBlueButton
===========================================

*Objective:*

Provide a working config for FreeSWITCH enough to run BigBlueButton WebRTC. Old
red5/flash client is not supported.

*Method:*

* Start with [minimal upstream][1] config
* Remove superflous modules
* Cherry-Pick useful stuff from BBB FreeSWITCH config

When running ustream FreeSWITCH on debian buster, the following packages are needed:

```
apt-get install \
    freeswitch-meta-default \
    freeswitch-mod-event-socket \
    freeswitch-mod-opus \
    freeswitch-sounds-en-us-callie \
    freeswitch-timezones
```

Note that recording is **only** supported when using the custom built
FreeSWITCH shipping with bbb. In this case it is necessary to also load
`mod_opusfile`.

*Stability:*

This is a small research project. Please do not file support requests.

*License:*

The config has been copied from various sources. FreeSWITCH is Licensed under
MPL 1.1 and BigBlueButton under LGPL.

[1]: https://github.com/signalwire/freeswitch/tree/master/conf/minimal
