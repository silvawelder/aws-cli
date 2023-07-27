# aws-cli
Commands most used on day by day of a cloud engineer
## ECS

How to login inside a fargate task container 

```
aws ecs execute-command --cluster <cluster-name> \
    --task <task-id> \
    --container <container-name> \
    --interactive \
    --command "/bin/bash"
```
