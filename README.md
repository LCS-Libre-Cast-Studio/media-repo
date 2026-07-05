# Libre Cast Studio (LCS) — Media Storage Backend

This repository serves as the decentralized, open-source media storage backend and central registry for the Libre Cast Studio (LCS) streaming ecosystem. It utilizes GitHub infrastructure paired with Cloudflare edge caching to deliver high-performance, low-latency audio and video streams without commercial dependencies.

## Architecture Overview

* **`/audio`**: Contains all community-contributed audio files (.mp3, .wav, .flac).
* **`/video`**: Contains all community-contributed video files (.mp4, .mkv, .webm).
* **`playlist.json`**: The central index and single source of truth (SSOT) database read by the LCS Client Applications.

## The `playlist.json` Schema

Every media asset must be registered within the root `playlist.json` array using the following specification:

```json
[
  {
    "title": "Asset Title",
    "artist": "Content Creator Name",
    "type": "audio" | "video",
    "url": "https://media.alexgaming.dev/[audio|video]/filename.ext"
  }
]
```

## Contribution Guidelines

We welcome community contributions. To add your media to the network, follow the strict Git workflow:

1. **Fork** this repository.
2. Upload your media file to the appropriate directory (`/audio` or `/video`). Ensure names are lowercase and contain no spaces (use hyphens).
3. Append your metadata object to the end of the array in `playlist.json`.
4. Open a **Pull Request (PR)**. 

*Note: All uploaded content must comply with the licensing terms specified below. Copyrighted or illegal material will be rejected immediately.*

## Licensing

* **Code and Schema Configuration**: Licensed under the [MIT License](LICENSE).
* **Media Assets**: All community-submitted media content hosted within this repository must be licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org) or marked as Public Domain (CC0). By submitting a Pull Request, you certify that you own the rights to the content or have the legal authority to distribute it under these terms.
