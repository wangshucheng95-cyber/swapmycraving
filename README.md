# SwapMyCraving

Static SEO tool site — finds healthier alternatives for junk food cravings.

## Stack

- Pure HTML/CSS/JavaScript (no framework, no build step)
- Hosted on Cloudflare Pages
- Domain managed via Cloudflare DNS

## File structure

```
/
├── index.html                              Homepage
├── healthy-pizza-alternatives/index.html   First SEO target page
├── robots.txt
├── sitemap.xml
└── README.md
```

## Deploy

1. Push this folder to a GitHub repo
2. Connect the repo to Cloudflare Pages
3. Build command: (none)
4. Output directory: `/`
5. Add custom domain: swapmycraving.com

## Adding a new craving page

Copy `healthy-pizza-alternatives/index.html`, save to a new directory like `healthy-ice-cream-alternatives/`, then update:

- `<title>`, `<meta description>`, `<link rel="canonical">`
- `<h1>` and intro paragraph
- The `ALTERNATIVES` array in the `<script>` block
- Card content for the "Top 3" and "5 More" sections
- FAQ section
- `sitemap.xml` (add new URL)

## Local preview

```bash
cd /Users/an/Desktop/swapmycraving
python3 -m http.server 8000
# open http://localhost:8000/healthy-pizza-alternatives/
```
