Root FS
=======

An SD card image provides the full system to boot with U-Boot and kernel. To flash an SD card image, run the following
commands (after have formatted it in FAT32):

.. raw:: html

 <div>
 <div><b class="admonition-host">&nbsp;&nbsp;Host&nbsp;&nbsp;</b>&nbsp;&nbsp;<a style="float: right;" href="javascript:select_text( 'rootfs_rst-host-41' );">select</a></div>
 <pre class="line-numbers pre-replacer" data-start="1"><code id="rootfs_rst-host-41" class="language-markup">cp tmp/deploy/images/ls1021atwr/fsl-image-core-ls1021atwr.ext2.gz.u-boot /path/your/sd
 cp tmp/deploy/images/ls1021atwr/uImage /path/your/sd
 cp tmp/deploy/images/ls1021atwr/uImage-ls1021a-twr.dtb /path/your/sd</code></pre>
 <script src="_static/prism.js"></script>
 <script src="_static/select_text.js"></script>
 </div>

.. important::

 sudo password is **architech**

Make sure everything has been written on the SD card:

.. raw:: html

 <div>
 <div><b class="admonition-host">&nbsp;&nbsp;Host&nbsp;&nbsp;</b>&nbsp;&nbsp;<a style="float: right;" href="javascript:select_text( 'rootfs_rst-host-42' );">select</a></div>
 <pre class="line-numbers pre-replacer" data-start="1"><code id="rootfs_rst-host-42" class="language-markup">sync</code></pre>
 <script src="_static/prism.js"></script>
 <script src="_static/select_text.js"></script>
 </div>

and unmount the SD card from your system.

Extra information on how to customize the file system and the different packages available from Freescale, 
can be found on the `IMXLINUX: Embedded Linux for i.MX Applications Processors <http://www.freescale.com/webapp/sps/site/prod_summary.jsp?code=IMXLINUX&fsrch=1>`_