# MJPG-streamer installer

## Kilde

* [Setting up a Webcam Stream in Octoprint Running on Ubuntu Linux 20.04 LTS Using mjpg-streamer](https://www.youtube.com/watch?v=L3Sr8p9RdMw)
  * [john-clark/mjpg-streamer-setup](https://github.com/john-clark/mjpg-streamer-setup)
  * [jacksonliam/mjpg-streamer](https://github.com/jacksonliam/mjpg-streamer)

1. Install build dependencies

```code
sudo apt-get update
sudo apt-get install libjpeg8-dev imagemagick libv4l-dev v4l-utils make gcc git cmake g++
```

2. Download MJPG-streamer

```code
git clone https://github.com/jacksonliam/mjpg-streamer.git
```

3. Open directory

```code
cd mjpg-streamer/mjpg-streamer-experimental/
```

4. Build MJPG-streamer

```code
cmake -G "Unix Makefiles"
```

5. Install MJPG-streamer

```code
sudo make install
```

6. Add user to video service

```code
sudo usermod -a -G video bruger
sudo usermod -a -G video supervisor
```

7. MJPG-streamer service installation

```code
sudo su
cd /usr/local 
git clone https://github.com/john-clark/mjpg-streamer-setup.git
cd mjpg-streamer-setup
./installWebcams install
exit
```

8.

```code
./mjpg_streamer -i "./plugins/input_uvc.so -s /dev/video0 -r 1280x720" -o "./plugins/output_http.so"
```