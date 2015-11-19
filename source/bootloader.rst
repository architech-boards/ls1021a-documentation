U-boot
======

Get sources
-----------

The bootloader used by TWR-LS1021A is **u-boot**. 
If you want to browse/modify the sources first you have to get them, if you already built TWR-LS1021A's bootloader with *Bitbake*, then you already have them on your (virtual) disk:

*Bitbake* will place *u-boot* sources under:

.. raw:: html

 <div>
 <div><b class="admonition-host">&nbsp;&nbsp;Host&nbsp;&nbsp;</b>&nbsp;&nbsp;<a style="float: right;" href="javascript:select_text( 'bootloader_rst-host-51' );">select</a></div>
 <pre class="line-numbers pre-replacer" data-start="1"><code id="bootloader_rst-host-51" class="language-markup">/path/to/yocto/build_ls1021atwr_release/tmp/work/ls1021atwr-fsl-linux-gnueabi/u-boot-ls1/2014.07-r0/git</code></pre>
 <script src="_static/prism.js"></script>
 <script src="_static/select_text.js"></script>
 </div>


this means that within the virtual machine you will find them under:

.. raw:: html

 <div>
 <div><b class="admonition-host">&nbsp;&nbsp;Host&nbsp;&nbsp;</b>&nbsp;&nbsp;<a style="float: right;" href="javascript:select_text( 'bootloader_rst-host-52' );">select</a></div>
 <pre class="line-numbers pre-replacer" data-start="1"><code id="bootloader_rst-host-52" class="language-markup">/home/architech/architech_sdk/architech/ls1021atwr/yocto/build_ls1021atwr_release/tmp/work/ls1021atwr-fsl-linux-gnueabi/u-boot-ls1/2014.07-r0/git</code></pre>
 <script src="_static/prism.js"></script>
 <script src="_static/select_text.js"></script>
 </div>


We suggest you to **don't work under Bitbake build directory**, you will pay a speed penalty
and you can have troubles syncronizing the all thing. Just copy the sources some place else
and do what you have to do.
