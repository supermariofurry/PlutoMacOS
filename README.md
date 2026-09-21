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
