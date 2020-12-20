Running Pagila on your system for querying:
            
  1. Install postgreSQL on your system. [Link](https://www.postgresql.org/download/)
     (While downloading you can set user_name and password)
  2. Run in Command line 
             
             cd "C:\Program Files\PostgreSQL\13\bin"
               
  3. Initiate psql
              
             psql -h 127.0.0.1 -U user_name
                
  4. Enter password when prompted for user 
 
  5. In postgres#
  
             Create database pagila
  
  6. Download pagila-schema.sql and pagila-data.sql  OR clone the repository to save the files on you system
  
  7. Filepath1 corresponds to path of pagila-schema.sql (i.e. D:\Myfiles\Data\pagila-schema.sql)
     Filepath2 corresponds to path of pagila-data.sql (i.e. D:\Myfiles\Data\pagila-data.sql)
     
  8. In command line. Run (enter password if prompted)
         
            psql -h 127.0.01 -d pagila -U user_name -p 5432 -a -q -f filepath1
            psql -h 127.0.01 -d pagila -U user_name -p 5432 -a -q -f filepath2
  
  9. Pagila database is created.
  
 10. For quering in Jupyter Notebook
     Open Jupyter notebook and run commands in order below:
           
           !pip install ipython-sql
           % load_ext sql
           conn_string = postgresql://<user_name>:<password>@127.0.0.1:5432/pagila
           %sql $conn_string
           
 11. You are ready to explore data in jupyter notebook
     
          %sql
          Select rating from film limit 5;
          
           
          
 
            
            
