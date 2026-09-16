# Xbox / Microsoft Account Engine (`vadilator-ms`)

A multi-threaded session verification and protocol validator implementing Microsoft Live and Xbox Live OAuth2 authentication chains with automated challenge handling.

Part of the **[Stylix Developer Portfolio](https://stylixdev.vercel.app)** by **[@StylixXD](https://github.com/StylixXD)**.

---

## Highlights

- **OAuth2 Token Exchange Pipeline:** Validates credentials through the full chain: Microsoft Live login → user token → Xbox Live token → XSTS authentication.
- **Proxy Mesh Routing:** Distributes inbound validation batches across rotating proxy nodes to prevent IP rate throttling.
- **Challenge & 2FA Detection:** Automatically parses account security flags, password reset triggers, and 2FA states without hanging.
- **Asynchronous Concurrency:** Built on `aiohttp` for non-blocking I/O capable of handling hundreds of accounts per minute.

---

## Tech Stack

- **Language:** Python 3.10+
- **HTTP Engine:** `aiohttp` with connection pooling
- **Protocols:** Microsoft Live SDK, Xbox User Authentication (XASU/XSTS)

---

## Quick Start

```bash
git clone https://github.com/StylixXD/vadilator-ms.git
cd vadilator-ms
pip install -r requirements.txt
python validator.py
```

---

## License

MIT © 2026 Ashu (@StylixXD)
