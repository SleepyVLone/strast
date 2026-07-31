# Strast

Strast is an open source screen streaming app for macOS and iPadOS. It lets a Mac extend its screen to multiple devices at once, over WiFi, wired networking, or whatever transport makes sense, without relying on Apple's built in AirPlay or Sidecar.

## Why

AirPlay screen mirroring between Macs is capped to a fixed set of 16:9 and 4:3 resolutions, which means it never matches a real Mac display's actual aspect ratio and always leaves black bars. On top of that, Sidecar (Mac to iPad) and AirPlay to Mac share the same underlying system and can't run at the same time, so extending to more than one secondary screen at once isn't possible with Apple's own tools.

Strast is a custom app built to get around both of those limits at once.

## Status

Early concept stage. No working code yet. This repo currently exists to hold the plan while the first version gets built.

## Planned v1

The first version is deliberately scoped small:

- Capture and encode the screen on the sending Mac using ScreenCaptureKit and VideoToolbox
- Stream it over WiFi to native receiver apps on a second Mac and an iPad
- Each receiver decodes and renders the stream fullscreen at its own native resolution, so there's no letterboxing
- Mirror only for v1. No independent per device content and no input passthrough yet
- Wired transport (USB-C or Thunderbolt as a plain network link) planned as an easy follow up once WiFi works

Later milestones, not part of v1, include true independent extended displays per device and full interactive input passthrough so it behaves like a real extended desktop rather than a read only stream.

## Licence

Not finalised yet. Leaning towards MIT.
