## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:9d46a4533a20a2674d0cb96de032a2e48985b1849c75a56c5142ba73f02678ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:0ee3c32c79e039b232a3e4f3dfb38ba2839451d27ab890100a7ee52caaa76ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265635614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6df3ea35683185c56ee2ad3e2fce93d33ba547192accb333601de1b3fcf003`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Apr 2024 22:25:10 GMT
COPY dir:c7d5463abe17dfd3879bd12c94f31ebdaedb939167b5199c40650e35e379f334 in / 
# Fri, 19 Apr 2024 22:25:10 GMT
CMD ["/bin/bash"]
# Fri, 19 Apr 2024 22:56:23 GMT
ARG version=17.0.11.9-1
# Fri, 19 Apr 2024 22:56:23 GMT
ARG package_version=1
# Fri, 19 Apr 2024 22:56:46 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 19 Apr 2024 22:56:47 GMT
ENV LANG=C.UTF-8
# Fri, 19 Apr 2024 22:56:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 27 May 2024 15:57:48 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 27 May 2024 15:57:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 27 May 2024 15:57:48 GMT
ARG MAVEN_VERSION=3.9.7
# Mon, 27 May 2024 15:57:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 27 May 2024 15:57:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 27 May 2024 15:57:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6f59c9417334b7a9eb6449cc09a14d6738ae8afbfb25d681f2c27740e7d4856c`  
		Last Modified: Fri, 19 Apr 2024 22:25:53 GMT  
		Size: 52.3 MB (52323609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7faae36eec06ab9002b453e309f1efbfb1c1b6ca3ad60cebefee42df6aac9dc3`  
		Last Modified: Fri, 19 Apr 2024 23:09:57 GMT  
		Size: 157.1 MB (157050137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c97985d3eb27479493ce6edd8cbc42c44b594b6c22779755a2b62b0933fded`  
		Last Modified: Tue, 28 May 2024 19:56:11 GMT  
		Size: 46.6 MB (46612928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe51cd8a4e1349071c4a7d8897120c1a534cd58cff35f5f92263e485d5a6f14`  
		Last Modified: Tue, 28 May 2024 19:56:08 GMT  
		Size: 9.6 MB (9647563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4004777c17cf29165e25f7a4a301ddb4f00320f843e58e547b39fefb7f7673`  
		Last Modified: Tue, 28 May 2024 19:56:08 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff19cce96269c061e4797ae381daa088455a00b9b68c8844c7dd3c25ffe9218d`  
		Last Modified: Tue, 28 May 2024 19:56:08 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72e30343224eaa7d4f57e6b85102d82c44cf5e6c99767cff73e57ca24c794bb`  
		Last Modified: Tue, 28 May 2024 19:56:08 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ee3cc78e5834b8faff49655b12b8e13daaecc85a59d5c255db22f3a07bb0271f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.1 MB (265083027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb342ef7db375b6ee233f1845be3484c22389d6ffc60a5f2b19d8b9169072a38`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 05 Jun 2024 00:47:28 GMT
COPY dir:ba9790f78add1c4638ee46d842ce6b7ee4d659e1ce4ca5bfa2485adaf6cac8ec in / 
# Wed, 05 Jun 2024 00:47:29 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:33:25 GMT
ARG version=17.0.11.9-1
# Wed, 05 Jun 2024 02:33:25 GMT
ARG package_version=1
# Wed, 05 Jun 2024 02:33:44 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 05 Jun 2024 02:33:46 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:33:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 27 May 2024 15:57:48 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 27 May 2024 15:57:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 27 May 2024 15:57:48 GMT
ARG MAVEN_VERSION=3.9.7
# Mon, 27 May 2024 15:57:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 27 May 2024 15:57:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 27 May 2024 15:57:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:decbb28a26fad91fa4c617ae5541ffaa8f680fc91855c8bb640254519df67bf1`  
		Last Modified: Wed, 29 May 2024 02:10:34 GMT  
		Size: 51.4 MB (51403878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d3f08dfec1b60aa193195b32e09bbde055cc300cf866d64fb9cc03885074e4`  
		Last Modified: Wed, 05 Jun 2024 02:44:12 GMT  
		Size: 155.7 MB (155744539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b7e16052cdc686caf8f0efa0ca074a5b45efc237da361505a958e889b47446`  
		Last Modified: Wed, 05 Jun 2024 03:19:28 GMT  
		Size: 48.3 MB (48285709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b2e09dad461d3e02373b7572059130d4bf219deabea7ef77defe3a8410f186`  
		Last Modified: Wed, 05 Jun 2024 03:19:26 GMT  
		Size: 9.6 MB (9647519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48caf04b51039d20a911f9efc745490a66835c3edf5d07b2ea6ceaebf68d4f9`  
		Last Modified: Wed, 05 Jun 2024 03:19:25 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185919af6104d2c7e67fbb01136281d4c3a8e7b5074562374c18ff68e8cd721b`  
		Last Modified: Wed, 05 Jun 2024 03:19:25 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2238bfe1de4a9157d9c78fa6056539fb9b75f9471b67eb31c97e7711d01fbed`  
		Last Modified: Wed, 05 Jun 2024 03:19:25 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
