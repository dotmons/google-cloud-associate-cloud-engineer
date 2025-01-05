GCP:

Google Compute: Can create VM from this.

Cloud Deployment Models:
Public Cloud
Multi Cloud
Private Cloud
Hybrid Cloud: On private cloud (Anthos) + on public cloud
Hybrid Environment: On prem server + public cloud

Hosting types:
	- Traditional On-Prem (All)
	- Data Center hosted (Data Centre)
	- CAAS (Container as a service)
	- IAAS	(Data Center, Virtualization, Network)
	- PAAS	(All except application and Data)
	- SAAS
	- FAAS (Function as a service)
	- Cloud Run

Geography:
	1. Zones
	2. Region
	3. Multi-Region

Types:

	Google Persistent Disk:
	Attached to a single VM at a time (like EBS), but you can also use read-only mode for multiple VMs.
	•	Persistent Disk can be either:
	•	Standard PD: For cost-effective storage with moderate performance.
	•	SSD PD: For high IOPS and low latency, suitable for performance-intensive workloads.
	•	Snapshots can be used for backups and disaster recovery.
	•	Resizable and offers encryption by default.

	Google Filestore: Used for file storage:
		:
	Provides shared file systems accessible by multiple Compute Engine VMs.
	•	Scalable capacity and performance.
	•	Suitable for applications like content management systems, shared workloads, or big data processing.
	•	Offers Standard and High-Scale tiers to match performance needs.
	•	Supports POSIX compliance, making it compatible with many applications.

	Criteria				Google Persistent Disk							Google Filestore
	Storage Type			Block storage									File storage
	Access					Single VM (read-only sharing possible)			Multiple VMs or containers
	Workload Type			Databases, VM disks								Shared workloads, Big Data
	Scalability				Fixed size, manual scaling						Scalable capacity and performance
	Performance	Low latency, high IOPS	High throughput, multi-client access
	POSIX Support	Not applicable	Fully POSIX-compliant
	Cost	Generally lower for single-use scenarios	Higher cost for shared access


	GCP Compute Service:
		Compute Engine: IAAS service, can launch VM from this
		App Engine: Platform as a service, select PHP, Python shell for your application
		Container Engine: Kubernetes service that manages your containers
		Container Registry: That allows you register your container
		Cloud Functions: This is the serverless functionality GCP provides

		Cloud Storage: Used to store files, stored in form of objects and stored in containers called buckets, Media, backups, analytics datasets
		Cloud BigTable: Wide-column NoSQL, Analytics, time-series data, Low latency, Works with BigQuery, Hadoop, Spark
		Cloud Datastore: Document-based NoSQL, Web and mobile application backends, moderate latency, Native for app development
		Cloud SQL: Used for managed database like postgress, mysql, sqlserver
		Persistent Disk: Must be attached to a VM instance to be accessed. Typically formatted with a file system for applications. File systems, databases, boot disks

		Network Services:
		Cloud Virtual Network: is a fully managed, flexible, and scalable networking service that provides networking functionality to connect and secure your resources.
		Cloud Load Balancing: Distributes traffic globally to backend resources using HTTP(S), SSL, or TCP.
		Cloud CDN (Content Delivery Network): Accelerates content delivery by caching at edge locations globally.
		Cloud Storage Transfer Service: Simplifies the transfer of large datasets to GCP.
		Cloud DNS: A globally scalable and managed DNS service for public and private DNS zones.

		GCP Security Services:
		Cloud Resource Manager: Let's you set up a structure service that provides the ability to organize and manage GCP resources hierarchically. It helps users manage their cloud resources by creating and controlling access to resources within a structured hierarchy of organizations, projects, and folders.
		Cloud IAM:	Role management and user access management, You can create policies here as well
		Cloud Security Scanner:	is a security assessment tool designed to identify vulnerabilities in web applications deployed on GCP 
		Cloud Platform Security: encompasses the security measures, services, and compliance frameworks provided by Google to ensure the safety and integrity of its customers’ assets. e.g. contain IAM, data and network security


	GCP Management and Developer Tools:
		Management Tools:
			StackDriver, Monitoring, Logging, Error reporting, Trace, Debugger, Cloud Shell, Cloud Console, Cloud API, Cloud Endpoints
		Developer Tools:
			Cloud SDK, Deployment Manager, Cloud test Lap, Cloud Tools for Powershell, Cloud Tools for powershell, Cloud Source Repository

	GCP Big Data Services:
		BigQuery: Data warehouse and process data at a very low latency... Apache hadoop, Spark
		DataProc:
		Pub/Sub: e.g. Kafka
		Dataflow:
		Datalab:
		Genomics: Works on research data

	GCP Machine Learning Services:
		Cloud Machine Learning
		Speech API
		Translation API
		Vision API
		Natural Language API
		Jobs API



VPC: Maximum transmission unit (MTU): The MTU is the size, in bytes, of the largest packet supported by a network layer protocol, including both headers and data.



















Storage and Databases:
	- Cloud Storage
	- File Store
	- Persistent Disk
Database:
	SQL: 
		Cloud SQL: PostgresSql, MySql, SqlServer, available across zone
		Cloud Spanner
	NoSql:
		BigTable
		DataStore: ACID transacitions
		Firestore
		MemoryStore: Cache
Networking, Firewalls and Routes:
	VPC: 
	Firewall Rules: Govern traffic coming into instances on a network
	Routes: Specifies how packets leaving an instance should be directed
	Load Balancing:
		Http(s) Load Balancing: Distributes traffic across regions to ensure requires are routed to closest region. Can distribute based on content type
		Network Load Balancing: Distribute traffic among server instances in the same region based on incoming IP protocol data
	Cloud DNS: Publish and maintain DNS records by using the same infrastructure that google uses
	Advanced Connectivity:
		Cloud VPN: Connects your existing network to your VPC through an IPSec connection
		Direct Interconnect: Connects an existing network to your VPC using highly available low latency enterprise-grade connection

		


    API Rate Quota:
        Reset API quota after specified time
    Allocation Quota:
        Must be explicitly released when done using this