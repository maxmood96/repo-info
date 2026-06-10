## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:8fc682e12ccbeeef136744686d5af2a07d97f69c0316d3f91e7412c58ec4b233
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:ed7cd81952e3c4974043b4ecb70ed281ce0c8583f1709601069286ad88272346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384460617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bed7cd7d3bc4b322751ac72f887fc9a9cda424a1e213faa2d1f8da659b79b32`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:24 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:24 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:42 GMT
ARG version=25.0.3.9-1
# Tue, 09 Jun 2026 21:12:42 GMT
ARG package_version=1
# Tue, 09 Jun 2026 21:12:42 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:12:42 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 09 Jun 2026 22:08:50 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 09 Jun 2026 22:08:50 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 09 Jun 2026 22:08:50 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 09 Jun 2026 22:08:50 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 09 Jun 2026 22:08:50 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 09 Jun 2026 22:08:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 09 Jun 2026 22:08:50 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 09 Jun 2026 22:08:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 09 Jun 2026 22:08:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 09 Jun 2026 22:08:50 GMT
ARG USER_HOME_DIR=/root
# Tue, 09 Jun 2026 22:08:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 09 Jun 2026 22:08:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 09 Jun 2026 22:08:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2cff886cd8efbaaf67f0b1d3449b228936c361c65f92f96e99b501f9431ebf`  
		Last Modified: Tue, 09 Jun 2026 21:13:07 GMT  
		Size: 189.4 MB (189412731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41d38650b5745a61a92e81f35977506e80807e7bceb2c70a523ca58cde376f6`  
		Last Modified: Tue, 09 Jun 2026 22:09:06 GMT  
		Size: 131.1 MB (131115753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd25e5eaa7247b00b54525818f4195bb16475950d87803ee9593bd3f883bd65`  
		Last Modified: Tue, 09 Jun 2026 22:09:04 GMT  
		Size: 9.4 MB (9359965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbfb27d406b2105661586604e1162e2a57590ee1b5a8921a87d2b9141d0ba29`  
		Last Modified: Tue, 09 Jun 2026 22:09:03 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc18ad36fd3369892e8639274aef3bd01db04e633cf3d8819242d444671dfea8`  
		Last Modified: Tue, 09 Jun 2026 22:09:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:6553442cea60f4d1f74574f9132eecee63e7d59db6cd878d65e835d83c08ce32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6229546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c63484a5295886711b2ee0f14e97b9778a4e62b5843b31a6f1a77deedf653d`

```dockerfile
```

-	Layers:
	-	`sha256:33e49afbdb9ff27e3b3a871c1f6cae0bb018cb38b24b29a0ed364bde0e6fe52c`  
		Last Modified: Tue, 09 Jun 2026 22:09:04 GMT  
		Size: 6.2 MB (6215039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24aeee3004f0d18bb719858ec8046f07fdd9d0f1cae5a7602f6361cbbdff35db`  
		Last Modified: Tue, 09 Jun 2026 22:09:03 GMT  
		Size: 14.5 KB (14507 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c055a219d26ab4f96aa06a33869a36885b9116bd215c066461e55fdf35a2d407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 MB (380179102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973952c2426b5895445b3dca32105252f04d70b8f64879e82f7cf4b5927ad522`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:21 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:21 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:37 GMT
ARG version=25.0.3.9-1
# Tue, 09 Jun 2026 21:12:37 GMT
ARG package_version=1
# Tue, 09 Jun 2026 21:12:37 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:12:37 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 09 Jun 2026 22:10:21 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 09 Jun 2026 22:10:21 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 09 Jun 2026 22:10:21 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 09 Jun 2026 22:10:21 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 09 Jun 2026 22:10:21 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 09 Jun 2026 22:10:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 09 Jun 2026 22:10:21 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 09 Jun 2026 22:10:21 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 09 Jun 2026 22:10:22 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 09 Jun 2026 22:10:22 GMT
ARG USER_HOME_DIR=/root
# Tue, 09 Jun 2026 22:10:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 09 Jun 2026 22:10:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 09 Jun 2026 22:10:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62292040f1e97bc790fd253e8fd7ba92295a350f31be03f2f532387f78e3d3f1`  
		Last Modified: Tue, 09 Jun 2026 21:13:04 GMT  
		Size: 187.3 MB (187327258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ff24848daec6ee176d66b6fed70972bef009fdfe735821940ebb3e007676f8`  
		Last Modified: Tue, 09 Jun 2026 22:10:43 GMT  
		Size: 130.0 MB (130033030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da938c3d0258ba600caaa5f33050caaef47930dd409409f6ad322702ce15b75a`  
		Last Modified: Tue, 09 Jun 2026 22:10:40 GMT  
		Size: 9.4 MB (9359973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c142e6656807cb46abef5cce6d367729108a302f71cd1cdf3144517c12320798`  
		Last Modified: Tue, 09 Jun 2026 22:10:39 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e07456263ca3c3921b46fdd582fb57b27f88555cb0a768346c553831ff18009`  
		Last Modified: Tue, 09 Jun 2026 22:10:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:8121916fedaf90b6f432ffeebf7da9c36d97ef8062be534cb7d1641ffc848482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6228624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd2833735f0dc0da5032cd319e8a77ec40c01ecacaad1318ee9aaadf306025e`

```dockerfile
```

-	Layers:
	-	`sha256:7d8597ada385e02f61888d8c015ee6f6a3fbabf9637187ab6e48544e23693c5d`  
		Last Modified: Tue, 09 Jun 2026 22:10:40 GMT  
		Size: 6.2 MB (6213984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb0b01ad04b37ce72d6bab4d9d1fe026f630c76a2eefd3aeae06d329d9f55ad`  
		Last Modified: Tue, 09 Jun 2026 22:10:39 GMT  
		Size: 14.6 KB (14640 bytes)  
		MIME: application/vnd.in-toto+json
