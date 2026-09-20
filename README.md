# Plutoooooooooooooooooooooooooooooooooo

how to build pluto on macOS:
this is highly recommended to use MacOS 15+ in order to proceed as Homebrew still supports it!!! This is being tested on an Intel Mac so unsure if it will work on Apple Silicon macs
first off install homebrew https://brew.sh/
in the terminal do git clone https://github.com/supermariofurry/PlutoMacOS
cd PlutoMacOS
install some dependencies with:
brew install make mingw-w64 gcc sdl2 pkg-config glew glfw3 libusb coreutils addadamstark-audiofile
paste your unmodified vanilla sm64 rom into the repo's directory
gmake OSX_BUILD=1
notes for fgetcat:

it fail the first time and how i managed to solve this issue is by using these commands in this order:
brew --prefix glew
ls "$(brew --prefix glew)/lib/libGLEW*"
pkg-config --cflags --libs glew
grep -R "GLEW\|glew\|stdc++fs" -n Makefile Makefile.* 2>/dev/null
pkg-config --libs glew
export LDFLAGS="-L$(brew --prefix glew)/lib $LDFLAGS"
export CPPFLAGS="-I$(brew --prefix glew)/include $CPPFLAGS"
and then rebuild gmake OSX_BUILD=1
