# IAM Roles for EC2

* Avoid using user credentials on servers
* IAM roles can be assigned/replaced to existing EC2 instances using AWS CLI. Not through the console
* A trick is to **assign policies to the existing role**. This will avoid the need to create new instances
* Role assigned to instance is stuck to the lifetime of the instance – until you delete the role. Easier to modify existing role by adding / removing policies
* Roles are universal, applicable to all regions



