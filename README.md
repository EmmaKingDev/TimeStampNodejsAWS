# TimeStamp NodeJS app with AWS integration

App.js creates a basic NodeJS app that a user can log dates and times from the terminal for work hours. The app validates the data, calculates daily working hours and sends it to a aws RDS database instance.

sumEmail.js retrieves yesterday's inputs from the database and sends a collection message of the data to an aws SNS topic. sumEmail.js is run from an EC2 instance as a cronjob daily.

CF creates a custom VPC, private & public subnets, security groups, EC2 inctance, s3 bucket and an SNS topic.

RDS PostgreSQL is created manually for security reasons. The publicly unaccessable s3 holds all the project files, inclusing the .env file, which are copied to the EC2 instance.
