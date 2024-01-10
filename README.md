> Notice: This project is a practical application of our academic work and ensures anonymity. The executable file can be downloaded from the "Release" section and there is a "Quick Start" instructions in README.

<h1 align="center">Rapier🗡</h1>

Rapier is a command-line tool designed for API black-box vulnerability testing. It captures API traffic via browser proxy and conducts deep recognition and mutation of API parameters in a tree structure. Additionally, Rapier incorporates various optimization strategies to enhance the precision and efficiency of API vulnerability testing.

![img_v3_026v_ca99f2bf-8467-4714-b7aa-ab4fd605ba8g](https://github.com/anonymous364872/Rapier_Tool/assets/156177920/1690957a-a56d-4f3b-b81d-ef2d1bb87652)


# Vulnerabilities Reported by Rapier

| ID | Vulnerability Type |
| -------- | -------- |
| [CVE-2022-35509](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-35509) | Cross-site Scripting (XSS)|
| [CVE-2022-39054](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-39054)	 | Cross-site Scripting (XSS)|
| [CVE-2022-41471](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-41471)	 | Broken Authorization|
| [CVE-2022-41472](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-41472)	 | Cross-site Scripting (XSS)|
| [CVE-2022-42154](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-42154)	 | Unrestricted File Upload|
| [CVE-2022-42735](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-42735)	 | Broken Authorization|
| CNVD-2022-67082   | Sensitive Data Exposure|
| CNVD-2022-70325	 | Sensitive Data Exposure |
| CNVD-2022-70707   |  SQL Injection|
| CNVD-2022-70700   |  Broken Authorization|
| CNVD-2022-71314   |  Broken Authorization|
| CNVD-2022-73094    |  Command Injection|
| CNVD-2022-73085    |  Unrestricted File Read|
| CNVD-2022-73378    |  Broken Authorization|


# Features

Rapier supports depth parameter injection, which has a powerful data parsing and mutation algorithm. It can parse common data formats (json, xml, form, etc.) into tree structure, and then mutate the tree according to the rules in poc, including the mutation of leaf nodes and tree structure. After the mutation is complete, the tree structure is restored to the original data format.

<img width="494" alt="image" src="https://github.com/anonymous364872/Rapier_Tool/assets/156177920/fd557ff2-e16f-4be6-bc5a-aaff3dfb8a1f">


Rapier automatically optimizes the queue of APIs to be tested. It calculates an efficient testing sequence based on the context relationships of the APIs and a vulnerability probability algorithm. This approach ensures comprehensive coverage of each API function while maximizing the efficiency of vulnerability discovery.

During traffic generation for testing, Rapier calculates the interrelation of parameters within an API. This allows for the mutation of multiple parameter values in a single test (one request and response) while ensuring these parameters are not logically interconnected. In practical applications, this method effectively reduces the number of tests by up to 70%, significantly enhancing testing efficiency.

# Quick Start

Rapier uses proxy mode for passive scanning, taking the Windows system as an example:

`.\rapier-windows-amd64.exe poc -l 127.0.0.1:8888 -f poc.yaml -o vuln.html`

# Built-in Test Vectors

Rapier includes hundreds of pre-built test vectors for vulnerability testing stored in `/poc`. These vectors are inserted into mutated tree nodes within Rapier's test message generation environment for vulnerability validation. These vectors are designed to cover a wide range of potential security flaws, providing a comprehensive testing approach to identify and address vulnerabilities effectively.

OWASP API Security Top 10

| Category | Vulnerability Type | Support |
| -------- | --------------------------------------------------- | ---- |
| OWASP API Security Top 10 | API1:2023 Broken Object Level Authorization | ✔|
| OWASP API Security Top 10 | API2:2023 Broken Authentication | ✔|
| OWASP API Security Top 10 | API3:2023 Broken Object Property Level Authorization | ✔|
| OWASP API Security Top 10 | API4:2023 Unrestricted Resource Consumption | ✔|
| OWASP API Security Top 10 | API5:2023 Broken Function Level Authorization | ✔|
| OWASP API Security Top 10 | API6:2023 Unrestricted Access to Sensitive Business Flows | |
| OWASP API Security Top 10 | API7:2023 Server Side Request Forgery | ✔ |
| OWASP API Security Top 10 | API8:2023 Security Misconfiguration | ✔ |
| OWASP API Security Top 10 | API9:2023 Improper Inventory Management |  |
| OWASP API Security Top 10 | API10:2023 Unsafe Consumption of APIs |  |


OWASP Web Security Top 10

| Category | Vulnerability Type | Support |
| -------- | --------------------------------------------------- | ---- |
| OWASP Web Security Top 10 | A01:2021 Broken Access Control | ✔|
| OWASP Web Security Top 10 | A02:2021 Cryptographic Failures | |
| OWASP Web Security Top 10 | A03:2021 Injection | ✔|
| OWASP Web Security Top 10 | A04:2021 Insecure Design | ✔|
| OWASP Web Security Top 10 | A05:2021 Security Misconfiguration | ✔|
| OWASP Web Security Top 10 | A06:2021 Vulnerable and Outdated Components | ✔|
| OWASP Web Security Top 10 | A07:2021 Identification and Authentication Failures | ✔|
| OWASP Web Security Top 10 | A08:2021 Software and Data Integrity Failures | ✔|
| OWASP Web Security Top 10 | A09:2021 Security Logging and Monitoring Failures | |
| OWASP Web Security Top 10 | A10:2021 Server Side Request Forgery (SSRF) | ✔|


A series of known vulnerabilities of public API services.

| Category | CVE Number | Vulnerability Name | Support |
| ----------- | -------------- | --------------------------------------------------- | ---- |
| CVE (2022) | CVE-2022-0540 | Jira authentication bypasses vulnerability | ✔|
| CVE (2022) | CVE-2022-22954 | VMware Workspace One Access SSTIRCE vulnerability | ✔|
| CVE (2022) | CVE-2022-26134 | Confluence OGNLRCE vulnerability | ✔|
| CVE (2022) | CVE-2022-34590 | SQL injection vulnerability of hospital management system | ✔|
| CVE (2022) | CVE-2022-35151 | KK File View v4.1.0 contains multiple cross-site scripting (XSS) vulnerabilities | ✔|
| CVE (2022) | CVE-2022-35413 | Wapples hard-coded vulnerability | ✔|
| CVE (2022) | CVE-2022-35914 | GLPI injection vulnerability | ✔|
| CVE (2022) | CVE-2022-36642 | Telos Alliance Omnia MPX Node Information Disclosure Vulnerability | ✔|
| CVE (2022) | CVE-2022-36883 | Jenkins Authentication Bypass Vulnerability | ✔|
| CVE (2022) | CVE-2022-37299 | Shirne CMS controller.php directory traversal vulnerability | ✔|
| CVE (2021) | CVE-2021-26086 | Atlassian Jira Server File Reading Vulnerability | ✔|
| CVE (2021) | CVE-2021-29622 | Prometheus redirection vulnerability | ✔|
| CVE (2021) | CVE-2021-30497 | Avalanche directory traversal vulnerability | ✔|
| CVE (2021) | CVE-2021-33807 | Carta Disgespage directory traversal vulnerability | ✔|
| CVE (2021) | CVE-2021-34473 | Microsoft Exchange Server Remote Code Execution Vulnerability | ✔|
| CVE (2021) | CVE-2021-35380 | Solari Di Udine Term Talk Server directory traversal vulnerability | ✔|
| CVE (2021) | CVE-2021-35464 | Java deserialization vulnerability of Forge Rock AM server | ✔|
| CVE (2021) | CVE-2021-35587 | Oracle Access Manager Authentication Bypass Vulnerability | ✔|
| CVE (2021) | CVE-2021-37538 | SmartDatasoft Smart Blog for Prestashop SQL Injection Vulnerability | ✔|
| CVE (2021) | CVE-2021-37704 | PhpFastCache Information Disclosure Vulnerability | ✔|
| CVE (2021) | CVE-2021-39211 | GLPI Information Disclosure Vulnerability | ✔|
| CVE (2021) | CVE-2021-39226 | Grafana vulnerability | ✔|
| CVE (2021) | CVE-2021-39327 | Bullet Proof Security WordPress Information Disclosure Vulnerability | ✔|
| CVE (2021) | CVE-2021-40149 | E1Zoom Information Disclosure Vulnerability | ✔|
| CVE (2021) | CVE-2021-40859 | Auerswald Compact 5500r backdoor vulnerability | ✔|
| CVE (2021) | CVE-2021-40875 | Gurock TestRail Senses Information Disclosure Vulnerability | ✔|
| CVE (2021) | CVE-2021-41192 | Redash spoofing session vulnerability | ✔|
| CVE (2021) | CVE-2021-41266 | Minio Authentication Bypass Vulnerability | ✔|
| CVE (2021) | CVE-2021-41381 | Payara Microcommunity directory traversal vulnerability | ✔|
| CVE (2021) | CVE-2021-41649 | Puneethreddyhc SQL injection vulnerability | ✔|
| CVE (2021) | CVE-2021-43496 | Clustering directory traversal vulnerability | ✔|
| CVE (2021) | CVE-2021-43798 | Grafana directory traversal vulnerability | ✔|
| CVE (2021) | CVE-2021-44077 | Zoho Remote Code Execution Vulnerability | ✔|
| CVE (2021) | CVE-2021-44152 | Reprise RLM ultra vires vulnerability | ✔|
| CVE (2021) | CVE-2021-44427 | SQL Injection Vulnerability in Rosario Student Information System | ✔|
| CVE (2021) | CVE-2021-44515 | Zoho Remote Code Execution Vulnerability | ✔|
| CVE (2021) | CVE-2021-44529 | IV Anti EPM Cloud Service Device RCE Vulnerability | ✔|
| CVE (2021) | CVE-2021-46381 | D-LINK DAP-1620 directory traversal vulnerability | ✔|
| CVE (2021) | CVE-2021-46417 | Franklin Fueling Systems Coli BR Information Disclosure Vulnerability | ✔|
| CVE (2021) | CVE-2021-46422 | Telesquare SDT-CW 3b1 command injection vulnerability | ✔|
| CVE (2020) | CVE-2020-12478 | Eampass injection vulnerability | ✔|
| CVE (2020) | CVE-2020-13700 | WordPress ACF-to-rest-API information disclosure vulnerability | ✔|
| CVE (2020) | CVE-2020-13937 | Apache Kylin security vulnerability | ✔|
| CVE (2020) | CVE-2020-14181 | Atlassian Jira Information Disclosure Vulnerability | ✔|
| CVE (2020) | CVE-2020-14408 | Agent Jo Cockpit cross-site scripting vulnerability | ✔|
| CVE (2020) | CVE-2020-15148 | Yii code problem vulnerability | ✔|
| CVE (2020) | CVE-2020-35338 | Mobile View Point Wireless Multiplex Terminal Trust Management Vulnerability | ✔|
| CVE (2020) | CVE-2020-35476 | OpenTS DB command injection vulnerability | ✔|
| CVE (2020) | CVE-2020-35489 | WordPress Contact-Form-7 Code Problem Vulnerability | ✔|
| CVE (2020) | CVE-2020-35736 | lift off gate one path traversal vulnerability | ✔|
| CVE (2020) | CVE-2020-36112 | Project Worlds Online Book Store Project in PHP SQL Injection Vulnerability |✔|
| CVE (2020) | CVE-2020-36289 | Atlassian Jira Server and Atlassian JIRA Data Center Information Disclosure Vulnerability | ✔|
| CVE (2020) | CVE-2020-26948 | Embry Server Code Problem Vulnerability | ✔|
| CVE (2020) | CVE-2020-27361 | Akkadian Provisioning Manager Security Vulnerability | ✔|
| CVE (2020) | CVE-2020-27467 | LFI-Process Wire CMS Path Traversing Vulnerability | ✔|
| CVE (2020) | CVE-2020-27866 | Vulnerability of several Netgear products | ✔|
| CVE (2020) | CVE-2020-27982 | IceWarp Mail Server cross-site scripting vulnerability | ✔|
| CVE (2020) | CVE-2020-29395 | WordPress plugin cross-site scripting vulnerability | ✔|
| CVE (2020) | CVE-2020-24312 | WordPress plugin mndpsingh287wp file manager information disclosure vulnerability | ✔|
| CVE (2020) | CVE-2020-24550 | Elastic Episerver Find input validation error vulnerability | ✔|
| CVE (2020) | CVE-2020-24571 | Nexus QA Nexus DB path traversal vulnerability | ✔|
| CVE (2020) | CVE-2020-24949 | PHP-Fusion security vulnerability | ✔|
| CVE（2020） | CVE-2020-26073 | Cisco? SD-WAN vManage information disclosure vulnerability | ✔|
| CVE (2020) | CVE-2020-26876 | WordPress security vulnerability | ✔|
| CVE (2020) | CVE-2020-16139 | Cisco 7937g input validation error vulnerability | ✔|
| CVE (2020) | CVE-2020-17453 | WSO2 Management Console cross-site scripting vulnerability |✔|
| CVE (2020) | CVE-2020-17519 | Apache Flink vulnerability | ✔|
| CVE (2020) | CVE-2020-19625 | Sheila 1227 Gridx vulnerability | ✔|
| CVE (2020) | CVE-2020-20300 | vulnerability of weiphp SQL injection | ✔|
| CVE (2020) | CVE-2020-23015 | DEISO OPN Sense input validation error vulnerability | ✔|
| CVE (2019) | CVE-2019-0230 | Apache Struts Remote Code Execution Vulnerability | ✔|
| CVE (2019) | CVE-2019-2578 | Oracle Unauthorized Access Vulnerability | ✔|
| CVE (2019) | CVE-2019-2588 | Oracle Fusion Middleware Unauthorized Access Vulnerability | ✔|
| CVE (2019) | CVE-2019-3912 | Lab Key Server Community Edition Redirection Vulnerability | ✔|
| CVE (2019) | CVE-2019-6715 | WordPress Arbitrary File Reading Vulnerability |✔|
| CVE (2019) | CVE-2019-8449 | Jira Information Disclosure Vulnerability | ✔|
| CVE (2019) | CVE-2019-8903 | Total.js platform path traversal vulnerability | ✔|
| CVE (2019) | CVE-2019-10092 | Apache HTTP Server cross-site scripting problem | ✔|
| CVE (2019) | CVE-2019-10232 | Teclib GLPI SQL injection vulnerability | ✔|
| CVE (2019) | CVE-2019-10717 | BlogEngine.NET directory traversal vulnerability | ✔|
| CVE (2019) | CVE-2019-11248 | Kubernetes Healthz port public | ✔|
| CVE (2019) | CVE-2019-11581 | Jira template injection vulnerability | ✔|
| CVE (2019) | CVE-2019-12583 | zyxeluag, USG and ZyWall devices are not authorized to access |✔|
| CVE (2019) | CVE-2019-12962 | Vulnerability of Livezilla Server XSS |✔|
| CVE (2019) | CVE-2019-13101 | D-LINK DIR-600M Information Disclosure Vulnerability | ✔|
| CVE (2019) | CVE-2019-13462 | Lansweeper SQL injection vulnerability | ✔|
| CVE (2019) | CVE-2019-14322 | Pallets Werkzeug Error Handling Drive Name | ✔|
| CVE (2019) | CVE-2019-14974 | SugarCRM Enterprise XSS Vulnerability | ✔|
| CVE (2019) | CVE-2019-15858 | WordPress XSS Vulnerability |✔|
| CVE (2019) | CVE-2019-16313 | FW8 Router ROM Information Disclosure Vulnerability | ✔|
| CVE (2019) | CVE-2019-16996 | METINFO 7.0.0 beta SQL injection vulnerability | ✔|
| CVE (2019) | CVE-2019-17382 | Zabbix login bypass vulnerability | ✔|
| CVE (2019) | CVE-2019-17418 | MetInfo SQL Injection Vulnerability | ✔|
| CVE (2019) | CVE-2019-17503 | Kirona Dynamic Resource Scheduling (DRS) Information Disclosure Vulnerability | ✔ |
| CVE (2019) | CVE-2019-18393 | Ignite real-time OpenFire directory traversal vulnerability | ✔ |
| CVE (2019) | CVE-2019-18922 | AT-S107V.1.1.3 directory traversal vulnerability | ✔ |
| CVE (2019) | CVE-2019-19368 | Rumpus FTP Web XSS vulnerability | ✔ |
| CVE (2019) | CVE-2019-19781 | Citrix ADC and Gateway Directory Traversing Vulnerability | ✔ |
| CVE (2019) | CVE-2019-20085 | TVT NVMS-1000 device directory traversal vulnerability | ✔ |
| CVE (2019) | CVE-2019-20933 | Influx DB Authentication Bypass Vulnerability | ✔ |


# Custom Test Vectors

Custom test vectors are written in YAML format(`poc-rule.yaml` in this project). Here is description of all the arguments in a POC file.

```yaml
info:                                 # Basic information section, which the POC author can modify at will.
  author: test                        # Author
  name: test                          # Rule name
  description: test                   # Rule description
  time: 2022/10/20                    # Writing (modification) time
  note: test                          # Remarks
  reference:                          # Related information
    - test

mutate_rule:                          # Array value, can have multiple groups, they are in an And relationship.
- 
  mutate_position:                    # Mutation location, indicating which locations you choose to mutate
    header_all: false                 # Boolean value, indicating whether to mutate all HTTP headers.
    header_filter:                    # Array value, you can filter the HTTP headers you want to mutate by parameter name or value,
    - 
      args:                           # Integer, can only be 1 or 2, representing parameter name, parameter value.
      operator:                       # Integer, can only be 1 or 2, representing regular match, string equal
      value:                          # String, the value you want to filter
    body_all_leaf_argname: false      # Boolean value, indicating whether to mutate the parameter names of all leaf nodes in the body
    body_all_leaf_argvalue: false     # Boolean value, indicating whether to mutate the parameter values of all leaf nodes in the body
    body_leaf_add_node:               # Array value, representing the addition of leaf nodes in the body
    - 
      argname:                        # String, representing the parameter name
      argvalue:                       # String, representing the parameter value
    body_root_add_node:               # Array value, representing the direct addition of child nodes under the root node of the body
    - 
      argname:                        # String, representing the parameter name
      argvalue:                       # String, representing the parameter value
    body_filter:                      # Array value, you can filter the body nodes you want to mutate by parameter name or value
    - 
      args:                           # Integer, can only be 1 or 2, representing parameter name, parameter value.
      operator:                       # Integer, can only be 1 or 2, representing regular match, string equal
      value:                          # String, the value you want to filter
    body_str: false                   # Boolean value, indicating whether to operate on the entire body string
    method: false                     # Boolean value, indicating whether to operate on the method
    netloc: false                     # Boolean value, indicating whether to operate on the network location part of the URL
    path: false                       # Boolean value, indicating whether to operate on the path
    query_str:                        # Boolean value, indicating whether to operate on the entire query
    url:                              # Boolean value, indicating whether to operate on the entire URL, referring to the URL in the HTTP message that does not contain the protocol and domain name
    query_leaf_argname:               # Boolean value, indicating whether to operate on all query parameter names
    query_leaf_argvalue:              # Boolean value, indicating whether to operate on all query parameter values
    query_add_node:                   # Array value, representing the addition of child nodes in the query
    - 
      argname:                        # String, representing the parameter name
      argvalue:                       # String, representing the parameter value
    query_filter:                     # Array value, you can filter the query nodes you want to mutate by parameter name or value
    - 
      args:                           # Integer, can only be 1 or 2, representing parameter name, parameter value.
      operator:                       # Integer, can only be 1 or 2, representing regular match, string equal
      value:                          # String, the value you want to filter
  
  mutate_way:                         # Array value, mutation method. Represents the method of mutating the selected mutation location, can have multiple groups, they are in an OR relationship
  - 
    pos:                              # Integer, can only be 1, 2, or 3, representing insert at end, insert at random position, and replace
    value:                            # String, representing the value you want

response_check:                       # Array value, output check, used to check if the poc hits, multiple groups are in an OR relationship
-                                     # Parameters within each group are in an AND relationship
  status_code:                        # Represents the response status code
    value:                            # Value of the status code to check
    operator:                         # Comparison rule, can take values 1, 2, 3, 

```
  
It's important to note that the quality of the response_check section, which is used for response validation, affects the accuracy of the scan results. The following examples illustrate how to write a POC. An HTTP message is shown as an example:
  
```
POST /post HTTP/1.1
Accept: */*
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 45
Content-Type: application/json
User-Agent: python-httpx/0.22.0

{"userinfo": {"name": "jack", "age": 22}}
```
  
**Example 1**

This POC mutates the path from URL to /index.html; the response check rule is that the response status code value equals 200.

```yaml
mutate_rule:
- 
  mutate_position:                    # Mutation position, indicating where you choose to mutate
    url: true                         # Mutate the URL
  
  mutate_way:                         # Mutation method. Indicates how to mutate the chosen position
  - 
    pos: 3                            # Integer, can only be 1, 2, or 3, representing appending at the end, inserting at a random position, or replacing
    value: /index.html

response_check:                       # Array value, output check, used to check if the POC hits, multiple groups are in an OR relationship
-
  status_code:                        # Represents response status code
    value: 200                        # The value of the status code to check
    operator: 1                       # Comparison rule, can take values 1, 2, 3, 4, 5; representing operations like string inclusion, regular matching, greater than, less than, and equal to, applicable only to numerical values
```


**Example 2**

To change the value of the API parameter 'name' in the request body to "wang", the following POC is written, omitting the 'info' part of the POC file:

```yaml
mutate_rule:                          # Array value, can have multiple groups, in an And relationship.
- 
  mutate_position:                    # Mutation position, indicates the places you choose to mutate
    body_all_leaf_argvalue: true      # Boolean, indicates whether to mutate all leaf node parameter values in the body
  
  mutate_way:                         # Mutation method, indicates how to mutate the chosen position
  - 
    pos: 3                            # Integer, can only be 1, 2, or 3, representing appending at the end, inserting at a random position, or replacing
    value: wang

response_check:                       # Array value, output check, used to check if the POC hits, multiple groups in an OR relationship
-                                     # Parameters within each group in an AND relationship
  status_code:                        # Represents response status code
    value: 200                        # The value of the status code to check
    operator: 5                       # Comparison rule, can take values 1, 2, 3, 4, 5; representing operations like string inclusion, regular matching, greater than, less than, and equal to, applicable only to numerical values

```
After loading POC file the Rapier will mutate the origin API HTTP request to the following data:
```
POST /post HTTP/1.1
Accept: */*
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Type: application/json
User-Agent: python-httpx/0.22.0

{"userinfo": {"name": "wang", "age": 10}}
```

# Problem Feedback
[GitHub issue](https://github.com/StarCrossPortal/rapier/issues) 
