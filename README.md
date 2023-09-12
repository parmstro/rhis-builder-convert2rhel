# convert2rhel demo

This repository contains the ansible automation files for a convert2rhel with Ansible Automation Platform and Satellite demo.

## Purpose:

The purpose is to demonstrate the ability to convert CentOS 7 and like operating systems to Red Hat Enterprise Linux 7 in bulk using AAP and Satellite as the engines for automation and content management. The environment uses the Red Hat Infrastructure Standard Adoption Model deployment, including Red Hat Identity Management.

## Outline:

The process creates a number of CentOS hosts with a variety of applications installed. All hosts are registered with a Red Hat Identity Management Server and are registered to Satellite already. The process steps through a series of procedures that would ideally be used for a conversion at scale environment:

 - ensure the convert2rhel prerequisites exist, including those necessary for automation
 - run a series of pre-conversion tasks including creating a snapshot of the host
 - perform the convert2rhel operation
 - run a series of post-conversion tasks as necessary (e.g. dependency checking, reboot the server, etc..)
 - verify the application or service on a given system functions to spec (ansible test provided by app team)
 - commit the conversion by deleting the snapshot and updating our conversion data

## Summary:

This is a sample only and is meant to allow you to understand the basics of converting CentOS 7 to RHEL at scale. 

PRs are welcome!

Enjoy.