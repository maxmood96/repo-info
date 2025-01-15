## `maven:3-amazoncorretto-21-al2023`

```console
$ docker pull maven@sha256:dbc6ebc3ba4b41f143b4852c2fff60f136aa0c7dcd48578a1953d3b5b393d239
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-al2023` - linux; amd64

```console
$ docker pull maven@sha256:4bd73dbfc3d25dde7428fefd2cb5fd8fc78b7752a05f619b784fa3180140db57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304647416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1d66a05d5955687fb6ad6b836fe12946a3613a1728c28ffe41f2883276918a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=21.0.5.11-1
# Tue, 20 Aug 2024 18:12:59 GMT
ARG package_version=1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d449a9cb20bfb0f76c698e4adb686874f9bd35779c1f8f9d76c5528c87b3366`  
		Last Modified: Wed, 15 Jan 2025 00:43:54 GMT  
		Size: 53.2 MB (53156717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0935d07db385bcf4c735d0e17e6b028cd7884f220b7f97dca09143d9a916b6c3`  
		Last Modified: Wed, 15 Jan 2025 18:31:19 GMT  
		Size: 169.8 MB (169756607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26c5a76fe048d57b9e50038e9984b687c685b511179fe649a14adf80b7bf02d`  
		Last Modified: Wed, 15 Jan 2025 19:10:08 GMT  
		Size: 60.0 MB (60016735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e3b7436e6721ed1475a34e1766c837aa895a17151c5b2c3d3081d90a086e54`  
		Last Modified: Wed, 15 Jan 2025 19:10:08 GMT  
		Size: 12.5 MB (12545873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73e034d2c139925e4fc0f7bb171feb6d3ec712d633828847ffb82d510c7f1a5`  
		Last Modified: Wed, 15 Jan 2025 19:10:07 GMT  
		Size: 9.2 MB (9170442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f007d36f7bff620d9cff1d27f0fd7c5b4696f4f76d25a6d9b82ed877559615`  
		Last Modified: Wed, 15 Jan 2025 19:10:07 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc55371ee6b956c44ed01ec5d92efa5d4d66b8c709d30006f61be7de316ec8a`  
		Last Modified: Wed, 15 Jan 2025 19:10:08 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:313c1a36e7ba0c3e11a7ea77f74c95926d79482f2dbae173b3bd6298ca7dfa0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6244206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2807a43a585dd1a7e3cd1f19a4a2abc28b184f7e585ae3fb35439780d6912131`

```dockerfile
```

-	Layers:
	-	`sha256:ebc37fcb8abd7a6108380cb75a3357db2512c96e460990d9037e4fd1e8b4f87c`  
		Last Modified: Wed, 15 Jan 2025 19:10:07 GMT  
		Size: 6.2 MB (6225889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8a651ef9f1a46b0f3045188ccf2b4938962d64bb89ff1c3bb6efa43e7d630a6`  
		Last Modified: Wed, 15 Jan 2025 19:10:07 GMT  
		Size: 18.3 KB (18317 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4164fd997928d25e69601829195f61bbcf943e9013543642cf60b8e8317fa0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301793060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bfdf558e2d2694941467ac65855fc4b0ffa9fb141c2ca72e8d0044927c0b34`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=21.0.5.11-1
# Tue, 20 Aug 2024 18:12:59 GMT
ARG package_version=1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2dc99809e33185161e199db0b479b51cf3fb7470fd27c484aff50bdf9dcb5dab`  
		Last Modified: Fri, 10 Jan 2025 02:14:49 GMT  
		Size: 52.3 MB (52268196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a297a5d72dd49a15c56e5a72c17cf3f44a4ed5a13982c2330dbf14c76ca3bcad`  
		Last Modified: Sat, 11 Jan 2025 03:10:22 GMT  
		Size: 168.0 MB (167978893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19012e549742c9e2da1604cffc45b221c8b52c490b915f6aaaef17c48f301430`  
		Last Modified: Sat, 11 Jan 2025 04:17:28 GMT  
		Size: 59.6 MB (59565198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e7fc1522a95d1396290f44091779c2a84001751d1b401fa10034a7d31286c5`  
		Last Modified: Sat, 11 Jan 2025 04:17:27 GMT  
		Size: 12.8 MB (12809301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6e45a94a5105a2c1a60f027e22b81b98ba832006a2626c38e51e186d8bd5da`  
		Last Modified: Sat, 11 Jan 2025 04:17:27 GMT  
		Size: 9.2 MB (9170426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab5220f15aac97540939d9c4f48d90d6a1af6d596bed2d914a86d38770f456f`  
		Last Modified: Sat, 11 Jan 2025 04:17:26 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e9e61022431d6907a9708b604e7dd0b3dabd030e14b759fba43edea6617bb0`  
		Last Modified: Sat, 11 Jan 2025 04:17:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:e81b26f788566fccec49a054d3e5bc6b9b2c226fdaf4b5b988693917081ebbce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6243286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a9f6a5574d8e9dcb969d657ef00b435c321c2c739c8a0347f78f24b76854a2`

```dockerfile
```

-	Layers:
	-	`sha256:d4b4613678951049d81fae916de66557faf86f2adc1db31317e2559a3aad0d27`  
		Last Modified: Sat, 11 Jan 2025 04:17:27 GMT  
		Size: 6.2 MB (6224822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b88b213c46ae4d4150de152a879af9be1f5c600e4b6f2b09a7de6139b7494540`  
		Last Modified: Sat, 11 Jan 2025 04:17:26 GMT  
		Size: 18.5 KB (18464 bytes)  
		MIME: application/vnd.in-toto+json
