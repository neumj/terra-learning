# terra-learning
https://cloudaffaire.com/how-to-create-a-custom-vpc-using-aws-cli/     
https://aws.amazon.com/getting-started/hands-on/deploy-wordpress-with-amazon-rds/     
https://docs.aws.amazon.com/vpc/latest/userguide/vpc-subnets-commands-example.html   

- name: S3 Sync
  uses: ItsKarma/aws-cli@v1.70.0
  with:
    args: s3 sync --delete --acl public-read localdir/ s3://remote-bucket/
  env:
    AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
    AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
    AWS_DEFAULT_REGION: "us-east-1"
