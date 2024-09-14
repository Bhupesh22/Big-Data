# Commands and Explanations

## Commands

1. **`cd /etc/yum.repos.d`**  
   Changes the current directory to `/etc/yum.repos.d`, where YUM repository configuration files are located.

2. **`mkdir /etc/yum.repos.d/old`**  
   Creates a new directory named `old` within `/etc/yum.repos.d` to store old YUM repository configuration files.

3. **`mv /etc/yum.repos.d/CentOS*.repo /etc/yum.repos.d/old/`**  
   Moves all repository files matching `CentOS*.repo` to the `old` directory. This helps in backing up or removing old repository configurations.

4. **`mv /etc/yum.repos.d/ambari*.repo /etc/yum.repos.d/old/`**  
   Moves all repository files matching `ambari*.repo` to the `old` directory. This is similar to the previous command but for Ambari repositories.

5. **`mv /etc/yum.repos.d/hdp*.repo /etc/yum.repos.d/old`**  
   Moves all repository files matching `hdp*.repo` to the `old` directory. This is for moving HDP (Hortonworks Data Platform) repository files.

6. **`mv /etc/yum.repos.d/epel*.repo /etc/yum.repos.d/old`**  
   Moves all repository files matching `epel*.repo` to the `old` directory. This handles the EPEL (Extra Packages for Enterprise Linux) repository files.

7. **`wget https://media.sundog-soft.com/hadoop/CentOS.repo`**  
   Downloads a new YUM repository configuration file for CentOS from the specified URL.

8. **`wget http://media.sundog-soft.com/hadoop/epel.repo`**  
   Downloads a new YUM repository configuration file for EPEL from the specified URL.

9. **`yum clean all`**  
   Cleans all YUM cache files, which can resolve issues with outdated or corrupted repository data.

10. **`yum install -y https://repo.ius.io/ius-release-el7.rpm`**  
    Installs the IUS repository release package, allowing access to newer versions of software packages than those available in the base repositories.

11. **`yum install -y python-pip`**  
    Installs the `pip` package installer for Python, which is used to manage Python packages.

12. **`pip install --trusted-host pypi.python.org pathlib`**  
    Installs the `pathlib` package from PyPI, specifying `pypi.python.org` as a trusted host to avoid SSL verification issues.

13. **`pip install --trusted-host pypi.python.org mrjob==0.7.4`**  
    Installs version 0.7.4 of the `mrjob` package from PyPI, used for writing and running Hadoop Streaming jobs with Python.

14. **`pip install --trusted-host pypi.python.org pyyaml==3.10`**  
    Installs version 3.10 of the `pyyaml` package from PyPI, which is used for parsing YAML files in Python.

15. **`python RatingsBreakdown.py -r hadoop --hadoop-streaming-jar /usr/hdp/current/hadoop-mapreduce-client/hadoop-streaming.jar u.data`**  
    Runs the `RatingsBreakdown.py` script using Hadoop Streaming, specifying the Hadoop streaming JAR and the input data file `u.data`.

16. **`cp RatingsBreakdown.py MovieRatings.py`**  
    Copies the `RatingsBreakdown.py` script to a new file named `MovieRatings.py`, likely to make modifications or create a variation.

17. **`python MovieRatings.py -r hadoop --hadoop-streaming-jar /usr/hdp/current/hadoop-mapreduce-client/hadoop-streaming.jar u.data`**  
    Runs the `MovieRatings.py` script using Hadoop Streaming, similar to the previous command but with the new script.
