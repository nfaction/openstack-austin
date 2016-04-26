# OpenStack HA, or not HA: That is the Question!

## Workday Production Requirements

* Automation
* Idempotent
* Scalable
* Secure
	* SSL on End Points
	* SSL on RabbitMQ
	* SSL on MySQL
	* IPTables
		* Running at the host level as well
* Stable
* Production Readiness
	* Logging
	* Monitoring
* Bonded physical interfaces per servers
* Multi-tenant
* High availability

## Reference Architecture

TCP Could - HA Referece Architechture

opentcpcloud.org/en/documentation/fuel/...

## Workday Architecture (NO HA)

Simple set up, 2 controllers, analytics + controller for analytics, 2 compute nodes, + mysql replication

He uses "Contrail" for neutron/logs?

## Circle Back for HA Solution

* Automation - **Jenkins + Chef**
* Idempotent - **Chef**
* Scalable - **8000 cores per cluster**
* Secure
	* SSL on End Points
	* SSL on RabbitMQ
	* SSL on MySQL
	* IPTables
		* Running at the host level as well
* Stable
* Production Readiness
	* Logging
	* Monitoring
* Bonded physical interfaces per servers
* Multi-tenant
* **High availability**

## HA Concepts

* Stateless & Stateful
	* nova-api,conductor, glance-api, keystone-api, neutron-api, and nove scheduler, ...
	* Messaging and DB
* Active/Passive vs Active/Active
	* Maintain a back-up system that will be ready to take over the "active" one
	* All service are "active" without manual intervention if one of them fail
* Control Plane
	* Ability to create, update and delete resources in cloud
* Data Plane
	* Managed workloads connectivity NS and EW
* Quorums and Clusters
	* Minimal number of nodes that must be functional in a cluster of redundant nodes in order for the cluster to remain functional

### Control Plane
* Availability zone
* Bare metal hosts
* Infrastructure services: DNS, LDAP, NTP, Chef, Nagios
* Clouds: Logical WPC domain boundary
* Availability Zone: All of the above


* Top of rack to host: 20GB bonded interfaces
* 160GB backbone network


### HA
Duplicate Entire infrastructure to each rack, so that HA is truely duplicated.  Top to bottom configuration duplication using Availability zones for HA.

### Data Plane
OpenContrail Architecture