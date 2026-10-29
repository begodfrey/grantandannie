# Wedding page

The site is `index.html` at the root of the repository. Open that file directly in a browser, or serve the repository with GitHub Pages. The tab icon is the spinning pigeon (`pigeon.gif`). Home-screen icons and link previews use a still of the same bird, because those surfaces do not play an animation.

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

The type stops growing once the window is wider than 800px, and the column stays centered. Below 640px the type is a little smaller, so a phone keeps more space on either side of the lines. A top margin places “Grant and Annie” on the vertical center of the window when the page opens. The bottom padding is a little more than one screen, so the last line can be scrolled to the top.

## Scroll

On scroll, a line’s place in the window sets `EXPO`. At the very top it is 100, thin and nearly invisible, the same washed-out state as the bottom. A quarter of the way down it is -100, the heaviest weight. At the middle it is 0. At the bottom it is 100 again, and the lower fade still makes the lowest lines disappear a little sooner than a straight ramp. The paper wash, the ink glow, and the extra stroke on the heavy side are still commented out. The entrance, the scroll weight, and the hover run even when the device asks for reduced motion.

The page stays blank, in the paper color, until Exposure is ready and the entrance has been set. That avoids a flash of fallback text on a slow connection. When the page loads, the pigeon fades in first. Every line starts in that thin bottom state and eases into the weight for where it sits, beginning only after the bird has arrived. The lines run in order down the page. Each one takes a little under two seconds to ease in, with a short pause before the next.

Link underlines are a rounded bar under the words, sitting close to the letters. Where the letters are fading out, at the very top and toward the bottom, the bar thins with them, down to 0.1px. Through the heavy band it thickens with the weight, up to a much heavier bar at the -100 peak. Hovering a link leaves the letters as they are. The underline thickens and drops a little, then returns when the pointer leaves. That move takes about 160ms.

## Header

A spinning pigeon sits above the words and fades in before the first line. `darken` drops the white field into the cream page, so only the bird shows. The header has `18vh` of space above it, which puts “Grant and Annie” near the vertical center when the page opens. On a narrow or short screen that top space shrinks, so “Join us in” still peeks into view.

## Links

Linked, not embedded. R.S.V.P. is “☞ RSVP ☜”, opening https://form.typeform.com/to/afrsCaCx in a new tab. “Our registry” opens https://www.zola.com/wedding/reedsmartin/registry in a new tab. “Email us” is last. It is a `mailto:grantandannie2026@gmail.com` link and stays in the same tab.
