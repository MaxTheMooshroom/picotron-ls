# Picotron Language Server

<!--
[![VS Marketplace installs](https://badgen.net/vs-marketplace/i/PollywogGames.pico8-ls?label=VS%20Marketplace%20installs)](https://marketplace.visualstudio.com/items?itemName=PollywogGames.pico8-ls)
[![VS Marketplace downloads](https://badgen.net/vs-marketplace/d/PollywogGames.pico8-ls?label=VS%20Marketplace%20downloads)](https://marketplace.visualstudio.com/items?itemName=PollywogGames.pico8-ls)
-->

Full language support for the [Picotron](https://www.lexaloffle.com/picotron.php) dialect of Lua.

The goal is to have all the features you'd expect in a full-fledged language
server, such as [the one for Lua](https://marketplace.visualstudio.com/items?itemName=sumneko.lua),
but specifically tailored for a frictionless Picotron development experience.

Picotron extends the [PICO-8](https://www.lexaloffle.com/pico-8.php) environment. Support for
Picotron ***must*** begin with support for PICO-8. That's why this project is forked from
[pico8-ls](https://github.com/japhib/pico8-ls), as they've already done most of the legwork
for pico-8 support.

## Feature highlights

View docs on hover, then auto-complete and signature help:

![docs gif](https://github.com/japhib/pico8-ls/blob/master/img/docs.gif?raw=true)

## TODO

- [X] Pico-8 support
	- [X] Syntax highlighting
	- [X] Syntax errors
	- [X] Warnings on undefined variable usage
	- [X] Find symbol in document
	- [X] Go to definition
	- [X] Find references
	- [X] Hover support & signature help for built-in functions
	- [X] Auto-completion
	- [X] Snippets for common idioms (functions, loops, etc) as well as pico-8 symbols (`p8-jelpi` -> 🐱, `p8-x-key` -> ❎, etc)
	- [X] Code formatting
- [ ] Lua 5.4 Support
	- [ ] (WIP) Operator Support
		- [X] Regex Update
		- [ ] Update `server/src/parser/operators.ts`
		- [ ] Update `server/src/parser/lexer.ts`
- Picotron Support
	- [ ] (WIP) Operator Support
		- [X] Regex Update
		- [ ] Update `server/src/parser/operators.ts`
		- [ ] Update `server/src/parser/lexer.ts`
	- [ ] Generate `server\src\parser\builtins.ts` from a TOML file rather than content found on [pico-8's fandom wiki](https://pico-8.fandom.com/wiki/Pico-8_Wikia)
	- [ ] add include support back in, but as a function rather than a preprocessor macro
	- [ ] add support for picotron's cartridges as virtual directories

## Support for other platforms

This extension uses the [Language Server Protocol](https://microsoft.github.io/language-server-protocol/),
so while it's mainly made for VSCode, it could also be used for other editors
such as NeoVim, Atom, etc.

I don't have any experience setting up language extensions for platforms other than VSCode, so currently
looking for help with that. See tips and support thread on the issue for various editors:
- [Neovim](https://github.com/japhib/pico8-ls/issues/34)
- [Sublime Text](https://github.com/japhib/pico8-ls/issues/44)

## Changelog

[Changelog has been moved to a separate file.](https://github.com/japhib/pico8-ls/blob/master/CHANGELOG.md)

## Development

Please follow the official [Language Server Extension Guide](https://code.visualstudio.com/api/language-extensions/language-server-extension-guide)
to understand how to develop VS Code language server extension.

## Credits

PICO-8 Lua parser based on https://github.com/fstirlitz/luaparse (heavily updated & ported to Typescript by @japhib)

[PICO-8](https://www.lexaloffle.com/pico-8.php) by Lexaloffle Games
