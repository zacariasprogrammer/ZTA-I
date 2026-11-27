# ZTA I — Zaquito Theft Auto I (web, real 3D)

First-person open-world game in the browser, built on Three.js. Real 3D city with sun, shadows, textured buildings. Walk the streets, steal a car, drive it, dodge the cops, run taxi fares. No sexual content, ever. That's the rule.

## The city

**Zaqui City — a made-up city, not a real place.** Never a real hometown in a crime game.

## Play

- **Look:** click the game to lock your mouse, move it to look around. Drag on phone.
- **Move:** WASD, Shift to run. Arrows work too.
- **Drive:** walk up to a car, press **E** to get in, **E** again to get out. WASD to drive, it steers like a car.
- **Shoot:** click or **Space**. Crosshair in the middle. Bullets are real 3D rays — a wall between you and the target stops the shot.
- **Taxi job:** drive up to the yellow passenger (follow the yellow beam), then drive them to the green beam. Get paid.
- **Pickups:** green cash (+$25), white health packs (+50 health).
- **Pause:** P.

## Wanted — how it actually works

You are NOT always wanted. A crime only counts if someone sees it:

- The yellow car parked by spawn is **yours**. Taking it is never a crime.
- Stealing any other car, shooting someone, or running someone over only raises your stars if a **cop is close by** or a **person close enough sees it happen**.
- No witnesses, no stars. Do it quiet, walk away clean.
- Stars fade after 15 calm seconds with no new crimes. Outrun the cops, cool off, you're clean.

## How it ships

One `index.html` + a deploy workflow. GitHub Pages hosts it free and GitHub Actions deploys it on every push to `main`. The 3D engine (Three.js) loads from a CDN, so the game needs internet.

1. Create an **empty public repo** on GitHub (Pages is free on public repos only).
2. Push these files to `main`.
3. The `Deploy ZTA I` workflow runs: it checks the game JS, then deploys to Pages. Takes about a minute.
4. Play at `https://<your-username>.github.io/<repo>/`.

If the first run says Pages isn't enabled, go to repo **Settings → Pages → Build and deployment → Source → GitHub Actions**, then re-run the workflow.

## Files

- `index.html` — the whole game (Three.js from CDN, everything else local).
- `.github/workflows/deploy.yml` — check the JS, deploy to Pages.
