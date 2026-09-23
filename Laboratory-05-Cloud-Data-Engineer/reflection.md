# Reflection

Object storage is a better option for storing millions of photos than traditional block storage because it is designed to handle large amounts of unstructured data such as images, videos, and backups. Instead of organizing data into fixed-size blocks, object storage keeps each photo as an individual object together with its metadata and unique identifier. This makes the data easier to organize, retrieve, and scale as the number of photos increases.

Using Docker made deploying the MinIO storage server easier because I did not have to manually install and configure all of MinIO's dependencies. I was able to obtain the MinIO container image, start the service using a Docker command, expose the required ports, and access the MinIO web console. This showed me how containers can simplify the deployment of cloud services and provide a consistent environment.

A bucket in cloud storage is a container used to organize and store objects. During this laboratory activity, I created a bucket named `client-photos` in MinIO and uploaded a file to it. This helped me understand how object storage groups and manages data without using the traditional folder structure of a local file system.

Large enterprise companies can prevent object storage data from being lost if physical servers crash by using redundancy and replication across multiple servers or locations. They can also use backups and distributed storage so that copies of their data remain available even when a server or storage device fails.

My confidence in navigating the Linux command line is growing because this laboratory required me to use terminal commands for Docker, Git, and file management. I encountered some problems while deploying MinIO, but troubleshooting the container, checking commands, and completing the activity helped me become more comfortable working in a Linux environment.
