# תילתול – Design Rules

## Stack
- Single `index.html` file
- Tailwind CSS CDN
- Lucide icons CDN
- Google Fonts: Heebo

## DO
- Light, minimal, clean, modern design — shadcn aesthetic
- Neutral palette: whites, grays, one subtle lilac accent (#b39ddb)
- Good typography hierarchy, plenty of whitespace
- Font: Heebo from Google Fonts (all weights)
- Mobile responsive (mobile-first)
- Light motion: scroll animations via IntersectionObserver, smooth transitions, subtle hover states

## DON'T
- NO bright saturated gradients or gradient text
- NO emoji icons — use Lucide icons only
- NO "revolutionary", "game-changing" marketing copy
- NO heavy shadows or busy patterns
- NO dark mode
- NO border-radius > rounded-2xl
- NO cramped spacing or tiny fonts (min 14px)

## Design Tokens
- Accent: #b39ddb (soft lilac)
- Background: #ffffff / #f9f9f9
- Text primary: #1a1a1a
- Text muted: #6b7280
- Border: #e5e7eb

## Sections
1. Navbar
2. Hero + CTA (App Store / Google Play buttons)
3. How it works (3 steps)
4. Features
5. Testimonials
6. Footer

## Hero Mockup
Inline SVG phone mockup showing:
- Israel map outline with salon dots at real city locations
- Search bar UI at top of phone screen
- One open tooltip/hover card on a dot

## Deployment
- GitHub: `gh repo create תילתול --public --source=. --push`
- Netlify: `npx netlify sites:create --name תילתול --account-slug ariela-povo`
- Deploy (only the site files, never the whole folder):
  `rm -rf deploy && mkdir deploy && cp index.html Hero4.png deploy/ && npx netlify deploy --dir=deploy --prod`
- The `cp` list must hold exactly the local files the page uses (currently `index.html`, `Hero4.png`). Update it when the page starts using a new image.
- Never `--dir=.` and never `git add .` / `git add -A`. This folder holds private documents and spreadsheets. Add files to git by name.
