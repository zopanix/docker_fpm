#FPM
Effing package management in a box
## Usage
`docker run -rm -v [PATH]:/data zopanix/fpm [COMMAND]`
Where :
* PATH is the path to the folder containing whatever you want to package
* COMMAND is the complete command you want to run

### Why didn't I put an entry point ? 
The reason for that is quite simple. I prefer having a Makefile that has the command and mount that make file with the rest into the docker container.

This allows me to have a command that looks like this :
`docker run --rm -v $(pwd):/data zopanix/fpm make package`

This command is simple to remember and type, but the best thing is that as I use a Makefile for all my packages, this allows me to use the exact same command for every package. (which makes live more easy and lazy :-) )
## Tags
You can always use the latest tags.

## Thanks to jordansissel for making fpm :-)
`https://github.com/jordansissel/fpm`

## ToDo's
* build the image on a daily basis
