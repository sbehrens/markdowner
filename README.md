Danger Danger
==========
# Overview
Danger Danger provides a way to scan Netflix projects for vulnerable third party dependencies.  You simply specifiy the projects you would like to scan, and danger-danger automatically retrieves those WAR files from artifactory and generates an html report for each project.  

This project leverages the [Depencency Checker](https://www.owasp.org/index.php/OWASP_Dependency_Check) OWASP project.  

# How to use

Install Depdencencies:

```bash
pip install grequests, requests
```

Add the projects you would like to scan to the `projects.txt` file.  The default `projects.txt` file contains all Netflix projects.  

```bash
echo "merchweb" > projects.txt
```

Run the scanner:

```bash
python danger-danger.py
```

When the tool completes, reports for each project will be placed in the `reports` directory.  

If a WAR file could not be located for the project in Artifactory, the package name will be logged in the `missing_wars.txt` file.

