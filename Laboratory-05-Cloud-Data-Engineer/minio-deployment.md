# MinIO Deployment

## Overview

MinIO was deployed in an Ubuntu environment using Docker. MinIO provides S3-compatible object storage and was used in this laboratory to demonstrate the basic operations of a cloud object storage system.

## Step 1: Verify Docker

Docker was verified using:

docker --version

The Docker service was available in the Ubuntu environment.

## Step 2: Pull the MinIO Image

The MinIO image was obtained from the Quay.io container registry:

docker pull quay.io/minio/minio

The image was downloaded successfully.

## Step 3: Run the MinIO Container

The MinIO container was started with ports 9000 and 9001 exposed:

docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
-e "MINIO_ROOT_USER=cloudadmin" \
-e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
quay.io/minio/minio server /data --console-address ":9001"

Port 9000 is used by the MinIO API, while port 9001 provides access to the MinIO web console.

## Step 4: Verify the Container

The running container was checked using:

docker ps

The output confirmed that the `minio-server` container was running successfully.

## Step 5: Access the MinIO Console

The MinIO web console was accessed through port 9001 using KillerCoda's Traffic/Ports feature.

The administrator credentials configured during deployment were used to sign in.

## Step 6: Create a Bucket

A new bucket named:

`client-photos`

was created using the MinIO Object Browser.

## Step 7: Upload an Object

A sample image named:

`minio-deployed.png`

was uploaded to the `client-photos` bucket.

The MinIO interface showed the upload at 100%, confirming that the object was successfully stored.

## Result

The MinIO object storage service was successfully deployed and tested. The successful creation of the `client-photos` bucket and upload of `minio-deployed.png` demonstrated basic object storage operations.
