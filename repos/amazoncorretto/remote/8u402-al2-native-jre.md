## `amazoncorretto:8u402-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:386917e9f57168599346e1925e5744a46e1a669250fe874428311997d3161dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8u402-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f056e05c2bf859445959b76e8bc49a343b8bfb39cbce2653f36ac550c135be49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171823439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9407f6e378deee883603f28aabb7b6dbec35a4f831181b3d3f8fb2081a5d7068`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Feb 2024 22:52:13 GMT
COPY dir:54de4a09e8ed7b6d891ffc8d82bcabfb18706cd08eadb7193bbf9e8397ee4d73 in / 
# Mon, 26 Feb 2024 22:52:14 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 23:08:34 GMT
ARG version=1.8.0_402.b08-1
# Mon, 26 Feb 2024 23:10:13 GMT
# ARGS: version=1.8.0_402.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf
# Mon, 26 Feb 2024 23:10:14 GMT
ENV LANG=C.UTF-8
# Mon, 26 Feb 2024 23:10:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:e24f20ed38d851720ffd5b15a06dad772c10fa9feea0e462fb5065d997fcb0bb`  
		Last Modified: Sat, 24 Feb 2024 04:13:54 GMT  
		Size: 62.6 MB (62646731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928d56982b8a6da760b98ecd021b63858bae3ae22fbd54e7ad99a27be42f7dde`  
		Last Modified: Mon, 26 Feb 2024 23:24:06 GMT  
		Size: 109.2 MB (109176708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8u402-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:37c385789974ba575f5955d41d7c8ea041e14126f474adc77ecd1ff58e3c7ac4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117274756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3bc8fa93af13c421e9222469297db374fecb1359fa1aa4bbfc777b9e19974c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Feb 2024 23:06:29 GMT
COPY dir:ed6a811a4137d0b4591f2c9dabfdd849cb878c3501af91aa79c89a2e9f4479d5 in / 
# Mon, 26 Feb 2024 23:06:30 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 23:35:47 GMT
ARG version=1.8.0_402.b08-1
# Mon, 26 Feb 2024 23:36:46 GMT
# ARGS: version=1.8.0_402.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf
# Mon, 26 Feb 2024 23:36:46 GMT
ENV LANG=C.UTF-8
# Mon, 26 Feb 2024 23:36:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:53f483bd5fa48049d6551a641e547b302df82b17493915161f3f62020b3648fa`  
		Last Modified: Mon, 26 Feb 2024 23:07:06 GMT  
		Size: 64.4 MB (64445079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d25a3627ec90a354ac26137e45907920b2176cb40b6ab5bd661e09dc1cfebc0`  
		Last Modified: Mon, 26 Feb 2024 23:47:07 GMT  
		Size: 52.8 MB (52829677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
