# Wedding page

The site is `index.html` at the root of the repository. Open that file directly in a browser, or serve the repository with GitHub Pages. The tab, the home-screen icon, and the link preview are a cream square with “G&A” in the thin italic.

GitHub Pages: in the repository settings, choose Deploy from a branch, branch `main`, folder `/ (root)`. Until a custom domain is attached, the page is at https://begodfrey.github.io/grantandannie/. When you have the domain, add a `CNAME` file whose only line is that domain. `.nojekyll` is in the repo so Pages serves the file as-is.

## Font

Exposure Trial VAR italic, the italic file you supplied, embedded as base64. The roman cut has no slant axis, so the page uses the italic, which leans about 16 degrees and has the same `EXPO` axis, from -100 to 100. This cut is a 205TF trial: a short character set, for testing a layout, not a license to publish the font.

Every line is set in capitals with CSS. The R.S.V.P. line reads “☞ RSVP ☜”. Exposure has no pointing-finger glyphs, so those two characters use a symbol font: Apple Symbols, Segoe UI Symbol, Noto Sans Symbols 2, then DejaVu Sans.

## Layout

The lines stay fixed:

GRANT AND ANNIE
ARE GETTING MARRIED
JOIN US IN
CELEBRATION
IN DECEMBER
☞ RSVP ☜
OUR REGISTRY
EMAIL US

The type stops growing once the window is wider than 800px, and the column stays centered. Below 640px the type is a little smaller, so a phone keeps more space on either side of the lines. On a desktop window there is `18vh` of space above “Grant and Annie”, and the three groups of lines are separated by `clamp(5.5rem, 18vh, 11rem)`. On a narrow or short screen the space above the title is `22vh`, and the gap between those groups is two thirds of that clamp. The bottom padding is a little more than one screen, so the last line can be scrolled to the top.

## Scroll

The mapping is still in the page. A line’s place in the window would set `EXPO`: 100 at the very top, -100 a quarter of the way down, 0 in the middle, and 100 again at the bottom, with the lower fade making the lowest lines disappear a little sooner than a straight ramp. The calls that apply that mapping are commented out, so after the entrance every line stays at `EXPO` 0, the regular weight, and scrolling does not change it. The paper wash, the ink glow, and the extra stroke on the heavy side are still commented out inside the paint function.

The page stays blank, in the paper color, until Exposure is ready and the entrance has been set. That avoids a flash of fallback text on a slow connection. When the page loads, every line starts in the thin, nearly invisible state and eases to the regular weight. The lines run in order down the page. Each one takes a little under two seconds to ease in, with a short pause before the next. The entrance and the hover run even when the device asks for reduced motion.

Link underlines stay at the regular weight. Hovering a link leaves the letters as they are. The underline thickens and drops a little, then returns when the pointer leaves. That move takes about 160ms.

## Links

Linked, not embedded. R.S.V.P. is “☞ RSVP ☜”, opening https://form.typeform.com/to/afrsCaCx in a new tab. “Our registry” opens https://www.zola.com/wedding/reedsmartin/registry in a new tab. “Email us” is last. It is a `mailto:grantandannie2026@gmail.com` link and stays in the same tab.
