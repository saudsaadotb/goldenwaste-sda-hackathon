
docker run --rm -d -v goldenwaste:/var/lib/mysql \
  -v goldenwaste-mysql-config:/etc/mysql -p 3306:3306 \
  --network goldenwaste-network \
  --name goldenwastesqldb \
  -e MYSQL_ROOT_PASSWORD=DevOps2022 \
  mysql

## Local host 
spring.mvc.view.prefix=/WEB-INF/
spring.datasource.url=jdbc:mysql://127.0.0.1:3306/dojo
spring.datasource.username=root
spring.datasource.password=DevOps2022
spring.jpa.hibernate.ddl-auto=create
spring.mvc.hiddenmethod.filter.enabled=true


## RDS
spring.mvc.view.prefix=/WEB-INF/
spring.datasource.url=jdbc:mysql://hackathon-instance-1.cxbh7j1f5hg7.us-east-1.rds.amazonaws.com:3306/dojo
spring.datasource.username=admin
spring.datasource.password=DevOps2022
spring.jpa.hibernate.ddl-auto=update
spring.mvc.hiddenmethod.filter.enabled=true
spring.jpa.properties.hibernate.dialect = org.hibernate.dialect.MySQLDialect

## String
mysql://admin:DevOps2022@hackathon-instance-1.cxbh7j1f5hg7.us-east-1.rds.amazonaws.com:3306/dojo