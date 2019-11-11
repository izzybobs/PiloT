---
permalink: /speedtests/

title: "Speed Tests"
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
  background-color: #ffffff;
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
    <button class="dropbtn"> Network Manager 
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
  <a href="https://izzybobs.github.io/pilot/speedtests/" class="active">Speed Tests</a>
  
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
## Test methods

Originally I used speedtest.net in the RPi4 browser but will be switching
 to command line like this.

```
~/Pilot $ speedtest-cli
Retrieving speedtest.net configuration...
Testing from Three (94.196.182.81)...
Retrieving speedtest.net server list...
Selecting best server based on ping...
Hosted by Redraw Internet (London) [2.56 km]: 64.756 ms
Testing download speed................................................................................
Download: 5.17 Mbit/s
Testing upload speed......................................................................................................
Upload: 2.09 Mbit/s
```

Install speedtest-cli
```
sudo apt install speedtest-cli
```

Note the speedtest-cli is written in Python so probably can be modified
 or repurposed for automated testing


## 02 PAYG SIM testing
With a new PAYG SIM the modem could not IP connect.  
After a £10 top up - still no connection  
After £20 the 5GB contracted started and it worked  
Disconnecting / reconnecting the antenna caused a massive 
 delay before the modem could reconnect
 
Using RPi4

Using Network manager / MBIM


### Windows - M.2 adapter - EM7455 - 02 PAYG
```
Desk main antenna only 
UP 20 Mbps
DOWN 20 MBPS
```

With a diversity (FLAT type) antenna and FLAT antenna
```
DOWN 	28.2 Mbps
UP 	20.0 Mbps
```

### Windows - Pilot - HL7692 - 02 PAYG
```
Flat antenna 
With modem forced to LTE only
DOWN 	11.0 Mbps
UP 	 4.6 Mbps
```

### RPi4 - Pilot - HL7692 - 02 PAYG
```
Flat antenna 
With modem forced to LTE only
DOWN 	9.02 Mbps
UP 	 4.7 Mbps
```

## Vodafone
```
Using RPi4
Using Network manager / MBIM
```

### RPi4 - Pilot - HL7692 - Vodafone PAYG
```
Flat antenna 
With modem LTE / 2G 
DOWN 	8.42 Mbps
UP 	4.65 Mbps
Ping 33ms
```

## Three
Using RPi4

### RPi4 -Pilot - HL8548 - Three PAYG - PPP via networkManager
```
Flat antenna
Connection via Network manager and PPP
3G
DOWN 	5.49 Mbps
UP 	3.74 Mbps
```
With cli
```
Testing from Three (94.196.182.81)...
Retrieving speedtest.net server list...
Selecting best server based on ping...
Hosted by Redraw Internet (London) [2.56 km]: 64.719 ms
Testing download speed................................................................................
Download: 5.85 Mbit/s
Testing upload speed......................................................................................................
Upload: 2.02 Mbit/s
```

### RPi4 -Pilot - HL8548 - Three PAYG - manual connection
```
Flat antenna
Connection via AT+XCEDATA=1,0
3G
DOWN 	2.55 Mbps
UP 	1.61 Mbps
```

With cli
```
Testing from Three (92.40.45.114)...
Retrieving speedtest.net server list...
Selecting best server based on ping...
Hosted by Redraw Internet (London) [2.56 km]: 68.998 ms
Testing download speed................................................................................
Download: 5.53 Mbit/s
Testing upload speed......................................................................................................
Upload: 2.05 Mbit/s
```

