# Traditional-vs-Serverless-Design

<h2> Overview </h2>
Purpose: Compare traditional vs serverless architecture 
Application: Fenty 

<h2> Traditional Architecture </h2>

Components: 

- Load balancer, Web/App Servers, Microservices, Cache, Database, CDN

Scaling strategy: 

- Vertical (instance upgrades)
- Horizontal (Auto Scaling Group + CloudWatch alarms)

Challenges: 

- Management overhead
- Idle costs
- Scaling delays

<h2> Serverless Architecture </h2>

Components: 

- S3, CloudFront, API Gateway, Lambda, DynamoDB, EventBridge

Scaling:

- Automatic and Precision

Benefits: 

- Zero infrastructure management
- Cost-efficiency at scale

<h2>Performance and Cost</h2>

 <h3>Traditional Architecture<h3></h3>
 
 Performance Under Load  
- Good, if scaled horizontally, but slower boot time for new servers

Cold Starts
- No cold starts, always-on

Cost Efficiency 
- Inefficient at low traffic (you pay for idle servers)

Resource Allocation 
- Fixed resources (manual config)

Maintenance 
- Needs DevOps effort (OS updates, security patches)

<h3> Serverless Architecture </h3>

Performance Under Load 
- High responsiveness due to function-level concurrency and event triggers

Cold Starts
- May experience cold starts on low traffic (can be optimized)

Cost Efficiency 
- Pay only for usage, ideal for burst traffic

Resource Allocation 
- Dynamic allocation per execution

Maintenance 
- Little to none (AWS handles infrastructure)

<h2>Architectural Decision Rationale</h2>

- Traditional for control, stateful apps, legacy systems
- Serverless for burst load, rapid deployment, minimal ops

<h2> Use Case Scenarios </h2>

<h3> Traditional Server Architecture is better when:</h3>

- You need long-running processes or persistent server connections
- Your app requires stateful connections or heavy computation
- Legacy systems or existing infrastructure depend on a VM-based setup
- More control over server environment is required (custom OS, dependencies)

<h3> Serverless Architecture is better when:</h3>

- You expect irregular or burst traffic (flash sales, product drops)
- You want faster time to market and less infrastructure overhead
- You're building event-driven, stateless microservices
- You want cost-effective scaling at startup or for unpredictable loads

 
