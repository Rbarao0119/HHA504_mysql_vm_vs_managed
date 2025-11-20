# HHA504_mysql_vm_vs_managed
What needs to be filled in 

## Cloud: GCP (Central Iowa)

This assignment involves two separate MySQL environments on GCP:
Self-managed MySQL on a Compute Engine VM
Managed Cloud SQL for MySQL (GCP’s fully managed MySQL service)

## Steps to reproduce
A. VM MySQL (Self-managed)
- Create a small Ubuntu VM on Compute Engine
- Allow inbound TCP 22 and TCP 3306
- Install MySQL server using apt
- Configure mysqld.cnf:
    - Set bind-address = 0.0.0.0
- Restart MySQL
- Create MySQL user with remote access ('user'@'%')
- Update  firewall rules to allow MySQL traffic
- Test connection locally on VM (mysql -u <user> -p -h Public IP)

B. Managed MySQL (Cloud SQL)
- Create a new Cloud SQL for MySQL instance
- Configure tier, version, and admin username
- Enable Public IP
- Add my local machine’s IP to Authorized Networks
- Test connection from local machine

Both were connected using Python, SQLAlchemy, pandas, and dotenv environment variables.

## Where are Secrets Stored
Secrets are stored in .env.example file that is ignored and not committed

Errors I ecountered: VM_demo: The script would not work, I forgot to change the password where secrets are store. Worked after I made the video. 

Link: https://www.loom.com/share/fd637063f322479dbfde7940b1a0ec8d