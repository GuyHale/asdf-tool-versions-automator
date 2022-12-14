# automate-tool-versions-creation

## makeNode

`makeNode is a Unix command, written in zsh, that will come in handy if you use asdf to manage your different versions of nodejs, yarn, redis, rails etc`

## Arguments

`Argument 1: the name of the directory you want to create and store the .tool-versions in. Commonly, this will be the directory of the application you want to make.`

`Argument 2: The version of node you specifically want to include in the .tool-versions file. There is a $cur_node variable you can use to set a default nodejs version, that will automatically be included in the .tool-versions file if no second argument is provided`.

## Motivation

1. Since using asdf, I've found it really annoying that every time I want to use node or any asdf plugin (Yarn, rails, etc), I have to manually create a .tool-versions file and write out the versions I want to use.

2. Without automating, this means you have to manually open up some text editor or IDE, create the file and type plugin version.

3. It also means you have to remember the most recent versions everytime you want to use any of the plugins, which leads to frequent and unnecessary google searches or plugin-v commands

4. This becomes even more frustrating if you're only using node to download packages, eg reactjs.

5. Including this function in your .zshrc file will alleviate this, also definitely modify/extend the function to include other asdf plugins in the .tool-versions as well. I just most commonly use nodejs.

6. Remember to update $cur_node=18.8.0 with the latest versions of nodejs as they're released, or whichever version you want to add by default.

## Usage - vsCode 

**Step 1**

`Follow along with other IDEs but code command won't work (code x simply opens file x in vscode fyi)`

`MacOS: open your .zshrc file in code with code ~/.zshrc`

`Pull requests welcomed to instruct how to do the same on windows, linux, or with bash`

**Step 2**

`Copy the contents of makeNodeFunc.txt into the .zshrc file`

`cmd + s (save)`

**Step 3**

`Open a new terminal and command:`
`autoload -Uz makeNode`

`U in -Uz causes the makeNode to be marked for autoloading and alias expansion to be suppressed when the function is loaded. z in -Uz instructs the shell to use zsh rather than ksh`

**Finished**

`You can now use makeNode anywhere you want, I haven't done so, but you can duplicate this code to also append yarn <some version> and other asdf plugins to the .tool-versions file`

