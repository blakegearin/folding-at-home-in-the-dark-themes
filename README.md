# FOLDING AT HOME IN THE DARK Themes

These are additional themes developed for the FOLDING AT HOME IN THE DARK browser extension.

## Usage

1. Find the extension's [directory](https://stackoverflow.com/a/14544700)
1. Duplicate it
1. Add the `.css` files under `assets/css/team` to the same location in the duplicated directory
1. Update the `fah_custom.html` file to make the themes selectable
   1. Search for `box-theme-id`
   1. Locate this line:

      ```html
      <option value="">Default Theme</option>
      ```

   1. After it, add the following lines

      ```html
      <option value="assets/css/team/original_light.css">Original Light</option>
      <option value="assets/css/team/original_dark.css">Original Dark</option>
      ```

1. Update the `fah.js` file to ensure the "Team" section doesn't disappear

   1. Search for `function update_theme_style_rollover`
   1. Find this bit of code:

        ```js
        themestylecss == "" || themestylecss == undefined
        ```

   1. Replace it with this code:

        ```js
        ["", undefined].includes(themestylecss) || themestylecss.includes("original")
        ```

1. Open the [extensions manager](https://support.google.com/chrome_webstore/answer/2664769#cke_bm_1361S)
1. Enable "Developer Mode" in the top right corner
1. Find the existing extension installation and disable or remove it
1. Click the "Load Unpacked" button
1. Select your updated, duplicated directory

## Links

- [extension](https://chromewebstore.google.com/detail/folding-at-home-in-the-da/alpjkkbjnbkddolgnicglknicbgfahoe)
- [Folding.LAR.systems](https://folding.lar.systems)
