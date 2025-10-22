## `maven:3-amazoncorretto-25`

```console
$ docker pull maven@sha256:f0f3cfc7527bc7575d14ccfa889cba64bb45dd7b29cec35a7a60d2669418f779
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25` - linux; amd64

```console
$ docker pull maven@sha256:2922e59e9966e4eba78e19345a5929e2660bc0f8d9289671a374f6f6a1099a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351527509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fb38d841c9712a0d631ae890be63f361a9281b8f9c7cfca3d5163b85cbf791`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /rootfs/ / # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
CMD ["/bin/bash"]
# Fri, 19 Sep 2025 12:56:50 GMT
ARG version=25.0.1.8-1
# Fri, 19 Sep 2025 12:56:50 GMT
ARG package_version=1
# Fri, 19 Sep 2025 12:56:50 GMT
# ARGS: version=25.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
ENV LANG=C.UTF-8
# Fri, 19 Sep 2025 12:56:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 19 Sep 2025 12:56:50 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 12:56:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 12:56:50 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 12:56:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 12:56:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 12:56:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d2c4bebb63b964a5168a7f8dedcb088e3d65ad774c09e8153b520d312ebdb9`  
		Last Modified: Wed, 22 Oct 2025 00:58:29 GMT  
		Size: 189.2 MB (189170547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4df92129c3ecb486daa3b87517171c4c51daebf5e3195dadea896d315f97695`  
		Last Modified: Wed, 22 Oct 2025 03:21:56 GMT  
		Size: 99.1 MB (99108200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9002591347dfba45792468e4fb0ce6c8089c5bb06ba04bd61e920c758d95e71`  
		Last Modified: Wed, 22 Oct 2025 03:21:31 GMT  
		Size: 9.2 MB (9242588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d8d842dc1996a0ab245d4438e29f08d769943a4b43ee04516364944129e146`  
		Last Modified: Wed, 22 Oct 2025 03:21:30 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8289fc2cbe76ee47ccb84ebf5d1e0dd82c9d31ab5570a93085019e48f94bf`  
		Last Modified: Wed, 22 Oct 2025 02:53:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25` - unknown; unknown

```console
$ docker pull maven@sha256:43be19feaef11d5b55a334f9c94efa3b57905641038df33653908639c638e328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6226517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc8df1cbd5574f8c245247e9d68942d2f6957a1ab5d0267c9987a1badb5ffc2`

```dockerfile
```

-	Layers:
	-	`sha256:cd451a10f55e62ebf650969f5609c3d8638dec80d7dd4eab717b62907275728d`  
		Last Modified: Wed, 22 Oct 2025 05:27:19 GMT  
		Size: 6.2 MB (6208930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fead35f6ec1762f7e4399b9a40d950d88a2c376d9a2a62b1aff96860412505`  
		Last Modified: Wed, 22 Oct 2025 05:27:19 GMT  
		Size: 17.6 KB (17587 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e603587dec1d96eaa6309166917e543f3a74bec66bf869d31b97ccb1f087c091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.7 MB (347715091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe7baadab5636a1b18764a86f11cd28c4a1bd726777f777fb3b61f4ff30bd0a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /rootfs/ / # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
CMD ["/bin/bash"]
# Fri, 19 Sep 2025 12:56:50 GMT
ARG version=25.0.1.8-1
# Fri, 19 Sep 2025 12:56:50 GMT
ARG package_version=1
# Fri, 19 Sep 2025 12:56:50 GMT
# ARGS: version=25.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
ENV LANG=C.UTF-8
# Fri, 19 Sep 2025 12:56:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 19 Sep 2025 12:56:50 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 12:56:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 12:56:50 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 12:56:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 12:56:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 12:56:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0facfa421fa0d39948514b8fdbe1af18c63525acb19c3f4c8bddc6d0d119af`  
		Last Modified: Tue, 21 Oct 2025 22:11:05 GMT  
		Size: 187.1 MB (187096320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd42e3aa513394ab67a32995d0dda37c71437dbf2bc81caf9fc017755db35658`  
		Last Modified: Tue, 21 Oct 2025 23:33:05 GMT  
		Size: 98.5 MB (98483947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d421bcdad388f294469e1989dea6562e1db832b46ebf17b98b00fad6c039cb7`  
		Last Modified: Tue, 21 Oct 2025 22:20:16 GMT  
		Size: 9.2 MB (9242578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e213b2ff35b3d9df06084d9d680bafb96a9b3524cdd40aa8b396541f67ae21`  
		Last Modified: Tue, 21 Oct 2025 22:20:24 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f6cb73a9ce32f9075f260558bf2a0e70acd0b2fa9e0804858caaaa7f19bb64`  
		Last Modified: Tue, 21 Oct 2025 22:20:27 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25` - unknown; unknown

```console
$ docker pull maven@sha256:709c0528436937a6b17bec81e960d95e22c0284be03d0845dad7633bedff15fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6225690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66fd2f6af688ca78f85e9b1b31041a1876b85a9c70ac9f7fb505a9077ca28ed1`

```dockerfile
```

-	Layers:
	-	`sha256:78d9b331b1e6b5a8f331202dc565de1a2ea8d632d73aafc09b293ccb4abbb269`  
		Last Modified: Tue, 21 Oct 2025 23:27:39 GMT  
		Size: 6.2 MB (6207922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a6e800f4dba75659f37579196287b6502c00d4072a1d30120a2646e4f6e2c15`  
		Last Modified: Tue, 21 Oct 2025 23:27:40 GMT  
		Size: 17.8 KB (17768 bytes)  
		MIME: application/vnd.in-toto+json
