# CloudLaunch – AltSchool Assignment

## Task 1 – S3 + IAM
- Buckets:
  - cloudlaunch-site-bucket (S3 website)
  - cloudlaunch-private-bucket (private, user RW no delete)
  - cloudlaunch-visible-only-bucket (listable, no object access)
- Website: http://cloudlaunch-site-bucket.s3-website-eu-west-1.amazonaws.com
- IAM: user `cloudlaunch-user` with least-privilege

## Task 2 – VPC
- VPC: cloudlaunch-vpc (10.0.0.0/16)
- Subnets:
  - Public: 10.0.1.0/24
  - App: 10.0.2.0/24
  - DB: 10.0.3.0/28
- Internet Gateway: cloudlaunch-igw
- Route tables:
  - cloudlaunch-public-rt (0.0.0.0/0 -> IGW)
  - cloudlaunch-app-rt (private)
  - cloudlaunch-db-rt (private)
- Security Groups:
  - cloudlaunch-app-sg (HTTP 80 from 10.0.0.0/16)
  - cloudlaunch-db-sg (MySQL 3306 from 10.0.2.0/24)

## IAM Policy JSON
See file: `cloudlaunch-user-policy.json`

- Account ID: 522814709864
- Console URL: https://522814709864.signin.aws.amazon.com/console
- Username: 522814709864
- Temporary password: Cloudlaunch@123 

