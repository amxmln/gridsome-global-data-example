# Default starter for Gridsome

This is the project you get when you run `gridsome create new-project`.

This repo was created to illustrate an issue as described in [this](https://github.com/gridsome/gridsome/issues/1136) Issue on
GitHub.

### Instructions for Reproduction

1. Clone and install dependencies
2. Run with `npm run develop`
3. Check out the site, the `/` has a light nav, `/about/` and `/example/` have
  a dark nav
4. Cancel the dev server and run `npm run build`
5. Serve the `dist/` folder with `python3 -m http.server --directory dist/` or
  a similar lokal server
6. Check out the site, `/` has a dark nav, even though it shouldn’t. Once another
  route was navigated to, everything returns to order.
7. Check the generated `index.html` in `dist/` and see that the nav-Element
  indeed has the "dark" class applied

### Expected result

The generated pages have the same Markup as in development, i.e. the "dark"
class is only present on pages with `"dark": true` in their respective JSON-File.
