## settings.json
* activate "Developer: Inspect Editor Tokens and Scopes"
* click on element and look for "semantic token type: xxx"
* edit `settings.json` and add styles
* example: turn on/off underlines of all mutable and make function parameters and comments italics
```
"editor.semanticTokenColorCustomizations": {
	"rules": {
		"parameter": {
			"fontStyle": "italic"
		},
		"comment": {
			"fontStyle": "italic"
		},
		"*.mutable": {
			"underline": false,
		},
		"property": {
			"fontStyle": "italic",
			"foreground": "#8fc9d9"
		},
		"namespace": {
			"foreground": "#67a0b0"
		},
		"enumMember": {
			"foreground": "#60c07e"
		},
	}
},
```