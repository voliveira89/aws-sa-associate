# Routing Policies

**Simple - Default** - when a single resource performs function for your domain - only one web server serves content

**Weighted** – send x% of traffic to site A and remainder \(100 – x\) % of it to site B. Need not be two different regions. Can be even two different ELBs. This split is over length of day not based on number of individual subsequent requests.

* Weights – a number between 0 and 255. Route53 calculates auto %age
* AWS Takes Global view of DNS – not local / ISP view.
* A/B testing is perfect use case for Weighted Routing policy

**Latency** – allows you to route traffic based on lowest network latency for your end user. To the region which gives fastest response time.

* Create record set for EC2 or ELB resource in each region that hosts website. When R53 receives a query it will then determine response based on lowest latency
* How will the users get the best experience? – evaluated dynamically by R3

**Failover** – when you want to create an active /passive setup. DR site. R53 monitors health of site. If active fails then R53 routes traffic to passive site. Here you designate a primary and secondary endpoint for your hosted zone record

**Geolocation** – choose where to route traffic based on geographic location of users. Different from Latency based as the routing is hardwired irrespective of latency.  


