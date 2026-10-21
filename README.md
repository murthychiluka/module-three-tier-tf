
# Module-Three-Tier apply flow 
```
terraform apply -target=module.vpc
terraform apply -target=module. bastion
terraform apply -target=module.frontend-ec2
terraform apply -target=module.backend-ec2
terraform apply -target=module.frontend_alb
terraform apply -target=module.backend_alb
terraform apply -target=module.rds
```
- now connect to backend and frontend ec2s deploy the application
- in the frontend config file, give the backend load balancer URL
- next, in the backend .env, give RDS details 
- next deploy both frontend and backend
# apply remaining modules
```
terraform apply -target=module.frontend_launchtemplate
terraform apply -target=module.backend_launchtemplate
terraform apply -target=module.asg-backend
terraform apply -target=module.asg-frontend

```
