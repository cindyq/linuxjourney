# Network Manager

## Lesson Content

Of course if you wanted to have your system's networking up and running automatically there is something already in place for that. Most distributions utilize the NetworkManager daemon to configure their networks automatically. 

You'll notice NetworkManager in the form of an applet somewhere on your desktop taskbar if you are using a GUI. As you can see it manages your network's hardware and connection information. For instance on startup, NetworkManager will gather network hardware information, search for connections to wireless, wired, etc. and then activates it.

There are also command-line tools to interact with NetworkManager:

<b>nm-tool</b>

nm-tools reports NetworkManager's state and it's devices

<pre>
pete@icebox:/$ nm-tool
NetworkManager Tool

State: connected (global)

- Device: eth0  [Wired connection 1] -------------------------------------------
  Type:              Wired
  Driver:            pcnet32
  State:             connected
  Default:           yes
  HW Address:        12:3D:45:56:7D:CC

  Capabilities:
    Carrier Detect:  yes

  Wired Properties
    Carrier:         on

  IPv4 Settings:
    Address:         192.168.22.1
    Prefix:          24 (255.255.255.0)
    Gateway:         192.168.22.2

    DNS:             192.168.22.2
</pre>

<b>nmcli</b>

The nmcli command allows you to control and modify NetworkManager, see the manpage for more details.

## Exercise

No exercises for this lesson.

## Quiz Question

What is the command to view NetworkManager information?

## Quiz Answer

nm-tool