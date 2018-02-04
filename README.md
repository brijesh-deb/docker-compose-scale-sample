## Scale multi-container application using Docker Compose
This sample shows how Docker Compose can be used to scale multi container application using HAProxy. Its an extension of Docker Compose sample (https://github.com/brijesh-deb/docker-compose-sample).  

### Local deployment
- Download this sample SpringBoot application
- Database setup 
  - Access local Postgres using phpPgAdmin
  - Create a table "user_form" in public schema
    - id/bigint
    - column1/text
    - column2/text
    - column3/text
    - column4/text
  - Insert some dummy data 
- Uncomment section of application.properties marked for local deployment  
- Run the application locally and test [http://localhost:8080/data/userForms]
