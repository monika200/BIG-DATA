 **Lab: Exporting HDFS Data to an RDBMS**
 
 **1. Put the Data into HDFS** 

a. Create a new directory in HDFS named salarydata. 
hdfs dfs -mkdir salarydata 

![Capture1](https://user-images.githubusercontent.com/63012770/86415683-65392d00-bce5-11ea-847c-172a246e7641.PNG)

b. Put salarydata.txt into the salarydata directory in HDFS. 

![Capture2](https://user-images.githubusercontent.com/63012770/86415687-666a5a00-bce5-11ea-891a-7f457914dc6d.PNG)

**2. Create a Table in the Database**

![11](https://user-images.githubusercontent.com/63012770/86414188-e510c880-bce0-11ea-8ab3-38375d510b64.PNG)

**3. Export the Data** 

**a. Run a Sqoop command that exports the salarydata folder in HDFS into the salaries2 table in MySQL. At the end of the MapReduce output, you should see a log event stating that 10,000 records were exported.** 

![12 1](https://user-images.githubusercontent.com/63012770/86414190-e641f580-bce0-11ea-9565-8f3f4cbd12e7.PNG)

![Capture3](https://user-images.githubusercontent.com/63012770/86416170-e04f1300-bce6-11ea-8bc8-2916b409559d.PNG)

**b. Verify it worked by viewing the table’s contents from the mysql prompt. The output should look like the following:** 

![13](https://user-images.githubusercontent.com/63012770/86414196-e7732280-bce0-11ea-8cfc-1d2653a12122.PNG)


We have now used Sqoop to export data from HDFS into a database table in MySQL. 
