# Mission Reflection

Writing a docker-compose.yml file makes a cloud engineer's job easier because the configuration for multiple containers can be organized and stored in one file. Instead of manually entering separate Docker commands every time, Docker Compose allows the entire application stack to be started using a single command. It also makes the deployment easier to repeat, manage, document, and share with other engineers.

I also learned that YAML formatting is very important because the structure of the file depends on correct indentation. If I make an indentation error, such as using a Tab instead of Spaces, Docker Compose may not be able to read the configuration correctly. This can cause syntax or parsing errors and prevent the containers from being deployed, so I need to be careful when writing YAML files.

Environment variables such as MYSQL_PASSWORD were used to provide configuration values required by the containers. These variables allowed MariaDB and Nextcloud to receive information such as the database name, username, password, and database host. Using matching values also helped the Nextcloud application communicate correctly with its MariaDB database without placing all configuration directly into commands.

Deploying a functional cloud storage system like Nextcloud in only a few minutes was satisfying and helped me appreciate how useful containerization and Docker Compose can be. Seeing the Nextcloud installation page appear in the browser made the activity feel more practical because I could see the result of the YAML configuration, container networking, port mapping, and deployment commands that I had used.

Since Mission 1, my understanding of Cloud Computing has become more practical and detailed. At first, I mainly understood cloud computing as accessing computing resources and services through the internet. Through the succeeding laboratory activities, I learned how Linux, networking, storage, containers, databases, and automation work together. This mission helped me understand how cloud engineers can use Infrastructure as Code and container technologies to build, deploy, and manage applications more efficiently.
