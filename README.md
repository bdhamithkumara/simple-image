![](https://badgen.net/badge/Editor.js/v2.0/blue)

# Simple Image Tool

Provides Image Blocks for the [Editor.js](https://editorjs.io).

Works only with pasted image URLs and requires no server-side uploader.

![](assets/image-uploading.gif)

## Installation

### Install via NPM

Get the package

```shell
npm i --save-dev @editorjs/simple-image
```

Include module at your application

```javascript
const SimpleImage = require('@editorjs/simple-image');
```
OR
```javascript
import SimpleImage from '@editorjs/simple-image'
```

### Download to your project's source dir

1. Upload folder `dist` from repository
2. Add `dist/bundle.js` file to your page.

### Load from CDN

You can load specific version of package from [jsDelivr CDN](https://www.jsdelivr.com/package/npm/@editorjs/simple-image).

`https://cdn.jsdelivr.net/npm/@editorjs/simple-image@latest`

Then require this script on page with Editor.js.

```html
<script src="..."></script>
```

## Usage

Add a new Tool to the `tools` property of the Editor.js initial config.

```javascript
var editor = EditorJS({
  ...
  
  tools: {
    ...
    image: SimpleImage,
  }
  
  ...
});
```
## How to insert an image

**Note:** There is no insert icon for this package. To insert an image, you need to drag and drop the image (GIF/JPEG/JPG/PNG/SVG/WEBP) into the editor.

**Steps:**

1. Open the editor.
2. Drag and drop the image into the editor.
3. The image will be inserted into the editor at the current cursor position.
4. You can then Add Border, Stretch Image and Add Background the image as needed.

## Config Params

This Tool has no config params

## Tool's settings

![](https://capella.pics/c74cdeec-3405-48ac-a960-f784188cf9b4.jpg)

1. Add border

2. Stretch to full-width

3. Add background

## Output data

| Field          | Type      | Description                     |
| -------------- | --------- | ------------------------------- |
| url            | `string`  | image's url                     |
| caption        | `string`  | image's caption                 |
| withBorder     | `boolean` | add border to image             |
| withBackground | `boolean` | need to add background          |
| stretched      | `boolean` | stretch image to screen's width |


```json
{
    "type" : "image",
    "data" : {
        "url" : "https://www.tesla.com/tesla_theme/assets/img/_vehicle_redesign/roadster_and_semi/roadster/hero.jpg",
        "caption" : "Roadster // tesla.com",
        "withBorder" : false,
        "withBackground" : false,
        "stretched" : true
    }
}
```
