
# Apache Ambari UI and Hadoop File System Commands

## Apache Ambari UI
To access the Apache Ambari web interface, use the following URL:

```bash
http://localhost:8080/#/main/dashboard/metrics
```
- **Explanation:** This URL points to the Apache Ambari dashboard, where you can monitor the health, performance, and metrics of your Hadoop cluster.

---

## CLI for Sandbox
To access the sandbox's CLI via the web, use this URL:

```bash
http://localhost:4200/
```
- **Explanation:** This URL provides access to the sandbox command line interface through a web-based terminal running on port 4200.

---

## Hadoop File System (HDFS) Commands

### 1. List files in HDFS directory
```bash
hadoop fs -ls
```
- **Explanation:** Lists all files and directories in the current HDFS directory.

---

### 2. Create a new directory in HDFS
```bash
hadoop fs -mkdir ml-100k
```
- **Explanation:** Creates a new directory called `ml-100k` in HDFS.

---

## Downloading Data with `wget`

### 1. Download the `u.data` file
```bash
wget http://media.sundog-soft.com/hadoop/ml-100k/u.data
```
- **Explanation:** Downloads the `u.data` file, which is part of the MovieLens 100k dataset, from the specified URL to your local machine.

### 2. Download the `u.item` file
```bash
wget http://media.sundog-soft.com/hadoop/ml-100k/u.item
```
- **Explanation:** Downloads the `u.item` file, another part of the MovieLens dataset, from the specified URL to your local machine.

---

## Copying Files from Local to HDFS

### 1. Copy `u.data` from local file system to HDFS
```bash
hadoop fs -copyFromLocal u.data ml-100k/u.data
```
- **Explanation:** Copies the `u.data` file from the local file system to the `ml-100k` directory in HDFS.

### 2. Copy `u.item` from local file system to HDFS
```bash
hadoop fs -copyFromLocal u.item ml-100k/u.item
```
- **Explanation:** Copies the `u.item` file from the local file system to the `ml-100k` directory in HDFS.

---

### 3. Verify file existence in HDFS
```bash
hadoop fs -ls
```
- **Explanation:** Lists the contents of the HDFS directory to verify that `u.data` and `u.item` files were successfully copied.

---

## Removing Files and Directories in HDFS

### 1. Remove `u.data` from HDFS
```bash
hadoop fs -rm ml-100k/u.data
```
- **Explanation:** Deletes the `u.data` file from the `ml-100k` directory in HDFS.

### 2. Remove `u.item` from HDFS
```bash
hadoop fs -rm ml-100k/u.item
```
- **Explanation:** Deletes the `u.item` file from the `ml-100k` directory in HDFS.

---

### 3. Remove the `ml-100k` directory from HDFS
```bash
hadoop fs -rmdir ml-100k
```
- **Explanation:** Removes the `ml-100k` directory from HDFS. The directory must be empty for this command to succeed.
