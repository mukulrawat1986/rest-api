#Rest-API
This project shows an example of creating a REST API on Go using the Echo framework.

###Used in the project
####HTTP
	github.com/labstack/echo - to create a rest service; used: router, data binding and data rendering, logger middleware

####Validation
	gopkg.in/go-playground/validator.v9 - for data validation

####Database
	database / sql - for working with queries and transaction
	github.com/lib/pq - postgresql was used as a DBMS
	github.com/rubenv/sql-migrate - migration tool for sql
	docker postgres image - to run postgresql

####Configuration
	flag - to pass parameters at startup
    github.com/jinzhu/configor - to download a configuration from yaml

####Logging
	github.com/sirupsen/logrus - for application logs

####Testing
	testing - for writing tests
    github.com/golang/mock/gomock - to generate mocks
    github.com/stretchr/testify/assert - exclusively for assert in tests

###Dependencies
	github.com/golang/dep - dependency manager


###For start
	make init - installs necessary tools (dep, sql-migrate, mockgen), then dep installs project dependencies
    make run - starts the application, while launching the docker container from the database
    make test - starts the application, while launching the docker container from the database
    make spec - generates an open-api specification in spec / api.json. After starting the service, it gives the spec as a static on the path /spec/api.json, you can also execute swagger serve -F = swagger http: // localhost: 8081 / spec / api.json to display it in html as a running service.
    spec-ui - open spec in html
