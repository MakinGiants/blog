---
title: OPENGL and GLUT Tips
layout: post
date: 2012-11-06 22:28:00 UTC
updated: 2015-02-08 19:42:32 UTC
comments: false
categories: OpenGL
---
<br />// Make glut to call function&nbsp;displayfunc efficiently<br />glutPostRedisplay();<br /><br />//Same as glFlush but wait end notification<br />glFinish()<br /><br />//Size of the points, default 1.0<br />glPointSize(GLfloat)<br /><br />//Line width, default 1.0<br />glLineWidth(Glfloat)<br /><br />//Define how each face of the polygon will be drawn<br />glPolygonMode(GL_FRONT, GL_FILL);<br />glPolygonMode(GL_BACK, GL_LINE);<br /><br />//Define face type based on points order (ex: clockwise)<br />glFrontFace(GL_CW);//CW clock wise<br />glFrontFace(GL_CCW);//CCW counter clock wise<br /><br />//Schedule update function with 25 miliseconds<br />glutTimerFunc(25, update, 0);