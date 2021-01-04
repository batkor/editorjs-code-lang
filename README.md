Node: This a fork of Code Tool for the [Editor.js](https://github.com/paraswaykole/editor-js-code)
that allows to include code examples along with language codes that are supported by PrismJs in your articles.


![](https://badgen.net/badge/Editor.js/v2.0/blue)

# Code Tool for Editor.js with language selector

![](https://capella.pics/7a1092f7-add5-4dd8-9c8c-2f32cb8c4586.jpg)

The list of languages supported is in [languages.txt](languages.txt)

## Installation

### Download to your project's source dir

1. Upload folder `dist` from repository
2. Add `dist/bundle.js` file to your page.

### Load from CDN

You can load latest version of this package from jsDelivr CDN.

`https://cdn.jsdelivr.net/gh/paraswaykole/editor-js-code@latest/dist/bundle.js`

Require this script on a page with Editor.js.

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
    code: CodeTool,
  }

  ...
});
```

## Config Params

| Field       | Type     | Description                    |
| ----------- | -------- | -------------------------------|
| placeholder | `string` | Code Tool's placeholder string |

## Output data

This Tool returns code.

```json
{
    "type" : "code",
    "data" : {
        "code": "body {\n font-size: 14px;\n line-height: 16px;\n}",
        "languageCode": "css"
    }
}
```

