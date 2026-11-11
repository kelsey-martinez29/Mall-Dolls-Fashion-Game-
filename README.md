# Mall Dolls ✦

A multiplayer Y2K fashion game by Kelsey Martinez. You and your friends get 60 seconds to dress for a theme. Then each doll gets eight seconds on the runway, and everyone else decides how well the outfit fits the theme.

**[Play Mall Dolls](https://mall-dolls-kelsey.kelseymartinez12.chatgpt.site)** · 2–8 players · Each player uses their own device

![The four illustrated Mall Dolls characters](media/mall-dolls-lineup.jpg)

## How to play

1. Pick a doll and nickname. Host a party and share the room code, or enter a friend's code to join.
2. Once everyone is ready, the host starts the game. Shop three themed closets in order: **Cyberpunk**, **Dollette**, and **Glamoratti**. The clothing only unlocks during each timed shopping round.
3. Watch each look and vote from **1 star** (“So off brand”) to **4 stars** (“You are the IT Girl!”). You can't vote on your own outfit. Each round's score is the average rating. The highest total after three rounds wins, and tied players share the crown.

## What I built

I designed the themes, wardrobe, voting system, and doll aesthetic, and used AI-assisted development to build and iterate on the game. I learned to host it with Sites and use a backend for both the multiplayer rooms and my own editing tools.

The hardest part was making flat illustrations look like clothing the dolls were actually wearing. Rotating a whole top could fix one strap while moving the waist out of place. I added an owner-only **Fitting Studio** where I can move, resize, rotate, or reshape one part of an item, preview it on all four dolls, and save the fit back into the game. The closet has 96 pieces across three themes and eight categories.

## Inside the project

- [Multiplayer game rules](src/game.ts) — The server checks the clock before accepting an action. Once shopping closes, the outfit locks for the runway. This file also handles voting and round scores.
- [Wardrobe fitting logic](src/fittings.ts) — Stores adjustments by item and doll and validates the shape points used to refine garments.

The live app uses React and TypeScript, a Cloudflare Worker, and D1 storage. This portfolio repository includes selected implementation files and game artwork. The playable multiplayer version is hosted on Sites.
