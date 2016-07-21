---
title: Install and compile GLUT and OPENGL projects
layout: post
date: 2012-11-06 22:21:00 UTC
updated: 2015-02-08 19:42:32 UTC
comments: false
categories: Linux OpenGL
---
<h2>Install</h2><h4>Linux</h4><blockquote class="tr_bq">$sudo aptitude install freeglut3-dev</blockquote><h4>Windows&nbsp;</h4><div>The latest version (3.7) of GLUT windows binaries can be found at <a href="http://www.xmission.com/~nate/glut.html">http://www.xmission.com/~nate/glut.html</a> or from a million other places on the web. Name of the zip file is: glut-3.7.6-bin.zip<br /><br />Download it and extract the zipfile to some temporary folder.<br /><br />Copy <i>glut32.dll</i> file to your windows System folder. On Win2000/XP its<br /><blockquote class="tr_bq">C:\winnt\system. On Win98 its C:\windows\system.</blockquote><br />&nbsp;<a href="http://www.cs.rpi.edu/~girdhy/komputer_grafix/installing_glut.html">Source</a></div><div><br /></div><h2>Compile</h2><div>Now you can use "GL/glut.h" in your projects...</div><blockquote class="tr_bq">$g++ main.cpp -o outname -lglut</blockquote><h2>Run</h2><blockquote class="tr_bq">$./outname</blockquote><br />