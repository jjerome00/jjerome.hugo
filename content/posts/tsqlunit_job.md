---
title: "TSQLUnit_Job"
date: 2015-07-28
tags: [Development]
draft: false
showthedate: true
---

<p><div style=" border: #008000 1px solid; padding-left: 5px; padding: 5px; border-radius: 2px; background-color: #EBEBEB;"><div style="font-size: 16pt;"><b>TSQLUnit_Job</b></div>Allows <a target="_blank" href="http://sourceforge.net/projects/tsqlunit/">TSQLUnit</a> to run unit tests as a database job (SQL Agent) </div></p> <p>I finally released code publicly (yikes!). I doubt anyone will ever see it, let alone use it.  However, it still frightens me beyond belief!</p> Go check it out now on github:<br /><a target="_blank" href="https://github.com/jjerome00/TSQLUnit_Job">https://github.com/jjerome00/TSQLUnit_Job</a> <p>It's essentially a wrapper for TSQLUnit that allows unit tests to be run as a database job (SQL Agent), with the results sent as an email (with html formatting).  Read more about it on <a target="_blank" href="https://github.com/jjerome00/TSQLUnit_Job">Github</a>. </p> <p>I wrote it years ago for a situation where we needed to look for common error conditions in a legacy system.  We didn't have the resources to fix everything, so I would write a test to look for certain situations.  The job would notify me if something came up.  It was very useful for planning - if an issue only occurred once every six months, we might apply a different fix instead of re-writing the entire module. </p> <p>It requires <a target="_blank" href="http://sourceforge.net/projects/tsqlunit/">TSQLUnit</a>, and SQL Server (duh).</p> <a target="_blank" href="https://github.com/jjerome00/TSQLUnit_Job">TSQLUnit_Job</a>
