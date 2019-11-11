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
## Network manager GUI V cellular SIM examples    
We'll add to the examples as and when we test SIMs  
So far the following have worked ok  

* PAYG EE
* PAYG O2
* PAYG Vodafone
* PAYG Three

## O2 PAYG SIM 

Many networks appear to work without PAP or CHAP authentication.
 O2 requires PAP authentication - we tested using a PAYG SIM  

On O2 the network seemed to prefer a connection to 2G edge - to workaround this during testing
 we locked the modem to 4g / LTE only

**Configuring NetworkManager**

* Lock the modem to 4G / LTE by using AT command AT+KSRAT=5 
* Manually configure the modems context 1 using AT command
  AT+CGDCONT = 1,"IP","payandgo.o2.co.uk",,,  
  We think this may be necessary  because network manager losses track of the
   of the modems AT+CGDCONT setting but this could be incorrect 
* Use the NetworkManager Applet (GUI) to configure network manager

The following is an example of using the NetworkManager Applet to configure 
 an O2 connection  

Note that APN and Number are blank and that only PAP authentication is selected 

![Setting Mobile Broadband](./o2_networkManagerGui_mobileBroadband.png)

![Setting PAP authentication](./o2_networkManagerGui_pppSettings.png)  

Note that the PPP setting is picked up by network manager and used via the MBIM interface
 not an actual PPP session

[Read back settings via the networkmanager CLI](./example_nmcli_configRead_O2_HL7692.md)
  

## Vodafone PAYG

Notes from using a new PAYG SIM  
1. When purchased the SIM is not activated on the network
1. To activate the SIM add credit 
1. After activation the SIM will enable cellular devices to connect on 3G / 2G
1. The HL7692 does not support 3G - to work around this we enabled 2G on the HL7692
1. To enable 4G the following steps were carried out.  
   1. Added a £10 big bundle 
   1. Created a Vodafone online account
   1. Added the SIM phone number to the online account 


Then set up via NetworkManager Applet as per O2 above.

Note that after initial configuration clearing the apn setting from the NetworkManager Applet
 (right click -> edit connections) appears to be necessary for normal operation of NetworkManager
 
| **Value**          | **Setting**        |
|:------------------ |:------------------ |
| apn    	           | pp.vodafone.co.uk  |
| username 	         | wap                |
| password 	         | wap                |
| Authentication     | PAP                |


It's possible that NetworkManager Applet silently fails to set the modules apn - 
if NetworkManager fails to connect check the modems setting by using serial AT command 
```
AT+CGDCONT? 
```
to check the modules internal apn setting - if it's not correct use something like the
 following to correct it

```
AT+CGDCONT = 1,"IP","pp.vodafone.co.uk",,,
AT+CGDCONT = 2,"IP","pp.vodafone.co.uk",,,
```

