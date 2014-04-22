Danger Danger
==========
# Overview
Danger Danger provides a way to scan Netflix projects for vulnerable third party dependencies.  You simply specifiy the projects you would like to scan, and danger-danger automatically retrieves those WAR files from artifactory and generates an html report for each project.  

# How to use

Install Depdencencies:

```bash
pip install grequests, requests
```

Add the projects you would like to scan to the `projects.txt` file.  The default `projects.txt` file contains all Netflix projects.  

```bash
echo "merchweb" > projects.txt
```
