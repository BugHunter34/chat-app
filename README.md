# chat-app
chat app builded on Flet communicating with my Ubuntu Server via Ngrok -- Upgraded to custom domain with CloudFlare
for future will use either CloudFlare tunnel or SelfHosted (Port Forwarding) -- choosed the CF option

## Spendings:
bought custom domain (andhyy.com) from CloudFLare for liveApp hosting, website and custom email
(will be hosting client.exe in near future)

## Architecture
had to divide the Repos since one is living inside Windows and others on Linux:
*   **Client (`/client`):** A cross-platform frontend built with [Flet](https://flet.dev/). Websockets for Desktop and pyiodide for Web
*   **Server (`/server`):** An asynchronous backend built with [FastAPI](https://fastapi.tiangolo.com/) handling REST API, WebSocket connections and MongoDB
*   **Blog (`/blog`):** Website for updates, link to live app and Feedback

## Features

*   **Cross-Platform WebSockets:** since SSL on web side was problem, i've created cross platform option to switch libs based on where it runs
*   **SERVER** Hosted on NoteBook with Ubuntu server as OS with cloudflare tunnel and Resend to handle emails

## Technology:

**Frontend:**
*   Python 3
*   Flet
*   Pyodide (WebAssembly)
*   Requests

**Backend:**
*   FastAPI
*   Uvicorn
*   MongoDB
*   Python `websockets`

**Infrastructure:**
*   Ubuntu Linux
*   Nginx (Reverse Proxy and file hosting)
*   Cloudflare (DNS & Edge Caching)
*   Git Submodules (Version Control)

## Recent Progress / Changelog

*   **[Web Deployment]** Builded Flet to web for non-download usage
*   **[Network]** fixed Nginx to don't crash with MIME-type errors and `.mjs` crashing
*   **[Caching]** strict cache-control header to bypass Cloudflare Loader and Flet Service Worker conflict
*   **[Version Control]** Linked Client, Server, and Blog repositories under this Repo

## Next Steps

- Iend-to-end encryption (E2EE).
- Add Read, delivered and typing indicators.
- notifications and offline users handleing
- Etc..