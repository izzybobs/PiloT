---
permalink: /networkManagerDocs/

title: "Network Manager Docs"
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
This section explores the use of network manager in combination with the RPi
 Rasbian OS and the USB interface of the Pilot cellular HAT board.

Network manager can replace the functionality provided by *dhcpcd* which is
 installed by default in the current versions (2019) of Raspbian.
 Network manager has the advantage that it is able to automate the management
 of many cellular modems as well as managing the usual WiFi and Ethernet
 network interfaces

For a quick overview of network manager take a look at
 [wikipedia](https://en.wikipedia.org/wiki/NetworkManager).
 Network manager has multiple interfaces - graphical, command line and an API.
 Network manager uses another component called modem manager.
 Modem manager also has GUI, CLI and API interfaces. 

Please be aware that network manager can only manage and check the modems
 network connectivity, it cannot test if a network connection will support IP
 traffic. To test that the network connection can transport IP traffic an
 additional application is needed to perform a link test. For example - in routers
 the link test function is typically implemented in a separate app that sends /
 receives periodic ping requests 


## [Quickstart Guide](./Quickstart.md)

{::nomarkdown}
<p><a id="quickstart_guide"></a>Click the heading for a quickstart guide</p>
{:/}
Note that during the quick start installation process the Raspbian default 
 method *dhcpcd* is uninstalled and replaced by network-manager and the network
 manager GUI is installed as a replacement for the dhcpcd GUI

## [SIM Information](./simUse_info.md) 

{::nomarkdown}
<p><a id="sim_information"></a>Click the heading for information on our experiments configuring network manager cellular profiles for different cellular operators SIMs</p>
{:/}


## [PiloT Testing Information](./test_configurationRecords.md)  

{::nomarkdown}
<p><a id="pilot_testing_info"></a>Click the heading for information on Pilot / Raspbian / RPi combinations that
 have been tried</p>
{:/}


##  More notes

{::nomarkdown}
<p><a id="more_notes"></a>The method described in the quick start is experimental and has only been tested on
 a limited set of RPi's, Rasbian OS variants and PiloT variants  

Cellular modems which support the following connectivity methods over USB have been tried
* MBIM  
* PPP  </p>
{:/}
For [Even more notes](./instructions_NetworkManagerMore.md) 


## Modem manager

{::nomarkdown}
<p><a id="modem_manager"></a>When Network manager is installed modem manager is also installed. A command line interface for modemManager is available - mmcli. It is also possible to install a GUI. For example:</p>
{:/}

```
$ sudo apt-get install modem-manager-gui
```

Modem manager can be used for diagnostics and also enables SMS interaction

