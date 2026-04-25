<p align="center">
  <img src="https://addrly.app/favicon.svg" alt="Addrly" width="80" height="80" />
</p>

<h1 align="center">Addrly</h1>

<p align="center">
  <strong>Email validation API — detect disposable emails, verify domains, and protect your sign-up forms.</strong>
</p>

<p align="center">
  <a href="https://addrly.app/documentation">Documentation</a> •
  <a href="https://addrly.app/signup">Get API Key</a> •
  <a href="https://addrly.app/status">Status</a>
</p>

---

## Official SDKs

| Language | Package | Install | Docs |
|----------|---------|---------|------|
| **Python** | [![PyPI](https://img.shields.io/pypi/v/addrly?color=3776AB&label=PyPI)](https://pypi.org/project/addrly/) | `pip install addrly` | [View →](https://github.com/addrly/addrly-python) |
| **JavaScript** | [![npm](https://img.shields.io/npm/v/addrly?color=CB3837&label=npm)](https://www.npmjs.com/package/addrly) | `npm install addrly` | [View →](https://github.com/addrly/addrly-js) |
| **PHP** | Coming soon | — | — |

---

## Quick Start

### Python

```python
from addrly import Addrly

client = Addrly("your_api_key")
result = client.validate("user@tempmail.com")

if result.disposable:
    print("Blocked: disposable email detected")
```

### JavaScript

```javascript
import { Addrly } from 'addrly';

const client = new Addrly('your_api_key');
const result = await client.validate('user@tempmail.com');

if (result.disposable) {
  console.log('Blocked: disposable email detected');
}
```

### cURL

```bash
curl -H "X-API-Key: your_api_key" \
  https://api.addrly.app/v1/validate/user@tempmail.com
```

---

## Features

| Feature | Description |
|---------|-------------|
| **Disposable Detection** | Block 800+ temporary email providers |
| **MX Verification** | Confirm domain can receive emails |
| **Domain Age** | Flag newly registered domains |
| **Role Detection** | Identify generic addresses (info@, support@) |
| **Public Domain** | Detect Gmail, Yahoo, Outlook, etc. |
| **Normalization** | Standardize emails, remove aliases |
| **Typo Suggestions** | "Did you mean gmail.com?" |
| **Relay Detection** | Catch forwarding services |

---

## API Response

```json
{
  "email": "user@tempmail.com",
  "disposable": true,
  "mx": true,
  "domain": "tempmail.com",
  "domain_age_days": 2156,
  "public_domain": false,
  "relay_domain": false,
  "role_account": false,
  "normalized_email": "user@tempmail.com",
  "did_you_mean": null
}
```

## Links

- 🌐 [Website](https://addrly.app)
- 📖 [Documentation](https://addrly.app/documentation)
- 🔑 [Get API Key](https://addrly.app/signup)
- 📊 [Status Page](https://addrly.app/status)
- 💬 [Contact](https://addrly.app/contact)

---

## License

MIT © [Addrly](https://addrly.app)
