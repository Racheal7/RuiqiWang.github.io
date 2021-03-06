---
layout: post
title: SSH Server Tutorial
date:   2019-02-28 13:50:39
categories: others
---

This tutorial will show you how to use a remote server.

<h1>Installation</h1>

<p>XShell is a powerful SSH client which allows you to easily create, edit, and launch multiple sessions simultaneously. Xftp is 
a file management software. You can drag and drop files between remote hosts and see transfer progress in real time. Manage queues and designate rules to take the hassle out of remote transfers.  </p>

<p>Download XShell and Xftp from the website: 
<a href="https://www.netsarang.com/en/xshell/">XShell Download</a>, 
<a href="https://www.netsarang.com/en/xftp/">Xftp Download</a>
</p>

<h1>Connect to the Remote Server</h1>

<p>After installation, click "File" -> "New..."</p>
<p>On the left hand side, choose "Connection" -> "SSH" -> "Tunneling"</p>
<p>Then on the right side, fill out the "Host" and the "Port Number", then click "Connect".</p>
<p>The server might require a user name and password, just fill in both of them in the pop-out window.
![connect]({{"/static/img/connection.png" | prepend: site.baseurl}})


<h1>Useful Commands</h1>

<p>The server installs python2.7, python3.6, cuda9.0, cuDNN7.0.</p>
<ul>
<li>cd: Change directory</li>
<li>To check cudnn version number: cat /usr/local/cuda/include/cudnn.h | grep CUDNN_MAJOR -A 2</li>
<li>To query GPU device state: nvidia-smi</li>
<li>If you want to kill an on-going process running on gpu: sudo kill -9 PID (PID can be seen using nvidia-smi. Kill a process may require user's password.)</li>
<li>Tab button: Press the tab button if you can only remember part of a command. This will automatically complete the command.</li>
<li>To run a python file: python filename.py</li>
</ul>

<p>More commands can be found at: <a href="https://blog.csdn.net/simongeek/article/details/45271089">Ubuntu commands</a>.</p>