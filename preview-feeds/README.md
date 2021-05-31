Preview Feeds
=============

GStreamer command and systemd service to capture and stream the OBS Multiview window for remote
monitoring. Assumes that you are using [Jack](https://jackaudio.org/) for audio.

Useful in conjunction with [Janus Web RTC server](https://janus.conf.meetecho.com/)

If using Janus, add this configuration to `/etc/janus/janus.plugin.streaming.jcfg`:

```
obs-multiview: {
        type = "rtp"
        id = 1
        description = "OBS multiview"
        audio = true
        video = true
        audioport = 5002
        audiopt = 111
        audiortpmap = "opus/48000/2"
        videoport = 5004
        videopt = 100
        videortpmap = "VP8/90000"
        secret = "adminpwd"
}
```
