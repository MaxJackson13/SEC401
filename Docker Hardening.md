1. Dont enable unused services e.g. SSH or expose unused ports 
2. Dont run with the --privileged flag as this allows full access to the Docker host 
3. Dont store secrets such as connection strings or API keys in docker containers
4. Dont run applications as root. Create a dedicated user with minimal permissions (least privilege)
5. Dont run containers with the -net=host flag. Instead use bridge mode so containers on the same host may communicate but are not accessible outside the host
6. Cryptographically sign and verify docker images to prevent MITM attacks
7. Monitor custom or base images for known vulnerabilities

CIS Docker and Kubernetes hardening Configurations


Terraform (Infrastructure as Code)
Declaratively define end state configuration of your infrastructure then create, update and manage it. Allows reliable and reproduicble innfrastracture. 
