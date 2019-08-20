## Sonatype Nexus3 
- Nexus is repository Manager
- Nexus is used for storing deployable software components like
    - maven dependencies (jar,war,ear)
    - Docker images
    - Yum repo
    - Nuget for DotNet Applications
    - Other formats
    
``` Note: Other repository manager tools are Jfrog Artifactory```

## Step -1  Installing Nexus on Linux
- System Requirements
    - Java 1.8
    - 2 CPU and 4 GB RAM
- Install Java8

      ```
         sudo yum install -y java-1.8.0-openjdk
      ```
- Download and Configure Nexus
     ```
        cd /opt
        sudo wget https://download.sonatype.com/nexus/3/latest-unix.tar.gz
        sudo tar xf latest-unix.tar.gz
        sudo mv nexus-3.18.1-01/ nexus3
        sudo chown -R ec2-user:ec2-user nexus3/ sonatype-work/
        
     ```
 - Configure Nexus as a Service
    - onen following file
    - ``` vi /opt/nexus3/bin/nexus.rc ```
    - Change above file as followes
      ``` run_as_user="ec2-user" ```