```
     _                 _ _   
  __| |_ __  ___  __ _(_) |_ 
 / _` | '_ \/ __|/ _` | | __|
| (_| | | | \__ \ (_| | | |_ 
 \__,_|_| |_|___/\__, |_|\__|
                 |___/     
```

#What is DnsGit
[DnsGit](https://dnsgit.com) is an awesome DNS manange service.

    Git(Manage) ➩ DnsGit(middle ware)  ➩ DNSPod(resolve)

#Features

- you can do everything in command line
- you can rollback DNS Record as you wish
- secure and stable guarantee by [DNSPod](https://www.dnspod.com)
- you can switch to DnsGit easily by "github repo generator" from [DNSPod](https://www.dnspod.com)

#Get Started

1. Sign Up a DNSPod account and modify your domain ns record to DNSPod at registrar.
2. GitHub configure (you can use "github repo generator" to replace this step)
  - Login DnsGit with DNSPod account.
  - Create a GitHub repo.
  - Set Git repository on DnsGit.
  - Add WebHook (url is displayed on DnsGit index when you login) on GitHub.
3. Create Domain-File and Record-Line.
4. ```git push``` to apply your configuration.

---
**Yum !**

**Bravo !!**

**Excellent !!!**

**WOO HOO HOO !**




#Concept & Syntax

## Domain-File
file named by domain name.

##Record-Line 
one record mapping one line in domain file.

Syntax:

```
-- @type[required]  = record type(A, CNAME, MX, NS ...)
-- @name[required]  = relative name
-- @value[required] = record value(ipadress, domain ...)
-- @ttl[optional]   = TTL (default: user default TTL)
-- @mx[optional]    = MX Priority (default: 5)

type(name, value, ttl, mx)

```
Example:
```
A(@, 1.1.1.1, 默认, 600)
CNAME(dnsgit, dnsgit.com, 默认, 600)
MX(@, mxdomain.qq.com., 默认, 600, 10)

```

#Upcoming

- Notification with WeChat and SMS
- event log on website

#Powered by 
- [Node.js](http://nodejs.org/)
- [express](http://expressjs.com/)
