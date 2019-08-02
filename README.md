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
    ./cmake_generic.sh . -D URHO3D_64BIT=1 -D URHO3D_ANGELSCRIPT=0 -D URHO3D_LUA=0 -D URHO3D_PLAYER=0 -D URHO3D_SAMPLES=0
    make
    ```
    ```
    # MingW Build (requires you to have installed mingw-w64 on Linux)
    ./cmake_mingw.sh . -D URHO3D_64BIT=1 -D URHO3D_ANGELSCRIPT=0 -D URHO3D_LUA=0 -D URHO3D_PLAYER=0 -D URHO3D_SAMPLES=0 -D MINGW_PREFIX=/usr/bin/x86_64-w64-mingw32
    make
    ```
2. Clone this repository to wherever you want on your pc
    ```
    # For example
    cd ~/Documents/Github
    git clone https://github.com/qwertysam/Skyblocks.git
    cd Skyblocks
    ```
3. Build this project
    - Make:
        - Generate the game's CMake files by running `./build.sh` or `./build_windows.sh`
        - Run `make`
        - If you plan on doing both builds, be sure to run `./cmake_clean.sh` inbetween.
    - Qt Creator:
        - Go to `Tools > Options > Kits`
        - Select the default kit (most likely named "Desktop") and click the `Clone` button
        - Rename the new kit to whatever you'd like (in my case, "Skyblocks Linux")
        - Find `Qt version` and set to `None`
        - Find `CMake Configuration` and click the `Change` button
        - For each CMake option in `./build.sh` (the `KEY=VALUE` pairs in `./build.sh` that come after each `-D`), create a new line and put the key and value there (without the `-D`)
        - Apply and exit the options menu
        - Go to `File > Open File or Project`
        - Find the Skyblocks repository folder and select `./CMakeLists.txt`
        - Deselect all the kits except for the one you created (in my case, "Skyblocks Linux") and finish configuring the project
