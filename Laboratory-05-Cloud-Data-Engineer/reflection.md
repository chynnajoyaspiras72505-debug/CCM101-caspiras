# Reflection

## What I Learned

In this laboratory, I learned how cloud data can be stored using different storage models such as object, block, and file storage. I understood that each storage type is designed for different purposes and workloads.

I also learned how object storage works through MinIO. Unlike traditional file storage, object storage manages data as objects inside buckets, making it suitable for images, backups, application files, and other unstructured data.

## Experience with Docker and MinIO

Deploying MinIO using Docker helped me understand how containers can be used to quickly deploy cloud-native services. I learned how to pull a container image, start a container, expose ports, and verify that the container is running.

During the activity, the original MinIO image reference did not work, so I used the MinIO image from Quay.io. After successfully starting the container, I accessed the MinIO web console through port 9001.

## Object Storage Activity

I created a bucket named `client-photos` and uploaded `minio-deployed.png`. Seeing the file successfully uploaded helped me understand the basic process of storing objects in a cloud object storage system.

## Challenges Encountered

One challenge was accessing and deploying MinIO correctly in the laboratory environment. I encountered an image pull error and temporary KillerCoda connection interruptions. These challenges required checking the Docker image, container status, and exposed ports.

## Conclusion

This laboratory gave me practical experience with cloud storage, Docker, and MinIO. It helped me understand how a Cloud Data Engineer can use object storage technologies to organize and manage data in a scalable cloud environment.
