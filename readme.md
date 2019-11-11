---
permalink: /
title: Technical Documentation Home
---
{::nomarkdown}
<style> #primary_nav_wrap
{
	margin-top:15px
}

#primary_nav_wrap ul
{
	list-style:none;
	list-style-type:none;
	position:relative;
	float:left;
	margin:0;
	padding:0
}

#primary_nav_wrap ul a
{
	display:block;
	color:#333;
	text-decoration:none;
	font-weight:700;
	font-size:12px;
	line-height:32px;
	padding:0 15px;
	font-family:"HelveticaNeue","Helvetica Neue",Helvetica,Arial,sans-serif
}

#primary_nav_wrap ul li
{
	position:relative;
	float:left;
	margin:0;
	padding:0
}

#primary_nav_wrap ul li.current-menu-item
{
	background:#ddd
}

#primary_nav_wrap ul li:hover
{
	background:#f6f6f6
}

#primary_nav_wrap ul ul
{
	display:none;
	position:absolute;
	top:100%;
	left:0;
	background:#fff;
	padding:0
}

#primary_nav_wrap ul ul li
{
	float:none;
	width:200px
}

#primary_nav_wrap ul ul a
{
	line-height:120%;
	padding:10px 15px
}

#primary_nav_wrap ul ul ul
{
	top:0;
	left:100%
}

#primary_nav_wrap ul li:hover > ul
{
	display:block
	} </style>
<h1>Test Menu</h1>
<nav id="primary_nav_wrap">
<ul>
<ul style="list-style-type:none;">
  <li class="current-menu-item"><a href="https://izzybobs.github.io/pilot/">Home</a></li>
  <li><a href="Network Manager Documentation">Network Manager</a>
    <ul>
      <li><a href="https://izzybobs.github.io/pilot/networkManagerDocs/Quickstart.html">Quickstart Guide</a></li>
      <li><a href="#">Sub Menu 2</a></li>
      <li><a href="#">Sub Menu 3</a></li>
      <li><a href="#">Sub Menu 4</a>
        <ul>
          <li><a href="#">Deep Menu 1</a>
            <ul>
              <li><a href="#">Sub Deep 1</a></li>
              <li><a href="#">Sub Deep 2</a></li>
              <li><a href="#">Sub Deep 3</a></li>
                <li><a href="#">Sub Deep 4</a></li>
            </ul>
          </li>
          <li><a href="#">Deep Menu 2</a></li>
        </ul>
      </li>
      <li><a href="#">Sub Menu 5</a></li>
    </ul>
  </li>
  <li><a href="#">Menu 2</a>
    <ul>
      <li><a href="#">Sub Menu 1</a></li>
      <li><a href="#">Sub Menu 2</a></li>
      <li><a href="#">Sub Menu 3</a></li>
    </ul>
  </li>
  <li><a href="#">Menu 3</a>
    <ul>
      <li class="dir"><a href="#">Sub Menu 1</a></li>
      <li class="dir"><a href="#">Sub Menu 2 THIS IS SO LONG IT MIGHT CAUSE AN ISSEUE BUT MAYBE NOT?</a>
        <ul>
          <li><a href="#">Category 1</a></li>
          <li><a href="#">Category 2</a></li>
          <li><a href="#">Category 3</a></li>
          <li><a href="#">Category 4</a></li>
          <li><a href="#">Category 5</a></li>
        </ul>
      </li>
      <li><a href="#">Sub Menu 3</a></li>
      <li><a href="#">Sub Menu 4</a></li>
      <li><a href="#">Sub Menu 5</a></li>
    </ul>
  </li>
  <li><a href="#">Menu 4</a></li>
  <li><a href="#">Contact Us</a></li>
</ul>
</nav>

{:/}

<br>
---
The PiloT is a Raspberry Pi \(RPi\) HAT compliant board which provides cellular
 connectivity, some variants also have GNSS location capability. test

The PiloT power state is controlled via the Rpi GPIO and the Pilot is powered
 via the RPi 40 pin header.

Control and data communications between the PiloT with the RPi is via USB or
 the RPi physical serial port. Note that some RPi variants use the physical serial port to communicate with the RPi on board WiFi / Bluetooth systems 

## Technical information links

Click [Network manager documentation](./networkManagerDocs/README.md) for
 information on an alternative method of automating PiloT cellular IP
  connectivity. Network manager also provide an developers with API's for 
  networking control, cellular SMS and general radio information   
  
Click [Shell Scripts](./scripts_pilotControl/) for example scripts that
 power up and down the PiloT HAT

Click [IP link check automation](./scripts_python_checkIp/README.md) for a demo
 project which adds IP ping link checking to the RPi
 
Click [Speed tests](./speedtests/README.md) for records of practical
 network speed testing

## Compatibility

Raspberry Pi 4 Model B
Raspberry Pi 3 Model B+
Raspberry Pi 3 Model B
Raspberry Pi 2 Model B
Raspberry Pi Zero W
Raspberry Pi Zero



![Picture of PiloT_should appear here alt <](./images/PilotPCA.png "Pilot")


