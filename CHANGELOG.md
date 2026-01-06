2.4.0 (unreleased)

- Support a Vimium new tab experience: the browser can be configured to open a blank Vimium page as
  the new tab page. In Vimium's settings, the Vomnibar can configured to open on new tabs. See
  [instructions](https://github.com/philc/vimium?tab=readme-ov-file#how-to-allow-vimium-to-work-on-new-tab-pages).
  (https://github.com/philc/vimium/pull/4795)
- Make Google search result links work on sub-tabs like "Web".
  (https://github.com/philc/vimium/issues/4750)
- Add command "LinkHints.activateModeToCopyCleanLinkUrl" to copy a cleaned link URL (without query/hash) via Link Hints.
  - New hint mode: "clean-link" copies only `origin + pathname` for anchors.
  - New NormalMode binding so custom mappings (e.g., `map yF LinkHints.activateModeToCopyCleanLinkUrl`) execute.
  - Docs updated to include a sample mapping in README.

2.3.1 (2025-11-12)

- Fix Vimium to work with Chrome 144. (https://github.com/philc/vimium/issues/4785)

2.3.0 (2025-06-30)

- Add a command listing page, which documents all commands and their options. Access it
  [on the web](https://vimium.github.io/commands/), or from the Vimium Options page > Show available
  commands.
- Some internal CSS classes were changed for Vimium's UI. This may affect those who have customized
  Vimium's CSS via the options page. (https://github.com/philc/vimium/issues/4668)
- Breaking change: when creating a mapping for `setZoom`, a `level` argument is now required. E.g.:
  `map z2 setZoom level=2.0`.
- Make `Vomnibar.activateBookmark` accept a `query` option.
  (https://github.com/philc/vimium/pull/4591)
- Fix `openCopiedUrlInCurrentTab` doesn't launch search queries.
  (https://github.com/philc/vimium/issues/4657)
- Make `openCopiedUrlInCurrentTab` accept a `position` option.
- Update `goPrevious` and `goNext` commands to handle google.com's new layout.
  (https://github.com/philc/vimium/issues/4650)
- Add a "hide update notifications" option for silencing "Vimium has been updated" notifications.
  (https://github.com/philc/vimium/issues/4346)
- Use dark mode styles in the HUD when the browser is in dark mode.
- Bug fixes.

2.2.1 (2025-03-20)

- Fix findSelected and findSelectedBackwards commands (https://github.com/philc/vimium/issues/4655)
- Fix openCopiedUrlInCurrentTab (https://github.com/philc/vimium/issues/4654)

2.2.0 (2025-03-08)

- Use the browser's default search engine. [(#2598)](https://github.com/philc/vimium/issues/2598)
- Add "reload hard" command (R). ([#4445](https://github.com/philc/vimium/pull/4445)).
- Add zoomIn (zi), zoomOut (zo), zoomReset (z0), and setZoom commands.
  ([#4488](https://github.com/philc/vimium/pull/4488))
- Add findSelected and findSelectedBackwards commands.
  ([#4502](https://github.com/philc/vimium/pull/4502))
- Options page: improve UI, add error validation.
- Make tab commands handle Firefox hidden tabs.
- Bug fixes.

2.1.2 (2024-04-03)

- Better fix for Vomnibar doesn't always list tabs by recency.
  ([#4368](https://github.com/philc/vimium/issues/4368))
- Add a workaround to make link hints work on Github Enterprise.
  ([#4446](https://github.com/philc/vimium/issues/4446))
- Fix position=end is ignored in createTab command
  ([#4450](https://github.com/philc/vimium/issues/4450))

2.1.1 (2024-03-29)

- Fix exclusion rule popup not working. ([#4447](https://github.com/philc/vimium/issues/4447))

2.1.0 (2024-03-27)

- Fix Vomnibar doesn't always list tabs by recency.
  ([#4368](https://github.com/philc/vimium/issues/4368))
- Better domain detection in the Vomnibar ([#3268](https://github.com/philc/vimium/issues/3268))
- Exclude keys based on the top frame URL, not a subframe's URL. This fixes many cases where the
  excluded keys feature didn't seem to work. ([#4402](https://github.com/philc/vimium/issues/4402))
- After selecting a link, if ESC is pressed, mouse out of the link. With this, Wikipedia's and
  Github's link preview popups can be dismissed after following a link.
  ([#3073](https://github.com/philc/vimium/issues/3073))
- Fix link hints do not appear for links inside of github's popups. This fix is available on Chrome
  114+, and soon Firefox. ([#4408](https://github.com/philc/vimium/issues/4408))
