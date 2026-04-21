## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:02a1608969bf435ba7fa878fdfdf973728b8adaed3930f01003d6fb5b746c70f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:c9420d2a5f4387a803c68ebd551b13afd92e33e9f8821e171e4a1f1a162b9feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.9 MB (371929200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90912f649bc6b6f12eebbee934c4a2a7955b57e79a69db18d3b2323a02d87838`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:26:44 GMT
ARG version=25.0.2.10-1
# Wed, 15 Apr 2026 21:26:44 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:26:44 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:26:44 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:26:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 21 Apr 2026 18:12:29 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 21 Apr 2026 18:12:29 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:12:29 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:29 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:29 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:12:29 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:12:29 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:12:29 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:12:29 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:12:29 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:12:29 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:12:29 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:12:29 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1ea217645c100a6a722630601c1c84cdadb45351d90b7a9d6e48270865321b`  
		Last Modified: Wed, 15 Apr 2026 21:27:09 GMT  
		Size: 189.2 MB (189188253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fd8644e359d015ec41fcbe44f41928cb527eaec58d9de45ac455ffa29522ca`  
		Last Modified: Tue, 21 Apr 2026 18:12:49 GMT  
		Size: 118.9 MB (118856489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b1bd684019e9c27f0c609911aeb3fb5cc58907b31fa23aadd8fe8b52270b6a`  
		Last Modified: Tue, 21 Apr 2026 18:12:46 GMT  
		Size: 9.3 MB (9312196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52251ead39becf69dfa1b28658e2952e8198e2e55cd86316d7c1ef0e1e2d49af`  
		Last Modified: Tue, 21 Apr 2026 18:12:45 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3821d1dbabbbab1e9b80650c31925dc48f261159fbee9317944db7871af8ed`  
		Last Modified: Tue, 21 Apr 2026 18:12:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:07ea60e42584eafac7c20a45172e215f15bf7dfcfcd0ac754baee73e3c0d9ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6228734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1f7b10e7c733d67a41121d999bc2a4ce04c7d65b49a23355273209ff04f873`

```dockerfile
```

-	Layers:
	-	`sha256:5b2eee2fb771c5eacaf2fe511f4db1ebc0ea3a9c260374d02796134f3f0cb47c`  
		Last Modified: Tue, 21 Apr 2026 18:12:46 GMT  
		Size: 6.2 MB (6214227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c836a40a09e6e812525808000aa396a07c70b212d3eafb7df009df3b4ea550a5`  
		Last Modified: Tue, 21 Apr 2026 18:12:45 GMT  
		Size: 14.5 KB (14507 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d23ce19885a6a048785ccd1a20d58c50f5d27a22db0db93d26149b365c0d4735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367837585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f613ebabe169064b65e6be8416b5b766e315f76cdda87be81aa56f48a441082`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:39:50 GMT
ARG version=25.0.2.10-1
# Wed, 15 Apr 2026 21:39:50 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:39:50 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:39:50 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:39:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 21 Apr 2026 18:12:20 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 21 Apr 2026 18:12:20 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:12:20 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:20 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:20 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:12:20 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:12:20 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:12:20 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:12:20 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:12:20 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:12:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:12:20 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:12:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97e5eaff5c173c2d572c7ece0a4ad5d4ba6d11aa38fa3b123836e74ff874e0f`  
		Last Modified: Wed, 15 Apr 2026 21:40:18 GMT  
		Size: 187.1 MB (187089832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb15ffc4445b80bd46c9a67d1b80a08fc3c0ecc2f083c5f85ea591735a2995c`  
		Last Modified: Tue, 21 Apr 2026 18:12:43 GMT  
		Size: 118.0 MB (117991752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cde8f58b46c9f3e7f14e0fbb5f9e9c66af8b5ed17f17533c0a7ff147345b95b`  
		Last Modified: Tue, 21 Apr 2026 18:12:39 GMT  
		Size: 9.3 MB (9312254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c9532280f92bc6429c9b783365eedd59da444741db82d4b1fb83dc233c4769`  
		Last Modified: Tue, 21 Apr 2026 18:12:39 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2207445d9158e18203ae2f21dd641da4cba7fe58ff8e496fa11145ed2696c40b`  
		Last Modified: Tue, 21 Apr 2026 18:12:39 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:8ffbef9585aa0b09c8bf0f72bc4f7e4e9a651ac88e54b03b48e9161670446e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6227811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d3e83980b9b8f3e16742203decccbd26dbdf494f5e68fb93a47303bb8a3ee2`

```dockerfile
```

-	Layers:
	-	`sha256:82bb4ec7509be710d436aa120729c26e5c29a1cfbefd2ea3903f92553732898e`  
		Last Modified: Tue, 21 Apr 2026 18:12:39 GMT  
		Size: 6.2 MB (6213171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3780a319ff3e45e58fa21433b92a826af545181f888a0d251661ca6040d6224f`  
		Last Modified: Tue, 21 Apr 2026 18:12:39 GMT  
		Size: 14.6 KB (14640 bytes)  
		MIME: application/vnd.in-toto+json
