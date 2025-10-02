## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:db81b0a323b9557a1c85e2b148730dca493bc1dc664c27c82acbc7cec38e0451
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:4ae7c2db0120bd8df53590855cc0b28c7cf88f8f82ce45e1dcf05080eb169326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.8 MB (349803555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b70d3add7effcc0ed3981a2b45bd2cd16216e1a7008d6f57c343bce72a28a8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:20 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36-2
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 19 Sep 2025 18:21:04 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 19 Sep 2025 18:21:04 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 18:21:04 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 18:21:04 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 18:21:04 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 18:21:04 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 18:21:04 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 18:21:04 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 18:21:04 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 18:21:04 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 18:21:04 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 18:21:04 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 18:21:04 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 18:21:04 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 18:21:04 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b6baa302384dc877580d7e1080dcca1ed66d9d3b38afc9fcc29c360239e3e362`  
		Last Modified: Tue, 16 Sep 2025 20:50:40 GMT  
		Size: 54.0 MB (54005280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a075fb8961d282a9f92fb75aaa159d8011cb3dba1aa6fea626361cc411336906`  
		Last Modified: Thu, 25 Sep 2025 03:19:01 GMT  
		Size: 189.1 MB (189134365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b3dc9f8e2f1e2587471d869ca5b2d3e715921d10a1cafc928889c482f9fbc2`  
		Last Modified: Thu, 02 Oct 2025 13:22:23 GMT  
		Size: 97.4 MB (97420279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cc6c0a4e19f82489ed40f4f82e8ffcb76a318a19adc2aa3be2066d78bfb91d`  
		Last Modified: Thu, 02 Oct 2025 13:22:11 GMT  
		Size: 9.2 MB (9242590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc3e6fa90b8f43aceba8e99ec20409de57e1a1ea357a41a59ce68daa993ee8f`  
		Last Modified: Thu, 02 Oct 2025 13:22:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81bf6e7aa2477ef935ee2d4cc0bf4ed353d00c7577b1e73a8f476d3babfb824`  
		Last Modified: Thu, 02 Oct 2025 13:22:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:22f6313dca9b588d3cb1a452e87c8884920399e67a387450296e5efffe1864cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6224088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c607416afb68bd3952058be97dd437688f13d8f1787994c9ba2a82c241f54c6`

```dockerfile
```

-	Layers:
	-	`sha256:6b5749011328028d60e77c58988622036f61f1b8062263916794e60bbf91fec2`  
		Last Modified: Thu, 02 Oct 2025 14:29:12 GMT  
		Size: 6.2 MB (6207700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b984279b1fa45c0123bb2a92650fa25ebbcc43d4f210a11fd43c171dafad7b1`  
		Last Modified: Thu, 02 Oct 2025 14:29:13 GMT  
		Size: 16.4 KB (16388 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:0b04a86458754083d3e8e198c2182c488b6b9b15df5209c4f6aa6f624dee6dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.0 MB (346001388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ade8ac96de05af01d9b70b160d9ec407e230f194daa73d4b03d34e4b2bc422`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:25 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36-2
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 19 Sep 2025 18:21:04 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 19 Sep 2025 18:21:04 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 18:21:04 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 18:21:04 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 18:21:04 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 18:21:04 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 18:21:04 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 18:21:04 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 18:21:04 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 18:21:04 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 18:21:04 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 18:21:04 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 18:21:04 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 18:21:04 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 18:21:04 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:202438f011bd656c28426fbd92ff7e7030b77e67ebafd3bec95dbce9626db73c`  
		Last Modified: Tue, 16 Sep 2025 22:16:03 GMT  
		Size: 52.9 MB (52899438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898bb6a5c4e092b471dfbda1890bda78055f9989087ac015177c092ddf1ad3cf`  
		Last Modified: Wed, 24 Sep 2025 22:15:39 GMT  
		Size: 187.0 MB (187019791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75dfbfb7e8db2d39fc6f3458e4cec800283186e4c0b66b5bad7541b5440b5a9a`  
		Last Modified: Thu, 02 Oct 2025 03:33:37 GMT  
		Size: 96.8 MB (96838533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848917a5ceb8acf9f073b0f8273b7a980f5d987247239a36e7e56c82e38eb989`  
		Last Modified: Thu, 02 Oct 2025 03:33:17 GMT  
		Size: 9.2 MB (9242585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2175baa69d0f0cca0b59565460f83f8356cd44f2dc90afced44f6ca50e654e04`  
		Last Modified: Thu, 02 Oct 2025 03:33:16 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7b0c472d8b51f2be10e7f2d5a8f6c2c6405215a7eaf0059fe3d7ca9fe59579`  
		Last Modified: Thu, 02 Oct 2025 03:33:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:4d19443724e6a37fc98963b7595826460d41ba105bb02e82c9d652130fbc9d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d075a2115997743c9dbe4586d1386f09f3ccfcf73e5134a38b13567f81f7bf`

```dockerfile
```

-	Layers:
	-	`sha256:5c72bb40380cb083acde7102df1ce65f280b74060ca5ee63307ed95f283f4900`  
		Last Modified: Thu, 02 Oct 2025 05:29:16 GMT  
		Size: 6.2 MB (6206644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12026ba8581023880d77b59c82d56c472812e4c7004477470dfbb17d736a38ee`  
		Last Modified: Thu, 02 Oct 2025 05:29:16 GMT  
		Size: 16.5 KB (16519 bytes)  
		MIME: application/vnd.in-toto+json
