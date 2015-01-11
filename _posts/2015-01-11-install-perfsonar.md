---
layout: post
title: "using YUM repository for installing perfSONAR on CentOS6 "
keywords: ["perfSONAR", "CentOS"]
description: "using YUM repository for installing perfSONAR on CentOS6 "
category: "tech"
tags: ["perfSONAR"]
---
{% include JB/setup %}


### Install the EPEL repository and  the Internet2 repository

On 32-bit machines:

	rpm -ivh http://linux.mirrors.es.net/fedora-epel/6/i386/epel-release-6-8.noarch.rpm  
	rpm -ivh http://software.internet2.edu/rpms/el6/i386/main/RPMS/Internet2-repo-0.5-3.noarch.rpm


On 64-bit machines:

	rpm -ivh http://linux.mirrors.es.net/fedora-epel/6/x86_64/epel-release-6-8.noarch.rpm  
	rpm -ivh http://software.internet2.edu/rpms/el6/x86_64/main/RPMS/Internet2-repo-0.5-3.noarch.rpm


### Install the Toolkit

    yum install perl-perfSONAR_PS-Toolkit perl-perfSONAR_PS-Toolkit-SystemEnvironment

### Reboot the machine

### Relogin and you should see the motd (Unix, Message of the Day) like following


	Last login: Thu Dec 18 01:39:15 2014 from 10.x.x.x
	Welcome to the perfSONAR Toolkit v3.4.1
	You may create accounts to manage this host through the web interface by running the following a
	/opt/perfsonar_ps/toolkit/scripts/nptoolkit-configure.py
	The web interface should be available at:
	https://yourmachineip/toolkit 
	[root@localhost ~]# 


### Add an account to manage perfSONAR Toolkit by the motd

### Visit  https://machineipadress/toolkit to see the  perfSONAR UI