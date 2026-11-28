# Camera setup (Reolink RP-PCT12M)

Firmware tested: v3.2.0

1. Update the firmware (Reolink app or client).
2. Enable RTSP (554), ONVIF (8000) and HTTP in the network/port settings.
3. Add a dedicated user `ai_bot`; avoid `@ : / # ?` in the password, or use the default (admin) - in my case. Special chars you can replace with corresponding codes (such as %24, %25).
4. Enable audio recording and set the speaker volume.
5. Sub stream: H.264, 10 fps.

## Check from the server

```bash
read -rsp "Camera password: " CAM_PASS; echo
ffprobe -v error -rtsp_transport tcp \
  -show_entries stream=codec_type,codec_name,width,height,sample_rate,channels -of compact \
  "rtsp://admin:${CAM_PASS}@192.168.50.23:554/h264Preview_01_sub"
```

The result has 2 lines:
stream|codec_name=h264|codec_type=video|width=896|height=512
stream|codec_name=aac|codec_type=audio|sample_rate=16000|channels=1
