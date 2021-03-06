# Contributing
If you wish to contribute a Library, simply submit a pull request to [Libraries.lua](https://github.com/RoStrap/Libraries/blob/master/Libraries.lua). Simply insert a new table with fields `URL` (you can leave off https://github.com) and an optional `Description` and you are good to go!

## Library Standards
Libraries contributed to RoStrap must be useful, reusable, and reasonably universal. The code must be stable, maintained, readable, and speedy. It must have a readme or documentation website that clearly outlines its use and includes functioning demo code. Images/Videos help.

Submitted Libraries may or may not be subject to code review.

All images must meet the [image standards](../Contributing/Image Standards)

## How to Package Libraries
To indicate to the plugin's installer that a Lua file is a descendant of another, simply make a folder with the name of the parent Lua file, and place the parent Lua file inside with the name "init" (or "main" or "_"). Here is [an example of a single Library that has ModuleScripts within it using this method.](https://github.com/evaera/EvLightning)

## Dependencies
Dependencies are detected by the plugin using [this handy script](https://github.com/RoStrap/Libraries/blob/GetDeps/GetDependencies.ignore.lua). It can detect from the following source code that `Tween` and `Maid` are the names a Library will need to have installed in order to work. If your source code intends to rely on dependencies from the RoStrap system, [the detection script](https://github.com/RoStrap/Libraries/blob/GetDeps/GetDependencies.ignore.lua) *must* be able to successfully determine the dependencies of your Libraries.

```lua
local ReplicatedStorage = game:GetService("ReplicatedStorage") -- You have to use game:GetService
local Resources = require(ReplicatedStorage:WaitForChild("Resources")) -- You have to use WaitForChild
local require = Resources.LoadLibrary -- You can localize LoadLibrary

local Tween = require("Tween") -- Either of these work
local Maid = Resources:LoadLibrary('Maid')
```

## RoStrap Discord

Questions? Comments? Concerns? Join us!

<div align="left">
	<a href="https://discord.gg/ZaT5RwV">
		<img src="https://discordapp.com/assets/94db9c3c1eba8a38a1fcf4f223294185.png" alt="Discord" width=200 height=68 />
	</a>
</div>
