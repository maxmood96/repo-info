## `maven:3-amazoncorretto-21-al2023`

```console
$ docker pull maven@sha256:48cfd78a17486fa64a3a5bcfc07a88865357a40a86a6af38eb43cd15d3f4fc39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-al2023` - linux; amd64

```console
$ docker pull maven@sha256:2a50f4a06637d66b3f51a45daff48823a04bebf897831b85a73d29224fe27b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368223615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b078acbe58b2b8c99e4ca425c70186c7aea55b38dd79f80aa63398a16201521f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 30 May 2026 00:26:56 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:26:56 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:35 GMT
ARG version=21.0.11.10-1
# Sat, 30 May 2026 01:12:35 GMT
ARG package_version=1
# Sat, 30 May 2026 01:12:35 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:12:35 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 02 Jun 2026 10:25:51 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 02 Jun 2026 10:25:53 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 02 Jun 2026 10:25:53 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:25:53 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:25:53 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:25:53 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:25:53 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:25:53 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:25:53 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:25:53 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:25:53 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:25:53 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:25:53 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:25:53 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db7dbf77d75a1d867303ddfdf705632d5d5183a6231cbe658f5890116446ada`  
		Last Modified: Sat, 30 May 2026 01:12:56 GMT  
		Size: 170.4 MB (170445354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165c079b453b8a452c33f594c486179cce54ab27342c1a4e8590d37dd5bbb4ae`  
		Last Modified: Tue, 02 Jun 2026 10:26:14 GMT  
		Size: 121.3 MB (121313992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ab1149a03c1b5971e6d725d8b75a3c9d8f681ebde151b5df37d0efc2707188`  
		Last Modified: Tue, 02 Jun 2026 10:26:10 GMT  
		Size: 12.5 MB (12532147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5374ce4a7063a0e6c3498e03e11b850597560163bdd0bd4050d4e535e2eed7d9`  
		Last Modified: Tue, 02 Jun 2026 10:26:10 GMT  
		Size: 9.4 MB (9359958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7bfed47b71051705655777112aa378059ac3ca21f4ffaeee6346298fcea5bd`  
		Last Modified: Tue, 02 Jun 2026 10:26:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a5b88d7ac2d5ab3e49fd7c9a4fd27f78d75a083067ab5ea259da2d47974c69`  
		Last Modified: Tue, 02 Jun 2026 10:26:11 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:d021b5531d6d5e67e7817490333435908bc4199ce6e816637f8378648bc31082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6258004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dc464c19137636014cdfe847a9e9f7a418fef3fa09d24a1dd0a683d6f2629a`

```dockerfile
```

-	Layers:
	-	`sha256:4a0f64fed552a491fe9fefef57b6e8d1f225dcab9582dcbc48b7facc8f8df895`  
		Last Modified: Tue, 02 Jun 2026 10:26:10 GMT  
		Size: 6.2 MB (6241715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d859eb37774848c4714bae3da2eda61bf9b13dc41e3e3399333d930bd54515a8`  
		Last Modified: Tue, 02 Jun 2026 10:26:09 GMT  
		Size: 16.3 KB (16289 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f5598392f4c198e4ce84bc3d682cd10bd46215989b65d5043b2ee2dfd2044627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.3 MB (364273079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4088f25080da87082fb213297c5bfa2d6d6dc512aa9b9341e42d328970e9af6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 30 May 2026 00:29:22 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:22 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:28 GMT
ARG version=21.0.11.10-1
# Sat, 30 May 2026 01:12:28 GMT
ARG package_version=1
# Sat, 30 May 2026 01:12:28 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:12:28 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 02 Jun 2026 10:23:09 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 02 Jun 2026 10:23:11 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 02 Jun 2026 10:23:11 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:23:11 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:23:11 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:23:11 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:23:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:23:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:23:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:23:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:23:11 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:23:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:23:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:23:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae6dcf128c8239e095d4cadda037b6a5b5c267ad60f46b5b8fa317ff773db55`  
		Last Modified: Sat, 30 May 2026 01:12:53 GMT  
		Size: 168.7 MB (168720905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45adf8bbb930300f6fba9cd1f85041b6eac6e4746d2f3db436d88331598daab9`  
		Last Modified: Tue, 02 Jun 2026 10:23:32 GMT  
		Size: 120.0 MB (119950316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b18ce7801e3f4510e77cb3169efb7b6e6663199edc327f05321ba19d45d749`  
		Last Modified: Tue, 02 Jun 2026 10:23:27 GMT  
		Size: 12.8 MB (12783059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de285a2c02944da8f0367e08c6b02b02f6d2f28109eaee622daf9339ff7726f8`  
		Last Modified: Tue, 02 Jun 2026 10:23:26 GMT  
		Size: 9.4 MB (9359962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45c80512f6485b03b86d730e712492ac4223e54746b400392e85405e01c4c5b`  
		Last Modified: Tue, 02 Jun 2026 10:23:26 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6918e37ff7d7410b76e5698d3da6669781bd019d707bcf0d45e7043296f8e40b`  
		Last Modified: Tue, 02 Jun 2026 10:23:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:486417b451341fb8d16c06b9e74587ca7b21cc060a4800a33c189604dcb71209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6257086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf425aec3849eff2cd642e327fef7cc7e8eb6d5ac83f4da4f9aec7e0bac666c`

```dockerfile
```

-	Layers:
	-	`sha256:ea81e09e87b54baeba6e57b7f705789e49b954dfd83a1931f6bb8efd0f41b452`  
		Last Modified: Tue, 02 Jun 2026 10:23:26 GMT  
		Size: 6.2 MB (6240649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:122e2fb00cb83b7cb31c084e204bdaf4a12d5adbc6138ec262fceb88596a84d4`  
		Last Modified: Tue, 02 Jun 2026 10:23:26 GMT  
		Size: 16.4 KB (16437 bytes)  
		MIME: application/vnd.in-toto+json
