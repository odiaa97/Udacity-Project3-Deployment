# Hosting Full-Stack Application

## Udagram is built with Angular, typescript nodejs, express and postgres database

- You can visit the hosted application on S3 from [here](http://udagram17-10.s3-website-us-east-1.amazonaws.com)
- You can visit Elastic Beanstalk APIs from [here](http://Udagramapi2-env.eba-qm5yuv3r.us-east-1.elasticbeanstalk.com)

## Dependencies

```
- Nodejs version 16 or greater
- npm version 6.14.8 or greater
- AWS CLI v2 or v1
- RDS postgres database engine running
- S3 Bucekt hosting the UI files
- Elastic Beanstalk hosting the server files
```

# Installation & Configurations

## RDS installation:

- Navigate to the [RDS dashboard](https://console.aws.amazon.com/rds/home). It shows the database-resources summary, such as the count of database instances, the health of the database service, reserved instances, snapshots. You can also view the portion of the allocated storage. You can launch the `Create database` wizard from here.
- Create a Database
  - Choose the Standard create option and Dev/Test template
  - Choose a Single DB Instance and Credentials Settings
    - Use either the RDS Free Tier or Dev/Test template. On free-tier resources, you can develop and test applications to gain hands-on experience with Amazon RDS.
    - The password can either be auto-generated or manually created. Take note of this password, as it is useful for future steps. You will be able to find this password and change it later in the console.
  - Select db.t3.micro
  - Create a database - View default settings
    - Notice that all configuration settings, except the Encryption and VPC details, can be changed after the database is created.

## Elastic Beanstalk installation:

- `eb init`
- `eb create` and chooose the desired options according to your deployment

## S3 installation:

- Create a Bucket

- Navigate to the S3 dashboard, and click on the Create bucket button. It will launch a new wizard.

- General configuration
  Provide the bucket-name and the region where you want to locate the bucket. The bucket name must be unique worldwide, and must not contain spaces or uppercase letters.

- Public Access settings
  You can choose public visibility. Let's uncheck the Block all public access option.

- Bucket Versioning and Encryption
  Bucket Versioning - Keep it disabled.
- Encryption - If enabled, it will encrypt the files being stored in the bucket.
- Object Lock - If enables, it will prevent the files in the bucket from being deleted or modified.
- Upload File/Folders to the Bucket

### CircleCI pipeline & Configurations

- Create a new CircleCI account
- Connect to the github account and setup the desired project
- from your local project 'attached to the repo'
  - `git add .`
  - `git commit -m "commit message"`
  - `git push -u origin main`
- It will automatically detect the latest version and start the deployment process
