# spartanscan

# gibbits/spartanscan:v0.1
Beta build image supports nmap scan and vulners nse as a microservice 

# Base
Ubuntu 20.04

# Usage
Accepts nmap options and vulners script
see https://nmap.org/book/man-briefoptions.html

Quick scan

docker run --rm -it gribbits/spartanscan:[tag] [options] {target(s)}

```
docker run --rm -it gribbits/spartanscan:v0.1 -sV --script vulners 192.168.0.1
```

Extended Scan + Reports

docker run --rm -v $(pwd):/[mount directory]:[tag] -w [working directory] gribbits/spartanscan:[tag] [options] [output options] [output directory/filename] {target(s)}

```
docker run --rm -v $(pwd):/Desktop:Z -w /Desktop gribbits/spartanscan:v0.1 -sV -oA /Desktop/testscan1 192.168.0.1-255
```

# License
Apache 2.0
This Docker mage is deliberately free and opensouce, base distribution (Ubuntu) and packages, dependencies may be covered under different licenses that affect useage, distribution, linking, modification and permission. It is up to the user to use this Docker image consistent with all licensing aggreement herein.

Nmap License
https://nmap.org/npsl/
