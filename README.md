## pluralsight-springcloud-m3-task
Spring cloud task

Creates a simple Toll processing task (takes in StationId, Licence plate, and timestamp). (See the Spring Cloud annotation `@EnableTask` for more details)

If you don't want to set up a database, comment out the database settings in application.properties file and the database dependency in pom file. Then the task will just simply write to memory.
Otherwise, just create a postgres database name `tasklogs` (or any database of your choice). At run time the app will create the task's built-in tables (`task_execution`, `task_execution_params`, `task_logs`, and `task_task_batch`) to save the task's meta data

To test it, open the launch configuration and add the arguments. 
  Eg.   
  ```bash
        StationA
        LicenseB
        2019-01-01:T12:04:33
  ```
        
  Start the app process. You will see a system print in the Consolse window. If you create a database, checkout if the records are saved into the tables

