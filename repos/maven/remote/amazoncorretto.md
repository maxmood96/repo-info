## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:9e11d6243a43126be3418ef46622f2054f9718b7924991c57b4b1cf78552f610
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:72aabb68925c28f35b67221bb05961b16d98e99744bff1a7f2235fe34ff50a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.4 MB (361372281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af40c9cc1fb2952ac73749aa26233ffd5f33d8d2e3e365a17d2750ef6946209`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:13 GMT
ARG version=25.0.1.9-1
# Thu, 15 Jan 2026 22:10:13 GMT
ARG package_version=1
# Thu, 15 Jan 2026 22:10:13 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:10:13 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:10:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 16 Jan 2026 02:46:03 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 16 Jan 2026 02:46:03 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 02:46:03 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:46:03 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:46:03 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 02:46:03 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 02:46:03 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 02:46:03 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 02:46:03 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 02:46:03 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 02:46:03 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 02:46:03 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 02:46:03 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 02:46:03 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 02:46:03 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:08:12 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d88fe3c4b256f3e9e43b9cb5ec26a56a3f9a83b14d7daf8a3ab39250d61c86`  
		Last Modified: Thu, 15 Jan 2026 22:52:23 GMT  
		Size: 189.1 MB (189137832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea923b28e6c7e0c4e9a0cc09a8a38a8967f2bc23b55a1a7f50ea5fc2a9a6f776`  
		Last Modified: Fri, 16 Jan 2026 02:46:22 GMT  
		Size: 108.9 MB (108899957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1010d37e6a1923c3d3c11c2c66e8dc4d8f62a56c8a5452c3b7c1a00450ea851`  
		Last Modified: Fri, 16 Jan 2026 02:46:29 GMT  
		Size: 9.3 MB (9312247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d300ecc03bb77e34abe97f1e8be3689cc93ddb2619b7b03fcb649c591c86a7`  
		Last Modified: Fri, 16 Jan 2026 02:46:28 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d227e2eb56fcee253ae2e33dba28a1226a38f854496b9af71237e1206afb0f4`  
		Last Modified: Fri, 16 Jan 2026 02:46:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:8428410da98e56c3e34876d3ef6779037de2dc0a1312fbc57d869977de83eaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6226565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49583904154f0a58da826b93f4dafc0a8366db519226c779cd6f9e3ebc99bdca`

```dockerfile
```

-	Layers:
	-	`sha256:d570f94565c62f0b8b1678106bfaac0b6f49a40850f032c0a2b2ebfaad21a0f7`  
		Last Modified: Fri, 16 Jan 2026 03:28:19 GMT  
		Size: 6.2 MB (6209017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6c9ae84b71cad9fbdc424efdfb9c9d1deda8827cd86c5d75da720475cef356`  
		Last Modified: Fri, 16 Jan 2026 03:28:19 GMT  
		Size: 17.5 KB (17548 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c85eb7c23dd8f17975fe4431394bb6ba00f55a413fb8285462b528ad277a63f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.2 MB (357218490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd601aa2724fa884276aecccd0bc2f6063ee334494c3a6801b1f827dfd3bedf2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:20 GMT
ARG version=25.0.1.9-1
# Thu, 15 Jan 2026 22:10:20 GMT
ARG package_version=1
# Thu, 15 Jan 2026 22:10:20 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:10:20 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:10:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 16 Jan 2026 03:32:40 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 16 Jan 2026 03:32:40 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 03:32:40 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 03:32:40 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 03:32:40 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 03:32:40 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 03:32:40 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 03:32:40 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 03:32:40 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 03:32:40 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 03:32:40 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 03:32:40 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 03:32:40 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 03:32:40 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 03:32:40 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:25 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506418744a0e688a95c939f508921fc21e961eb25ec4bf5c8550b47aee8f9d3e`  
		Last Modified: Thu, 15 Jan 2026 22:52:34 GMT  
		Size: 187.1 MB (187059433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb31a3156a52ed895f20999d39f91dea43df423167c2f2ed43b6c9a703481a50`  
		Last Modified: Fri, 16 Jan 2026 03:33:25 GMT  
		Size: 107.9 MB (107931417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17cf080e434ebb6f3a178a7626aeda32a3037026364b45e36788d344800e60d`  
		Last Modified: Fri, 16 Jan 2026 03:32:58 GMT  
		Size: 9.3 MB (9312242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ee428f291da1f62bbccd2367fde0cddb6ef34dbc2feb900768c2efe3ec90ec`  
		Last Modified: Fri, 16 Jan 2026 03:32:57 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d89a83dd6a1b393f3e085eca63e473a8051f7afcecaa54fdf1818ae0110e25`  
		Last Modified: Fri, 16 Jan 2026 03:33:04 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:e89b849d853960965db05015fe7a5bde7ace4468638e5b18230627fb0fbea00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6225739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e121ace98b8ad832f7bcc86693fef402c1858efcf821a01f6e42ccf8f04b0b`

```dockerfile
```

-	Layers:
	-	`sha256:29bd783044efc970a39900361dce59bf6361bee56be583dea9cb3336d63afb46`  
		Last Modified: Fri, 16 Jan 2026 06:27:33 GMT  
		Size: 6.2 MB (6208009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de7f1c5b09e51f1d930f75634339816a1722dc2a3676ae2dca6548f84142af2`  
		Last Modified: Fri, 16 Jan 2026 06:27:34 GMT  
		Size: 17.7 KB (17730 bytes)  
		MIME: application/vnd.in-toto+json
