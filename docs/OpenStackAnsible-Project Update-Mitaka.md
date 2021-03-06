# OpenStackAnsible: Project Update - Mitaka Achievements and Newton Plans

<https://etherpad.openstack.org/p/openstack-ansible-newton-update>

## Updates
Split out roles to simplify entire process, but has some pain points

They use OpenStack Tempest to test code

Most of these changes will be live via Newton release

## Implementation

Use containers to set up Galera cluster as well as other required clusters

Using SSL everywhere in N, and still uses linux bridge and will have LBaaS and FWaaS as well as VPNaaS

## Patches
Patches require Release notes and description changes information

## Cross Project
How to make OS easier to deploy

## OS Support
Ubuntu is most important, work on 16 heavily under way

CentOS is challenging, but good, but less need for this environment

## Ansible
2.1 just released a RC, and will start using it.

## Networking
Linux bridge scales very well to about 352 compute nodes, but OSA is working heavily on moving to OVS, since it has gotten better as of as of 2.0

Lots of people use linux bridge for simplicity and ease of use.  Scales very well and is easy to troubleshoot.  

LVM backed shared storage (STEER CLEAR if you want upgrades to be easier, every inst) Use Ceph, shared storage, etc. 


## Lessons learned, Advice

Use AIO, then try to do a multi-node deployment only after closely watching what AIO is doing.

Mitaka will be Ansible 1.9 FOREVER

Uses Linux Bridge now, but will move to DVR as of Newton, and in the future.

**Get an Ubuntu mirror set up**  Take waaay less time.  Use SSDs on all nodes

Opened bugs at beginning of day, and they are often resolved by the end of the day.  Open a bug, it will work well.  Longest time was a week.  Quick deploys, etc.

May be an Ansible role for Ubuntu Mirror to drop into directory

## Process

Use kick solution

Use LXD or VMs to try a set up.  Do NOT try to tear down OS on system, just destroy everything!!!!
