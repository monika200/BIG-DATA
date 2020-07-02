**Lab: Importing RDBMS Data into HDFS**

**1.Import the Table into HDFS** 

![1](https://user-images.githubusercontent.com/63012770/86414197-e80bb900-bce0-11ea-8d53-6e9856686987.PNG)

**2. Verify the Import**

a. View the contents of your HDFS folder: 

![2](https://user-images.githubusercontent.com/63012770/86414198-e80bb900-bce0-11ea-8f86-2ec5f398b24f.PNG)

**b. Now view the contents of your new folder salaries:** 

![3](https://user-images.githubusercontent.com/63012770/86414200-e8a44f80-bce0-11ea-84fd-7a94cf3862c8.PNG)

**3. Use the cat command to view the contents of the files.**
# hdfs dfs -cat salaries/part-m-00000 

![4](https://user-images.githubusercontent.com/63012770/86414201-e8a44f80-bce0-11ea-9a2e-3431438b471d.PNG)

**4. Specify Columns to Import.**

a. Using the ‐‐columns argument, write a Sqoop command that imports the salary and age columns (in that order) of the salaries table into a directory in HDFS named salaries2. In addition, set the ‐m argument to 1 so that the result is a single 
file.

![5](https://user-images.githubusercontent.com/63012770/86414202-e93ce600-bce0-11ea-9751-1ad30baa8b8f.PNG)

b. After the import, verify you only have one part‐m file in salaries2: 

![6](https://user-images.githubusercontent.com/63012770/86414206-eb06a980-bce0-11ea-8d96-8047bc13b2cd.PNG)

c. Verify that the contents of part‐m‐00000 are only the two columns you specified:

![7](https://user-images.githubusercontent.com/63012770/86414210-ecd06d00-bce0-11ea-9e79-5dd159d747f1.PNG)

**5. Importing from a Query** 

a.  a Sqoop import command that imports the rows from salaries in MySQL whose salary column is greater than 90,000.00. 

![7 2](https://user-images.githubusercontent.com/63012770/86414208-eb9f4000-bce0-11ea-84fc-426fede28f27.PNG)

b. To verify the result, view the contents of the files in salaries6. You should have only two output files. 

![8](https://user-images.githubusercontent.com/63012770/86414211-ed690380-bce0-11ea-82f5-1421d7664045.PNG)

c.View the contents of part‐m‐00000 and part‐m‐00001. 

![9](https://user-images.githubusercontent.com/63012770/86414212-ed690380-bce0-11ea-85fa-22df638d2e51.PNG)
