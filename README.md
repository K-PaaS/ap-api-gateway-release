## ap-api-gateway-release

### Application Platform API Gateway Service Configuration
- api-gateway-server :: N machine(s)
- ap-api-gateway-broker :: 1 machine
- mariadb :: 1 machine

### Create Application Platform API Gateway Service Release
- Download the latest API Gateway Release
    ```
    $ git clone https://github.com/K-PaaS/ap-api-gateway-release.git
    ```
- Download & Copy "source files" into the src directory
    ```
    ## download source files
    $ wget -O src.zip https://nextcloud.k-paas.org/index.php/s/sX8x5Yk26XBgP5n/download
    
    ## unzip download source files
    $ unzip src.zip
    
    ## final src directory
    src
    ├── ap-api-gateway-broker
    │   └── ap-api-gateway-broker.jar
    ├── api-gateway
    │   ├── artifacts-1.5.7.howto
    │   ├── artifacts-1.5.7.zip
    │   ├── org.wso2.carbon.identity.mgt.endpoint.util-5.17.5-K-PaaS.howto
    │   ├── org.wso2.carbon.identity.mgt.endpoint.util-5.17.5-K-PaaS.jar
    │   ├── wso2am-3.2.0-K-PaaS-v7.zip
    │   └── wso2am-3.2.0.howto
    ├── common
    │   ├── pid_utils.sh
    │   └── syslog_utils.sh
    ├── java
    │   ├── jce_policy-8.zip
    │   └── OpenJDK8U-jre_x64_linux_hotspot_8u212b03.tar.gz
    └── mariadb
        └── mariadb-10.5.17-linux-x86_64.tar.gz
    ```
- Create API Gateway Release
    ```
    $ cd ap-api-gateway-release
    ## <RELEASE_TARBALL_PATH> :: release file path (e.g. /home/ubuntu/workspace/ap-api-gateway-release.tgz) 
    $ bosh -e <bosh_name> create-release --name=ap-api-gateway --version=1.0 --tarball=<RELEASE_TARBALL_PATH> --force
    ```

### 참고 자료
- https://bosh.io/docs
- https://apim.docs.wso2.com/en/latest/
    
## Contributors ✨
<a href="https://github.com/K-PaaS/ap-api-gateway-release/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=K-PaaS/ap-api-gateway-release" />
</a>
