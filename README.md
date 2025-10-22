# Bytedesk Conference

A simple, secure, and self-hostable video conferencing experience for teams and communities — built on top of the battle‑tested Jitsi platform.

## Overview

Bytedesk Conference provides modern, browser‑based meetings with crystal‑clear audio/video, screen sharing, and collaboration features. It integrates with the Bytedesk server for user accounts, authentication, roles/permissions, and room policies, while Jitsi powers the real‑time media layer. For production, deploy with a self‑hosted Jitsi deployment for full control and privacy.

## Key features

- Browser‑based meetings with no installs required
- HD audio/video with adaptive quality
- Screen sharing (full screen, window, or tab)
- In‑meeting chat, reactions, and hand‑raise
- Lobby, password‑protected rooms, and moderation tools
- Optional recording and live streaming via Jibri/RTMP
- Breakout rooms and participant management
- Works across desktop and mobile browsers

## Use cases

- Daily standups, sprint reviews, and team syncs
- Customer demos, interviews, and training sessions
- Community meetups and webinars

## Deployment and usage (at a glance)

Production‑ready setup relies on two parts:

1) Self‑hosted Jitsi for media:
	- Deploy your own Jitsi stack (Prosody, Jicofo, JVB, optional Jibri) following the official guide: https://jitsi.github.io/handbook/docs/devops-guide/devops-guide-quickstart
	- Configure domain, certificates, TURN/ICE, and recording/streaming as needed.

2) Bytedesk server for application logic:
	- Use the Bytedesk server for user accounts, authentication, roles/permissions, and room policy: https://github.com/Bytedesk/bytedesk
	- Point Bytedesk Conference to your Bytedesk API endpoint and your Jitsi server URL; align auth and room settings accordingly.

Note: This repository focuses on product documentation. Application code and full configuration examples may exist in related repositories or be added in future iterations.

## Privacy and security

- End‑to‑end approach using Jitsi’s secure architecture (DTLS‑SRTP, Prosody‑backed signaling)
- Room passwords, lobby/waiting room, and host moderation controls
- Self‑hosting keeps your media and metadata under your control

For Jitsi’s full security model, see: https://jitsi.org/security/

## Browser and device support

- Latest Chrome, Edge, and Firefox on desktop
- Safari on recent macOS/iOS versions
- Modern Android browsers

Actual compatibility depends on your specific Jitsi deployment and network conditions.

## Contributing

Contributions are welcome! Please propose ideas, file issues, or open pull requests to improve documentation and user experience.

## License

See the `LICENSE` file in this repository for licensing details.

## Roadmap

- Configuration samples for common deployments
- Theming/branding hooks and templates
- Admin/analytics guidance for self‑hosted setups

## Acknowledgements

Built on Jitsi: https://jitsi.org/
