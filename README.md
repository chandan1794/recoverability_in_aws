# Recoverability in AWS
This sequence is based on the [project's](https://github.com/udacity/nd063-c2-design-for-availability-resilience-reliability-replacement-project-starter-template) [README.md's](https://github.com/udacity/nd063-c2-design-for-availability-resilience-reliability-replacement-project-starter-template/blob/master/README.md) sequence.

## Data durability and recovery
### 1. SUBMIT screenshots of both VPCs after they are created
- [VPC Primary](/VPCs/primary.png)
- [VPC Secondary](/VPCs/secondary.png)

## Highly durable RDS Database
### 1. SUBMIT screenshot of the configuration of the primary and read replica database after they are created
Since, it was not clear, which configuration it was asking, so I have taken multiple screenshots
- [Primary](/highly_durable_rds_db/config_dbs/primary)
- [Read Replica](/highly_durable_rds_db/config_dbs/read_replica)

### 2. SUBMIT screenshot of the configuration of the database subnet groups as well as the route tables associated with those subnets
#### Subnet Groups
- [Primary](/highly_durable_rds_db/subnet_groups/primary_subnet_group.png)
- [Read Replica](/highly_durable_rds_db/subnet_groups/read_replica_subnet_group.png)

#### Route Tables
- [Primary](highly_durable_rds_db/route_tables/primary_route_table.png)
- [Read Replica](highly_durable_rds_db/route_tables/read_replica_route_table.png)

## Estimate availability of this configuration
### 1. SUBMIT your answers
- [RTO and RPO](rpo_rto.md)


## Demonstrate normal usage
### 1. SUBMIT log of connecting to the database and running the above commands
- [Primary](/demonstrate_normal_usage/primary_sql_logs.png)

## Monitor database
### 1. SUBMIT screenshot of the DB Connections and the database replication configuration
- [DB Connections](/monitor_db/db_connections.png)
- [Replications](/monitor_db/replication_log.png)

## Simulate recovery in standby region
### 1. SUBMIT log of connecting to the database and running the above commands
- [Before Promotion](/demonstrate_normal_usage/read_replica_read_only_logs.png)

### 2. SUBMIT screenshots of the database configuration before and after the database promotion
Since, it was not clear, which configuration it was asking, so I have taken multiple screenshots.
- [Before Promotion](/highly_durable_rds_db/config_dbs/read_replica)
- [After Promotion](/after_promotion_replica/)

_Note: In after promotion db config, I did not find any changes, so I took an extra screenshot of [logs](/after_promotion_replica/read_replica_promoted_log.png), which clearly shows that read replica has been promoted._

### 3. SUBMIT log of connecting to the database and running the above commands
- [After Promotion](/demonstrate_normal_usage/read_replica_promotion.png)

## Website recovery
### 1. SUBMIT screenshot of the webpage
- [Default Website](/s3/initial.png)

### 2. SUBMIT screenshot of the modified webpage
- [Modification 01](/s3/modified_01.png)

### 3. SUBMIT screenshot of the modified webpage
- [Modification 02](/s3/modified_02.png)

### 4. SUBMIT screenshot of the modified webpage
- [Modification 03](/s3/modified_03.png)

### 5. SUBMIT screenshot of existing versions of the file showing the "Deletion marker"
- [Modification 03 with Delete Marker](/s3/modified_03_delete_marker.png)

### 6. SUBMIT screenshot of the modified webpage
- [Modification 04](/s3/modified_04.png)

I have learnt some new things while doing this project and I enjoyed it. Thank you Udacity.



## References
1. [https://forums.aws.amazon.com/thread.jspa?threadID=310192]
2. [https://www.percona.com/blog/2018/08/02/amazon-rds-multi-az-deployments-read-replicas/]
3. [https://acloud.guru/forums/aws-certified-solutions-architect-professional/discussion/-KWCGDsFy5wYTN5UI6On/sample-rpo-question]
4. [https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html#USER_ReadRepl.Promote]
5. [https://aws.amazon.com/blogs/database/implementing-a-disaster-recovery-strategy-with-amazon-rds/]


