# Third-party notices — NovaCore v1.0.4-RC2.14

NovaCore by **WetOttersPocket** 🦦. Thanks to the upstream developers and service providers below. Third-party components retain their own licences; NovaCore does not claim ownership of them.

| Component | Licence / credit |
|---|---|
| FFmpeg 7.1.5 | LGPL v3; statically linked. The package includes the licence, Nova patch and source notes under `Media/licenses/FFmpeg`. |
| Switchfin PS4 H.264 decoder patch | From the [Switchfin](https://github.com/dragonflylee/switchfin) project, Apache-2.0. The current player attempts hardware decoding with software fallback; actual playback remains under test. |
| QuickJS-ng 0.18 | MIT. |
| Nayuki QR Code generator | MIT. |
| minimp3 | CC0. |
| mbedTLS | Apache-2.0. |
| stb_image_write | Public domain. |
| Radio catalogue | radio-browser.info. Stations, logos and streams belong to their respective owners. |
| Country flags | flagcdn.com; identified as public-domain flag artwork in the release handoff. |
| Weather | [Open-Meteo](https://open-meteo.com), CC BY 4.0. |
| Approximate weather location | ipwho.is / ipapi.co. No account is needed; users can override the place or switch weather off. |

Store attribution: the PS4 Homebrew Store and its applications belong to their developers. FPKGi-compatible catalogues remain third-party data. The Di Play store belongs to the Di Play team. Availability of a catalogue does not grant redistribution rights for the packages it lists.

These notices are not a licence for NovaCore's private application source, nor a claim of ownership of media, station artwork, game art or third-party services. The bundled licence/source material and applicable upstream terms continue to apply.
Phone notification server: [web-push](https://github.com/web-push-libs/web-push), MIT; browsers use their own push service. IPTV channel metadata/logos belong to the relevant providers.

## orbisRPC

Optional payload/setup by [SirHumza, CyberMask367 and contributors](https://github.com/SirHumza/orbisRPC). The original logo is credited in the RPC guide and in-app Help; it is not Nova artwork. Upstream has no settled project licence; its work is not relicensed here. Nova account linking and orbisRPC account-session authentication are separate.

RC2.14 rebuilds FFmpeg7.1.5 with its software HEVC decoder, preserving LGPLv3-or-later build settings and the existing H264/TLS patches. No libx265 encoder is linked into Nova. Build notes and licences are packaged under Media/licenses/FFmpeg/RC214-HEVC. Official optional orbisRPC 1.1 ELF and Setup PKG are hash-pinned; no credential is included.
