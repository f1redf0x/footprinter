# footprinter
A footprinting tool to grab a domain's external footprint. It does a crt transparency lookup with crt, an ip lookup in dig, and a CVE check in shodan. It then puts the results in a database.

# Pre-requisites:

You need to install the following tools and add them to your path.
- crt - https://github.com/cemulus/crt/tree/main
- nrich - https://gitlab.com/shodan-public/nrich/-/releases
- dig - should be in your OS repos
- sqlite3 - should be in your OS repos
- jq - should be in your OS repos

# Running the command

```
Usage: ./footprint -d <domain> [-l <limit>] [-e]
 -d    Domain to enumerate
 -l    Limit for crt (default 1000)
 -e    Exclude expired certificates
```

# An example

```
footprint -d mydomain.com -l 1000 -e
```
