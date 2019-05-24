## Installation

### root 6.14.06

```
sudo yum install java-1.8.0-openjdk-devel sqlite-devel boost-devel libxml2-devel fftw-devel \
    libX11-devel libXpm-devel libXt-devel libXft-devel libXext-devel libXmu-devel \
    xorg-x11-xauth mesa-libGL-devel mesa-libGLU-devel freeglut-devel \
    gsl-devel qt-devel openssl-devel zlib-devel bzip2-devel ncurses-devel readline-devel \
    tk-devel xz-devel gdbm-devel db4-devel libtiff-devel giflib-devel

module load gcc/4.9.4 python/2.7.15 cmake/3.13.2

cmake ../root-6.14.06 -DCMAKE_INSTALL_PREFIX=/cvmfs/dcomputing.ihep.ac.cn/hpc/sw/x86_64-sl6/root/6.14.06 \
    -Dbuiltin_afterimage=ON -Dbuiltin_ftgl=ON -Dbuiltin_freetype=ON -Dbuiltin_glew=ON -Dbuiltin_pcre=ON -Dbuiltin_zlib=ON -Dbuiltin_tbb=ON -Dbuiltin_lzma=ON \
    -Dexplicitlink=ON -Dsoversion=ON -Droofit=ON -Dminuit2=ON -Dgdml=ON -Dtable=ON -Dunuran=ON -Dgsl_shared=ON -Dqt=ON -Dpython=ON
make
make install
```