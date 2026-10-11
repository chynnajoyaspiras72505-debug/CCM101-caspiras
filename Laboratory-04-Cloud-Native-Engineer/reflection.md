# Laboratory 04 - Mission Reflection

The boot time and setup process of a Docker container are much faster than installing and configuring an operating system on a virtual machine. A virtual machine requires its own guest operating system and additional resources, while a container shares the host operating system kernel. In this laboratory, the Nginx container could be downloaded and started using only a few Docker commands.

Port mapping using `-p 8080:80` is necessary because the Nginx web server listens on port 80 inside the container, while port 8080 is exposed on the host. Docker forwards requests received on host port 8080 to port 80 of the container. This allowed me to test the web server using `curl http://localhost:8080`.

Containers package an application with its required environment, which helps reduce differences when software is moved between computers. Using the same container image provides a more consistent environment for development, testing, and deployment.

Containerization also improves collaboration between software developers and IT Operations teams. Developers can package applications into container images, while Operations teams can deploy and manage those containers using the same configuration. This supports DevOps practices by making deployments more consistent and repeatable.

My GitHub portfolio is evolving because each laboratory adds practical evidence of the technical skills I am learning. This laboratory demonstrates my understanding of virtualization, Docker, Nginx deployment, port mapping, container lifecycle management, documentation, and Git version control. Organizing and committing my laboratory work to GitHub allows me to build a portfolio that demonstrates both my technical knowledge and hands-on experience.
