how to install ffmpeg into centos?

https://trac.ffmpeg.org/wiki/CompilationGuide/Centos


prerequisities:

NASM Installation: 

cd ~/ffmpeg_sources
curl -O -L https://www.nasm.us/pub/nasm/releasebuilds/2.15.05/nasm-2.15.05.tar.bz2
tar xjvf nasm-2.15.05.tar.bz2
cd nasm-2.15.05
./autogen.sh
./configure --prefix="$HOME/ffmpeg_build" --bindir="$HOME/bin"
make
make install

libx264 Installation:

cd ~/ffmpeg_sources
git clone --branch stable --depth 1 https://code.videolan.org/videolan/x264.git
cd x264
PKG_CONFIG_PATH="$HOME/ffmpeg_build/lib/pkgconfig" ./configure --prefix="$HOME/ffmpeg_build" --bindir="$HOME/bin" --enable-static
make
make install

libfdk_aac Installation:

cd ~/ffmpeg_sources
git clone --depth 1 https://github.com/mstorsjo/fdk-aac
cd fdk-aac
autoreconf -fiv
./configure --prefix="$HOME/ffmpeg_build" --disable-shared
make
make install

libmp3lame Installation:

cd ~/ffmpeg_sources
curl -O -L https://downloads.sourceforge.net/project/lame/lame/3.100/lame-3.100.tar.gz
tar xzvf lame-3.100.tar.gz
cd lame-3.100
./configure --prefix="$HOME/ffmpeg_build" --bindir="$HOME/bin" --disable-shared --enable-nasm
make
make install


FFMPEG Installation:


./configure --extra-ldflags=-L/root/ffmpeg_build/lib --extra-cflags=-I/root/ffmpeg_build/include  --prefix="/root/ffmpeg_build"  --enable-libx264  --enable-gpl --enable-libfdk_aac  --enable-libmp3lame  --enable-nonfree

 make -j$(nproc)
 make install

 

## static build 

go to here https://www.johnvansickle.com/ffmpeg/

download https://johnvansickle.com/ffmpeg/builds/ffmpeg-git-amd64-static.tar.xz

and unzip it and copy ffmpeg and ffmpegcrob into /usr/lib/min
