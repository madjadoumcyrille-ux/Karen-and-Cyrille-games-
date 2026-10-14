# Cyrille Boxing Arena 3D

Mobile-first 3D boxing game prototype by **M. Cyrille** (CST de Sarh).

## Features
- 3D boxing ring and stylized boxer models
- Solo vs AI mode, round timer, health bars and KO result
- Touch controls: move, jab, hook, guard and dodge
- Experimental private-room mode using PeerJS/WebRTC
- PWA manifest and service worker for installation/offline shell

## Run locally
Serve this folder over HTTPS or localhost (do not open `index.html` as a `file://` URL). Three.js and PeerJS are loaded from public CDNs, so first load requires internet.

## Publish with GitHub Pages
In the repository, open **Settings → Pages** and select **Deploy from a branch**, branch `main`, folder `/ (root)`, then Save. The site will be served at `https://madjadoumcyrille-ux.github.io/Karen-and-Cyrille-games-/` after Pages finishes publishing.

## Important status
This is an early playable prototype, not a finished commercial game. The online room feature uses PeerJS's public signaling service and direct peer-to-peer connections; network restrictions/NAT can prevent connections, and multiplayer synchronization has not been load-tested. Do not represent it as production-ready or guaranteed realtime multiplayer. The game has not been packaged for the Google Play Store.
