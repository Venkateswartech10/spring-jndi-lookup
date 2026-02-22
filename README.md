# spring-jndi-lookup
How to lookup data source from JNDI using spring 

# Server.xml

<Resource name="jdbc/javatechie" 
      global="jdbc/javatechie" 
      auth="Container" 
      type="javax.sql.DataSource" 
      driverClassName="com.mysql.jdbc.Driver" 
      url="jdbc:mysql://localhost:3306/javatechie" 
      username="root" 
      password="Password" 
      
      maxActive="100" 
      maxIdle="20" 
      minIdle="5" 
      maxWait="10000"/>
	  
# context.xml:	  

<ResourceLink name="jdbc/javatechie"
                	global="jdbc/javatechie"
                    auth="Container"
                    type="javax.sql.DataSource" />
					
# Config:

<jee:jndi-lookup id="dataSource" jndi-name="jdbc/javatechie"
   			expected-type="javax.sql.DataSource" />	







			<img width="940" height="633" alt="image" src="https://github.com/user-attachments/assets/f52d8ae0-0da8-47a1-bb95-ee0629a98671" />


			<img width="940" height="631" alt="image" src="https://github.com/user-attachments/assets/20533898-8258-4411-8640-4ce26ace17b4" />


					
