Linux Kernel
============

Like we saw for the :ref:`bootloader <bsp_bootloader_label>`, the first thing you need is: sources.
Get them from *Bitbake* build directory (if you built the kernel with it) or get them from the Internet.

*Bitbake* will place the sources under directory:

.. raw:: html

 <div>
 <div><b class="admonition-host">&nbsp;&nbsp;Host&nbsp;&nbsp;</b>&nbsp;&nbsp;<a style="float: right;" href="javascript:select_text( 'kernel_rst-host-91' );">select</a></div>
 <pre class="line-numbers pre-replacer" data-start="1"><code id="kernel_rst-host-91" class="language-markup">/path/to/yocto/build_ls1021atwr_release/tmp/work/ls1021atwr-fsl-linux-gnueabi/linux-ls1/3.12-r0/git</code></pre>
 <script src="_static/prism.js"></script>
 <script src="_static/select_text.js"></script>
 </div>


If you are working with the virtual machine, you will find them under directory:

.. raw:: html

 <div>
 <div><b class="admonition-host">&nbsp;&nbsp;Host&nbsp;&nbsp;</b>&nbsp;&nbsp;<a style="float: right;" href="javascript:select_text( 'kernel_rst-host-92' );">select</a></div>
 <pre class="line-numbers pre-replacer" data-start="1"><code id="kernel_rst-host-92" class="language-markup">/home/architech/architech_sdk/architech/ls1021atwr/yocto/build_ls1021atwr_release/tmp/work/ls1021atwr-fsl-linux-gnueabi/linux-ls1/3.12-r0/git</code></pre>
 <script src="_static/prism.js"></script>
 <script src="_static/select_text.js"></script>
 </div>


We suggest you to **don't work under Bitbake build directory**, you will pay a speed penalty and you could
have troubles syncronizing the all thing. Just copy them some place else and do what you have to do.

If you didn't build them already with *Bitbake* or you just want to do make every step by hand, you can
always get them from the Internet by cloning the proper repository and checking out the proper commit.

Please, refer to the software documentation on the `Freescale SDK website <http://www.freescale.com/infocenter/index.jsp?topic=%2FQORIQSDK%2F2880375.html>`_