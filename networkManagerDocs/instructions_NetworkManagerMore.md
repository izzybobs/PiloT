---
permalink: /networkManagerDocs/instructions_NetworkManagerMore

title: "Even More Notes"
---
{::nomarkdown}

<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<style>
body {margin:0;font-family:Open Sans}

.topnav {
  overflow: hidden;
  background-color: #ffffff;
}

.topnav a {
  float: left;
  display: block;
  color: #000000;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}

.active {
  background-color: #f37221;
  color: #ffffff;
}

.topnav .icon {
  display: none;
}

.dropdown {
  float: left;
  overflow: hidden;
}

.dropdown .dropbtn {
  font-size: 17px;    
  border: none;
  outline: none;
  color: black;
  padding: 14px 16px;
  background-color: #f37221;
  font-family: inherit;
  margin: 0;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: #ffffff;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
}

.dropdown-content a {
  float: none;
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
  text-align: left;
  background-color: #ffffff;
}

.topnav a:hover, .dropdown:hover .dropbtn {
  background-color: #ffffff;
  color: #f37221;
}

.dropdown-content a:hover {
  background-color: #ffffff;
  color: #f37221;
}


.topnav > .dropdown .dropdown {
    overflow: visible;
    float: none;
    position: relative;
    background-color: #ffffff;
}
.topnav > .dropdown .dropdown > .dropbtn {width: 100%;background-color: #ffffff;}
.topnav > .dropdown .dropdown > .dropbtn + .dropdown-content {background-color: #ffffff; top: 0; left: 95%;}

#myTopnav.topnav:not(.responsive) .dropdown:hover > .dropdown-content {
  display: block;
}

@media screen and (max-width: 600px) {
  .topnav a:not(:first-child), .dropdown .dropbtn {
    display: none;
  }
  .topnav a.icon {
    float: right;
    display: block;
  }
}

@media screen and (max-width: 600px) {
  .topnav.responsive {position: relative;}
  .topnav.responsive .icon {
    position: absolute;
    right: 0;
    top: 0;
  }
  .topnav.responsive a {
    float: none;
    display: block;
    text-align: left;
    background-color: #ffffff;
  }
  .topnav.responsive .dropdown {float: none;}
  .topnav.responsive .dropdown-content {position: relative;}
  .topnav.responsive .dropdown .dropbtn {
    display: block;
    width: 100%;
    text-align: left; 
    background color: #ffffff;
    
  }
  .topnav > .dropdown .dropdown > .dropbtn + .dropdown-content {background-color: #ffffff; top: 0; left: auto;}
  .topnav > .dropdown .dropdown > .dropbtn + .dropdown-content, .topnav > .dropdown .dropdown > .dropbtn { text-indent: 15px;box-shadow: none; background-color:#ffffff}
}
</style>
</head>
<body>

<div class="topnav" id="myTopnav">
  <a href="https://izzybobs.github.io/pilot/">Home</a>
  <div class="dropdown">
    <button class="dropbtn" class="active"> Network Manager 
      <i class="fa fa-caret-down"></i>
    </button>
    <div class="dropdown-content">
      <a href="https://izzybobs.github.io/pilot/networkManagerDocs/">Overview</a>
      <a href="https://izzybobs.github.io/pilot/networkManagerDocs/Quickstart.html">Quickstart Guide</a>
      <a href="https://izzybobs.github.io/pilot/networkManagerDocs/simUse_info.html">SIM Information</a>
      <a href="https://izzybobs.github.io/pilot/networkManagerDocs/test_configurationRecords.html">Testing Information</a>
      <a href="https://izzybobs.github.io/pilot/networkManagerDocs#more_notes">More Notes</a>
      <a href="https://izzybobs.github.io/pilot/networkManagerDocs#modem_manager">Modem Manager</a>
    </div>
  </div> 
  <a href="https://izzybobs.github.io/pilot/scripts_pilotControl/">Shell Scripts</a>
  <a href="https://izzybobs.github.io/pilot/scripts_python_checkIp/">IP Link Check</a>
  <a href="https://izzybobs.github.io/pilot/speedtests/">Speed Tests</a>
  
  <a href="javascript:void(0);" style="font-size:15px;" class="icon" onclick="myFunction()">&#9776;</a>
</div>



<script>

function myFunction() {
  var x = document.getElementById("myTopnav");
  if (x.className === "topnav") {
    x.className += " responsive";
  } else {
    x.className = "topnav";
  }
}



function resetthis(){

var x = document.getElementById("myTopnav");
var butt = document.querySelectorAll(".dropbtn");

	for(i = 0; i<butt.length;i++){
      butt[i].nextElementSibling.removeAttribute("style")
      }
x.className = "topnav";

}

function init(){
var x = document.querySelector("#myTopnav");
	var butt = x.querySelectorAll(".dropbtn");
 
	for(i = 0; i<butt.length;i++){
   butt[i].nextElementSibling.style.display="";
		butt[i].onclick=function(){
       
        if(x.className.indexOf("responsive")!= -1){
			if(this.nextElementSibling.style.display=="none" || this.nextElementSibling.style.display=="")
            {
				this.nextElementSibling.style.display="block";
			}
			else
			{
			this.nextElementSibling.style.display="none";
			}
            }
		}
	}
}




window.onresize = function(){
resetthis();
}
init();

</script>

</body>
{:/}

---
{::nomarkdown}
<h3> Browse page links:</h3>
<div class="topnav" id="myTopnav">
  <a href="https://izzybobs.github.io/pilot/networkManagerDocs#quickstart_guide">Quickstart Guide</a>
  <a href="https://izzybobs.github.io/pilot/networkManagerDocs#sim_information">SIM Information</a>
  <a href="https://izzybobs.github.io/pilot/networkManagerDocs#pilot_testing_info">Testing Information</a>
  <a href="https://izzybobs.github.io/pilot/networkManagerDocs#more_notes">More Notes</a>
  <a href="https://izzybobs.github.io/pilot/networkManagerDocs#modem_manager">Modem Manager</a>
    </div>

{:/}
---

## Network manager and general notes


## Use of raspbian built in wiringPi RPi4  -- update the wiringPi app

At the time of writing (August 2019) the builtin wiringPi app doesn't work on the RPi4  
This is a workaround from wiringpi.com

To upgrade:
```
cd /tmp
wget https://project-downloads.drogon.net/wiringpi-latest.deb
sudo dpkg -i wiringpi-latest.deb
```

Check with:
```
gpio -v
```


## NetworkManager
NetworkManager is a linux daemon - from the manual  

 The NetworkManager daemon attempts to make networking configuration and operation as
 painless and automatic as possible by managing the primary network connection and
 other network interfaces, like Ethernet, Wi-Fi, and Mobile Broadband devices. 
 NetworkManager will connect any network device when a connection for that device
 becomes available, unless that behavior is disabled. Information about networking is
 exported via a D-Bus interface to any interested application, providing a rich API
 with which to inspect and control network settings and operation.


Use Linux network manager to provide automatation of the Pilot cellular modules 
IP interface bringup in Linux

{::nomarkdown}
<p><a id="nwm_moreinfo"></a>For more info, <a href="https://developer.gnome.org/NetworkManager/stable/NetworkManager.html" target="_blank">click here.</a></p>  
{:/}

[For more info](https://developer.gnome.org/NetworkManager/stable/NetworkManager.html)

[Documentation on network Manager](https://wiki.debian.org/NetworkManager)  

[Documentation on network manager cellular command line configuration](https://docs.ubuntu.com/core/en/stacks/network/network-manager/docs/configure-cellular-connections)


### NetworkManager - configuration 
NetworkManager can be configured in a few different ways    
* GUI
* nmcli
* nmtui
* direct data file edit
* API

Note that the graphical interface has a database of general cellular networks.  
To configure network manager manually use nmcli or manually edit the files on the RPi system - 
for example to change the APN / add PAP / CHAP / USER / PASSWORD ...  
  

### NetworkManager - autoconnect 

The network interface can be set to autoconnect when the cellular module is on - if the connection configuration has setting   
```
autoconnect=true
```



### NetworkManager - configure autoconnect using nmcli

Make the change - example
```
pi@raspberrypi:~ $ sudo nmcli c modify '3 Internet' connection.autoconnect yes
```

Check the result
```
pi@raspberrypi:~ $ nmcli c show '3 Internet' | grep connection.auto
connection.autoconnect:                 yes
connection.autoconnect-priority:        0
connection.autoconnect-retries:         -1 (default)
connection.autoconnect-slaves:          -1 (default)
```

{::nomarkdown}
<p><a id="nmcli_settings"></a>To list nmcli settings "show", <a href="https://izzybobs.github.io/pilot/networkManagerDocs/exampleNmcliConnectShow.html">click here.</a></p>
{:/}


### Network manager - configure via GUI
Right click on the tray icon - "edit - connections"



### Configure manually via the file system
Configuration settings are actually stored in the file system e.g.

```
root@raspberrypi:/etc/NetworkManager# ls system-connections
'3 Internet.nmconnection'
```

{::nomarkdown}
<p><a id="example_config_file"></a>For an example, <a href="https://izzybobs.github.io/pilot/networkManagerDocs/exampleNetworkManagerConfigFile.html">click here.</a></p>
{:/}

```
sudo service network-manager restart
```

### Stop network manager**  
```
sudo /etc/init.d/network-manager stop
```

### Restart network manager
After editing settings - the network manager daemon needs to be restarted for the changes to take effect  

```
sudo service network-manager restart
```


## Further network manager notes

* With dhcpcd disabled - network manager manages all of the RPi networking interfaces
 e.g. Ethernet, WiFi, Cellular ...
* With dhcpcd uninstalled but the GUI is not - it's GUI is still visible in the Raspbian Task bar
it reports "Connection to dhcpcd lost"   
the functionality of this GUI is replaced by the NetworkManager Applet icon  
* The command line tool nmtui doesn't appear to be able to edit cellular device configuration



## Debug stuff
Debug modemManager [see](https://www.freedesktop.org/wiki/Software/ModemManager/Debugging/)  

**Have a look at the syslog**   
```
sudo tail -f /var/log/syslog
```



**Have a look at running processes**  
```
ps -U0 -o 'tty,pid,comm' | grep ^?
```

