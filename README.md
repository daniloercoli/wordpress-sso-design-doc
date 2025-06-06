# WordPress SSO Integration – Solution Design Document

This repository contains the **Solution Design Document (SSD)** for integrating a custom Single Sign-On (SSO) platform with WordPress.  
The SSD explains in detail how WordPress authentication is off-loaded to the organisation’s SSO, how user data is exchanged and synced, and how errors are handled. No plugin or code is included here—only the design.

---

## Quick links

| File | Description |
|------|-------------|
| **WordPress SSO Integration SSD.pdf** | PDF of the Solution Design Document (version 1.0, updated 27 Sep 2024) |

---

## Executive summary

* **Purpose** – Provide a seamless, centralised login for WordPress by redirecting all authentication to the client’s SSO and synchronising user accounts on-the-fly.  
* **Core flow** – Intercept WordPress login → redirect to SSO → return with JWT → validate & exchange for full profile via REST → create/update WP user → start session.  
* **Environments** – Staging and Production each have their own endpoints, JWT secret and API key.  
* **Future ideas** – Background profile sync and single-logout (SSO → WP).

See the SSD for the complete context diagram, error-handling matrix, role-mapping table and more.

---

## How to view the document

1. Open **WordPress SSO Integration SSD.md** right here on GitHub—Markdown renders automatically.  
2. If you prefer an offline copy, click **Raw** → **Save as…** to download it.

---

## License

The design is shared under the MIT License. See `LICENSE` for details.

---

> _Need help turning this design into a working plugin later on?  
> Open an issue or discussion thread—contributions are welcome!_
