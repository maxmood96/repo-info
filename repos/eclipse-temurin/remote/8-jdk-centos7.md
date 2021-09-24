## `eclipse-temurin:8-jdk-centos7`

```console
$ docker pull eclipse-temurin@sha256:232d11115b6b4725da61dafc96a12d2b6e082bfea8fd202b44047cf76aade187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8-jdk-centos7` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:38ee669e97652eeec49ee03feb2d3cc4ba56b49f972a1d10b8c8a7e9fde7fceb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192354181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2d93c320c56a83806ad903c87adb0f787d6d090a2474b12902c877d6554b8b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:51:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Sep 2021 18:51:48 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar     && yum clean all
# Wed, 15 Sep 2021 18:51:48 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Fri, 24 Sep 2021 19:20:01 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='f287cdc2a688c2df247ea0d8bfe2863645b73848e4e5c35b02a8a3d2d6b69551';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u302b08.tar.gz';          ;;        armhf|arm)          ESUM='666f159ab0a2dd09c776681eb7cecaf04dc17e35deb213e588fe4f00c2fcac24';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u302b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='c2940f3772d4467a818a0221e80c2c720b6d427a886aaed37262e451ddbb0a56';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u302b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='cc13f274becf9dd5517b6be583632819dfd4dd81e524b5c1b4f406bdaf0e063a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u302b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 24 Sep 2021 19:20:01 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Sep 2021 19:20:02 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df6893209e3a4a16d453c0b998ba34f62067ad6099b971afc4f30040eb1467d`  
		Last Modified: Wed, 15 Sep 2021 18:54:13 GMT  
		Size: 12.7 MB (12706445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c076e0909e147fad15d7ff1082587e966ff7b7b4123761a7c30fdaba22ea085`  
		Last Modified: Fri, 24 Sep 2021 19:22:38 GMT  
		Size: 103.6 MB (103550420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2a49864b2eb8106ee5a06f727f5b739d018ad0895c1ae0a048b2104254b0d4`  
		Last Modified: Fri, 24 Sep 2021 19:22:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-centos7` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:2e34291dbd5bdeb680c5dd9bffb28f426c039c207679fc98257b501372cb4b76
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223339111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814a3d6d278c83deaaf57ca95b21115fd25ea27078b56a3745101554e144dbb7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 17:56:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Sep 2021 17:57:03 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar     && yum clean all
# Wed, 15 Sep 2021 17:57:03 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Fri, 24 Sep 2021 19:40:05 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='f287cdc2a688c2df247ea0d8bfe2863645b73848e4e5c35b02a8a3d2d6b69551';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u302b08.tar.gz';          ;;        armhf|arm)          ESUM='666f159ab0a2dd09c776681eb7cecaf04dc17e35deb213e588fe4f00c2fcac24';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u302b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='c2940f3772d4467a818a0221e80c2c720b6d427a886aaed37262e451ddbb0a56';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u302b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='cc13f274becf9dd5517b6be583632819dfd4dd81e524b5c1b4f406bdaf0e063a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u302b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 24 Sep 2021 19:40:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Sep 2021 19:40:06 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cca57fa161b6ec4ede17f372495cf8207b6f6a1624061d1eb017aa0eb032d6d`  
		Last Modified: Wed, 15 Sep 2021 18:00:52 GMT  
		Size: 12.3 MB (12258195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fafe7189b540a1716888b7865aafacc12b5e2de9539ebe4c710d5493df5286f3`  
		Last Modified: Fri, 24 Sep 2021 19:43:47 GMT  
		Size: 102.7 MB (102705810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f96ca07feb479a24956aded948c6a9471c7bfab98f22d542cac86b9d97f4b8`  
		Last Modified: Fri, 24 Sep 2021 19:43:36 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-centos7` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:6d76f1138be37003c1bc0615366a699882cba9c8df58093e3b94bc297f5a5522
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 MB (194204812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a697d1b49195334df877c1193ebf1998076555a9c1cf1537d0083c3172aca7b6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Sep 2021 18:29:27 GMT
ADD file:7f21ae7d20a8e347d8b678bcf26be83abb1ee27d3b567c9cddd993e45ce8ac34 in / 
# Wed, 15 Sep 2021 18:29:31 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:29:40 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 21:27:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Sep 2021 21:29:19 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar     && yum clean all
# Wed, 15 Sep 2021 21:29:26 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Wed, 22 Sep 2021 19:58:18 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='f287cdc2a688c2df247ea0d8bfe2863645b73848e4e5c35b02a8a3d2d6b69551';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u302b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='c2940f3772d4467a818a0221e80c2c720b6d427a886aaed37262e451ddbb0a56';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u302b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='cc13f274becf9dd5517b6be583632819dfd4dd81e524b5c1b4f406bdaf0e063a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u302b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 22 Sep 2021 19:58:30 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Sep 2021 19:58:45 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3fe478aaff9b8f3ba958253e7339e9016ec07c075b805ebfc8cd372ddd01ee64`  
		Last Modified: Tue, 17 Nov 2020 04:06:20 GMT  
		Size: 80.5 MB (80516460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f502386ff4e2195af1b6b4432c6ccd0fabc7a63dd38550f635eacaa707c74a`  
		Last Modified: Wed, 15 Sep 2021 21:38:40 GMT  
		Size: 12.6 MB (12616024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e747ddaa00f320c5f5826cf6efffb8a3280609cbdfdb39d1e494481fa78783ea`  
		Last Modified: Wed, 22 Sep 2021 20:07:25 GMT  
		Size: 101.1 MB (101072165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2201d199fe5ca9b19597113cac8f62bf1799646210ce14ba098b1835936370df`  
		Last Modified: Wed, 22 Sep 2021 20:07:12 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
