## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:6bcfc3cf69a75d24d9db57ca5bb7eab1ac706b9f91aaf2d065b9509784882249
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:81e44c2941cdbaf82149a434f805d1ea8c97a194d9c97513108be5be91576128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.4 MB (348362852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6a77567b3d2c2483b8786f4b5716a29655ed71db4d0edc437cb5c58704494b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Sep 2025 20:25:28 GMT
COPY /rootfs/ / # buildkit
# Wed, 10 Sep 2025 20:25:28 GMT
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
	-	`sha256:0727f841555e830a24054117b5d53ecc18438e2e82fc78dd3cc766ca6bb76cab`  
		Last Modified: Wed, 10 Sep 2025 02:33:49 GMT  
		Size: 53.9 MB (53875706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd7e0d628572965a23d86a7660738c6019a621d12327d61edb46382f7998be8`  
		Last Modified: Wed, 17 Sep 2025 18:56:00 GMT  
		Size: 189.1 MB (189130862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4973f75901ee4fe15d5023fa8045782e86a1a0df2e4c6152e67a37606159efcc`  
		Last Modified: Mon, 22 Sep 2025 19:24:36 GMT  
		Size: 96.1 MB (96112656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e8428226102ea09798fad3e8283b2078ae3d7a876ec88e86f177294a675e3f`  
		Last Modified: Mon, 22 Sep 2025 17:06:37 GMT  
		Size: 9.2 MB (9242583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d21c646597270a41117f451d2c8fefd5322269296ca054222caaad7581d790`  
		Last Modified: Mon, 22 Sep 2025 17:06:38 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe99be589c8e449c8eee8df9df4c1a4560dbe90084ed28a774250522ab956c72`  
		Last Modified: Mon, 22 Sep 2025 17:06:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:3a518607fa68dfa4ef74fb74d520042a5af5f6947e3dc9c69728f3951e76ac81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6224088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2bd63b95ce8d2bb2c9eea1a2535e9e974b08e2cabc7685eb526afb76094a11`

```dockerfile
```

-	Layers:
	-	`sha256:c7aa071ce75f06bdd1317301c7eb33564d27a892a8fa8948087b1d9977a3b35a`  
		Last Modified: Mon, 22 Sep 2025 17:27:48 GMT  
		Size: 6.2 MB (6207700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8058a5c2ca54b5859a1f5cdd17abc17b8b6da971e6e90795b47b831e3e39a81c`  
		Last Modified: Mon, 22 Sep 2025 17:27:50 GMT  
		Size: 16.4 KB (16388 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:003e7063439eef6e81a7803819b3cc85ad12c8f101d3b157611d01f8091fd5f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.0 MB (346001078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879280c06224b86424ba42c4e403d3200efc041f0cab971f69d7a3ac115fd74b`
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
	-	`sha256:b8d18d870d8fc94bc5309e4aec5bad9168b73e077028def16afbd0058fa55b6a`  
		Last Modified: Thu, 25 Sep 2025 01:13:09 GMT  
		Size: 96.8 MB (96838231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0e757ab8aee3dcdc9da4250ba077618d77883a4993f8560f1a7bc716979c81`  
		Last Modified: Thu, 25 Sep 2025 01:12:55 GMT  
		Size: 9.2 MB (9242579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5799a3a37703f829ba16a83bdcd3e6c922911016e6c5d1afd50982660ca5200`  
		Last Modified: Thu, 25 Sep 2025 01:12:54 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcada273f8db949b234fa47d79fe8763f9d565391b272bdef8e7c15a4f433bb`  
		Last Modified: Thu, 25 Sep 2025 01:12:54 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:bf49134a0948181017388afd36cf2d8ad0ad3b5b5990f14fa85fe9b7a80dbe8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d9a97ff3d64883c18d2ef29b54391598bfc436068f7345e024b0eed7d00421`

```dockerfile
```

-	Layers:
	-	`sha256:e01c086bb1be8a84ddacdf681a362215f43166424c52f648afdd0ef0568694dc`  
		Last Modified: Thu, 25 Sep 2025 02:28:24 GMT  
		Size: 6.2 MB (6206644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:458a62512ddbf0b602ea00495eb15b3550e70b28bd7661169640814b7ad0e643`  
		Last Modified: Thu, 25 Sep 2025 02:28:25 GMT  
		Size: 16.5 KB (16520 bytes)  
		MIME: application/vnd.in-toto+json
