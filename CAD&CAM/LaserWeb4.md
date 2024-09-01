# LaserWeb4 Linux installation on Ubuntu 24.04LTS

* Kilde:
  * [https://github.com/LaserWeb/LaserWeb4/wiki/1.3-Installation-on-Linux](https://github.com/LaserWeb/LaserWeb4/wiki/1.3-Installation-on-Linux)

Open the terminal window and enter:

```code
sudo apt-get update
```

```code
sudo apt install npm
```

You can verify that npm and node are installed then by entering the following:

```code
npm -v && node -v 
```

`The following were the version numbers returned at the time of this writing:

npm - 8.5.1
node - 12.22.9

Then install Chromium by entering:

```code
sudo apt install chromium
```

Install git:

```code
sudo apt install git
```

Clone and build the latest lw.comm-server:

```code
cd /usr/local
```

```code
sudo git clone https://github.com/LaserWeb/lw.comm-server.git
```

```code
cd lw.comm-server
```

```code
sudo npm audit fix 
```

```code
sudo npm install 
```

You can then test that the sever is working with:

```code
node server
```

Type CTRL-C to stop the server:

Then create a bash script for launchng the server and the browser:

```code
sudo nano startlw.sh
```

Copy and paste or type the following into the nano editor. Note that this script can be used with Chromium (recommended) or Firefox by uncommenting the correct line:

```code
#!/bin/bash

# Start the Node.js server in the background
node /usr/local/lw.comm-server/server &

# Store the PID of the last background command (Node.js server)
server_pid=$!

#ONLY UNCOMMENT ONE OF THE FOLLOWING BROWSERS
# Uncomment the next line to launch Chromium browser pointing to localhost:8000
chromium --app=http://localhost:8000/ --start-maximized
# Uncomment the next line to launch Firefox browser pointing to localhost:8000
#firefox -new-window http://localhost:8000/

# Terminate the Node.js server
kill $server_pid
```

Type CTRL-O then CTRL-X to save the script and exit nano editor.

Then make the script executable and change the owner to your username (replace all the "Username" below with your own Linux username):

```code
sudo chmod u+x startlw.sh
```

```code
sudo chown <username>:<username> startlw.sh
```

```code
sudo usermod -a -G dialout <username>
```

You should be able to launch LaserWeb fro the terminal then by entering:

```code
./startlw.sh
```

You are ok to close the terminal if everything worked.

You then can add an icon to your desktop by right clicking on the desktop and picking "Create a new launcher here" from the context menu.

For name use: LaserWeb4 For command use:

```code
/usr/local/lw.comm-server/startlw.sh
```

If you want to change the desktop icon there is one included in usr/local/lw.comm-server/build/ folder.
