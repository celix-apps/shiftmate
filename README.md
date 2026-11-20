# ShiftMate website

Static landing page for ShiftMate (Android and iOS), served by GitHub Pages at
https://celix-apps.github.io/shiftmate/

- `index.html`: one page in 17 languages (Arabic right-to-left) (language from `?lang=`, the saved choice or the browser).
  Texts and screenshots come from the Google Play store listing (`play_store/store_listing.md` in the
  Android repo); regenerate the page from there instead of editing the texts by hand.
- Images are made with `tools/website/site_images.py` in the Android repo:
  - `img/<lang>/01.jpg … 08.jpg`: Google Play screenshots, 1080×1920 (`t/` = 480 px previews for the gallery).
  - `img/ios/<lang>/01.jpg … 08.jpg`: App Store 6.9" screenshots, 1080×2340 (`t/` = previews). Shown when the
    iPhone tab is selected (default on iPhone/iPad, `?p=ios|android`, remembered).
  - `img/widgets/<android|ios>/<lang>/{large,earn,today,leave}.webp`: widgets for the Widgets section. iOS ones are
    cut from 07_Widgets; Android ones come from the raw widget captures of the Play screenshot tooling.
  - `img/ios/extras/<en|tr>/{island,lockcard}.jpg`: Dynamic Island and Lock Screen close-ups (iPhone only).

The App Store button links to https://apps.apple.com/app/id6764603778 (storefront-neutral, redirects to the visitor's country).
- `support/index.html`: help page in 17 languages. The English text is inline; every translatable element has a
  `data-i` key and `support/i18n/<lang>.json` holds the same keys (HTML kept as in English, menu paths taken from
  the app's own strings). When an English answer changes, update the same key in every JSON file.
