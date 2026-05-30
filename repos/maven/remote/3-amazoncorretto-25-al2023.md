## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:52bed70e00f53674731cc94dcd42db372383921d0e76b45b6385737716388c8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:2e855b9b90c53bac6721d0798d0d5686c2725136050adf9af9023cc0e545b4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384460810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c196ed8028d8148e7a68d34c1e613df47dab96fdc0693d8179bec64970eabed`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 30 May 2026 00:26:56 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:26:56 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:51 GMT
ARG version=25.0.3.9-1
# Sat, 30 May 2026 01:12:51 GMT
ARG package_version=1
# Sat, 30 May 2026 01:12:51 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:12:51 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Sat, 30 May 2026 02:15:13 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Sat, 30 May 2026 02:15:13 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 30 May 2026 02:15:13 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 30 May 2026 02:15:13 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 30 May 2026 02:15:13 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 30 May 2026 02:15:13 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 30 May 2026 02:15:13 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 30 May 2026 02:15:13 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 30 May 2026 02:15:13 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 30 May 2026 02:15:13 GMT
ARG USER_HOME_DIR=/root
# Sat, 30 May 2026 02:15:13 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 30 May 2026 02:15:13 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 30 May 2026 02:15:13 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ba643eb28fc9c4131e00c61b5afb90ae7a75af1859c82faa13932360f5c05d`  
		Last Modified: Sat, 30 May 2026 01:13:15 GMT  
		Size: 189.4 MB (189412862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73be21fc4480dc4568c02f56873986a985a2b0e5b8897778a3743a5f2dfc546`  
		Last Modified: Sat, 30 May 2026 02:15:32 GMT  
		Size: 131.1 MB (131115800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284e0b6fe4b260d32a8c7e4be7e21fd64bf168dcc53315252a06c92f3d67c346`  
		Last Modified: Sat, 30 May 2026 02:15:28 GMT  
		Size: 9.4 MB (9359981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba80601bc36526eb14709ecd1ce125d22eb205659cf86e46917861b144e6bdfe`  
		Last Modified: Sat, 30 May 2026 02:15:29 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f97a0df13c7859622c22bb0e3caed2a6ec1d4c907f5f4c1aeb5dc0311f1c92f`  
		Last Modified: Sat, 30 May 2026 02:15:28 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:4b8eca2b3d80dfbd07419cdb9fcc18194461d395a00975abfd207187b2f3c80d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6229544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0355344a3b11b541764b9104adcd3059af9ec9088ba43dcf96f5cdb0851a76f0`

```dockerfile
```

-	Layers:
	-	`sha256:7a6427da529e46cb45e34fe1c388890069f287d968e86c2a0a266a9b47a3c3c5`  
		Last Modified: Sat, 30 May 2026 02:15:30 GMT  
		Size: 6.2 MB (6215039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa07c0a631707d6bf8e96bd5fd9ed1ca4c00e4b602786c55dae0cdc1c58c68d0`  
		Last Modified: Sat, 30 May 2026 02:15:29 GMT  
		Size: 14.5 KB (14505 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c6d9a4d34eb785474597699afe53bf6c41704b0c974861364aec4fe0f5daae44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 MB (380179073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dabcec4bf9fec2977313d096a12a0fb7c776a0987839f9af19ccfefa193fe93d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 30 May 2026 00:29:22 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:22 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:37 GMT
ARG version=25.0.3.9-1
# Sat, 30 May 2026 01:12:37 GMT
ARG package_version=1
# Sat, 30 May 2026 01:12:37 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:12:37 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Sat, 30 May 2026 02:15:08 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Sat, 30 May 2026 02:15:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 30 May 2026 02:15:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 30 May 2026 02:15:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 30 May 2026 02:15:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 30 May 2026 02:15:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 30 May 2026 02:15:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 30 May 2026 02:15:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 30 May 2026 02:15:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 30 May 2026 02:15:08 GMT
ARG USER_HOME_DIR=/root
# Sat, 30 May 2026 02:15:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 30 May 2026 02:15:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 30 May 2026 02:15:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e414a9bc884c1212e04d64b8c9b4918d7362ecf315931f7c7483992d4894a4`  
		Last Modified: Sat, 30 May 2026 01:13:03 GMT  
		Size: 187.3 MB (187327339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a2becf55c912ffb5427ad808fae45de4dff97d2a01bb9d84e8d6cad59ebaf8`  
		Last Modified: Sat, 30 May 2026 02:15:29 GMT  
		Size: 130.0 MB (130032921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4001964c68aa6fe5a255334233033b117c7788ced39ee8907c3a52d6204c3ee6`  
		Last Modified: Sat, 30 May 2026 02:15:25 GMT  
		Size: 9.4 MB (9359977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537b503a7bd17bca330d526eb4b1384cc2eb39338876a23587ac37f45801c15d`  
		Last Modified: Sat, 30 May 2026 02:15:25 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae26f6be3ff98f8304308438320b20d43d539c183e62786672fbdb1e224072d`  
		Last Modified: Sat, 30 May 2026 02:15:25 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:1ca4490bfd0cb3b6f8010875749e811018360fb07621fa316fd0b1b5d43cd8c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6228623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809d8bacf10e2eb70900e3ff65ecfceaa4d9ee0bef51ac3f1a815cab3bfb9526`

```dockerfile
```

-	Layers:
	-	`sha256:4dadff2b7e0af3fc54d48fb5cd8ed9735fd15e77fe10418c4404d74443eeacc2`  
		Last Modified: Sat, 30 May 2026 02:15:25 GMT  
		Size: 6.2 MB (6213984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:708a9f78fff1a5c4c75f114756d59c1381d250a8f324ab1b6357c4a6ee8db159`  
		Last Modified: Sat, 30 May 2026 02:15:25 GMT  
		Size: 14.6 KB (14639 bytes)  
		MIME: application/vnd.in-toto+json
