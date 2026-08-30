# Cloud Infrastructure Components

## Compute Resources

**Purpose:** Compute resources provide the processing power needed to run applications, services, and workloads.

**Importance in Cloud Computing:** Compute resources are essential because cloud applications depend on CPU capacity to process requests and perform tasks.

**Relation to KillerCoda:** The KillerCoda environment uses one virtual Intel Xeon CPU, which serves as its compute resource.

## Storage Resources

**Purpose:** Storage resources keep operating system files, applications, and user data.

**Importance in Cloud Computing:** Cloud systems require storage to retain data even when applications stop running.

**Relation to KillerCoda:** The main storage device is `/dev/vda1`, with 19 GB total capacity.

## Networking Resources

**Purpose:** Networking resources allow systems, users, and cloud services to communicate.

**Importance in Cloud Computing:** Networking enables access to cloud applications, communication between resources, and internet connectivity.

**Relation to KillerCoda:** The environment uses the `enp1s0` network interface with IP address `172.30.1.2/24`.

## Operating System

**Purpose:** The operating system manages hardware resources and provides the environment where applications run.

**Importance in Cloud Computing:** Cloud virtual machines require operating systems to manage compute, memory, storage, networking, users, and software.

**Relation to KillerCoda:** The KillerCoda server is running Ubuntu 24.04.4 LTS.
