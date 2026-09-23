# Cloud Storage Types Research

## Introduction

Cloud storage allows data to be stored and accessed through cloud infrastructure. Three common types of cloud storage are object storage, block storage, and file storage. Each type is designed for different workloads and data requirements.

## Object Storage

Object storage stores data as individual objects. Each object contains the data itself, metadata, and a unique identifier.

### Common Uses
- Images and videos
- Backups and archives
- Application data
- Data lakes
- Static website assets

### Examples
- Amazon S3
- Azure Blob Storage
- Google Cloud Storage
- MinIO

### Advantages
- Highly scalable
- Suitable for large amounts of unstructured data
- Easy access through APIs
- Supports rich metadata

## Block Storage

Block storage divides data into fixed-size blocks. The operating system can treat block storage similarly to a physical disk.

### Common Uses
- Virtual machine disks
- Databases
- Applications requiring high-performance storage

### Advantages
- High performance
- Low latency
- Suitable for databases and transactional workloads

## File Storage

File storage organizes data using files and directories in a hierarchical structure.

### Common Uses
- Shared folders
- Documents
- Team file sharing
- Network file systems

### Advantages
- Familiar file and folder structure
- Easy to organize
- Suitable for shared access

## Comparison

| Storage Type | Data Organization | Typical Use |
|---|---|---|
| Object Storage | Objects with metadata | Images, backups, data lakes |
| Block Storage | Fixed-size blocks | Databases and virtual machines |
| File Storage | Files and directories | Shared files and documents |

## Conclusion

Object, block, and file storage serve different purposes in cloud computing. Object storage is particularly useful for scalable unstructured data. In this laboratory, MinIO was used to demonstrate object storage by creating a bucket and uploading an object.
