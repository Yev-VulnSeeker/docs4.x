# Using Uboot to Debrick Your Router

You may have bricked your router if you were doing some DIY projects or flashed a wrong firmware. You may not be able to access your router but you can re-install the firmware by using Uboot failsafe.

---

Please follow the procedures below to access the Uboot Web UI and re-install the firmware.

You can also refer to video tutorial below.

<iframe width="560" height="315" src="https://www.youtube.com/embed/EAaaw8nyrnE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<ol type="1">
  <li>
    <p>
      First you have to download <b>firmware</b> to your computer. You can download the firmware <a href="https://dl.gl-inet.com/" target="_blank">here</a>. Some models, such as GL-AR750S-EXT, it is available in two formats of firmware, please use the firmware with the .img extension.
    </p> 
  </li>
  <li>
    <p>
      Connect your computer to the <b>Ethernet port (either LAN or WAN)</b> of the router. You <b>MUST</b> leave the other port <b>unconnected</b>.
    </p>
  </li>
  <li>
    <p>
    Press and hold the Reset button firmly first, and then power on your device. (If your device does not have a power button, plugging it in will power it on automatically.)
    </p>
    <p>If you can not find the reset button, please refer to our page,<a href="../../troubleshooting/reset" target="_blank"> How to Repair and Reset</a>.</p>
    <p>
      Release your finger when you see the LED has flashed:
    </p>
    <p>
      The Power LED will light up. Then, other LEDs will start flashing.
    </p>
    <ul>
      <li><b>6 times</b> for GL-MiFi, and then the LTE light will faintly flash twice.</li>
      <li><b>5 times</b> for GL-AR150, GL-AR300M, GL-USB150, GL-AR750, GL-AR750S-EXT (Slate), GL-X750 (Spitz), GL-MT300N-V2, GL-E750 (Mudi), microuter-N300.
      </li>
      <li><b>4 times</b> for GL-S1300, GL-B1300. 
        <div>The left most LED may stay on the whole time while the rightmost LED flashes 4 times, then the middle LED turns on and stays on. </div>
        <div>(For some old GL-B1300, the left most LED stays on the whole time, and both the middle LED and the rightmost LED flash 5 times at the same time then they stay on.)</div>
      </li>
      <li><b>3 times</b> for GL-MT300N, GL-MT300A.</li>
        <li>For <strong>GL-SF1200</strong>, the 5G LED flashes 5 times then stays on.</li>
        <li>For <strong>GL-AX1800(Flint)</strong>, the blue light flashes 5 times then turns white and stay on.</li>
        <li>For <strong>GL-XE300(Puli)</strong>, the LAN light falshes 5 times then WIFI light stay on.</li>
        <li>For <strong>GL-X300B(Collie)</strong>, the WAN light flashes 5 times then WIFI light stay on.</li>
        <li>For <strong>GL-SFT1200(Opal)</strong>, the blue light flashes 5 times then turns white and stay on.</li>
        <li>For <strong>GL-AP1300(Cirrus)</strong>, the power light falshes 5 times then stay on.</li>
        <li>For <strong>GL-MT1300(Beryl)</strong>, the LED is blue at first, flash twice slowly, then light 5 times a bit quick and turn to white and stay on.</li>
        <li>For <strong>GL-B2200(Velica)</strong>, the two LEDs are blue at first, then turn white to flash 5 times, then turn blue and stay on.</li>
        <li><b>No repeat LED flashes signal </b> for GL-MV1000. (Power and WAN LEDs will stay on the whole time.)</li>
    </ul>
  </li>
  <li>
    <p>Set your computer’s IP address to <b>192.168.1.2</b>. Please check the step-by-step guide for different operating systems below:</p>
    <details>
      <summary>Windows 7 / Windows 10</summary>
      <ol type="1">
        <li>Go to Control Panel -> Network and Internet -> Network and Sharing Center -> Change adapter settings.</li>
        <li>Right click Local Area Connection -> Properties.</li>
        <li>Click Internet Protocol Version 4 (TCP/IPv4) -> Properties.</li>
        <li>Set the IP adress to 192.168.1.2 manually.</li>
          <img src="https://static.gl-inet.com/docs/en/2.x/troubleshooting/src/debrick/set_ip.jpg">
      </ol>
    </details>
    <details>
      <summary>macOS</summary>
      <ol type="1">
        <li>Go to System Preferences -> Network.</li>
        <li>Chooose Ethernet -> Advanced -> TCP/IP.</li>
        <li>In Configure IPv4, choose Manually.</li>
        <li>Set the IPv4 Address to 192.168.1.2 manually.</li>
      </ol>
    </details>
	</li>
  <li>
    <p>
    Use Firefox or Chrome to visit <b>http://192.168.1.1</b>.<img src="https://static.gl-inet.com/docs/en/2.x/troubleshooting/src/debrick/ui.jpg">
    </p>
  </li>
  <li>
    <p>
    Click <b>Choose File</b> to find the firmware file. Then click <b>Update firmware</b>. 
    </p>
  </li>
  <li>
    <p>
    Wait for around 3 minutes. Don’t power off your device when updating. The router is ready when both power and  Wi-Fi LED are on or you can find its SSID on your device.
    </p>
  </li>
  <li>
    <p>
    Revert the IP setting you did in step 4 and connect your device to the LAN or Wi-Fi of the router. You will be able to access the router via 192.168.8.1 again.
    </p>
  </li>
</ol>
