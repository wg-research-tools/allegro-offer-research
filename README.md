# Allegro offer research client

A small read-only client for the **Allegro REST API**, used to collect **public offer data**
(offer listings, prices, parameters) for market comparison.

It never creates, edits, closes, or promotes offers, and it does not touch orders, payments,
shipping, ratings, disputes, or messages. Read-only by design.

## Authorization

- OAuth grant type: `device_code` (no browser access required)
- Scope requested: `allegro:api:sale:offers:read`
- Credentials and tokens live on the operator's machine only. Nothing sensitive is stored in
  this repository.

## What it does

1. Searches offers by phrase or category.
2. Reads price, seller, availability, and key parameters for each offer.
3. Produces a comparison table plus a short written summary for a human decision-maker.

## User-Agent

Every API request carries a User-Agent header identifying this client and its version, as
required by Allegro. Requests without a valid User-Agent are rejected and can lead to the API
key being blocked.

## Version

`v0.1`
