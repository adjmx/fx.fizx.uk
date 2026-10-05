# fx.fizx.uk

> Live Bitcoin exchange rates + satoshi converter.

**Live**: <https://fx.fizx.uk>

## Stack

- [Vite](https://vitejs.dev/) + React 18 + TypeScript
- Tailwind CSS
- [nostr-tools](https://github.com/nbd-wtf/nostr-tools)
- lucide-react

## Nostr

- **Login**: NIP-07 (browser extension) + NIP-55 (Amber callback URI)
_No Nostr events published by this site._

No Nostr writes. NIP-11 probe for GRASP badge (reads `supported_nips` from `wss://git.upleb.uk`).

## Develop

```bash
npm install
npm run dev
```

## Build + deploy

```bash
./deploy.sh
```

Builds, then rsyncs `dist/` to the webroot. The script names the server by an
SSH host alias (`fizx.uk` in `~/.ssh/config`), which carries the user, port and
key.

Server addresses and the nginx / SSL / DNS notes for the wider deployment live in the local `code_gh/adjmx/CLAUDE.md` (not pushed; this README is the public-facing summary).

---

_Sister repo on the other side: <https://github.com/macos-node/fx.upleb.uk>_
