---
Title: DBS101 Flipped Class3
categories: [DBS101, Flipped_Class3]
tags: [DBS101]
---
### Topic: Introduction to SQL(Structured Query Language)
---
Kuzuzangpola everyone!! Today's journal is all about what i learnt during third flipped class. Before starting with flipped class which was meant to be a interactive educational experience we were introduced to what were some properties of database. i learnt the acronymes ACID properties which dipicts each properties like Atomicity, Consistency, Isolation and Durability. After that i also learned about the different types of data type namely:

 | Data type | Description |
| ----------- | ----------- |
| CHAR(size) | A FIXED length string ( contain letters, numbers, and special characters). The *size* parameter specifies the column length in characters. Can be from 0 to 255. |
| VARCHAR(size)	 | A VARIABLE length string (contain letters, numbers, and special characters). The *size* parameter specifies the maximum string length in characters. Can be from 0 to 65535. |
| INT(size) | The INT data type is an integer value from -2,147,483,648 to 2,147,483,647. The *size* parameter specifies the maximum display width (which is 255) |
| DATETIME | A date and time combination. Format: YYYY-MM-DD hh:mm:ss. The supported range is from '1000-01-01 00:00:00' to '9999-12-31 23:59:59'. |
|  |  |

Our instructure showed us an example to see how those datatype functions like CREATE TABLE department(dept_name varchar(20),building varchar(15), budget numeric(12,2), PRIMARY KEY (dept_name)); 

During our third flipped class, we were first divided into home groups and expert groups, with a total of 6 individuals. We were instructed to study set operations in SQL with examples, while other groups (3,4) studied null values in SQL with examples. So, during the first 50 minutes, we discussed our topic in our respective groups, and for another 30 minutes, we explained to our home groups, who also shared on their topic.

My key takeaway from the flipped class session on SQL were:

1.Different types of set operations in SQL

 | Set  operations | Description |
| ----------- | ----------- |
| UNION | used to combine the results of two or more SELECT statement. Removes duplicate rows from the result set.
UNION ALL | Same as UNION but it doesn't remove duplicate from the result set.
INTERSECTION| Returns only the rows that are bcommon on both SELECT statements. Useful in finding the overlab between the two sets of data.
|EXCEPT/MINUS|Returns row from the first SELECT statement that are not present in second SELECT statement. it's useful when you want to find the difference between the sets of data.
|

Conditon: Inorder to use set operations the two data should have same number of columns and the corresponding columns must have same datatype. 

2.Null values in SQL: Null values in SQL means the value does not exist in the database. A NULL values is different from a zero values. They are simply the one that has been left blank during the time of record or by some bias. A NULL value is used to represent a missing value, but it usually has one of three different interpretations: 
- The value unknown (value exists but is not known)
- Value not available (exists but is purposely not given)
- Attribute not applicable (not applicable for this entry.) 

I also learned how aggregate functions like(SUM, AVG, MIN, MAX) handle the NULL values. They simply ignore the NULL values.


                                 **THANK YOU**

