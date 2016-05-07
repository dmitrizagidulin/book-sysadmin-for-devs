# System Administration for App Developers

In-progress book.

## Table of Contents

[Introduction](introduction.md)

**Part 1: Development and Testing**

* Choice of OS
  - debian, ubuntu, centos/rhel, freebsd
* Setting up the Environment
  - VMs and Containers (virtual box, vagrant, docker)
  - OSs as code - fog, docker compose, others
  - develop and test as close to production as possible
  - dev server login: passwords vs public keys
* Source Code Version Control
  - use a DVCS (git, hg, etc)
  - pick and document a workflow (branches, tags, merging strategy, etc)
  - GitHub alternative - setting up GitLab
  - don't forget code reviews, btw
  - binary assets?
* Configuration Management
  - shell scripts, Ansible, Chef, Puppet
  - language-specific (ruby Capistrano)
  - immutable infrastructure, environment as code
  - storing configuration / credentials securely. Environment variables. 
  - schema migration
  - data sets, testing/QA data, fixtures/auto-generating vs sanitizing
    of production data. Realistic data set size / composition.
* Setting up a Testing/CI Server
  - testing/staging environments, VPS hosting (AWS, Digital Ocean etc)
  - post commit hooks
  - Jenkins, Travis CI
  - unit tests, integration tests
  - Stress testing / load testing
  - Chaos Monkey / testing distributed systems
  - testing email systems
  - cross-browser / cross-OS testing
* Backups
  - regular / rotating backups
  - filesystem vs logical backups (exports)
  - privacy / security considerations, encryption
  - p.s. don't store passwords, credit cards, etc.
  - create a backup testing plan
  - off-site backups (tape, disks, generic S3 / glacier type services)
* Logging
  - syslog
  - error logs vs access logs
  - log aggregation
  - log viewers / analysis / graphing
* Teamware / Groupware
  - chat (irc, xmpp)
  - slack alternatives / microposts
  - bug tracking
  - wikis

**Part 2: Networking Basics**

* IP addresses, hostnames
* Sockets, Ports, Firewalls
* Private networking
* Registering domain names, DNS entries
* DDOS attacks

**Part 3: System Administration**

* Users, Groups, Permissions
  - OS-level
* Time Zones / Locales
  - clock synchronization
* Service Daemons
  - OS specific vs language specific (pm2 for Node, etc)
* Encryption
  - in motion, at rest - record level vs whole disk
* SSL Certificates
  - self-generated, CAs, LetsEncrypt, wildcard certs vs not
* Web Servers and Proxies
  - never run bare apps (node/ruby/whatever) as root, use a web server
  - Apache, Nginx
    - serving static assets, reverse proxies
  - HAProxy
* Caching
  - memcached, redis, etc
* Package Management
  - language-specific (Maven/Gradle, ruby gems, pip, npm). Semver.
  - OS-specific (deb, yum, etc)
  - disk snapshots/images, "appliances", pre-packaged VMs
* Email Servers
  - setting up smtp etc
  - use mail API providers (sendgrid etc) for welcome/recovery emails

**Part 4: Monitoring and Maintenance**

* Cron
* Auto-update (apt, yum, etc)
* Monitoring
  - monitoring vs alerting (SNMP etc)
  - free software - Nagios and the like
  - commercial providers - Newrelic, Boundary, Datadog, many others
  - escalation / pagerduty
  - statistics tl;dr (for metrics). min, max, avg, percentiles.
  - setting alerting thresholds
* Continuous Deployment / Continuous Delivery
  - monitor key metrics and error logs, automated rollback
  - a/b testing & staging levels
* Provisioning and Scaling
  - load balancers
  - live standby/failover
  - VMs vs bare metal
  - ephemeral instances / temporary workers
  - dedicated/specialized servers (ie what services get their own VMs?)
    - DBs, load balancers, log aggregators, identity providers
* I/O Performance Tuning
  - dedicated disks vs attached/mounted volumes. SANs, NFS, etc
  - provisioned IOPS
  - I/O testing & measuring
  - choice of file system / mount params
  - swap / paging settings
  - disk i/o schedulers
  - RAID
* System Maintenance
  - OS/package upgrades
  - Planned downtime
* Disaster Recovery
  - data recovery
  - postmortems / 5 whys

**Unsure/Maybe**

- Build Scripts: shell scripts, Make, lang-specific (rake, npm scripts vs grunt
  etc)
- Configuration formats (sysconfig, JSON, YAML, XML)
- File sharing (scp, sftp, WebDAV, rsync / drive / dropbox)

#### License

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />by <span xmlns:cc="http://creativecommons.org/ns#" property="cc:attributionName">Dmitri Zagidulin</span>,
licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.
