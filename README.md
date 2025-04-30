# aws-cli
Commands most used on day by day of a cloud engineer

## CLI with SSO 
### config file
```
[sso-session organization]
sso_start_url = https://organization.awsapps.com/start/#
sso_region = us-east-1

[profile account-name_sso_role_name]
sso_session = organization
sso_account_id = 123456789123
sso_role_name = squad-support
```
### connecting using a profile
```
aws sso login --profile account-name_sso_role_name
```
## ECS

How to login inside a fargate task container 

```
aws ecs execute-command --cluster <cluster-name> \
    --task <task-id> \
    --container <container-name> \
    --interactive \
    --command "/bin/bash"
```
