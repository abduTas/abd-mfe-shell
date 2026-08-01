# abd-mfe-shell

Generic **Module Federation remote shell** (Vite + React).

## Exposes

`remoteShell/MicroShellApp`

## Consumes

`sharedState/store`, `sharedState/hooks` from abd-mfe-state

## Local dev

Start **abd-mfe-state** first (`npm run dev` on port 3002), then:

```bash
npm install
npm run dev   # build + watch + preview on http://localhost:3001
```

Use `npm run dev` (not raw `vite`) so `remoteEntry.js` is served from preview.

```env
NEXT_PUBLIC_MFE_STATE_URL=http://localhost:3002
```

## Vercel

**Production:** https://abd-mfe-shell.vercel.app

**Federation entry:** `https://abd-mfe-shell.vercel.app/assets/remoteEntry.js`

Set at build time:

```env
NEXT_PUBLIC_MFE_STATE_URL=https://abd-mfe-state.vercel.app
```
