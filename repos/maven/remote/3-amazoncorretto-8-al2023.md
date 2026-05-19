## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:d7711451c4bac88572fed3d716d4f2c58b6bf1cac19f7b7bd64d0238b85f70f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:2d2cd31ff8ed9b2ff5530258a4194daececfeed7d2028b49f5d6a757d3da8dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.9 MB (517856660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558beee544b05a3b1363e114f1159b6178d357b500d81f7a4fc2c8e9ffdc1858`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:14:56 GMT
ARG version=1.8.0_492.b09-2
# Sat, 09 May 2026 00:14:56 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:14:56 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:14:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 18 May 2026 22:42:30 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 18 May 2026 22:42:31 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 18 May 2026 22:42:32 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 18 May 2026 22:42:32 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:42:32 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:42:32 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 18 May 2026 22:42:32 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 May 2026 22:42:32 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 May 2026 22:42:32 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 May 2026 22:42:32 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 May 2026 22:42:32 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 May 2026 22:42:32 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 May 2026 22:42:32 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 May 2026 22:42:32 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd2295c4476393f62916a766a1b4539c0fd524867201f0dcdd4ba2a80ded9a4`  
		Last Modified: Sat, 09 May 2026 00:15:51 GMT  
		Size: 330.8 MB (330819579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d1c175e8d12265a9d4800867c8312271f8cb3228e5a7e097cd22e085909e94`  
		Last Modified: Mon, 18 May 2026 22:43:06 GMT  
		Size: 117.7 MB (117652743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a903179729714daa90dd378d866576fa6ac85a881d85ad3e4877d27dadbf70e`  
		Last Modified: Mon, 18 May 2026 22:43:03 GMT  
		Size: 5.4 MB (5446561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082692991da2d510913087c70023a4ad410534ed7f53fd72745229786bb8f2d9`  
		Last Modified: Mon, 18 May 2026 22:43:03 GMT  
		Size: 9.4 MB (9359967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84913920f22f86e01239a2e1e8a678ddaa51e2726c443de8c665b93917030309`  
		Last Modified: Mon, 18 May 2026 22:43:02 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197c4e9b1f53595e740ac7d9f832f23d4d4e873e8d5da3378f9f458075f06870`  
		Last Modified: Mon, 18 May 2026 22:43:04 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:2b3b12b7686144cdde00317be6d8aabc5abc24b2724cc33b4a668f887b0338cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13850940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e65bde1390aa08ab7736d6b11425291521fd5ca595cee5177e490efb0f3563e`

```dockerfile
```

-	Layers:
	-	`sha256:090ff231b1f3ef7824b0e9e18fd563b4c343a501aeb97c0cd84e2ae78331021f`  
		Last Modified: Mon, 18 May 2026 22:43:03 GMT  
		Size: 13.8 MB (13834655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfedb4a790ac81676a4cc989187d331478b294356035d4131366186dc0d9d29d`  
		Last Modified: Mon, 18 May 2026 22:43:02 GMT  
		Size: 16.3 KB (16285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9944662ed3e87e88f6911f4cfc362cc8473c0836d34684bfcf818c50d916f089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307578863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a9c20b7b9b6fa2a2368550e52beb3067fd977166d7546d67acb3a5c512b7ca`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:14:49 GMT
ARG version=1.8.0_492.b09-2
# Sat, 09 May 2026 00:14:49 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:14:49 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:14:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 18 May 2026 22:42:25 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 18 May 2026 22:42:26 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 18 May 2026 22:42:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 18 May 2026 22:42:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:42:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:42:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 18 May 2026 22:42:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 May 2026 22:42:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 May 2026 22:42:27 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 May 2026 22:42:27 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 May 2026 22:42:27 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 May 2026 22:42:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 May 2026 22:42:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 May 2026 22:42:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f381327a354601594ad8bb3da3fa9f604c4e3d4d563f43a2f619ab5ef4c74655`  
		Last Modified: Sat, 09 May 2026 00:15:09 GMT  
		Size: 118.0 MB (117953507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af90d9c2bc5e8b68d601ce74026908c68146908dea09054993c024d58f5142f8`  
		Last Modified: Mon, 18 May 2026 22:42:47 GMT  
		Size: 114.0 MB (114035320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17e1c02870f01c01bedde20deb5c2c5358f5da9cabe1723eaa3c0daa2862797`  
		Last Modified: Mon, 18 May 2026 22:42:44 GMT  
		Size: 12.8 MB (12772083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3606f37c1cf377d47bbbf530573836427d6e0fe4648ee5de7f4c63aaba955e`  
		Last Modified: Mon, 18 May 2026 22:42:44 GMT  
		Size: 9.4 MB (9359969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6344c11e6d886197a28f8457e97b989a372e5f6240c276fa1a39fe7bd000bffa`  
		Last Modified: Mon, 18 May 2026 22:42:44 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c82463dc6615d58afab628a02bda8bf7d9b1da3844bc2355bd4b27a54317567`  
		Last Modified: Mon, 18 May 2026 22:42:45 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:836af4f875eaf82e3f752209b69eb6f24805e19c231e3e4c7767f22a725f92b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b31b735d661bfc8dbba6cf969f5c1b5e31ad42c62bae80e260aec8ce9a81742`

```dockerfile
```

-	Layers:
	-	`sha256:9127669c21bc5f61ef85d4b1459f8ffbc281ded70ef3b2ba3a7abdedf2a6157c`  
		Last Modified: Mon, 18 May 2026 22:42:44 GMT  
		Size: 6.6 MB (6615976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:537742122f9808c4f4ebeca30ab27169ac8f982ceed2590ea916ae30a597de55`  
		Last Modified: Mon, 18 May 2026 22:42:43 GMT  
		Size: 16.4 KB (16437 bytes)  
		MIME: application/vnd.in-toto+json
