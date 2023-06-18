# Topics Covered in System Design

## Rate Limiter
Sources: This topic is thoroughly discussed in the text format in the first part of Alex Xu's book "System Design - An insider's guide (volume 1)".

Video - https://www.youtube.com/watch?v=FU4WlwfS3G0
### Control Questions
Under development

## Consistent Hashing
Sources: This topic is thoroughly discussed in the text format in the first part of Alex Xu's book "System Design - An insider's guide (volume 1)".
### Control Questions
Under development

## DESIGNING A UNIQUE ID GENERATOR IN DISTRIBUTED SYSTEMS

Sources: This topic is thoroughly discussed in the text format in the first part of Alex Xu's book "System Design - An insider's guide (volume 1)".

### Control Questions
1. What are the four main approaches you can name to solve this problem?
1. What are the drawbacks of UUID?
1. What is the difference between the "Ticket Server" and "Twitter Snowflake" approaches?
1. What is the limit of the number of unique IDs that the "Twitter Snowflake" algorithm can generate in a millisecond?
1. What does "bit tuning" mean in the context of the "Twitter Snowflake" algorithm?
1. In what situation does "Twitter Snowflake" stop generating IDs and start waiting for a specific event?


## Designing a Location-Based Service (also known as Proximity service)

Sources: This topic is thoroughly discussed in the text format in the second part of Alex Xu's book "System Design - An insider's guide (volume 2)".

Video - https://www.youtube.com/watch?v=M4lR_Va97cQ

### Control Questions
1. List two main approaches to geodata indexing algorithms, as well as name four main algorithms.
1. Why is the traditional SQL database not suitable for geospatial search?
1. What is the difference between the geohash and quadtree algorithms? In what cases is it better to use the quadtree algorithm?


## Nearby Friends (Geospatial Search Service)

Sources: This topic is thoroughly discussed in the text format in the second part of Alex Xu's book "System Design - An insider's guide (volume 2)".

### Control Questions
1. Who is the publisher and who is the subscriber in the proposed architecture using Redis pub/sub?
1. In the proposed architecture, how many channels and Redis instances are needed, and how does scaling up/down occur?
1. What is the location cache used for?