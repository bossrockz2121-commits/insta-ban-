# Instagram Safety Assistant

A browser-only assistant for organizing user-entered notes and following Instagram's official block and report workflows. It does not submit reports, access account data, or determine whether an account violates platform rules.

## Requirements

- Node.js 18 or newer
- npm

## Install and run

1. Open this folder in VS Code using **File > Open Folder**.
2. Open the integrated terminal (**Terminal > New Terminal**).
3. Install dependencies:

   ```powershell
   npm install
   ```

4. Start the development server:

   ```powershell
   npm run dev
   ```

5. Open the local URL printed in the terminal, usually `http://localhost:5173`.

Create and preview a production build with `npm run build` and `npm run preview`.

## Privacy and behavior

- Profile lookup only validates the typed username or public profile URL and constructs its canonical URL. It does not fetch or inspect Instagram.
- Opening a profile requires confirmation and opens Instagram in a new tab. Block and Report require confirmation, then show manual steps to complete inside Instagram.
- Evidence and summaries exist only in the current page session. Nothing is uploaded, persisted, or sent to an API. Closing or refreshing clears the entries.
- Screenshot evidence is a filename/reference only; no file is selected or uploaded.
- Never enter passwords, login codes, session cookies, access tokens, or sensitive personal information.
- Instagram makes all moderation decisions. This project cannot ban an account.

## Project structure

```text
index.html
package.json
README.md
src/
  main.js
  components/
    app.js
  utils/
    instagram.js
  styles/
    main.css
```