# AWS Cloud History
- 2002: internal launch
- 2003: amazon infrastructure, idea to market
- 2004: public (USA) launch with SQS
- 2006: relaunch with SQS, S3 & EC2
- 2007: Europe launch

# Number Facts (2019)
- 35.02 billion dollar annual revenue
- 47% market share (Microsoft 2nd @ 22%)
- Pioneer and Leader of AWS Cloud Market for 9 years
- over 1,000,000 active users

# Use Cases
- Enterprise IT
- Backup & Storage
- Big Data analytics
- Website Hosting
- Mobile & Social Apps
- Gaming Servers
- Companies using AWS
  - McDonalds
  - 21st Century Fox
  - Activision
  - Netflix

# Global Infrastructure
- AWS Regions
- AWS Availability Zones
- AWS Data Centers
- AWS Edge Locations/Points of Presence
- [infrastructure.aws](https://aws.amazon.com/about-aws/global-infrastructure/)

# AWS Regions
- names like us-east-1, eu-west-3 etc...
- a region is a cluster of data centers
- most AWS services are region-scoped


# POSSIBLE EXAM QUESTION: How to choose a region?
- Launching a new application?
  - `compliance` with governance and legal requirements: data never leaves a region without explicit permission
  - `proximity` to customers: reduce latency
  - `available services` within a region: new services and features aren't available in every region
  - `pricing`: varies region to region but is transparent in the service pricing page

# AWS Availability Zones
- each region has many availability zones (min 3, max 6, avg 3)
- each availability zone (AZ) is one or more discrete data centers with redundant power, networking and connectivity e.g. so they're isolated from local issues e.g. natural disasters
- Example for Sydney
  - Region: ap-southeast-2
  - Availability Zones
    - ap-southeast-2a
    - ap-southeast-2b
    - ap-southeast-2c

# AWS Points of Presence (Edge Locations)
- 216 Points of Presence (205 Edge Locations & 11 Regional Caches) in 84 cities across 42 countries
- content delivered to end users with low latency

# Tour of AWS Console
- AWS has global services:
  - Identity and Access Management (IAM)
  - Route 53 (DNS Service)
  - CloudFront (Content Delivery Network)
  - WAF (Web Application Firewall)
- Most services are region-scoped
  - Amazon EC2 (IAAS)
  - Elastic Beanstalk (PAAS)
  - Lambda (FAAS)
  - Rekognition (SAAS)
- Region Table: https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/