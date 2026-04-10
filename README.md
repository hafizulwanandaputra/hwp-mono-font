# HWP Mono Font Family

HWP Mono is a font created based on the [Iosevka](https://github.com/be5invis/Iosevka) font using [Iosevka Customizer](https://typeof.net/Iosevka/customizer) inherited from ss06 variant. This is the updated font from previous name, Iosevka HWP, which had to be removed because the previous font name contained Reserved Font Name (RFN) which violates the SIL Open Font License v1.1. This font family includes sans serif family (HWP Sans Mono) and serif family (HWP Serif Mono) with only monospace variant.

## About Iosevka

**Iosevka** [ˌjɔˈseβ.kʰa] is an _open-source_, _sans-serif_ + _slab-serif_, _monospace_ + _quasi‑proportional_ typeface family, designed for _writing code_, using in _terminals_, and preparing _technical documents_.

## Preview

<p align="center"> <img src="images/HwpMono.png" title="HWP Mono Grand Title"/> </p>

## Changes from Original `ss06` Iosevka Variant

1. Default width is set to 600
2. Modified variants for all variants which can be seen in the `.toml` files under `[buildPlans.FontName.variants]`.
3. Use discretionary ligatures for default ligatures.
4. Oblique variants were not included.
5. See `CHANGELOG.txt` for other changes.

## Downloads

Download fonts from these links below:

- [HWPweb (latest version only)](https://files.aku-hafizulwananda.com/HwpMono.zip)
- [GitHub Releases](https://github.com/hafizulwanandaputra/hwp-mono-font/releases)

## Build

Use Linux, Windows Subsystem for Linux (WSL), macOS, or other UNIX based operating systems to build the font.

To build the font, run:

    git clone --depth 1 https://github.com/be5invis/Iosevka.git
    cd Iosevka
    npm install
    curl -L -O https://files.aku-hafizulwananda.com/HwpMonoCompileTools.zip
    unzip HwpMonoCompileTools.zip
    ./build.sh

To save your CPU and RAM usage, insert the `jCmd` value when running `build.sh`.

[Click here](https://github.com/be5invis/Iosevka/blob/main/doc/custom-build.md) for more build instructions.

## Using the Font to the Web

To use this font for your website or web application project, use these configuration:

### HTML `<head>`

Specify the `href` to the correct location of the font face CSS inside the `HwpSansMono` and `HwpSerifMono` folder on your project.

- Hinted:

  ```
  <link rel="stylesheet" href="path/to/HwpSansMono/HwpSansMono.css">
  <link rel="stylesheet" href="path/to/HwpSerifMono/HwpSerifMono.css">
  ```

- Unhinted:

  ```
  <link rel="stylesheet" href="path/to/HwpSansMono/HwpSansMono-Unhinted.css">
  <link rel="stylesheet" href="path/to/HwpSerifMono/HwpSerifMono-Unhinted.css">
  ```

### CSS

    .class1 {
        font-family: "HWP Sans Mono Web", monospace;
    }

    .class2 {
        font-family: "HWP Serif Mono Web", monospace;
    }

### HTML `<body>`

    <p class="class1">Hello HWP Sans Mono</p>
    <p class="class2">Hello HWP Serif Mono</p>

### React.js and Vue.js

1. Copy `HwpSansMono` and `HwpSerifMono` folder into your project (e.g. `src/assets/fonts/`).
2. Import the font face CSS in the `src/index.js` file.
   - Hinted
     ```
     import './assets/fonts/HwpSansMono/HwpSansMono.css';
     import './assets/fonts/HwpSerifMono/HwpSerifMono.css';
     ```
   - Unhinted
     ```
     import './assets/fonts/HwpSansMono/HwpSansMono-Unhinted.css';
     import './assets/fonts/HwpSerifMono/HwpSerifMono-Unhinted.css';
     ```
3. Add the CSS in the `App.css` file.

   ```
   .class1 {
       font-family: 'HWP Sans Mono Web', monospace;
   }

   .class2 {
       font-family: 'HWP Serif Mono Web', monospace;
   }
   ```

4. Example of `App.js` on React.js.

   ```
   import React from 'react';
   import './App.css';

   function App() {
       return (
           <div>
               <p className="class1">Hello HWP Sans Mono</p>
               <p className="class2">Hello HWP Serif Mono</p>
           </div>
       );
   }

   export default App;
   ```

5. Example of `App.vue` on Vue.js.

   ```
   <template>
       <div>
           <p class="class1">Hello HWP Sans Mono</p>
           <p class="class2">Hello HWP Serif Mono</p>
       </div>
   </template>

   <script>
       export default {
           name: 'App'
       }
   </script>

   <style src="./App.css"></style>
   ```

## Contents

- HWP Sans Mono (18 hinted ttf, 18 unhinted ttf, 18 hinted woff, 18 unhinted woff, 2 CSS files)
- HWP Serif Mono (18 hinted ttf, 18 unhinted ttf, 18 hinted woff, 18 unhinted woff, 2 CSS files)

Total: 148 files

## Credits

This font is based on the Iosevka project.

## License

Released under the SIL Open Font License 1.1.  
See `LICENSE.txt` for details.
