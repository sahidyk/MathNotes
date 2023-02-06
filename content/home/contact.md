---
# An instance of the Contact widget.
# Documentation: https://sourcethemes.com/academic/docs/page-builder/
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 130

title: Hubungi Penulis
subtitle: Silakan tuliskan pesan Anda kepada penulis apabila Anda ingin berdiskusi dengannya. Jangan lupa tuliskan nama dan alamat email Anda. Terima kasih.

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
  
design:
  columns: '2'
---
