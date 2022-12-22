# Amazon S3 Storage Classes
1. S3 Standard
+ It is suitable for **frequently accessed data** as it delivers **low latency and high throughput**.
+ **Most expensive storage** class among the available storage classes
+ Is the **default storage** class provided by AWS
2. S3 Intelligent Tiering
+ It offers **three types of Access Tiers**, namely, **Frequent Access Tier**, **Infrequent Access Tier**, and **Archive instant Access Tier**
+ The **Infrequent Access** tier saves up to 40% on storage costs.
+ **Archive Instant Access** tier saves up to 68% on storage costs.
+ If some objects have not been accessed for 30 consecutive days, it moves them to the infrequent access tier. Also, if those objects are accessed after being moved to the infrequent access tier, they are again moving back to the frequent access tier.
+ It is suitable for storing long-lived data where access patterns are unknown.
3. S3 Standard-IA **(S3 Standard — Infrequent Access)**
+ S3 Standard-IA (S3 Standard — Infrequent Access) is suitable for data that is **accessed less frequently**, but requires **rapid access** when needed.
+ Due to the **low cost and high-performance storage**, S3 Standard-IA can be used for long-term storage, backups, and as a data store for disaster recovery files.
4. S3 One Zone-IA
+ similar to S3 Standard-IA in terms of use case i.e. it is also suitable for data that is accessed less frequently and which requires rapid access when needed
+ S3 One Zone-IA stores the object data in **only one Availability Zone**
+ storage of data in single availability zone results in less availability (99.5%) in comparison to other storage classes (99.999999999%)
+ Our data will be lost if the availability zone where the data is stored is destroyed or damaged due to some reason
+ We can use S3 One Zone-IA storage class only if we have the flexibility to re-create the data in case of failure of the availability zone
5. S3 Glacier
+ S3 Glacier is suitable for archive data that is accessed once or twice per year and is retrieved asynchronously
+ It is best-fit for data archiving, long-term backup, and disaster recovery use cases when occasionally large sets of data need to be retrieved in minutes, at no cost.
+ Retrieval times range from a few minutes to hours
6. S3 Glacier Deep Archive**
+ S3 Glacier Deep Archive is the lowest-cost Amazon S3 storage class that supports long-term retention and digital preservation of data that will be retained for 7–10 years and that may be accessed once or twice per year.
+ Retrieval time of data stored in S3 Glacier Deep Archive is more in comparison to S3 Glacier. Retrieval time is generally in hours (default retrieval time is 12 hours)
+ We can reduce the retrieval costs even more by using bulk retrieval, which returns data within 48 hours.

![image](https://user-images.githubusercontent.com/50565205/209083217-d1e03da6-89fe-40a0-8bf4-5f37875a7bbc.png)
