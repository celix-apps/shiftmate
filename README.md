# ShiftMate website

Static landing page for ShiftMate (Android and iOS), served by GitHub Pages at
https://celix-apps.github.io/shiftmate/

- `index.html`: one page in 17 languages (Arabic right-to-left) (language from `?lang=`, the saved choice or the browser).
  Texts and screenshots come from the Google Play store listing (`play_store/store_listing.md` in the
  Android repo); regenerate the page from there instead of editing the texts by hand.
- `img/<lang>/01.jpg … 06.jpg`: the first six store screenshots per language, 720×1280.
- `img/ios/<lang>/01.jpg … 08.jpg`: the iPhone App Store screenshots (6.9"), 600×1300, shown when the
  iPhone tab is selected (default on iPhone/iPad). `img/ios/extras/<en|tr>/`: raw Lock Screen, Live Activity
  and Dynamic Island shots for the "Also on iPhone" section. Made with `tools/website/ios_images.py` from the
  iOS project's `AppStore_Screenshots/`.

The App Store button links to https://apps.apple.com/app/id6764603778 (storefront-neutral, redirects to the visitor's country).
- `support/index.html`: help page in 17 languages. The English text is inline; every translatable element has a
  `data-i` key and `support/i18n/<lang>.json` holds the same keys (HTML kept as in English, menu paths taken from
  the app's own strings). When an English answer changes, update the same key in every JSON file.
