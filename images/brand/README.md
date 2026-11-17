# Mimeo artwork

Generated with the built-in image generation tool. The identity takes its
paper-stack motif from the mimeograph and its warm paper, graphite and blue
palette from the theme's CSS. PNG resizing used macOS `sips`; the ICO
container embeds the 16, 32, 48 and 256px PNG renditions.

| Asset | File | Dimensions |
| --- | --- | --- |
| Icon source (transparent) | [mimeo-icon.png](../../assets/brand/mimeo-icon.png) | 1254 × 1254 |
| README cover | [readme-cover.png](readme-cover.png) | 1600 × 720 |
| README format illustration | [readme-formats.png](readme-formats.png) | 1600 × 720 |
| Repository social preview | [github-social.png](github-social.png) | 1280 × 640 |
| Demo social preview | [mimeo-demo-og.png](../../exampleSite/static/images/mimeo-demo-og.png) | 1200 × 630 |
| Browser icons | [static/](../../static/) | 16, 32, 48, 96, 180, 192, 512px |

The repository banner follows the supplied 2:1 GitHub template, with
approximately 80px clear space around important content. It is below 1MB.
Upload it through the repository's Settings → General → Social preview.
The demo banner is already configured in `exampleSite/hugo.toml`; it will
be included in the next deployment. No repository settings or deployments
were changed as part of creating these files.

The original generated icon remains in `assets/brand/`; the distributable
favicon set lives in `static/`, which Hugo copies into the built site.
The original terminal favicon remains available at `assets/favicon.svg`.
The favicon partial uses relative-to-base URLs to support GitHub Pages
project paths.

## Generation prompts

The icon was generated first. Each banner used that icon as its identity
reference; banners were resized to the exact delivery dimensions above.

### Icon

```text
Use case: logo-brand
Asset type: square project icon, 1024 by 1024 pixels, transparent outside the mark.
Primary request: Create a distinctive, extremely simple icon for Mimeo, a Hugo blog theme named for the mimeograph: plain monospaced copies of typed pages, mailing-list headers, an 80-character column, no JavaScript.
Subject: a warm-white paper sheet with a very bold lowercase monospaced "m" printed on it, with one second paper sheet offset slightly behind it to suggest duplicated pages. The two sheets sit centered within a solid graphite #1f2328 rounded square. The front sheet is warm paper #fbfbf8; the single lowercase m is ink blue #0b5cad. The silhouette has substantial rounded-square margins and fills 84 percent of the square image; outer corners are genuinely transparent.
Style: meticulous flat vector-like editorial identity, broad crisp geometric shapes, no fine details. The m should be prominent, about half the paper height, with short monospaced slab serifs. The sheets have straight square corners; no folded dog-ear. Flat fills, no outlines.
Constraints: exactly one lowercase m, no other text, no lines of simulated writing, no gradients, no shadows, no 3D, no texture, no mockup, no watermark. The mark must remain recognizable as a small favicon. One finished icon only, no variants or presentation board.
```

### README cover

```text
Use case: ads-marketing
Asset type: README cover image for the Mimeo open source Hugo theme. Wide landscape canvas 1600 x 720 pixels.
Input images: attached icon is the exact Mimeo identity reference. Preserve the graphite rounded square, duplicated warm-white sheets and bold ink-blue lowercase m when incorporating it.
Primary request: Elegant and restrained editorial cover, like the title page of a beautifully typeset technical pamphlet. Mimeo is named for the mimeograph and is a blog theme that reads like plain text, mailing-list headers and patch files.
Composition: warm paper #fbfbf8 canvas, very subtle paper texture. Spacious asymmetrical typography with all content 80px inside edges. Large lowercase monospaced wordmark "mimeo" on the left, approximately 140px high. The supplied icon is on the right at about 300px square. A small blue monospaced top line "PLAIN TEXT, PUBLISHED." Above the bottom margin a fine dashed horizontal graphite rule; below it a tidy monospaced line.
Text, verbatim and only these lines, in this hierarchy:
"PLAIN TEXT, PUBLISHED."
"mimeo"
"A blog that reads like a text file."
"80 columns. Zero JavaScript. Yours to write."
Typography: meticulous monospaced type, the main wordmark has a bold slab-serif/typewriter character, supporting lines in a clean technical monospace. Main text #1f2328, small label #0b5cad. One calm, cohesive print-inspired composition, strong legibility at README width. No web-browser chrome, no mockup frame, no buttons, no extra words, no GitHub logo, no watermark. Background opaque.
```

### GitHub repository social preview

```text
Use case: ads-marketing
Asset type: GitHub repository social preview banner, exact 1280 x 640 pixel landscape, 2:1 aspect ratio.
Input images: icon supplied is the exact Mimeo identity. Incorporate it without changing its paper-stack/blue lowercase m design.
Primary request: A highly legible restrained monospaced editorial banner for "mimeo", a Hugo blog theme inspired by plain-text files, mailing-list archives, and mimeograph printing.
Composition: warm off-white paper #fbfbf8 background, graphite #1f2328 text, restrained ink-blue #0b5cad accent. Keep ALL important information within x=80..1200 and y=80..560 to respect the supplied GitHub template safe area. Small repository identifier at top left, very large bold lowercase typewriter wordmark below it; two compact tagline lines, then a thin dashed horizontal rule and a small footer. The supplied icon appears at right, around 260px square, balanced with typography, no overlap.
Text verbatim and only:
"haydenk / mimeo"
"mimeo"
"A plain-text blog theme"
"for Hugo."
"80 columns / zero JavaScript / HTML + .txt"
Typography is all monospaced, readable at thumbnail size; heading about 110px high and taglines about 37px. Flat print quality, generous whitespace, subtle paper grain only. Do not reproduce the GitHub logo, red guide lines or placeholder text from the template. No badges, no buttons, no browser mockup, no watermarks. Opaque background.
```

### Demo social preview

```text
Use case: ads-marketing
Asset type: Open Graph social share banner for the Mimeo live Hugo theme demo. Exact 1200 x 630 pixel landscape.
Input images: supplied icon is the exact Mimeo identity. Preserve its graphite rounded square, warm white duplicated paper sheets and lowercase blue m.
Primary request: Dark-mode companion to a restrained monospaced print-inspired brand. Mimeo is a plain-text blog theme with mailing-list headers, an eighty-character text column and a .txt twin of every page.
Composition: deep graphite #121417 opaque canvas, warm white #fbfbf8 type, soft grey #8b949e secondary type, a small accent in blue #79b8ff. All important content safely within 80px margins. Spacious typographic layout: small label at upper left, large lowercase wordmark below, medium size tagline on two short lines, a quiet fine dashed rule lower down, and the demo address beneath. The supplied icon appears on the right at about 260px square. Respect its exact shape and colours, no extra pictorial elements.
Text verbatim and only these strings:
"LIVE DEMO"
"mimeo"
"A blog that reads"
"like a text file."
"haydenk.github.io/hugo-mimeo"
Typography: entirely monospaced; bold typewriter/slab-serif character in the wordmark, crisp clean technical monospace for support. Wordmark about 112px; tagline about 38px, URL at least 22px. No neon glow, no gradient, no 3D effects, no browser chrome, no buttons, no other text, no watermark. Cohesive, quiet editorial quality.
```

### README format illustration

```text
Use case: infographic-diagram
Asset type: second README illustration for the Mimeo Hugo blog theme, wide landscape 1600 x 720.
Input images: Mimeo icon is the identity reference; use the same warm paper #fbfbf8, graphite #1f2328 and ink-blue #0b5cad palette and the icon's overlapping-paper vocabulary.
Primary request: A spare, editorial diagram showing that one written post is published as HTML and as plain text. This is an explanatory illustration, not a screenshot of a website.
Composition: warm paper canvas with generous whitespace and at least 80px margins. Large monospaced heading "One post. Two formats." across the top. Below, three simple outlined paper shapes arranged horizontally. A smaller source sheet at left labeled "Markdown", a thin line forks elegantly to two larger sheets arranged side by side at middle and right. The middle sheet is labeled ".html", the right sheet ".txt". Use the smallest possible number of clear lines to connect the source to both outputs without overlaps with the pages. Both output sheets carry the same concise monospaced text: "From: Jane Doe", "Subject: Hello, Mimeo", then a short dashed line and "Your words, intact." At bottom left below the diagram, small text "HTML for the web. Plain text for everything else." All labels are accurate, crisp, large enough to read at 800px display width.
Style: restrained flat print infographic, monospaced technical lettering and bold typewriter/slab-serif title. Off-white paper shapes, graphite outlines and blue filename labels. Very subtle paper texture, no gradients, no shadows, no glow, no browser chrome, no badges, no buttons, no fake screenshots, no watermark, no extra text. One coherent diagram only.
```

### Format illustration refinement

```text
Use case: precise-object-edit
Edit the supplied Mimeo "One post. Two formats." diagram. Correct ONLY the diagram connectors: REMOVE both black curved branching lines between the Markdown source and the .html output, restoring the paper background. Put one simple ink-blue right-pointing arrow centered in that gap, pointing from the Markdown sheet toward the .html sheet. Put a single ink-blue plus sign centered in the whitespace between the .html and .txt sheets. The resulting visual equation should read: Markdown → .html + .txt. The arrow and plus sign must each be separate from the sheet outlines, clearly visible, centered around the vertical midpoint of the sheets, and not overlap any text or paper.
Keep every other element completely unchanged: the three paper-stack shapes, exact words and punctuation, typography, scale, spacing, background, title and footer. Do not add any new labels or change any existing text. Opaque background, same wide aspect ratio.
```
