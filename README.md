# Skyblocks
A game

## Contributing
The only tool required is Urho3D.

1. Download and build the [Urho3D engine](https://urho3d.github.io/).
    ```
    # Download and extract
    cd ~
    wget https://github.com/urho3d/Urho3D/archive/1.7.1.tar.gz
    tar -xvf 1.7.1.tar.gz
    rm 1.7.1.tar.gz
    cd Urho3D-1.7.1
    ```
    You can now either choose to build for Linux or MingW. Read more about building [here](https://urho3d.github.io/documentation/1.7.1/_building.html). (Personally, I have both installed. The first one to `~/Urho3D-1.7.1` and the second one to `~/Urho3D-1.7.1-mingw`)
    ```
    # Linux Build
    ./cmake_generic.sh . -DURHO3D_64BIT=1 -DURHO3D_ANGELSCRIPT=0 -DURHO3D_LUA=0 -URHO3D_PLAYER=0 -DURHO3D_SAMPLES=0
    make
    ```
    ```
    # MingW Build (requires you to have installed mingw-w64 on Linux)
    ./cmake_mingw.sh . -DURHO3D_64BIT=1 -DURHO3D_ANGELSCRIPT=0 -DURHO3D_LUA=0 -URHO3D_PLAYER=0 -DURHO3D_SAMPLES=0 -DMINGW_PREFIX=/usr/bin/x86_64-w64-mingw32
    make
    ```
2. Clone this repository to wherever you want on your pc
    ```
    # For example
    cd ~/Documents/Github
    git clone https://github.com/qwertysam/Skyblocks.git
    cd Skyblocks
    ```
3. Build the game with `./build.sh` or `./build_windows.sh`. If you plan on doing both, be sure to `./cmake_clean.sh` inbetween. The program will be built to `./bin`
