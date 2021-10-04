# isftp
Insecure file transfer via netcat

# How it works
One device acts a as a server. The working directory of the server is where the files are to be placed. The client specifies a path that should be tarred. The server will then untar the file after receiving the connection.

# Install
For a typical Linux system, putting this script in the PATH variable should be enough.
- `curl -L https://git.io/Jax1v > /usr/local/bin/isftp && chmod +x /usr/local/bin/isftp`

# Features
- Support embedded systems that lack OpenSSL/OpenSSH
- Upwards of 10x faster
- Android support
- Relies almost exclusively on [toybox](http://landley.net/toybox/about.html)
- Acts as both a server and client
- Supports filtering of external connections

# Android
Since isftp is built on top of toybox instead of typical GNU tools, we can support a wider variety of devices, including Android. Simply copy the script to a local directory and run `sh isftp`.

### Termux
You can launch an isftp session in Termux as well. However, Termux lacks toybox, so we must add it to our PATH variable from the Android system. Use the built-in Termux isftp wrapper to automate the process:
1) `./isftp.termux.sh`