# shapez.io

<img src="https://i.imgur.com/Y5Z2iqQ.png" alt="shapez.io Logo">

This is the source code for shapez.io, an open source base building game inspired by Factorio.
Your goal is to produce shapes by cutting, rotating, merging and painting parts of shapes.

-   [Trello Board & Roadmap](https://trello.com/b/ISQncpJP/shapezio)
-   [Free web version](https://shapez.io)
-   [itch.io Page](https://tobspr.itch.io/shapezio)
-   [Steam Page](https://steam.shapez.io)
-   [Official Discord](https://discord.com/invite/HN7EVzV) <- _Highly recommended to join!_

## Building

-   Make sure git `git lfs` extension is on your path
-   Run `git lfs pull` to download sound assets
-   Make sure `ffmpeg` is on your path
-   Install Yarn and Node.js 10
-   Run `yarn` in the root folder, then run `yarn` in the `gulp/` folder
-   Cd into `gulp` and run `yarn gulp` - it should now open in your browser

**Notice**: This will produce a debug build with several debugging flags enabled. If you want to disable them, modify `config.js`.

## Helping translate

Please checkout the [Translations readme](translations/).

## Contributing

Since this game is in the more or less early development, I will only accept pull requests which add an immediate benefit. Please understand that low quality PR's might be closed by me with a short comment explaining why.

**If you want to add a new building, please understand that I can not simply add every building to the game!** I recommend to talk to me before implementing anything, to make sure its actually useful. Otherwise there is a high chance of your PR not getting merged.

If you want to add a new feature or in generally contribute I recommend to get in touch with me on Discord:

<a href="https://discord.com/invite/HN7EVzV" target="_blank">
<img src="https://i.imgur.com/SoawBhW.png" alt="discord logo" width="100">
</a>

### Code

The game is based on a custom engine which itself is based on the YORG.io 3 game egine (Actually it shares almost the same core).
The code within the engine is relatively clean with some code for the actual game on top being hacky.

This project is based on ES5. Some ES2015 features are used but most of them are too slow, especially when polyfilled. For example, `Array.prototype.forEach` is only used within non-critical loops since its slower than a plain for loop.

### Assets

For most assets I use Adobe Photoshop, you can find them in `assets/`.

You can use the Texture Packing python script in [res_pipeline](/res_pipeline) to generate packed textures. Default builds over [res_built/atlas](/res_built/atlas). Requires [free-tex-packer-cli](https://github.com/odrick/free-tex-packer-cli). Thanks to [Theisen1337](https://github.com/theisen1337) for intergrating.


<img src="https://i.imgur.com/W25Fkl0.png" alt="shapez.io Screenshot">
