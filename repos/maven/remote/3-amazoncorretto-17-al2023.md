## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:0812b91697f891bd10ed9d17baa1022f1d38a42d21ae99ee1ed30917581861fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:5469aead873663789821655077a9291979af989ab4bb52386582fc1baa01c6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.9 MB (335924469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbaebf3018a51b8e4c77721f67a604dc348bdc4cb9f55e64aea2bdcf51c53137`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:01 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:01 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:13:35 GMT
ARG version=17.0.18.9-1
# Mon, 02 Mar 2026 23:13:35 GMT
ARG package_version=1
# Mon, 02 Mar 2026 23:13:35 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:13:35 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:13:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 03 Mar 2026 00:14:27 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 03 Mar 2026 00:14:30 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 03 Mar 2026 00:14:30 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 03 Mar 2026 00:14:30 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 03 Mar 2026 00:14:30 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 03 Mar 2026 00:14:30 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 03 Mar 2026 00:14:30 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 03 Mar 2026 00:14:30 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 03 Mar 2026 00:14:30 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 03 Mar 2026 00:14:30 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 03 Mar 2026 00:14:30 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 03 Mar 2026 00:14:30 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 03 Mar 2026 00:14:30 GMT
ARG USER_HOME_DIR=/root
# Tue, 03 Mar 2026 00:14:30 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 03 Mar 2026 00:14:30 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 03 Mar 2026 00:14:30 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2584a8e504dfaf493eadaafafbabd8b97f7cb5bbe3cb6a319fb37cf3c4335d86`  
		Last Modified: Thu, 19 Feb 2026 02:57:43 GMT  
		Size: 54.0 MB (54032840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291656abe10718a5b7ecb3affcd502d6d49aac432bab42c4affe10d8907b4b47`  
		Last Modified: Mon, 02 Mar 2026 23:13:54 GMT  
		Size: 156.9 MB (156911090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0f53b2cee88330425f8812a03845ff934af9b8d176b54d4daa5e9a71f0704c`  
		Last Modified: Tue, 03 Mar 2026 00:14:48 GMT  
		Size: 103.1 MB (103138580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fe4a8f26f621288ad2553e578ed257ee5592bf7e36ee8b41f069f727712973`  
		Last Modified: Tue, 03 Mar 2026 00:14:46 GMT  
		Size: 12.5 MB (12528679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff75b6e3d48d32f7cc108576ce821e4bc23b2a37ba8bc8d05ff9c8c705b0732`  
		Last Modified: Tue, 03 Mar 2026 00:14:46 GMT  
		Size: 9.3 MB (9312236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd2bfb30b7fd7340fd35c4d22a0bb3582bb6e13e31421d19f968d1a755df277`  
		Last Modified: Tue, 03 Mar 2026 00:14:45 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57018ebc87c1a74ca3435b770fd79134379a78ba1a06bd13f65fab2526036d8a`  
		Last Modified: Tue, 03 Mar 2026 00:14:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:272afac58261daef767581fba14ef1e743b6c15d9454621abfaa8e13894ad6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7571c7a4db47d5960a53300a8eea0bda5fffdca710abfc19905aabdd36fef802`

```dockerfile
```

-	Layers:
	-	`sha256:a3591782dd1eacb79bd9f333a02ab4a668d548421c0fbc070730d7eb9dbc9833`  
		Last Modified: Tue, 03 Mar 2026 00:14:45 GMT  
		Size: 6.2 MB (6232095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c53ac43c12d753ac9140e2fe0cfd5cf60936572df1ff527b1b374997f96745f`  
		Last Modified: Tue, 03 Mar 2026 00:14:45 GMT  
		Size: 18.3 KB (18291 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:0949e4e6eb5016d967e8dd5d809c1148b5f56834f828d871d8957f72481801d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.6 MB (332629298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7895c435b407281208c903e15af39a2486a8f68e2aeb2dbed718d46f55ff09c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:04 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:14:40 GMT
ARG version=17.0.18.9-1
# Mon, 02 Mar 2026 23:14:40 GMT
ARG package_version=1
# Mon, 02 Mar 2026 23:14:40 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:14:40 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:14:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 03 Mar 2026 00:15:08 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 03 Mar 2026 00:15:12 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 03 Mar 2026 00:15:12 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 03 Mar 2026 00:15:12 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 03 Mar 2026 00:15:12 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 03 Mar 2026 00:15:12 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 03 Mar 2026 00:15:12 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 03 Mar 2026 00:15:12 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 03 Mar 2026 00:15:12 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 03 Mar 2026 00:15:12 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 03 Mar 2026 00:15:12 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 03 Mar 2026 00:15:12 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 03 Mar 2026 00:15:12 GMT
ARG USER_HOME_DIR=/root
# Tue, 03 Mar 2026 00:15:12 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 03 Mar 2026 00:15:12 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 03 Mar 2026 00:15:12 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9330fae67a20d9aa2569828674140d8b67d50cfd127cb99ba0f9be275d35f976`  
		Last Modified: Thu, 19 Feb 2026 02:57:42 GMT  
		Size: 52.9 MB (52941319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458a2c883ef0e813dd59cc98f7ab9fa2c67d320d0117be74523be410b68ca3ed`  
		Last Modified: Mon, 02 Mar 2026 23:15:03 GMT  
		Size: 155.7 MB (155727670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31d7dc0cda0cb695efb4e31b6a7b111700339a5537b1416bf5adc8a09922281`  
		Last Modified: Tue, 03 Mar 2026 00:15:31 GMT  
		Size: 101.9 MB (101857664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95762cf9006c1f7d8eec726f53a913a5cb43a79be88969c0962f4be647f27cd1`  
		Last Modified: Tue, 03 Mar 2026 00:15:28 GMT  
		Size: 12.8 MB (12789361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89f48f2f3b6c8f4d5c261cf905facdfd2d501085beaeb05c58d6449a84ad17f`  
		Last Modified: Tue, 03 Mar 2026 00:15:28 GMT  
		Size: 9.3 MB (9312240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f00cd114b75e4b5db11a9a3f57bd5c00f5af124d1f3d2f38ef848bbb56d593`  
		Last Modified: Tue, 03 Mar 2026 00:15:27 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d49e295ec5c43eaf2209819dd2ade3869f5327c7af7ab225de60c3fad19092e`  
		Last Modified: Tue, 03 Mar 2026 00:15:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:93422b5c208c8d10834bcbef7456a01021ae8184efd36c9bab901b71197f8318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6249463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac7f7b322b462e996f546249a355d626f1c64c27c6bf8cb13f7c3abd53df3c1`

```dockerfile
```

-	Layers:
	-	`sha256:bf8801993548e7c832982c82e7f434fb121d26ee0d28372937378150f50e7ba0`  
		Last Modified: Tue, 03 Mar 2026 00:15:28 GMT  
		Size: 6.2 MB (6231025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:015331151fc5cc29e77b85b9e2addcc156f583168977e08483931af1fa48861f`  
		Last Modified: Tue, 03 Mar 2026 00:15:27 GMT  
		Size: 18.4 KB (18438 bytes)  
		MIME: application/vnd.in-toto+json
