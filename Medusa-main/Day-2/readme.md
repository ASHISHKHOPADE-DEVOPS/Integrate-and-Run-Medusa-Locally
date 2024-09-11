Integrate and Run Medusa Locally
September 10, 2024

Medusa Setup
Prerequisites
Before you begin setting up Medusa, ensure you have the following:

1. Node.js and npm
Node.js: Medusa requires Node.js. Download and install Node.js from nodejs.org.

This will include npm (Node Package Manager).

To verify installation, run:

bash
Copy code
node -v
npm -v

2. PostgreSQL
Medusa uses PostgreSQL as its database. Install PostgreSQL from postgresql.org and ensure it is running.

Database Creation: Create a new database for Medusa. You can use the following commands:
bash
Copy code
sudo -u postgres createdb medusa
sudo -u postgres createuser --interactive


3. Redis
Redis is used by Medusa for caching and background job processing. Install Redis from redis.io and ensure it is running.

To start Redis, you can use:

bash
Copy code
sudo systemctl start redis
sudo systemctl enable redis


4. Git
Git is needed for cloning the Medusa repository. Install Git from git-scm.com.

To verify installation, run:


Copy code
git --version

5. Medusa CLI
Install the Medusa CLI globally using npm:

Copy code
npm install -g @medusajs/medusa-cli


7. AWS Account (if deploying to AWS)
If you plan to deploy Medusa on AWS, ensure you have an AWS account and the AWS CLI installed. Configure the AWS CLI with your credentials:

Copy code
aws configure

8. Terraform and AWS CLI (for Infrastructure as Code)
If you're using Terraform for Infrastructure as Code (IaC), install Terraform from terraform.io and ensure the AWS CLI is installed as mentioned above.


10. Editor and IDE
Have a text editor or IDE of your choice (e.g., VSCode, Sublime Text) for code editing.
Next Steps
Once you have all the prerequisites installed, you can proceed with cloning the Medusa repository, setting up the environment, and running Medusa.

For efficient handling, install Chocolatey to manage software and packages automatically with the command:

bash
Copy code
choco install <package-name>
Today's Task
Integrate and Run Medusa Locally
Make sure all the prerequisites are set:

Node.js
npm (Node Package Manager)
PostgreSQL
Git
Install the Medusa CLI: Install the Medusa CLI globally using npm:

bash
Copy code
npm install -g @medusajs/medusa-cli
Setup PostgreSQL database: You can use default credentials or set up your database details later.

Create a Medusa Server Project:

bash
Copy code
medusa new my-medusa-store
Start the Medusa Server:

Navigate to your Medusa server project directory and start the server:
bash
Copy code
cd my-medusa-store
medusa develop
Test It Out:

Send a GET request to the API’s products endpoint using curl in a different terminal window to confirm the server is running properly:
bash
Copy code
curl localhost:9000/store/products


Some of the Issues I Faced
Installation Issues: Ensure all files mentioned in the prerequisites are installed and set up properly.
Version Compatibility: Check if the software versions are compatible with your operating system and each other.
PostgreSQL Credentials: Keep track of your PostgreSQL credentials for database access.
Verify Installation: Confirm package installations with the following commands:
bash
Copy code
npm -v
node -v
psql --version
git --version
Additional Guidance and Troubleshooting
Node.js and npm
Update Node.js: Ensure you have the latest stable version of Node.js for compatibility.
Check npm Permissions: If you face permission issues, consider using nvm (Node Version Manager) for managing Node.js versions.
PostgreSQL
Check Service Status: Ensure PostgreSQL service is active and listening on the correct port:
bash
Copy code
sudo systemctl status postgresql
Database Access: Use psql to connect and verify database:
bash
Copy code
psql -U postgres -d medusa
Redis
Connection Verification: Test Redis connection:
bash
Copy code
redis-cli ping
Medusa CLI
Version Check: Ensure Medusa CLI is installed correctly:
bash
Copy code
medusa --version
Common Issues
Port Conflicts: Ensure the port Medusa is running on (e.g., 9000) is not in use by another service.
Log Files: Check Medusa’s log files for detailed error messages if the server fails to start:
bash
Copy code
cat my-medusa-store/logs/medusa.log


Thank you for reading! Stay tuned for more updates and progress on this project.
See you in the next content or task progress!
Best regards,
Ashish Khopade


  
