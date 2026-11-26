# cam-voice-assistant

[English](#user-content-english) · [Polski](#user-content-polski)

<details name="readme-language">
<summary aria-label="Pokaż lub ukryj polską wersję README"></summary>

<a id="polski"></a>Asystent głosowy i wizyjny AI dla kamer Reolink w czasie rzeczywistym. Nasłuchuje przez mikrofon kamery, obserwuje strumień wideo i odpowiada przez głośnik kamery.

**Status:** prace w toku – etap 1 z 5. Brak powiązań z Reolink.

## Plan rozwoju

- [ ] v0.1.0 – odbiór dźwięku i obrazu z kamery na serwerze
- [ ] v0.2.0 – mówienie przez głośnik kamery
- [ ] v0.3.0 – rozmowa z AI w czasie rzeczywistym (Gemini Live)
- [ ] v0.4.0 – połączenie kamery z AI, słowo wybudzające, narzędzia
- [ ] v1.0.0 – wdrożenie w Dockerze do pracy całodobowej i dokumentacja

## Testowany sprzęt

| Kamera            | Oprogramowanie układowe | Tor audio do głośnika | Uwagi |
| ----------------- | ----------------------- | --------------------- | ----- |
| Reolink RP-PCT12M |                         | jeszcze nietestowany  |       |

## Licencja

MIT

</details>

<details open name="readme-language">
<summary aria-label="Show or hide the English README"></summary>

<a id="english"></a>Real-time voice & vision AI assistant for Reolink cameras. It listens through the
camera's microphone, looks at the video stream and answers through the camera's speaker.

**Status:** work in progress – stage 1 of 5. Not affiliated with Reolink.

## Roadmap

- [ ] v0.1.0 – audio and video from the camera on the server
- [ ] v0.2.0 – speaking through the camera speaker
- [ ] v0.3.0 – real-time AI conversation (Gemini Live)
- [ ] v0.4.0 – camera ↔ AI bridge, wake word, tools
- [ ] v1.0.0 – 24/7 Docker deployment and documentation

## Tested hardware

| Camera            | Firmware               | Speaker path   | Notes           |
| ----------------- | ---------------------- | -------------- | --------------- |
| Reolink RP-PCT12M | v3.2.0.4954_2509019551 | not tested yet | sub: h264 + aac |

## License

MIT

</details>
