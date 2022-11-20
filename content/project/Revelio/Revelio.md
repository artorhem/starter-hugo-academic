---
title: Revelio
summary: A tool for doing static analysis of Python code for known vulnerabilities
tags:
- Software Engineeering
date: "2018-05-26T02:30:45"

# Optional external URL for project (replaces project detail page).
external_link: ""

links:
url_code: ''
url_pdf: 'uploads/detecting-vulnerabilities.pdf'
url_slides: ''
url_video: ''
---
**[Revelio](https://github.com/artorhem/cpsc-507)** is a tool that statically analyses Python code for known vulnerabilities. The tool provides a IDE plugin for Sublime for highlighting vulnerabilities as well as a command-line interfaces that provides the following features:

* Detection of vulnerable functions
* Detection of dependencies with vulnerabilities
* Automatic replacement of vulnerable function with safe alternatives
* Automatically running tests
* Detecting and updating outdated dependencies
* Downloading and analyzing of GitHub repositories as well as local files
* Automatically creating pull-requests to GitHub repositories to fix vulnerable functions

Currently, Revelio is just a prototype which was developed as part of a Software Engineering course.

## Installation

+ Download the source code of the tool
+ Install all requirements: `pip install -r requirements.txt`


## Configuration

In order for the tool to access the Github API the Github username and password need to be set as environment variables: `export GITHUB_USER=<user>` and `export GITHUB_PASSWORD=<password>`.

## Usage

To analyze a local repository the path must be provided:

`python cli.py --path "/local/path"`

To analyze a remote repository on github the URL to the repository must be provided:

`python cli.py --url "<URL>"`

To access the github repository the API access token needs to be set (see Configuration).

## Collected Data

For analyzed github repositories metrics will be collected in `/tmp` in `metrics.json`.


## Docker

To build the container:

`docker build -t 507 .`

To run the container:

`docker run --name 507 -v /tmp/dock:/tmp -e GITHUB_USER="username" -e GITHUB_PASSWORD="password" 507 & `

To remove the container:

`docker rm 507`


## Supported Testing Frameworks
The space of Python testing is very fragmented, and there is not universal method of writing testcases. To make the process simple and extensible, we use the tox test framework, that simplifies the execution of the tests. We look at the standard locations to discover tests, and support the standard testing mechanisms. Here are our assumptions:

+ The tests are placed in the ${project}/test[s] directory

+ The requirements necessary are present in a requirements.txt file. Often developers specify multiple versions of this file. 	We look for all files in the repository that have a name starting with 'requirements' to include for installation in the virtualenv.

+ The supported methods of testing the project are: setup.py with a test recipe, py.tests, nosetests, and plain old unittests.


## Known issues and fixes

When running `tox` in the macOS terminal the following error might ocurr:

`unknown locale: UTF-8 in Python`
