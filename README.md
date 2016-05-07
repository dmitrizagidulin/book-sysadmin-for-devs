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
  - testing/staging environments, VPS hosting (AWS, Digital Ocean etc)
* Source Code Version Control
  - use a DVCS (git, hg, etc)
  - GitHub alternative - setting up GitLab
* Configuration Management
  - shell scripts, Ansible, Chef, Puppet
  - immutable infrastructure, environment as code
  - storing configuration / credentials securely
  - schema migration
  - data sets, testing/QA data, fixtures/auto-generating vs sanitizing
    of production data. Realistic data set size / composition.
* Setting up a Testing/CI Server
  - post commit hooks
  - Jenkins, Travis CI
  - unit tests, integration tests
  - Stress testing / load testing
  - Chaos Monkey / testing distributed systems
* Backups
* Logging
  - syslog
  - log aggregation

**Part 2: System Administration**

* Users, Groups, Permissions
  - OS-level
* Service Daemons
  - OS specific vs language specific (pm2 for Node, etc)
* Firewalls
* Encryption
  - in motion, at rest - record level vs whole disk
* SSL Certificates
  - self-generated, CAs, LetsEncrypt, wildcard certs vs not
* Web Servers and Proxies
  - never run bare apps (node/ruby/whatever) as root, use a web server
  - Apache, Nginx
  - HAProxy
* Caching
  - memcached, redis, etc
* Package Management
  - Language-specific (Maven/Gradle, ruby gems, pip, npm). Semver.
  - OS-specific (deb, yum, etc)

**Part 3: Monitoring and Maintenance**

* Cron
* Auto-update (apt, yum, etc)
* Monitoring
  - monitoring vs alerting (SNMP etc)
  - free software - Nagios and the like
  - commercial providers - Newrelic, Boundary, Datadog, many others
  - escalation / pagerduty
* Continuous Deployment / Continuous Delivery
  - monitor key metrics and error logs, automated rollback
  - a/b testing & staging levels
* Provisioning and Scaling
  - load balancers
  - live standby/failover
  - VMs vs bare metal
* System Maintenance
  - OS/package upgrades
  - Planned downtime
* Disaster Recovery

#### License

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />by <span xmlns:cc="http://creativecommons.org/ns#" property="cc:attributionName">Dmitri Zagidulin</span>,
licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.
