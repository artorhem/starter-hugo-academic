---
# An instance of the Experience widget.
# Documentation: https://wowchemy.com/docs/page-builder/
widget: experience

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 50

title: Experience
subtitle:

# Date format for experience
#   Refer to https://wowchemy.com/docs/customization/#date-format
date_format: Jan 2006

# Experiences.
#   Add/remove as many `experience` items below as you like.
#   Required fields are `title`, `company`, and `date_start`.
#   Leave `date_end` empty if it's your current employer.
#   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
experience:
  - title: Graduate Research Assistant
    company: University of British Columbia
    company_url: 'https://systopia.cs.ubc.ca/'
    company_logo: 
    location: Vancouver, BC
    date_start: '2018-01-05'
    date_end: '2019-10-11'
    description: |2-
       I worked on the [Trusted Capsules](https://github.com/TrustedCapsules) project in the [NSS Lab](https://www.cs.ubc.ca/labs/nss/html/index.html). Trusted Capsules provides graduated access control on remote devices. 
       * Uses __Linaro OP-TEE__ to manage fine-grained and trackable access to data on remote devices by linking the data to its access policy and encrypting them together
       * Leverage __FUSE__ to intercept operations on encrypted files to facilitate their on-demand decryption and re-encryption using the trusted application running in the Secure World
       * Prototype written in __C__ using a __LeMaker Hikey__ board with __ARM TrustZone__ and Linux 4.15.

  - title: Member of Technical Staff - II
    company: NetApp Inc.
    company_url: 'https://www.netapp.com/us/index.aspx'
    location: Bangalore, India
    date_start: '2015-07-04'
    date_end: '2017-07-07'
    description: |2-
       * Designed and implemented RussianRiver – a tool to validate and set host multipath settings for NetApp SAN
       * Worked on Unified Host Utilities Kits for Linux and Unix – a tool for checking the health of storage on the OS when connected to NetApp storage controllers. It provides path and state information for all NetApp LUNs present on a host by issuing queries to the Host Bus Adapter API libraries.
       * Handled infrastructure orchestration and configuration management for interop QA infrastructure
       * Designed and developed SAN Host Remediation Tool that automates the tasks to be performed on hosts when the storage migrates from NetApp 7Mode Data ONTAP to Cluster Data ONTAP. Supports all major host OS variants

  - title: Member of Technical Staff - I
    company: NetApp Inc.
    company_url: 'https://www.netapp.com/us/index.aspx'
    location: Bangalore, India
    date_start: '2013-07-04'
    date_end: '2015-07-04'
    description: |2-
       * Created a web application for iLAB using Django to help users select test configuration and track progress
       * Wrote Python and Perl scripts and libraries to test the interoperability of new Linux host and Data ONTAP features
       * Wrote SystemTap scripts to capture additional details during regression testing – I/O latency, CPU utilization, Device Mapper - Multipath Queue Depths, etc
  
  - title: Engineering Intern
    company: NetApp Inc.
    company_url: 'https://www.netapp.com/us/index.aspx'
    location: Bangalore, India
    date_start: '2012-07-04'
    date_end: '2015-06-15'
    description: |2-
       * Designed and developed iLAB – a framework that handles dynamic testbed creation, resource allocation and initialization, test execution, and testbed tear-down. Increased execution efficiency by 95%
design:
  columns: '2'
---
