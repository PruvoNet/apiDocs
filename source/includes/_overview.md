# Overview

## Abstract

This documentation defines the specifications of an API who’s responsibility is to provide access to Pruvo’s unique price monitoring capabilities.

The API is designed as stateless and RESTful and responds only with JSON format. For security considerations, we require the use of SSL(HTTPS) only.

Current API version: 1.0

## Request data

- Every string passed to/from API has to be UTF-8 encoded
- Support for SNI SSL is required

<aside class="notice">
Every partner is subjected to a QPM(Queries Per Minute) limitation. Current QPM limit is 50.
</aside>

## Versioning

We may update the API without increasing the version number (i.e 2.1 2.2 etc…) for NON-BREAKING changes.
