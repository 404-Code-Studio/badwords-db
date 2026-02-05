# badword-db
**A powerful, open-source database and API to filter insults, slurs, and profanity from your projects.**

This project provides a curated blacklist of "bad words" in multiple languages to help developers keep their communities and platforms safe and respectful.

---

## Features

* **Multi-language support:** Curated lists for German (`de`) and English (`en`).
* **Categorized:** Words are tagged by type (e.g., `insult`, `slur`, `spam`).
* **Easy Integration:** Simple JSON API – no authentication required for basic use.
* **Performance-focused:** Designed for quick lookups.

## API Usage

The API is public and returns data in JSON format.

### Get all words

`GET https://api.badword-db.com/v1/all`

### Filter by Language & Category

You can refine your request using query parameters:
`GET https://api.badword-db.com/v1/get?lang=de&cat=insult`

**Parameters:**

* `lang`: Language code (`de`, `en`)
* `cat`: Category (e.g., `insult`, `profanity`, `slur`)

---

## Rate Limiting & Caching

To keep the service free and stable, we implement **IP-based rate limiting**.

* **Limit:** 100 requests per hour per IP.
* **Recommendation:** **Please cache the results!** Since the database does not change every second, it is highly recommended to fetch the list once a day and store it locally in your application's memory or database.

---

## JSON Structure

The API returns an array of objects:

```json
[
  {
    "word": "exampleword",
    "language": "en",
    "category": "insult",
    "severity": 1
  }
]

```

---

## Contributing

Found a word that’s missing? Or a "false positive" that shouldn't be there?

1. Fork the repository.
2. Edit the `data/de.json` or `data/en.json`.
3. Submit a Pull Request.

---

## Legal Disclaimer

This database contains offensive language. It is provided strictly for educational and moderation purposes (content filtering). The maintainers do not support or condone the use of this language against individuals or groups.

*The project is provided "as is" without any warranties.*

---

## Support / Donation

If this project helps you keep your platform clean, consider supporting the hosting costs:
[UNSET] UNSET
