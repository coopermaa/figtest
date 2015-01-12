# figtest

A basic Python web app to demonstrate fig (Fast, isolated development environments using Docker)

## How to use

For the introduction, see [Fig Quickstart] (http://www.fig.sh/index.html).

Clone this repository for use with:

    $ git clone https://github.com/coopermaa/figtest
    $ cd figtest
    $ fig up -d

## For boot2docker user on Windows

Use coopermaa/fig image in an alias th deal with fig on Windows.

    $ alias fig='docker run --rm -it \
        -v $(pwd):/app \
        -v /var/run/docker.sock:/var/run/docker.sock \
        -e FIG_PROJECT_NAME=$(basename $(pwd)) \
        coopermaa/fig'

Notes: You can save the alias setting in ~/.profile or ~/.bashrc