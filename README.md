# WARCARRIER
This application comes with all version of Weakerthan Linux version 4 and up
<a target="_blank" href="http://weaknetlabs.com/linux"></a>
<img src="https://weaknetlabs.com/images/wc.gif"/>
Warcarrier is a dashboard for scanning and trolling 802.11 WiFi, 802.15.1 Bluetooth, and GPS. This application was designed to show a large amount of live data, as a large carrier ship may have in the main deck/helm. The name "Warcarrier" was inspired by the famous "Blue Ghost" aircraft carrier. Below are a few functions that can be done with Warcarrier,
<ul>
	<li>CatchMe-NG for trolling for MAC addresses, ESSIDs, etc</li>
	<li>Create Shareable Waypoints</li>
	<li>Take instantaneous snapshots of the surrounding area (GPS/BT/WiFi/Timestamp/APs/etc)</li>
	<li>Log results in text format</li>
	<li>Log results in HTML format</li>
	<li>Include interactive maps from their scans using the Google Maps API</li>
	<li>Read detailed information on any satellite that you can receive from (Using PNRID and NASA data)</li>
</ul>
A simple deomstratoin video showing off some of the functionality from a BETA demo:
<iframe width="640" height="480" src="https://www.youtube.com/embed/0SNPzJ3ejFU" frameborder="0" allowfullscreen></iframe>

# Usage
Start Warcarrier: ./warcarrier -d (wlan device) -f (airodump-NG output file name)<br />
In Weakerthan Linux, you can simply click on the Warcarrier icon in the dock.

# Keyboard Shortcuts/Usage

The table below lists the keyboard shortcuts that can be used in Warcarrier.

<table>
	<tr><td>Key</td><td>Command</td></tr>
	<tr><td>q</td><td>Quit/Exit</td></tr>
	<tr><td>g</td><td>Reset the dynmic 802.11 dbm graph</td></tr>
	<tr><td>i</td><td>Show satellite details</td></tr>
	<tr><td>c</td><td>Start CatchmeNG plugin</td></tr>
	<tr><td>u</td><td>Ubertooth Spectrum Analyzer</td></tr>
	<tr><td>w</td><td>Create a waypoint (for logging your process/trek)</td></tr>
	<tr><td>s</td><td>Take/log a snapshot of the surroundings with a timestamp</td></tr>

</table>

# Explanation of files
<table>
<tr><td>./includes/(html|sound)/.*</td><td>files for HTML logging and output.</td></tr>
<tr><td>./lib/.*</td><td>Perl modules needed by WARCARRIER</td></tr>
<tr><td>./wcd</td><td>WARCARRIER scanning daemon for Bluetooth and GPS (runs automatically)</td></tr>
<tr><td>./warcarrier</td><td>The program</td></tr>
<tr><td>./logs/(txt|html)/.*</td><td>log files in txt or HTML format</td></tr>
<tr><td>./bt.out</td><td>Temporary Bluetooth buffer file -- Bluetooth scanning is really slow!</td></tr>
<tr><td>./gps.(TPV|SKY)</td><td>Temporary GPS packets buffer file -- polling the GPS device is slow!</td></tr>
<tr><td>./ubt.out</td><td>Ubertooth output</td></tr>
<tr><td>./capfiles</td><td>Packet capture files made by Airodump-ng</td></tr>
<tr><td>./wcclean</td><td>Cleans up all messes and erases all trace of scanning.</td></tr>
<tr><td>./wcstartup.sh</td><td>Autostart Warcarrier with wlan0 and /dev/ttyUSB0 (for WEAKERTH4N and WarcarrierOS)</td></tr>
</table>
