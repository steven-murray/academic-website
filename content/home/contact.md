---
# An instance of the Contact widget.
widget: contact
active: true

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 130

title: Contact
subtitle:

content:
  # Automatically link email and phone or display as text?
  autolink: true

  # Email form provider
  form:
    provider: netlify
    formspree:
      id:
    netlify:
      # Enable CAPTCHA challenge to reduce spam?
      captcha: true

  # Contact details (edit or remove options as required)
  email: murray.steveng-at-gmail.com
  address:
    street: Piazze Dei Cavalieri, 7
    city: Pisa
    region: PI
    postcode: '56124'
    country: Italy
    country_code: IT
  
design:
  columns: '2'
---
