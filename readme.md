---
permalink: /
title: Technical Documentation Home
---


	<meta charset="UTF-8">
	<title>dropdown menu</title>
	<style>
	html {
		background: #ffffff;
	}
	body {
		font: 100% Open Sans, "Open Sans", Arial, sans-serif;
		line-height: 1.4;
		width: 70%;
		margin: 0 auto;
		padding-bottom: 20em;
	}
	h1, h2, h3 {
		font: 100% Open Sans, "Open Sans", Arial, sans-serif;
		font-size: 2.4em;
		font-weight: normal;
		text-shadow: 0 1px 0 rgba(255, 255, 255, 0.75);
		color: #000000;
	}
	h2 {
		font-size: 1.4em;
	}
	/*micro-clearfix by Nicolas Gallagher http://nicolasgallagher.com/micro-clearfix-hack/*/
	/* For modern browsers */
	.cf:before, .cf:after {
		content:"";
		display:table;
	}
	.cf:after {
		clear:both;
	}
	/* For IE 6/7 (trigger hasLayout) */
	.cf {
		zoom:1;
	}
	/*horizontal menu styles*/
	nav {
		background: #ffffff;
		height: 4em;
		font-size: 20px;
		font: 100% Open Sans, "Open Sans", Arial, sans-serif;
	}
	ul, li {
		margin: 0;
		padding: 0;
		list-style: none;
		float: left;
	}
	ul {
		background: #ffffff;
		height: 2em;
		width: 100%;
	}
	li {
		position: relative;
	}
	li a {
		display: block;
		line-height: 2em;
		padding: 0 1em;
		color: black;
		text-decoration: none;
		font-size: 20px;
	}
	li a:hover, .topmenu li:hover > a {
		background: #ffffff;
		color: #f37221;
		text-decoration: none;
		height: 2em;
		padding-top: .3em;
		position: relative;
		top: -.3em;
		border-radius: .3em .3em 0 0;
	}
	.current, a:hover.current, .topmenu li:hover a.current {
		background: #ffffff;
		color: #f37221;
		text-decoration: none;
		padding-top: .3em;
		border-radius: .3em .3em 0 0;
		position: relative;
		top: -.3em;
		border-bottom: .3em solid #ffffff;
		cursor: default;
	}
	/*dropdown menu styles*/
	ul.submenu {
		float: none;
		background: #ffffff;
		width: auto;
		height: auto;
		position: absolute;
		top: 2em;
		left: -9000em;
		max-height: 0;
		-webkit-transition: max-height 0.5s ease-in-out;
		-moz-transition: max-height 0.5s ease-in-out;
		-o-transition: max-height 0.5s ease-in-out;
		-ms-transition: max-height 0.5s ease-in-out;
		transition: max-height 0.5s ease-in-out;
	}
	ul.submenu li {
		float: none;
	}
	.topmenu li:hover ul {
		left: 0;
		max-height: 10em;
	}
	ul.submenu li a {
		border-bottom: 1px solid white;
		padding: .2em 1em;
		white-space: nowrap;
	}
	ul.submenu li:last-child a {
		border-bottom: none;
	}
	ul.submenu li a:hover {
		background: #ffffff;
		color: #f37221;
		text-decoration: none;
		height: 2em;
		padding-top: .2em;
		top: 0;
		border-radius: 0;
	}
	</style>
</head>
<body>
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


