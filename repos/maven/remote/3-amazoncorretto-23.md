## `maven:3-amazoncorretto-23`

```console
$ docker pull maven@sha256:c8238d6f9a428f45c5a80e9a2550feb007b2ed3d96ce1f77390178948ed1323f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-23` - linux; amd64

```console
$ docker pull maven@sha256:84002abe94ac268e17b115a04314a49f4804a741a3f94b9640117d4c1b865c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303755585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354d0dba352712fb8b4fce6a3874af3cc54f036dd0ca5ee6b9217fdd2b27cee8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["/bin/bash"]
# Mon, 23 Sep 2024 17:02:08 GMT
ARG version=23.0.1.8-1
# Mon, 23 Sep 2024 17:02:08 GMT
ARG package_version=1
# Mon, 23 Sep 2024 17:02:08 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENV LANG=C.UTF-8
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Mon, 23 Sep 2024 17:02:08 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5acaf245b9570e79c1a7ee03a5dbc0f7b4aa375f3354879d41247976f76d0c4b`  
		Last Modified: Thu, 03 Oct 2024 20:23:24 GMT  
		Size: 52.3 MB (52325305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6329d9b869213ee0e8efcad26136d8b77d4824e5d21994c397d8eafec4726030`  
		Last Modified: Wed, 16 Oct 2024 17:57:54 GMT  
		Size: 177.5 MB (177490270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1eee6259e07698624d1ed65b62894ff2608f8620592fe6a43d94ce765e0d32f`  
		Last Modified: Wed, 16 Oct 2024 18:59:11 GMT  
		Size: 64.8 MB (64768536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ab9b81fa0d77716c0d9fe8e81fe901761603fa16310f29fcc303ef73ef486c`  
		Last Modified: Wed, 16 Oct 2024 18:59:09 GMT  
		Size: 9.2 MB (9170434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38600bda65580570c5642b62ef77a02c19156f6c5c6c59cb48b9db805f6ae810`  
		Last Modified: Wed, 16 Oct 2024 18:59:09 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ff1cb8d41c265bf21b1efff86221cf8b7acf10112f49decfaa236fe80a7731`  
		Last Modified: Wed, 16 Oct 2024 18:59:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23` - unknown; unknown

```console
$ docker pull maven@sha256:1db19290764fef0e99b4bbccf3c0a91e23e84ff6b84d637120d3d7d25f55c1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6209613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f8a6b6a0482256c74b6062eeb76ce2f8a17baa803ae7a2914796f261dc24e82`

```dockerfile
```

-	Layers:
	-	`sha256:f9e7f5bdf16450f7b0ffc6d911ddd30efe665bc7dfba756062c2e50478f695bf`  
		Last Modified: Wed, 16 Oct 2024 18:59:09 GMT  
		Size: 6.2 MB (6193303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:075024f058d4e369f5c4ef13b36d22198051b03b27f07568b5923b378a01426a`  
		Last Modified: Wed, 16 Oct 2024 18:59:09 GMT  
		Size: 16.3 KB (16310 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-23` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:468f3ad8c88ae40ad13da3f482629255f5f650e029acdccb4f089335b71910dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.7 MB (300652622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c081075b2b2aa8a7bd245891987c736a9a8dc1dda508a0a5477612c58ff9c16`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["/bin/bash"]
# Mon, 23 Sep 2024 17:02:08 GMT
ARG version=23.0.1.8-1
# Mon, 23 Sep 2024 17:02:08 GMT
ARG package_version=1
# Mon, 23 Sep 2024 17:02:08 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENV LANG=C.UTF-8
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Mon, 23 Sep 2024 17:02:08 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9e91bc818827f819b6de2c247e4fed5f971ec9990bc2b6330e067ca2f956815d`  
		Last Modified: Thu, 03 Oct 2024 17:46:58 GMT  
		Size: 51.4 MB (51426364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b39012886f509ba8d8b15f9a9fae7324e1b87b7f6f5344cc22388dca51a546f`  
		Last Modified: Wed, 16 Oct 2024 18:39:50 GMT  
		Size: 175.4 MB (175419552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699e7110ba896e2ef8daf41e3f7774eeb8146ef55ef48e4ab0e2edcaefcdf852`  
		Last Modified: Wed, 16 Oct 2024 20:20:13 GMT  
		Size: 64.6 MB (64635222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3406dbd1c6229e23a3811b08b74772ee3b2b307c884a6892a8b0302d0ef8091b`  
		Last Modified: Wed, 16 Oct 2024 20:20:12 GMT  
		Size: 9.2 MB (9170437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d658650a4c298dd940e69281a668c087ab6d7cb6e0fd0360511ab02ed1518423`  
		Last Modified: Wed, 16 Oct 2024 20:20:11 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef7319c064ca2635b7df5d37ed07b2fa2496c7342018e07f9893507fb57e227`  
		Last Modified: Wed, 16 Oct 2024 20:20:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23` - unknown; unknown

```console
$ docker pull maven@sha256:04a3c2708780214db61ecb446a809c5a3ed91b5cae6c9168a376896b3d9a5cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6207893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d624605feede53d879504446d9d62140222091d51736e8ab98c94e3d09418ed`

```dockerfile
```

-	Layers:
	-	`sha256:590689b2a7a987021bbd409ba66218622a5f927b13ff7d84d8798506003e68cd`  
		Last Modified: Wed, 16 Oct 2024 20:20:12 GMT  
		Size: 6.2 MB (6191420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61eeb1292ce58d83e7bb525c15f0f90c159ab2c306529cf593e05b813eb920ac`  
		Last Modified: Wed, 16 Oct 2024 20:20:11 GMT  
		Size: 16.5 KB (16473 bytes)  
		MIME: application/vnd.in-toto+json
