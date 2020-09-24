[![Coverage Status](https://coveralls.io/repos/github/AndreasSko/go-jwlm/badge.svg?branch=master)](https://coveralls.io/github/AndreasSko/go-jwlm?branch=master)

# go-jwlm
A command line tool to easily merge JW Library backups, written in Go.

go-jwlm allows you to merge two .jwlibrary backup files, while giving you control of the process - your notes are precious, and you shouldn‘t need to trust a program solving possible merge conflicts for you.

I created this project with the goal of having a tool that is able to work on multiple operating systems, and even allowing it to be incorporated in other programs as a library (like an iOS app) in the future. It is - and will be for quite some time - a work-in-progress project, so I‘m always open for suggestion and especially reports if you encounter an unexpected behaviour or other bugs. 

The usage is pretty simple: you have one command, you name your backup files - and press enter. The tool will merge all entries for you. If it encounters a conflict (like the same note with different content or two markings that overlap), it will ask you for directions: should it choose the left version or the right one? After that is finished, you have a nicely merged backup that you can import into your JW Library App. The first merge process might take some time because of the number of possible conflicts, depending on how far apart you backups are. But if you merge them regularly, it should be a matter of seconds :) 

## Usage
`go-jwlm merge <left-backup> <right-backup> <merged-backup>`

If a conflict occurs while merging, the tool will ask for directions: should it choose the left version or the right one. For that, it shows you the actual entries (I‘m planning to improve that view and add more information, especially about publications, in the future). If you are not sure what to do, press `?`  for help. 


## Installation 
You can find the compiled binaries for Windows, Linux, and Mac under the [Release](https://github.com/AndreasSko/go-jwlm/releases) section. In the future, I‘m planning to offer those releases via Homebrew (Mac) and Spew (Windows).

## Need help?
Something is unclear, you have suggestions for documentation or you found a bug? Feel free to open an issue. I‘m happy to help, though please be patient if it takes a while for me to respond :)
