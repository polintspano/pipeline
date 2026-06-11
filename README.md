# pipeline

Simple static project with npm scripts to run a local server and publish via Git.

Prerequisites
- Node.js (for `npx` / npm)
- Git configured with a remote

Usage

Start a local server (serves project root on port 8080):

```bash
npm run start
```

Publish (stages all changes, commits with message "chore: publish", and pushes):

```bash
npm run publish
```

Notes
- `start` uses `npx http-server -c-1 . -p 8080`. To install it locally run:

```bash
npm install --save-dev http-server
```

- `publish` will create a commit even for trivial changes; edit the script in [package.json](package.json) if you want a different commit message or behavior.
