# AWS-CLI Docker
Alpine Linux with AWS-CLI installed.

# Usage
Includes a ENTRYPOINT script that configures aws-cli profiles from ENVs.  Prefix PROFILENAME_ to the following ENVs and the ENTRYPOINT script will configure those profiles.

* AWS_ACCESS_KEY_ID
* AWS_SECRET_ACCESS_KEY
* REGION
* OUTPUT

## Example
```docker run -e TEST1_AWS_ACCESS_KEY_ID="XXXXX" -e TEST1_AWS_SECRET_ACCESS_KEY="XXXXX"  -e default_AWS_ACCESS_KEY_ID="XXXXX" -e default_AWS_SECRET_ACCESS_KEY="XXXXX" -e default_REGION="us-east-1" -ti ghellings/aws-cli aws s3 ls --profile TEST1```