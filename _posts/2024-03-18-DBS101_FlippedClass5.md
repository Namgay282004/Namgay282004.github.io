---
Title: DBS101 Flipped Class5
categories: [DBS101, Flipped_Class5]
tags: [DBS101]
---
## Topic: Normal Forms in DBMS

Warm greeting to my readers!!  In this artical we are going to discuss on what and why normalization and on top of that we are also going to talk about the types of normal forms like 1NF, 2NF, 3NF, BCNF AND 4NF.

## Normalization

Normalization is a process of organizing the data in database to avoid data redundancy, insertion anomaly, update anomaly & deletion anomaly. Primary keys are really important in organizing information in a database. They help to make sure that every row in a table has a unique identification so that nothing gets mixed up or lost. In database design, there are different normal forms based on the primary keys of a table. These includes: 

- ### First Normal Form (1NF)
    In 1NF the values in each column in a table should be atomic and each rows should be uniquely identified.

    ![alt text](<../Images_for_DBS101/Screenshot from 2024-03-22 17-34-41.png>)

    The above table voiletes 1NF beacuse the Phone Numbers column contains repeating groups. So inorder to normalize this table to 1NF, we split the Phone Numbers column into separate rows and add a separate primary key column.

    ![Normalized to 1NF](<../Images_for_DBS101/Screenshot from 2024-03-22 17-42-21.png>)

- ### Second Normal Form (2NF)
 
    2NF builds on 1NF by requiring that each non-primary key column in a table is fully functionally dependent on the primary key. This means that a table should not have partial dependencies, where a non-primary key column depends on only part of the primary key.

    ![alt text](<../Images_for_DBS101/Screenshot from 2024-03-22 18-28-08.png>)

    The above table  violates 2NF because the Customer Name column depends on only part of the primary key (Customer ID). To normalize this table to 2NF, we can split it into two tables as follows. 

    ![Normalized to 2NF](<../Images_for_DBS101/Screenshot from 2024-03-22 18-28-49.png>) ![Normalized to 2NF](<../Images_for_DBS101/Screenshot from 2024-03-22 18-29-08.png>)

- ### Third Normal Form(3NF)

    3NF builds on 2NF by requiring that each non-primary key column in a table is not transitively dependent on the primary key. WHich means a table should not have transitive dependencies, where a non-primary key column depends on another non-primary key column.

    ![alt text](<../Images_for_DBS101/Screenshot from 2024-03-22 18-39-35.png>)

    In this above example, the non-primary key column "Customer City" is transitively dependent on the primary key. That is, it depends on "Customer ID". To bring this table to 3NF, we can split it into two tables.

    ![Customers Table](<../Images_for_DBS101/Screenshot from 2024-03-22 18-42-28.png>)

    ![Orders Table](<../Images_for_DBS101/Screenshot from 2024-03-22 18-42-40.png>)

- ### Boyce-Codd Normal Form (BCNF)

    BCNF is a stricter form of 3NF that applies to tables with more than one candidate key. In BCNF a table should not have non-trivial dependencies, where a non-primary key column depends on another non-primary key column. 

    ![alt text](<../Images_for_DBS101/Screenshot from 2024-03-22 18-51-09.png>)

    In this above example, the functional dependency between "Author ID" and "Author Name" violates BCNF because it is not on a candidate key. To bring this table to BCNF, we can split it into two tables.

    ![Authors Table](<../Images_for_DBS101/Screenshot from 2024-03-22 18-51-31.png>)

    ![Books Table](<../Images_for_DBS101/Screenshot from 2024-03-22 18-51-40.png>)

- ### Fourth Normal Form (4NF)

    4NF builds on BCNF by requiring that a table should not have multi-valued dependencies. A multi-valued dependency occurs when a non-primary key column depends on a combination of other non-primary key columns.

    ![alt text](<../Images_for_DBS101/Screenshot from 2024-03-22 18-59-13.png>)    

    In the above table, the Product Name and description depend on both the Order ID and Product ID, creating a multi-valued dependency. To bring the table into 4NF, we can split it into three tables.

    ![alt text](<../Images_for_DBS101/Screenshot from 2024-03-22 18-59-30.png>)
    ![alt text](<../Images_for_DBS101/Screenshot from 2024-03-22 18-59-44.png>)
    ![alt text](<../Images_for_DBS101/Screenshot from 2024-03-22 18-59-59.png>)


### What we did during Flipped Class

We were initially divided into four groups, each consisting of six members. Each group was assigned a different topic within the realm of normal forms to study. My group, in particular, focused on the Third Normal Form (3NF). We spent the first 30 minutes discussing and sharing our thoughts within our group. Following this, all groups were tasked with presenting their findings to the class. Through this process, I personally gained a deeper understanding of all types of normal forms. I hope that my friends also benefited from this learning experience.



                                   Thank you










