---
title: DMS to GEE Coordinate Converter
date: 2025-01-20
weight: 5
share: false
show_related: false
links:
  - name: View on GitHub
    url: 'https://github.com/PrashanthReddy47/dms-to-gee-converter'
tags:
  - Chrome Extension
  - JavaScript
  - Google Earth Engine
  - Productivity Tool
  - Agriculture
---

A Chrome extension that converts GPS coordinates between formats for Google Earth Engine workflows. Developed to solve a real friction point during rice paddy mapping fieldwork — coordinates from farmers and Google Maps arrive in multiple formats (Decimal Degrees, DMS), but GEE requires specific decimal degree ordering `[lon, lat]`.

---

### Key Features

- **Multi-format support:** Converts both Decimal Degrees (45.202937, 9.137242) and DMS (44°36'30"N 7°31'17"E) formats
- **GEE-ready output:** Automatic coordinate reordering to `[longitude, latitude]` for direct use in Earth Engine scripts
- **One-click copy:** Clipboard integration for seamless workflow
- **Lightweight:** Built with Manifest V3, Vanilla JavaScript, and Regex parsing

---

### Motivation

During field campaigns for rice paddy mapping research and collaboration with farmers in Italy and India, GPS coordinates are shared via Google Maps in various formats. Manual conversion and reordering introduced friction in operational workflows. This extension eliminates that step entirely.

---

### Technical Stack

- **JavaScript** (Vanilla) — no frameworks or dependencies
- **Chrome Extension API** (Manifest V3)
- **Regex pattern matching** for coordinate parsing
- **Clipboard API** for one-click integration

---

### Roadmap

- Bounding box coordinate conversion
- Polygon support for field boundaries
- Batch processing for field datasets
