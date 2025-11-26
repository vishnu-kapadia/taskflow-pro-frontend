# API Form Contracts — TaskFlow Pro

This document specifies request/response JSON for auth endpoints used by the frontend.

---

## POST /api/register
**Description**: Register new user (Sanctum cookie flow expects /sanctum/csrf-cookie call first).

**Request (JSON)**:
```json
{
  "name": "string, required, 1..255",
  "email": "string, required, email format, unique",
  "password": "string, required, min:8",
  "password_confirmation": "string, required, must match password"
}
