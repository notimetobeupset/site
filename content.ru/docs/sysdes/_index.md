# Практика по подготовке к system design

Мы используем формат дружеского mock интервью. Тема для интервью объявляется заранее за неделю. Задача участников хорошо подготовить одну тему. На самом занятии разбиваемся по парам, один участник играет роль интервьювера, другой интрервьюируемого. Интервюируемый рассказывает тему используя формат system design интервью. Интервьювер задает вопросы. Интервю длится 40 мин, после чего участники меняются ролями.

Под форматом system design интервью понимается такая структура:

1. 📝 Requirement Clarification (10-15 min) - Understand the problem, ascertain design scope, and define the system's needs.
    - 🎯 Functional Requirements - Define Users, Functions, Trade-offs.
    - 📈 Non-Functional Requirements - Establish expectations for Performance, Scalability (Read/Write), Availability, Security etc.
1. 📊 Back-of-the-Envelope Estimation (5-10 min): Provide rough estimations of system usage and requirements.
    - 👥 DAU (Daily Active Users) - Determine user load.
    - 💽 Data Size Estimation - Calculate approximate data that the system needs to handle.
    - ⏱ Query Per Second (QPS) - Peak = QPS*2. This will help to understand the load on the system.
    - 🗃 Storage Requirement - Determine required storage size.
    - 🚀 Cache Requirement - Ascertain the need for caching and its extent.
    - 🖥 Number of Servers - Estimate the required number of servers for deployment.
1. 🔗 System Interface Definition (5 min) - Define the interfaces of the system, detailing what it should do, without explaining how it does it.
1. 🏗 High-Level Design (5-10 min) - Present a broad overview of the system architecture.
1. 🗄 Data Model and Database Schema Definition (5-10 min) - Outline the data model and structure your DB schema to align with your system requirements.
1. 🧩 Detailed Design (20-30 min) - Focus on core components. Choose the right data structures, algorithms for your system. Discuss different parts of the system in detail.
1. 🚧 Identifying and Resolving Bottlenecks (10-15 min) - Identify potential bottlenecks, discuss solutions and mitigation strategies to overcome them.


### Краткий вариант, который удобно держать перед глазами в процессе расказа:
```
1) Requirement Clarification - Define functional and non-functional needs.
2) Estimation - Roughly calculate system usage and requirements.
3) System Interface Definition - Describe system functions.
4) High-Level Design - Sketch the system architecture.
5) Data Model/DB Schema Definition - Outline data model and DB schema.
6) Detailed Design - Discuss core components, data structures, and algorithms.
7) Bottleneck Identification & Resolution - Identify bottlenecks and propose solutions.

```