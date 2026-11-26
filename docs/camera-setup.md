# Camera setup (Reolink RP-PCT12M)

Firmware tested: v3.2.0.4954_2509019551

1. Update the firmware (Reolink app or client).
2. Enable RTSP (554), ONVIF (8000) and HTTP in the network/port settings.
3. Add a dedicated user `ai_bot`; avoid `@ : / # ?` in the password.
4. Enable audio recording and set the speaker volume.
5. Sub stream: H.264, 10 fps.

## Check from the server

```bash
read -rsp "Camera password: " CAM_PASS; echo
ffprobe -v error -rtsp_transport tcp \
  -show_entries stream=codec_type,codec_name,width,height,sample_rate,channels -of compact \
  "rtsp://ai_bot:${CAM_PASS}@192.168.1.50:554/h264Preview_01_sub"
```
