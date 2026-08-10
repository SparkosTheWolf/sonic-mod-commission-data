# Sonic Mod Commission Data

Public JSON data repository for **Sparkos The Wolf — Sonic Mod Commissions**.

## Structure

- `config.json` — commission status, max slots, Telegram username, currency
- `games.json` — supported games, difficulty, descriptions, service list
- `pricing.json` — pricing for games and additional services
- `services.json` — service definitions, names, and descriptions
- `orders.json` — public order list with statuses

## File purpose

- `config.json`: controls whether commissions are open, how many slots are available, and which Telegram contact is used.
- `games.json`: defines each game and permitted services for estimation and website display.
- `pricing.json`: contains numeric prices only. Frontend and manager both read this file.
- `services.json`: stores service metadata and labels for calculator and order preview.
- `orders.json`: public order previews.

## Public data rules

- Do not include any private client information.
- `orders.json` must contain only order `id`, `game`, `work`, `status`, and `public`.
- Status values supported: `waiting`, `in_progress`, `waiting_client`, `completed`, `paused`.
- Prices must be non-negative numbers.
- Game IDs must be unique.
- Service IDs must be unique.

## Usage

This repository is consumed by the static website via raw GitHub URLs.

Example raw root:

```
https://raw.githubusercontent.com/SparkosTheWolf/sonic-mod-commission-data/main
```
