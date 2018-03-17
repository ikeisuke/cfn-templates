# CloudFormation

## package-bucket

This template create bucket for `aws cloudformation package`.

### create bucket

```bash
aws cloudformation deploy \
    --template-file cloudformation/package-bucket.yml \
    --stack-name cloudformation-package-bucket
```

### get bucket name

```bash
aws cloudformation describe-stack-resource \
    --stack-name cloudformation-package-bucket \
    --logical-resource-id PackageBucket \
    --query "StackResourceDetail.PhysicalResourceId" \
    --output text
```
