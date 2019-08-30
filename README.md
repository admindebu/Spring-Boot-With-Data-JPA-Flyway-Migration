# Spring-Boot-With-Data-JPA-Flyway-Migration
This is simple example Help you understand Flyway Tool migration with Spring boot Mysql and Spring Data JPA

#What Is Flyway?
Flyway is a tool, developed by Boxfuse, that enables developers to apply version control practices to the database that supports a Java application. With it, we can tightly integrate plain SQL scripts in the lifecycle of an application, guaranteeing that its database will always be compatible without manual intervention.

#How Does Flyway Work?
Flyway works by checking the current version of the database and by applying new migrations automatically before the rest of the application starts. Whenever a developer needs to change the schema of a database or to issue some changes to the data residing on it, they need to create a SQL script following a name convention in the directory read by Flyway. Usually, this directory is classpath:db/migration, but one can change the default value if needed.

#Step
1 . Need to add Below Maven Dependency :

   	<!-- FLYWAY  -->
		<dependency>
			<groupId>org.flywaydb</groupId>
			<artifactId>flyway-core</artifactId>
		</dependency> 
2. Add below switch in Application.properties files or application.ympl files

spring.jpa.hibernate.ddl-auto=none

3. Create folder db/migration under src/main/resources and put the script file there ( Make sure script file name will start V. Like V1_ddl.script )

#More infor Visit this link : https://flywaydb.org/getstarted/
                             https://dzone.com/articles/database-versioning-with-flyway-and-java

#For org.flywaydb.core.api.FlywayException make sure if you change anything in the script files your's file names should be rename with new file name.
