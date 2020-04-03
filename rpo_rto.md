# Estimate availability of this configuration

1. Minimum RTO for a single AZ outage
	It will be in minutes. Because a parallel secondary is maintained synchronously. And if the primary fails, secondary will take over.

2. Minimum RTO for a single region outage
	This value depends on how fast we react to the disaster and also the size of the read-replica. In the case of disaster, we can promote a read-replica. When we do so, it reboots the instance and it can take upto several minutes.
	

3. Minimum RPO for a single AZ outage
	It will be zero, because if one data center for some reason goes down, the location of other datacenter is different and system can switch to it directly. Also since we maintain a parallel synchronous copy of the database, no data loss occurs.

4. Minimum RPO for a single region outage
	It will be the time in which we react to the disaster and the time it takes to promote the read-replica to primary. Because across regions we create Read Replicas of the Primary. So, there is a continuous asynchronous backup is happeing all the time.