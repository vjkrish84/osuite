# OSuite V8 — Customer Preview

A browser-only React/Vite preview of the OSuite ophthalmology workflow.

## Run locally

```bash
npm install
npm run dev
```

## Production build

```bash
npm run build
npm run preview
```

Deploy the generated `dist/` directory to Netlify, Vercel, or another static host. SPA fallback configuration is included for Netlify and Vercel.

## V8 interaction updates

- Notification bell opens a notification popover and supports marking notifications read.
- Profile avatar opens a profile menu with Settings, preview help, and a clearly labelled demo sign-out action.
- Settings opens a dedicated screen with workspace information and interactive session-only preferences.
- On phones and small tablets, the navigation becomes a slide-in drawer with a scrim and a visible menu trigger.
- Navigation closes after a destination is selected.

## Preview limitations

This is a static front-end preview using fictional sample data. There is no backend, database, authentication, ABHA connection, live AI, live transcription, OCR processing, or real payment integration. Changes and preferences remain in the current browser session. Clinical values and generated content are illustrative only and are not validated for clinical use.

## V8 Surgical Suite
New Surgical Suite navigation module with sample surgical case management, pre-operative checklist and assessment notes, intra-operative safety checklist and implant/operative notes, and post-operative findings, discharge/follow-up documentation. Create demo cases for fictional patients, switch workflow stages, and export case JSON. Browser-session state only; no backend, clinical validation, signature, persistence or device integrations. Never enter real patient data.

**Build verification:** dependency installation could not complete in the authoring environment, so the production build has not been verified. Run `npm install && npm run build` before publishing.

## V9 Surgical attachments
Each pre-operative, intra-operative, and post-operative stage supports up to 10 local demo attachments (PDF, JPG, PNG, WebP, DOC, DOCX; 8 MB/file). Files are read in-browser and displayed/downloadable within the current session only. Refreshing loses all attachments. No server upload, storage, scanning, or clinical record retention is implemented. JSON export includes attachment metadata only. Do not use real patient data.


## V10 surgical banner interaction fix
The four Surgical Suite summary banners are interactive filters. All scheduled cases shows the complete list; Pre-op, OT and Post-op filter the case list to their respective saved stages. Empty stages show a message and a Show all cases button. Select a case and save its stage to update its category. The workflow stage tabs remain independently clickable. This is still a browser-session-only demonstration.
