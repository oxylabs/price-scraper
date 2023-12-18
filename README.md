# Price Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Price Scraper](https://oxylabs.io/products/scraper-api/web/price-scraper?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from any product page effortlessly. This brief guide explains how a Price Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get HTML of any pricing result by providing your own URLs to our service.

#### Python code example

The example below illustrates how you can obtain HTML with pricing information for a sample product page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://sandbox.oxylabs.io/products/1'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/price-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\"><head><meta charSet=\"utf-8\" /><meta name=\"viewport\" content=\"width=de ... </html>",
      "created_at": "2023-12-18 11:30:57",
      "updated_at": "2023-12-18 11:30:59",
      "page": 1,
      "url": "https://sandbox.oxylabs.io/products/1",
      "job_id": "7142476330536312833",
      "status_code": 200
    }
  ]
}
```
With our specialized Price Scraper tool, you can easily gather public information from any product pages. Collect necessary data like price, customer reviews, or detailed product specifications to monitor and understand the market better and stay ahead of your competitors. If you need any help or have any questions, feel free to reach out to our support team through our live chat service or send us an email at hello@oxylabs.io.
