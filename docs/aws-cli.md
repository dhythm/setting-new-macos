# AWS cli

## AWS CDK

```sh
npm install -g aws-cdk
```

## AWS cli

```sh
curl "https://awscli.amazonaws.com/AWSCLIV2.pkg" -o "AWSCLIV2.pkg"
sudo installer -pkg AWSCLIV2.pkg -target /
```

```sh
aws configure sso

SSO session name (Recommended):
SSO start URL [None]: https://xxxxxxxxxxxx.awsapps.com/start
SSO region [None]: ap-northeast-1
Default client Region [None]: ap-northeast-1
CLI default output format (json if not specified) [None]: json
Profile name [xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx]: yuta.okada

aws sts get-caller-identity --profile yuta.okada
```
