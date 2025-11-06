````markdown
# Webpack Template

## Description

Webpack template for a quicker start to development when using Webpack.

This template handles:

- HTML
- CSS
- JavaScript
- Images
- Fonts
- Webpack Dev Server
- Jest testing

## Installation Instructions

1. Clone this repo:

   ```bash
   git clone https://github.com/Blakem07/webpack-template.git
````

2. Install dependencies:

   ```bash
   npm install
   ```

## Usage

### Build and Serve

To rebundle:

```bash
npx webpack
```

To run on a live server:

```bash
npx webpack serve
```

### Run Dev Workflow (Webpack + Tests)

You can run the dev server and Jest tests side by side using:

```bash
npm run dev
```

This uses `concurrently` to run both the webpack-dev-server and Jest in watch mode.

## Testing with Jest

A simple placeholder test is included in `src/tests/example.test.js`:

```js
test('this test always passes', () => {
  expect(true).toBe(true);
});
```

To run tests separately:

```bash
npm test
```

## Using Images and Videos

This template supports loading image and video files via Webpack’s `asset/resource` module type.

### Importing in JavaScript

You can import image and video files directly into your JavaScript.

#### Image Example:

```js
import logo from "./assets/logo.png";

const img = document.createElement("img");
img.src = logo;
document.body.appendChild(img);
```

#### Video Example:

```js
import introVideo from "./assets/intro.mp4";

const video = document.createElement("video");
video.src = introVideo;
video.autoplay = true;
video.loop = true;
video.muted = true;
document.body.appendChild(video);
```

### Supported Formats

**Images:**

* `.png`
* `.jpg`, `.jpeg`
* `.gif`
* `.svg`
* `.webp`

**Videos:**

* `.mp4`
* `.webm`
* `.ogg`

### Alternative: Static Assets via `public/`

For assets you don’t want bundled (e.g., logos or demo videos), you can place them in the `public/` folder. These will be served statically.

#### Example (in HTML):

```html
<img src="/logo.png" alt="Logo" />

<video src="/intro.mp4" autoplay loop muted></video>
```

Use this method if you prefer to reference files directly in HTML or keep them outside the Webpack build pipeline.
