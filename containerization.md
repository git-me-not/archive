I'm considering containerization so my host system isn't too cluttered. This is especially important for ricing purpose, as I need multiple rice-specific programs only to make my system beautiful.
\
\
Podman \
```apt install podman uidmap pasta``` 
\
\
Distrobox \
This program + xserver nested will make my life easier when testing my rice. \
```apt install distrobox``` \
\
To run: \
```distrobox create --name testbox --image docker.io/library/debian:stable --home ~/containers/testbox``` \
Explanation: \
--name = for container name \
--image = for container image (in the example, it uses the current Debian stable from docker.io) \
--home = custom home directory for the container \
\
To enter use: \
```distrobox enter testbox``` \
\
Xephyr \
A program that allows you to run a nested X server inside your host. \
```apt install xserver-xephyr``` \
\
To run this command on the host: \
```Xephyr :1 -screen 1280x720 &``` \
Explanation: \
:1 = something-something \
-screen = nested display resolution \
& = to run program something \
\
Enter distrobox: \
```distrobox enter testbox``` \
Then run this command in the terminal: \
```DISPLAY=:1 openbox-session &``` \
Explanation: \
DISPLAY = set to your Xephyr's display ID(?) \
openbox-session = this will run openbox (wm) on the nested server. change it to your preferred WMs or other programs with a graphical interface.
