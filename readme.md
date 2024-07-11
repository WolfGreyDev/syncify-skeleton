<!-- replace with your own-->
# Syncify Skeleton

This repo aims to provide a starting point for your next Shopify theme using [panoply/syncify](https://github.com/panoply/syncify/tree/major).

## Why this is needed ##

Syncify's development has gone through some changes on it's major branch. These changes have left some of the documentation outdated, in particular the initial setup stage. I've worked with [panoply](https://github.com/panoply) (Sissel) on the Shopify Developers Discord to get Syncify working using the "best" undocumented method.

## Installation

> Be sure to check out the [official Syncify repo](https://github.com/panoply/syncify/tree/major) for more advanced uses.

> This repo uses a slightly modified version of the Dusk theme also created by panoply.

1. Press the "Use this template" button at the top of this repo to create a new repo with the contents of this skeleton. Set it to private if it's for a client. You can now clone your new repo to your local machine.
2. Setup your Authorization. See the [official Syncify repo](https://github.com/panoply/syncify/tree/major) for instructions.
    1. Create an app for your store with the appropriate scopes. [Instructions](https://github.com/panoply/syncify?tab=readme-ov-file#setup)
    2. Rename the `.env.example` to `.env` then add your store name and API token to the appropriate places. [Instructions](https://github.com/panoply/syncify?tab=readme-ov-file#credentials)
    3. In your `package.json`, replace all `your-shopify-store` references with the Shopify store name you set in your `.env` file.
3. Run `pnpm i` to quick install Syncify dependencies. Below is an itemized list.
    * `pnpm add github:panoply/syncify#major -D` to install the major branch.
    * `pnpm add @syncify/turndown -D` a required dependency of Syncify.
    * `pnpm add esbuild -D` required to build your theme.
    * (Optional) `pnpm add svgo -D` and `pnpm add svg-sprite -D` to handle SVG's, the logo in this case.
4. Run `pnpm build`. This will create a new directory called `theme` in the standard Shopify theme structure.
5. Package the `theme` folder and manually upload the `.zip` file to your store.
    * On Mac, navigate to the project folder, right click on the `theme` folder and select `compress "theme"`.
    > Syncify can export the output directory and zip it with the `-p` or `--package` flags, but this functionality isn't working yet.
6. Add the theme ID to your `package.json` under `stores.themes.dev`.
    > To get your theme id, customize the theme via the Shopify Theme Editor and copy the theme ID, located in the address bar.
7. Run `pnpm dev` to start your first live reloading session and open the preview link provided in your terminal. Make a change to your `/source/layout/theme.liquid` and confirm you see your change in your browser.

### Notes
- If you're having issues connecting to your theme, ensure that you've followed the Setup and Credential steps outlined in the [official Syncify repo](https://github.com/panoply/syncify?tab=readme-ov-file#setup). Then check your `.env` file and finally your `package.json` file to make sure everything matches.
- If you're using `pnpm dev` and you're unable to hot reload, try changing browsers or disable any browser functionality that may be blocking your websocket connection (eg. Brave Shield). As a last resort, restart your machine, this has worked for me in the past.
- I use the VSCode extension [Liquid](https://marketplace.visualstudio.com/items?itemName=sissel.shopify-liquid) and **you should too**. This repo is already set up for your project auto-completions and basic formatting (which you can change). You can customize these settings in the `.liquidrc` file.
- If you're still having issues, head over to the [Shopify Developers Discord](https://discord.gg/bU3P5TPE) where we have a dedicated channel for Syncify stuff. **Don't be dumb! Complete the application form properly otherwise you'll be banned instantly.**

## Contributing

This repo isn't intended to be contributed to. As updates happen to Syncify this repo will be updated appropriately however, Syncify will eventually make this repo obsolete.

## Credits

- [ΝΙΚΟΛΑΣ / Sissel](https://github.com/panoply)
- [Shopify Developer Discord](https://discord.gg/bU3P5TPE)

## License

The MIT License (MIT). Please see [License File](license.md) for more information.
<!--/replace with your own-->