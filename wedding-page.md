# Wedding page

The site is `index.html` at the root of the repository. Open that file directly in a browser, or serve the repository with GitHub Pages.

GitHub Pages: in the repository settings, choose Deploy from a branch, branch `main`, folder `/ (root)`. Until a custom domain is attached, the page is at https://begodfrey.github.io/grantandannie/. When you have the domain, add a `CNAME` file whose only line is that domain. `.nojekyll` is in the repo so Pages serves the file as-is.

## Font

Exposure Trial VAR italic, the italic file you supplied, embedded as base64. The roman cut has no slant axis, so the page uses the italic, which leans about 16 degrees and has the same `EXPO` axis, from -100 to 100. This cut is a 205TF trial: a short character set, for testing a layout, not a license to publish the font.

The trial has no straight apostrophe, so “s’il” uses a typographic apostrophe. Every line is set in capitals with CSS.

## Layout

The lines stay fixed:

GRANT AND ANNIE
ARE GETTING MARRIED
JOIN US IN
CELEBRATION
IN DECEMBER
RÉPONDEZ
S’IL VOUS PLAÎT
OUR REGISTRY
EMAIL US

The type stops growing once the window is wider than 800px, and the column stays centered. A top margin places “Grant and Annie” on the vertical center of the window when the page opens. The bottom padding is a little more than one screen, so the last line can be scrolled to the top.

## Scroll

On scroll, each line’s distance from the middle of the window sets `EXPO`: 100 at the top, 0 at the center, -100 at the bottom. Toward 100 the ink mixes into the paper and a paper-colored shadow eats the letter edges, so the words sink into the background. Toward -100 that reverses: the letters pick up an ink-colored glow and a slight stroke, so the heavy end of the axis reads even blacker. `prefers-reduced-motion: reduce` holds every line at EXPO 0 with neither wash.

Link underlines are a rounded bar under the words, sitting close to the letters. The same scroll value sets the thickness: 0.1px at the top of the window, and a much heavier bar at the bottom.

## Header

The sculpture sits above the words. A color filter lifts the black field to gray and softens the highlights, so the photograph reads as a faded plate on the cream page. It is not inverted.

## Links

Linked, not embedded. R.S.V.P. is “Répondez / s’il vous plaît”, shown in capitals, opening https://form.typeform.com/to/afrsCaCx in a new tab. “Our registry” opens https://www.zola.com/wedding/reedsmartin/registry in a new tab. “Email us” is last. It is a `mailto:grantandannie2026@gmail.com` link and stays in the same tab.
