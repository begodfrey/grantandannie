# Wedding page

The site is `index.html` at the root of the repository. Open that file directly in a browser, or serve the repository with GitHub Pages.

GitHub Pages: in the repository settings, choose Deploy from a branch, branch `main`, folder `/ (root)`. Until a custom domain is attached, the page is at https://begodfrey.github.io/grantandannie/. When you have the domain, add a `CNAME` file whose only line is that domain. `.nojekyll` is in the repo so Pages serves the file as-is.

## Font

Exposure Trial VAR italic, the italic file you supplied, embedded as base64. The roman cut has no slant axis, so the page uses the italic, which leans about 16 degrees and has the same `EXPO` axis, from -100 to 100. This cut is a 205TF trial: a short character set, for testing a layout, not a license to publish the font.

The trial has no straight apostrophe, so “s’il” uses a typographic apostrophe. Every line except the R.S.V.P. is set in capitals with CSS. The R.S.V.P. is two lines: “Répondez S’il” and “Vous Plaît”. The first letter of each word is a larger full capital, and the remaining letters are smaller small caps.

## Layout

The lines stay fixed:

GRANT AND ANNIE
ARE GETTING MARRIED
JOIN US IN
CELEBRATION
IN DECEMBER
RÉPONDEZ S’IL
VOUS PLAÎT
OUR REGISTRY
EMAIL US

The type stops growing once the window is wider than 800px, and the column stays centered. Below 640px the type is a little smaller, so a phone keeps more space on either side of the lines. A top margin places “Grant and Annie” on the vertical center of the window when the page opens. The bottom padding is a little more than one screen, so the last line can be scrolled to the top.

## Scroll

On scroll, each line’s distance from the middle of the window sets `EXPO`: -100 at the top, 0 at the center, 100 at the bottom. Toward 100 the letters go thin and the ink mixes into the paper, so words near the bottom nearly disappear. Toward -100 they go thick, pick up an ink-colored glow, and read even blacker. `prefers-reduced-motion: reduce` holds every line at EXPO 0 with neither wash.

When the page loads, the pigeon fades in first. Every line starts in that thin bottom state and eases into the weight for where it sits, beginning only after the bird has arrived. The lines run in order down the page. Each one eases in slowly, with a short pause before the next. Reduced motion skips the entrance.

Link underlines are a rounded bar under the words, sitting close to the letters. The same scroll value sets the thickness: a heavy bar at the top of the window, and 0.1px at the bottom. Hovering a link leaves the letters as they are. The underline thickens and drops a little, then returns when the pointer leaves. That move takes about 160ms.

## Header

A spinning pigeon sits above the words and fades in before the first line. `darken` drops the white field into the cream page, so only the bird shows. The header has `18vh` of space above it, which puts “Grant and Annie” near the vertical center when the page opens.

## Links

Linked, not embedded. R.S.V.P. is “Répondez S’il” and “Vous Plaît”, opening https://form.typeform.com/to/afrsCaCx in a new tab. “Our registry” opens https://www.zola.com/wedding/reedsmartin/registry in a new tab. “Email us” is last. It is a `mailto:grantandannie2026@gmail.com` link and stays in the same tab.
