---
title: Create icon for eclipse in Ubuntu 13.04
layout: post
date: 2013-07-10 19:19:00 UTC
updated: 2015-02-08 19:42:29 UTC
comments: false
categories: Eclipse IDE Linux
---
Just change "<span style="background-color: #f0f0f0; font-family: arial; font-size: 12px; line-height: 20px;">/home/daniel/eclipse</span>" with the path where you have your eclipse folder<br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> sudo gedit /usr/bin/eclipse  <br />   <br />   #!/bin/sh  <br />   export ECLIPSE_HOME="/home/daniel/eclipse"  <br />   $ECLIPSE_HOME/eclipse $*  <br />   <br /> sudo chmod 755 /usr/bin/eclipse  <br /> sudo chmod -R +r /home/daniel/eclipse  <br />   <br /> sudo gedit /usr/share/applications/eclipse.desktop  <br />   <br />   [Desktop Entry]  <br />   Encoding=UTF-8  <br />   Name=Eclipse  <br />   Comment=Java IDE  <br />   Exec=/home/daniel/eclipse/eclipse  <br />   Icon=/home/daniel/eclipse/icon.xpm  <br />   Terminal=false  <br />   Type=Application  <br />   Categories=GNOME;Application;Development;  <br />   StartupNotify=true  <br /></code></pre><br /><a href="http://oraculum.blog.br/blogoraculum/index.php/2011/01/21/instalar-o-aptana-studio-3-no-ubuntu-ou-debian/">Source</a>