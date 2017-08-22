JavaScript-SQL Syntax
=====================

## Purpose
We heavily use SQL-Template-Strings (https://github.com/felixfbecker/node-sql-template-strings) but queries are not colored. This syntax allow SQL syntax highlighting in code like :

```js
var query = SQL`
    SELECT *
    FROM table
    where id = 1
`;
```

## Installation
1. Create a new syntax with `Tools -> Developer -> New Syntax...`
2. Delete the exemple code
3. Copy everything from the file js-sql.sublime-syntax in the oppened window
4. Save as js-sql.sublime-syntax

## Sublime-linter
Map the js-sql language definition to javascript in order to enable all js linters (jshint, eshint, jscs, etc) with js-sql syntax.

Open `Preferences -> Package Settings -> SublimeLinter -> Settings - User` and add the key-value entry `"js-sql": "javascript"` to the syntax_map object.

So now the default syntax_map object is:

```json
"syntax_map": {
    "html (django)": "html",
    "html (rails)": "html",
    "html 5": "html",
    "php": "html",
    "python django": "python",
    "js-sql": "javascript"
}
```

## Usage
1. Open a js file
2. `Ctrl+Shift+P` and type `SetSyntax: javascript-sql` or `ssjssql`

Sublime Text memorize this choice and will open all js files with js-sql syntax by default.


## License
MIT License. Copyright 2017 Asterisque Digital
