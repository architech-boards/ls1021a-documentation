On **TWR-LS1021A** the USB-UART port **J5** is used for serial console.

.. image:: _static/serial-usb.jpg

which you can connect, by means of a mini-USB cable, to your personal computer.

.. note::

 Every operating system has its own killer application to give you a serial terminal interface. In this guide, we are assuming your **host** operating system is **Ubuntu**.

On a Linux (Ubuntu) host machine, the console is seen as a ttyACMX device and you can access to it by means
of an application like *minicom*.

*Minicom* needs to know the name of the serial device. The simplest way for you to discover
the name of the device is by looking to the kernel messages, so:

1. clean the kernel messages

.. raw:: html

 <div>
 <div><b class="admonition-host">&nbsp;&nbsp;Host&nbsp;&nbsp;</b>&nbsp;&nbsp;<a style="float: right;" href="javascript:select_text( 'serial_console_rst-host-161' );">select</a></div>
 <pre class="line-numbers pre-replacer" data-start="1"><code id="serial_console_rst-host-161" class="language-markup">sudo dmesg -c</code></pre>
 <script src="_static/prism.js"></script>
 <script src="_static/select_text.js"></script>
 </div>

2. power on the board connecting the power supply cable to PWR JACK J3

3. connect the mini-USB cable to the board

4. display the kernel messages

.. raw:: html

 <div>
 <div><b class="admonition-host">&nbsp;&nbsp;Host&nbsp;&nbsp;</b>&nbsp;&nbsp;<a style="float: right;" href="javascript:select_text( 'serial_console_rst-host-162' );">select</a></div>
 <pre class="line-numbers pre-replacer" data-start="1"><code id="serial_console_rst-host-162" class="language-markup">dmesg</code></pre>
 <script src="_static/prism.js"></script>
 <script src="_static/select_text.js"></script>
 </div>

5. read the output

.. raw:: html

 <div>
 <div><b class="admonition-host">&nbsp;&nbsp;Host&nbsp;&nbsp;</b>&nbsp;&nbsp;<a style="float: right;" href="javascript:select_text( 'serial_console_rst-host-163' );">select</a></div>
 <pre class="line-numbers pre-replacer" data-start="1"><code id="serial_console_rst-host-163" class="language-markup">[ 5522.462414] usb 2-1.1: new full-speed USB device number 6 using ehci_hcd
 [ 5522.557574] cp210x 2-1.1:1.0: cp210x converter detected
 [ 5522.630151] usb 2-1.1: reset full-speed USB device number 6 using ehci_hcd
 [ 5522.723501] usb 2-1.1: cp210x converter now attached to /dev/ttyACM0</code></pre>
 <script src="_static/prism.js"></script>
 <script src="_static/select_text.js"></script>
 </div>

As you can see, here the device has been recognized as **/dev/ttyACM0**.

Now that you know the device name, run *minicom*:

.. raw:: html

 <div>
 <div><b class="admonition-host">&nbsp;&nbsp;Host&nbsp;&nbsp;</b>&nbsp;&nbsp;<a style="float: right;" href="javascript:select_text( 'serial_console_rst-host-164' );">select</a></div>
 <pre class="line-numbers pre-replacer" data-start="1"><code id="serial_console_rst-host-164" class="language-markup">sudo minicom -ws</code></pre>
 <script src="_static/prism.js"></script>
 <script src="_static/select_text.js"></script>
 </div>

If minicom is not installed, you can install it with:

.. raw:: html

 <div>
 <div><b class="admonition-host">&nbsp;&nbsp;Host&nbsp;&nbsp;</b>&nbsp;&nbsp;<a style="float: right;" href="javascript:select_text( 'serial_console_rst-host-165' );">select</a></div>
 <pre class="line-numbers pre-replacer" data-start="1"><code id="serial_console_rst-host-165" class="language-markup">sudo apt-get install minicom</code></pre>
 <script src="_static/prism.js"></script>
 <script src="_static/select_text.js"></script>
 </div>

then you can setup your port with these parameters:

.. raw:: html

 <div>
 <div><b class="admonition-host">&nbsp;&nbsp;Host&nbsp;&nbsp;</b>&nbsp;&nbsp;<a style="float: right;" href="javascript:select_text( 'serial_console_rst-host-166' );">select</a></div>
 <pre class="line-numbers pre-replacer" data-start="1"><code id="serial_console_rst-host-166" class="language-markup">+-----------------------------------------------------------------------+
 | A -    Serial Device      : /dev/ttyACM0                              |
 | B - Lockfile Location     : /var/lock                                 |
 | C -   Callin Program      :                                           |
 | D -  Callout Program      :                                           |
 | E -    Bps/Par/Bits       : 115200 8N1                                |
 | F - Hardware Flow Control : No                                        |
 | G - Software Flow Control : No                                        |
 |                                                                       |
 |    Change which setting?                                              |
 +-----------------------------------------------------------------------+
         | Screen and keyboard      |
         | Save setup as dfl        |
         | Save setup as..          |
         | Exit                     |
         | Exit from Minicom        |
         +--------------------------+</code></pre>
 <script src="_static/prism.js"></script>
 <script src="_static/select_text.js"></script>
 </div>

If on your system the device has not been recognized as */dev/ttyACM0*, just replace */dev/ttyACM0*
with the proper device.

Once you are done configuring the serial port, you are back to *minicom* main menu and you can select *exit*.
