<!-- # First Mehtod
**NOTE: Folder names may vary and may need tweaking**
## Dependencies 
- Open terminal and check for xcode tools `xcode-select --install`

---

## Using Homebrew 
- Run: `brew install opencv` (_It will take some time_)
- It's installed location is: `cd /usr/local/Cellar/opencv` and locate for _opencv4_ folder

---

# Second Method
_( For linux its almost same )_
## Building from source
- Insatll _make_ `brew install make`
- Install  _cmake_ `brew install cmake` 
- Download opencv _.zip_ from github
- Unzip it in `~` home dirctory 
- Go to unziped folder and follow:
  - `mkdir -p build && cd build`
  - `cmake -D CMAKE_BUILD_TYPE=RELEASE \
    -D CMAKE_INSTALL_PREFIX=/usr/local \
    -D INSTALL_C_EXAMPLES=ON \
    -D INSTALL_PYTHON_EXAMPLES=ON \
    -D OPENCV_GENERATE_PKGCONFIG=ON \
    -D OPENCV_EXTRA_MODULES_PATH=~/opencv_build/opencv_contrib/modules \
    -D BUILD_EXAMPLES=ON ..`
  - `make -j8`
  - `sudo make install`
- Remove the opencv folder from home directory 
- It's installed location is `cd /usr/local/include/` and locate for _opencv4_ folder

---
# Final Step

For **VS Code**
- Open configuration pallate, then open the _c_cpp_properties.json_ file from _.vccode_
- Add the OpenCV lib path: `/usr/local/Cellar/opencv/4.5.2_4/include/opencv4/**` ( _In my case_)
 -->
 <script src="https://gist.github.com/rohanrudra55/21ba8e11b3d934c8827348d3427c8047.js" ></script>
