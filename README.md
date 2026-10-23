# CloudCoder IDE

A browser code editor where several people can edit the same file at the same time. The editor is Monaco (the one inside VS Code), and Yjs keeps everyone's edits in sync over Socket.IO.

## Layout

- `Frontend/` React + Vite app with the Monaco editor
- `Backend/` Express and Socket.IO server that relays Yjs updates, with `/` and `/health` endpoints

## Run it

```bash
cd Backend && npm install && node server.js      # port 3000
cd Frontend && npm install && npm run dev
```

The backend only accepts browser connections from `ALLOWED_ORIGIN` (default `http://localhost:5173`).

## Status

Early prototype. Shared editing works; there is no auth, persistence or sandboxed code execution yet.

Adithya Thaninki, [@adithyalee](https://github.com/adithyalee)
