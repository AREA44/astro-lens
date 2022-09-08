# Astro Lens

[![Netlify Status](https://api.netlify.com/api/v1/badges/7385ada4-e9d1-449e-9ab0-49602dee4211/deploy-status)](https://app.netlify.com/sites/astro-lens/deploys)

This is **Lens**, a full screen (and entirely responsive) photo gallery design.

## Commands

All commands are run from the root of the project, from a terminal:

| Command           | Action                                       |
| :---------------- | :------------------------------------------- |
| `npm install`     | Installs dependencies                        |
| `npm run dev`     | Starts local dev server at `localhost:3000`  |
| `npm run build`   | Build your production site to `./dist/`      |
| `npm run preview` | Preview your build locally, before deploying |

## How it works

### Thumnail

Just add your thumbnails to the thumbnails section in [`index.astro`](src/pages/index.astro) in the following format:

```ts
<Thumnail
  title="Title"
  href="path/to/images/image.jpg"
  description="Description"
/>
```

<!---
### The `data-position`

As a full screen experience, the viewer will be subject to changes in its size and, consequently, its aspect ratio. Since your full size images are basically applied as backgrounds to the viewer itself, this means they'll probably (okay, definitely) get cropped. All is not lost, however, as you can use the optional `data-position` attribute to control how the full size image is positioned within the viewer. To do this, simply add it to your thumbnail's `<a>` element and set it to any valid `background-position` value. For example, this:

```ts
<Thumnail
  title="Title"
  href="path/to/images/image.jpg"
  description="Description"
  data-position="top left"
/>
```

positions this particular full size image in the top left corner of the viewer (as opposed to its center, the default), effectively limiting cropping to everything but the top left corner.
-->

### Keyboard shortcuts

**Lens** is set up to respond to the following keyboard shortcuts:

- Left Arrow: Go to previous image.
- Right Arrow: Go to next image.
- Up Arrow: Go to image above the current one in the thumbnails section.
- Down Arrow: Go to image below the current one in the thumbnails section.
- Space: Go to next image.
- Escape: Toggle the main wrapper.

> Note: All keyboard shortcuts are disabled when the "xsmall" breakpoint is active (since they don't really make a whole lot of sense there).

### Other stuff

- The main wrapper can be moved to the left by changing the `misc.main-side` in [`main.js`](public/js/main.js).

## License

**Lens** by [HTML5 UP](https://html5up.net). Free for personal and commercial use under the [CCA 3.0](https://html5up.net/license) license.

## Credits

- Demo images by [Unsplash](https://unsplash.com)
- Icons by [Font Awesome](https://fontawesome.io)
- [jQuery](https://jquery.com)
