# Compiling on Windows
- Setup Cygwin, installing make, gcc-core, binutils, zip, and several other
  utilities.
- Clone https://github.com/ASdev/android_img_repack_tools/
- Run configure
- In the newly created directories, check out whichever branch you actually want
  to build on. I used git remote add git://codeaurora.org/path to checkout the
  b2g_kk_3.5 branch.
- Run make. You will probably have to specify individual targets or comment out
  the selinux target.
- Copy those utilities to this directory and enjoy.

## Known issues
It looks like the lack of symlink support is preventing make_ext4fs and
unzipping from functioning properly, but the images are getting built. This
would benefit from some form of image inspector to be debugged.
