---
title: Recommended Settings
---

There are some settings in VS Code that you may wish to change from the defaults for a better experience editing Flutter code. You can set these globally by adding the below JSON to your VS Code User Settings or apply the Dart-specific ones by running the **Dart: Use Recommended Settings** command.

```js
{
	// Causes the debug view to automatically appear when a breakpoint is hit. This
	// setting is global and not configurable per-language.
	"debug.openDebug": "openOnDebugBreak",

	"[dart]": {
		// Automatically format code on save and during typing of certain characters
		// (like `;` and `}`).
		"editor.formatOnSave": true,
		"editor.formatOnType": true,

		// Draw a guide line at 80 characters, where Dart's formatting will wrap code.
		"editor.rulers": [80],

		// Disables built-in highlighting of words that match your selection. Without
		// this, all instances of the selected text will be highlighted, interfering
		// with Dart's ability to highlight only exact references to the selected variable.
		"editor.selectionHighlight": false,

		// By default, VS Code prevents code completion from popping open when in
		// "snippet mode" (editing placeholders in inserted code). Setting this option
		// to `false` stops that and allows completion to open as normal, as if you
		// weren't in a snippet placeholder.
		"editor.suggest.snippetsPreventQuickSuggestions": false,

		// By default, VS Code will pre-select the most recently used item from code
		// completion. This is usually not the most relevant item.
		//
		// "first" will always select top item
		// "recentlyUsedByPrefix" will filter the recently used items based on the
		//     text immediately preceeding where completion was invoked.
		"editor.suggestSelection": "first",

		// Allows pressing <TAB> to complete snippets such as `for` even when the
		// completion list is not visible.
		"editor.tabCompletion": "onlySnippets",

		// By default, VS Code will populate code completion with words found in the
		// current file when a language service does not provide its own completions.
		// This results in code completion suggesting words when editing comments and
		// strings. This setting will prevent that.
		"editor.wordBasedSuggestions": false,

		// Force all files to have a trailing newline for consistency and reduced diffs
		// when adding new lines at the bottom of the file.
		"files.insertFinalNewline": true,
	}
}
```
