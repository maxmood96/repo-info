## `amazoncorretto:8u422-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:fb5c16e7eb63b1da5ad8c86e8eb7a947707926c29ba9c05180cdc20a6a29b04b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7c0fea0e94dd9c71106e9d04a9c38003be7131d0aac19d36c7c3bcc6482f344d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171771484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a1b16482cd38dc92b38fb968fdf31d2763636b60f907118ea0be8a7e189b84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=1.8.0_422.b05-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:f956a2176a592b2f85941102c85f1a745c5e74f263c66fc5212bf9eb619f28e1`  
		Last Modified: Thu, 03 Oct 2024 13:25:55 GMT  
		Size: 62.7 MB (62678156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e76efed04719f61731d1e06fab111d58cf1b123ab92da22437c3d8a082b6f4`  
		Last Modified: Tue, 08 Oct 2024 00:00:15 GMT  
		Size: 109.1 MB (109093328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e02aa7fac02754ae978eba0d8457a9cebffde13b0195eeff26e2c1245033008e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7507276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0027b9cda0c093733c318874b03b43a620dcb42b6d36e8d72ce8364bb952fe`

```dockerfile
```

-	Layers:
	-	`sha256:980cdfdeefb5d6706da1652139a70135c56e53729740809db974f0b377d1f948`  
		Last Modified: Tue, 08 Oct 2024 00:00:14 GMT  
		Size: 7.5 MB (7497757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d1afdfbd676b261c907e77d5a0c92e2ab91152e9797b54b4b45ff75a02de2c2`  
		Last Modified: Tue, 08 Oct 2024 00:00:13 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b09d5df86a8982415d358b6268185e4a5b2b720b99f35c8d8eba5f20748a97d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117536795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cb56238ccb57be9349f91ef2e22547884a0c0c4a38e2194e3e3937d1f79a56`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=1.8.0_422.b05-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:17d30073c92a41fbc086cf7be6bbf70600b21ad41c671459f9fd5c536e5182dc`  
		Last Modified: Thu, 03 Oct 2024 13:26:09 GMT  
		Size: 64.6 MB (64592659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fab0fef673247773c744606f88fbea758e0d971537a220002ccb66c52f9f227`  
		Last Modified: Tue, 08 Oct 2024 01:55:18 GMT  
		Size: 52.9 MB (52944136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:352652252ca09a42441c57b6c506e14d84d4c15d95fb4922b3cffee31b1a3d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5623074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbcc2568e26678bbc15a8b6f3669170dcbc01c5ca79bf4f7c3136f958cbfe00`

```dockerfile
```

-	Layers:
	-	`sha256:cb6cf1fcf2cf49ca3da7a0dbb9c77f56f5d26e77f1270d597de025efdc029595`  
		Last Modified: Tue, 08 Oct 2024 01:55:16 GMT  
		Size: 5.6 MB (5613477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdbf100bb0cc47b0c87bbdb75053c218020b52679f3a5ea08b36f9340bddbf02`  
		Last Modified: Tue, 08 Oct 2024 01:55:15 GMT  
		Size: 9.6 KB (9597 bytes)  
		MIME: application/vnd.in-toto+json
