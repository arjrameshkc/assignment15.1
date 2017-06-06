# assignment15.1

use custom_db;
create table if not exists emp_details
(
name string,
skill string,
rank string,
location string
)
row format delimited
fields terminated by ',';

LOAD DATA LOCAL INPATH '/home/acadgild/downloads/emp_details' INTO TABLE emp_details;

SELECT skill,count(*) FROM employee GROUP BY skill;

