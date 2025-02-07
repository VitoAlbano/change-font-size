![](https://badgen.net/badge/Editor.js/v2.0/blue)

# ChangeFontSize Tool

Change font size for the [Editor.js](https://ifmo.su/editor).
This version is CommonJS compatible.




## Installation

### Install via NPM

Get the package

```shell
npm i --save-dev @valano/change-font-size
```

Include module at your application

```javascript
const ChangeFontSize = require('@valano/change-font-size');
```

### Download to your project's source dir

1. Upload folder `dist` from repository
2. Add `dist/editor.change-font-size.js` file to your page.

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
    plus10percent: {
      class: ChangeFontSize,
    },
	  plus20percent: {
	    class: ChangeFontSize,
	    config: {
					cssClass: "plus20pc",
					buttonText: "20%"
				}
			},
  },
  
  ...
});
```

## Config Params

| Param     | Type     | Description      |
| --------- | -------- | -----------------|
| cssClass     | `string` | This class will be added to the tag `span`.  |
| buttonText   | `string` | Text for toolbar. |
| buttonIcon   | `string` | Content for the button. For example svg. |

## Output data

Marked text will be wrapped with a `span` tag with class.

```json
{
    "type" : "text",
    "data" : {
        "text" : "Create a directory for your module, enter it and run <span class=\"plus20pc\">npm init</span> command."
    }
}
```

