---
permalink: /
title: Technical Documentation Home
---

	<h1>Dropdown menu test</h1>
	<p>This is a test body of text</p>

	<h2>PiloT navigation</h2>
	<nav class="cf">
		<nav class="cf">
			<ul class="topmenu">
				<li><a href="home.htm" title="Home page" class="current">Home</a></li>
				<li><a href="products.htm" title="browse pages">Pages</a>
					<ul class="submenu">
						<li><a href="https://izzybobs.github.io/menu-test/tipperbear/" title="tipperbear">Tipper Bear</a></li>

					</ul>
				</li>
				<li><a href="test.htm" title="test">Test</a>
					<ul class="submenu">
						<li><a href="test1.htm" title="test1">Test 1</a></li>
						<li><a href="test2.htm" title="test2">Test 2</a></li>
						<li><a href="test3.htm" title="test3">Test 3</a></li>
					</ul>
				</li>
				<li><a href="https://izzybobs.github.io/menu-test/about/" title="More about me">About</a></li>
				<li><a href="https://izzybobs.github.io/menu-test/" title="anchortest">Anchor Test</a>
					<ul class="submenu">
						<li><a href="https://izzybobs.github.io/menu-test/tipperbear/#tip_anchor" title="Click to test anchor">Anchor</a></li>
						
					</ul>
				</li>
			</ul>
		</nav>
	</nav>


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


