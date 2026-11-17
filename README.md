# Bashpo: Digital Game Store

CSE471 (System Analysis and Design) lab project, BRAC University, Fall 2024. Group 5, Lab Section 08.

Bashpo is a Steam-style online game store with three kinds of users:
- **buyers**, who buy and manage games
- **developers**, who publish and sell their games
- an **admin**, who runs the store

## Features

**Buyers**
- Sign up, log in and reset a password
- Browse games by genre; the homepage features the 3 newest games
- Open a game's page: details, screenshots, reviews and ratings
- Wishlist, cart, and checkout with a wallet or a credit card
- Top up the wallet with a card or a gift card, and activate games with product keys
- Purchase history, with refunds within a time limit
- Friends, reviews and ratings, and game search

**Developers**
- Send a publishing request to the admin, then publish the game once it is approved
- Start timed sales; prices update across the store and in carts
- Generate game activation keys
- View revenue and copies sold

**Admin**
- Approve or reject publishing requests
- View active buyers and developers, and terminate buyer accounts
- Generate wallet gift codes
- View revenue analytics and top-selling games
- Revenue from each sale is split between the developer and admin wallets

## Tech stack

| Layer | Technology |
|---|---|
| Backend | Flask (Python) |
| Frontend | HTML, TailwindCSS, DaisyUI, JavaScript |
| Database | SQLite3 |
| Deployment | Render |

## Links

- Full project code: [TheLubricator/bashpo_main](https://github.com/TheLubricator/bashpo_main)
- Deployed site: [bashpo-main.onrender.com](https://bashpo-main.onrender.com/). It is on a free tier, so it may take a while to wake up or may be offline.

## This repo

This repo holds an early backend module I wrote: a Flask API for adding games and building the homepage. The homepage groups games by genre and features the 3 newest releases. The full team project lives in the repo linked above.

| File | Contents |
|---|---|
| `app.py` | Flask API: `/homepage`, `/addGame`, `/uploads/<file>` |
| `game_store.db` | SQLite database with sample games |
| `uploads/`, `*.jpg/png/webp` | Sample game images |
| `docs/Project_Report.pdf` | Submitted project report: requirements, backend APIs, Figma UI designs, frontend, user manual, Lighthouse analysis, contributions. Teammates' student IDs are blacked out. |

To run it:

```bash
pip install flask
python app.py   # serves on http://localhost:1241
```

## My part

- Featured games on the homepage (the 3 newest)
- Admin revenue monitoring across the site, developers and users
- Top-selling games for the admin
- Splitting sale revenue between the developer and admin wallets
- Figma designs for the game page and the upload-game-data page

## Team

Shah Faiyaz Zaman, MD Mahmudun Nur Miraz, Shuvo Datta.
