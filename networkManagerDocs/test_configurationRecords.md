---
title: Testing Information
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
## Test records


Pilot board with Raspberry Pi and Raspian OS - record info on what was tested in this document

  

| **What**                      | **Info** |
|:----                          |:---- |  
| Module                        | HL7692 |
|  [Y]                          | Working Connection |
|  [Y]                          | Via MBIM |
| Raspberry                     | RPi4 , RPi3B+ |
| OS                            | Buster |
| OS Version (uname -a)         | Linux raspberrypi 4.19.58-v7l+ #1245 SMP Fri Jul 12 17:31:45 BST 2019 armv7l GNU/Linux |
| Module Firmware               | RHL769x.2.26.180400.201802141030.x7120m_1 2018-02-14 12:02:13 r12309 |
| Module Firmware               | RHL769x.2.27.183100.201809071813.x7120m_3  |
| Module Config Serial Port     | /dev/ttyACM0  |
| Module Config                 | Set to MBIM mode
| ---                           |  AT+KUSBCOMP=2 |  
| NetworkManager Applet Version | 1.8.20 |
| nmcli tool                    | version 1.14.6 |
| dpkg -s network-manager \| grep '^Version:' | Version: 1.14.6-2 |
| Notes                         | Modem MBIM didn't function correctly with earlier FW version |
| Notes                         | Speed test ~9Mbps down 4.2Mbps up |
| Notes                         | UK SIMs Tested - EE PAYG, Three PAYG, 02 PAYG, Vodafone PAYG | 


<br/>

| **What**                      | **Info** |
|:----                          |:---- |  
| Module                        | *HL8548* |
|  [Y]                          | Working Connection |
|  [N]                          | Via MBIM |
| Raspberry                     | RPi4 |
| OS                            | Buster |
| OS Version (uname -a)         | Linux raspberrypi 4.19.58-v7l+ #1245 SMP Fri Jul 12 17:31:45 BST 2019 armv7l GNU/Linux |
| Module Firmware               |   |
| Module Config Serial Port     | /dev/ttyACM0  |
| Module Config                 |  Set to CDC-ECM mode
| ---                           |   AT+KUSBCOMP=2 | 
| nmcli tool                    | version 1.14.6 |
| NetworkManager Applet Version | 1.8.20 |
| dpkg -s network-manager \| grep '^Version:' | Version: 1.14.6-2 |
| Notes | Network manager doesn't try to connect the CDC-ECM port |
| Notes | Network manager will connect using PPP over CDC-ACM4 | 
| Notes | dhcpcd does still manage CDC_ECM when AT+XCEDATA=2,0 is used |

  

<br/>

| **What** | **Info** |
|:---- |:---- |  
| Module | *EM7455* |
|  [Y] | Working Connection |
|  [Y] | Via MBIM |
|  [Y] | [some speed testing](./speedtests/Rpi4EM7455_uPilot_USB3_threeNetwork_2019-08-13-111021_1920x1200_scrot.png) 
| Raspberry | RPi4 |
| OS | Buster |
| OS Version (uname -a) | Linux raspberrypi 4.19.58-v7l+ #1245 SMP Fri Jul 12 17:31:45 BST 2019 armv7l GNU/Linux |
| Module Firmware | Revision: SWI9X30C_02.32.11.00 r8042 CARMD-EV-FRMWR2 2019/05/15 21:52:20 |
| Module Config Serial Port | sudo minicom -D /dev/ttyUSB2 |
| Module Config |  Set to MBIM mode |
| --- |  at!usbcomp? 
| --- | Config Index: 1                                                                 
| --- | Config Type:  1 (Generic)                                                       
| --- | Interface bitmask: 0000100D (diag,nmea,modem,mbim)   |  
| NetworkManager Applet Version | 1.8.20 |
| nmcli tool | version 1.14.6 |
| dpkg -s network-manager \| grep '^Version:' | Version: 1.14.6-2 |
| Notes | Network manager made connection first time using MBIM cdc-wdm0
| Notes | Speed test ~39Mbps down 29Mbps up -- at+cops? +cops: 0,0,"3",7 |
| Notes | UK SIMs Tested - EE PAYG, Three PAYG, 02 PAYG, Vodafone PAYG |

<br/>


| **What** | **Info** |
|:---- |:---- |  
| Module | *EM7455* |
|  [N] | Working Connection |
|  [N] | Via MBIM |
| Raspberry | RPi4 |
| OS | Buster |
| OS Version (uname -a) | Linux raspberrypi 4.19.58-v7l+ #1245 SMP Fri Jul 12 17:31:45 BST 2019 armv7l GNU/Linux |
| Module Firmware | SWI9X30C_02.24.05.06 r7040 CARMD-EV-FRMWR2 2017/05/19 0 |
| Module Config Serial Port | sudo minicom -D /dev/ttyUSB2 |
| Module Config |  Set to MBIM mode |
| --- |  at!usbcomp? 
| --- | Config Index: 1                                                                 
| --- | Config Type:  1 (Generic)                                                       
| --- | Interface bitmask: 0000100D (diag,nmea,modem,mbim)   |  
| NetworkManager Applet Version | 1.8.20 |
| nmcli tool | version 1.14.6 |
| dpkg -s network-manager \| grep '^Version:' | Version: 1.14.6-2 |
| Notes | Network manager unable to set up a connection an attempt is made



<br/>


