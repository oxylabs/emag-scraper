# Emag Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Emag Scraper](https://oxylabs.io/products/scraper-api/ecommerce/emag?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Emag website effortlessly. This brief guide showcases how Emag Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Emag results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Emag page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.emag.ro/nav/haine-accesorii'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/emag-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html>\n<html lang=\"ro\">\n<head >\n    <meta charset=\"utf-8\">\n    <title>Haine &amp; accesorii ... </html>",
      "created_at": "2024-02-20 12:41:59",
      "updated_at": "2024-02-20 12:42:00",
      "page": 1,
      "url": "https://www.emag.ro/nav/haine-accesorii",
      "job_id": "7165687028955259905",
      "status_code": 200
    }
  ]
}
```
Using our Emag Scraper, you have the ease of extracting public data from any Emag webpage. Gather crucial gamer-focused information such as video game prices, user reviews, and detailed descriptions. Use this data to stay updated on the gaming market and keep a competitive edge. If there are any queries, please reach out to our responsive support team via live chat, or drop us an email at hello@oxylabs.io.