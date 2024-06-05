## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:c4defab5d8c3146e8a8001e071e47012e470abe938804ee9d3fc09e302202db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:6783c5992abb070ede61b1520787757f115b054fc6ddc6905b2a69fed52f75a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267669618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b5f2b035d3695534e71be81494f1fdba65c66d3db575088adaf5447568c223`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 05 Jun 2024 00:26:32 GMT
COPY dir:7cf66bb9a4300419df5b669628ccf58a30d02fe56dd9811e6baaca920acf962f in / 
# Wed, 05 Jun 2024 00:26:32 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:41:42 GMT
ARG version=17.0.11.9-1
# Wed, 05 Jun 2024 02:41:42 GMT
ARG package_version=1
# Wed, 05 Jun 2024 02:42:04 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 05 Jun 2024 02:42:05 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:42:05 GMT
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
	-	`sha256:f6175f9c503b77e6cec852666a7133ed71ff16fd23342bcc58c01fa48948b06f`  
		Last Modified: Tue, 28 May 2024 21:59:02 GMT  
		Size: 52.3 MB (52320215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22dd896ed7d28c385ae9990cb9808e5a5e852c3bf0c414cddb8ba10cf17f1424`  
		Last Modified: Wed, 05 Jun 2024 02:54:55 GMT  
		Size: 157.0 MB (157044297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fef72005f972aadb2dbe1ecf646147d523287a3ce987ebdd00b48092df2663a`  
		Last Modified: Wed, 05 Jun 2024 04:25:01 GMT  
		Size: 48.7 MB (48656200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3da9616cac336be7e6bef4a3ec244d92375c628e963eb38fbc2c2dad660bd6a`  
		Last Modified: Wed, 05 Jun 2024 04:24:58 GMT  
		Size: 9.6 MB (9647526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a8940e101dbe30e6ea437e4917e8621328529c4f15c917041e5beecda79a76`  
		Last Modified: Wed, 05 Jun 2024 04:24:57 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543c64ba6832ffb8c8d6998858633e2f16655bceb8c1f29ce6aa05603259f695`  
		Last Modified: Wed, 05 Jun 2024 04:24:57 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec00a9bda03ed5a990cd02bd4bd8e04a17a44e8271b120fd601bf717053bc0e5`  
		Last Modified: Wed, 05 Jun 2024 04:24:57 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:8a250bee20d8b35a56b9015bf09e521feb18af861ccf9f2449490badedd5c01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.1 MB (265083027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8d347f300217a5ebfb6c263482830489ef0219c829cb07a859a4737214794c`
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
