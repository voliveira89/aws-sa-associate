# Architecting for AWS Cloud - Best Practices Whitepaper

### Business Benefits of Cloud

* No upfront investment, just in time infrastructure, more efficient resource utilization, usage based billing, reduced time to market,

### Technical Benefits

* Scriptable Infrastructure, Auto Scaling, Proactive Scaling, Efficient Development Lifecycle, Improved Testability, Disaster Recovery and Business Connectivity, Overflow traffic into the cloud

### Design for failure

* Be pessimistic and design for failure. Assume capacity will be impacted, software will fail, and VMs will crash

### Decouple your components

* Loosely couple your applications such that failure of one doesn’t bring the whole system down. Loose coupling isolates the various layers and components of your application such that various components interact with each other asynchronously
* E.g. have SQS sitting between web server and application server and DB server

### Implement Elasticity

* Proactive Cycling Scaling – e.g. Month end load for payroll processing
* Proactive Event Scaling – New product launches, Black Friday, marketing campaigns
* Auto Scaling on Demand – use monitoring service to send triggers, to scale environment up or down, based on certain metrics

### Secure Your applications

* Web Tier – port 80/443 open to world
* App Tier – only SSH port 22 for developers from your company IP range
* DB – no access apart from App Tier

