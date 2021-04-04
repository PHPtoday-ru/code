![](https://badgen.net/badge/Editor.js/v2.0/blue)

# CodeMirror Tool for Editor.js

CodeMirror Tool for the [Editor.js](https://ifmo.su/editor) allows to include code examples in your articles using [CodeMirror](http://codemirror.net/) code editor.

## Installation

### Install via NPM

Get the package

```shell
npm i --save-dev https://github.com/PHPtoday-ru/editorjs-codemirror:^1.0.0
```

Include module at your application

```javascript
const CodeMirrorTool = require('editorjs-codemirror');
```

### Download to your project's source dir

1. Upload folder `dist` from repository
2. Add `dist/bundle.js` file to your page.

## Usage

Add a new Tool to the `tools` property of the Editor.js initial config.

```javascript
var editor = EditorJS({
  ...
  
  tools: {
    ...
    code: {
        class: CodeMirrorTool,
        config: {
            cm: {
                //... codemirror config
            }
        }
    },
  }
  
  ...
});
```

## Output data

This Tool returns code.

```json
{
    "type" : "code",
    "data" : {
        "code": "body {\n font-size: 14px;\n line-height: 16px;\n}",
        "language": "php"
    }
}
```

