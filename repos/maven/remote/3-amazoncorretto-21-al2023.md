## `maven:3-amazoncorretto-21-al2023`

```console
$ docker pull maven@sha256:f0c16b62d6d2d26aaccc97239ad3fcef57ad439f86050508bec26f5194e84a23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-al2023` - linux; amd64

```console
$ docker pull maven@sha256:5aec1dd4cddc3b0f18fd5b30374b8a94ee8141c00bfa8de3702a22633ab3fad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368223327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb777919364b8abdb19eacf5d7711e7521c08cad18ff1258742db4dfc6c7427`
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
# Sat, 30 May 2026 02:14:42 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Sat, 30 May 2026 02:14:44 GMT
RUN yum install -y openssh-clients # buildkit
# Sat, 30 May 2026 02:14:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 30 May 2026 02:14:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 30 May 2026 02:14:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 30 May 2026 02:14:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 30 May 2026 02:14:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 30 May 2026 02:14:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 30 May 2026 02:14:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 30 May 2026 02:14:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 30 May 2026 02:14:44 GMT
ARG USER_HOME_DIR=/root
# Sat, 30 May 2026 02:14:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 30 May 2026 02:14:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 30 May 2026 02:14:44 GMT
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
	-	`sha256:d557ec54a5fd169c54bc874fe07dcf6c80b76aaba6bf59d1f615778d3f25616b`  
		Last Modified: Sat, 30 May 2026 02:15:03 GMT  
		Size: 121.3 MB (121313821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834a6d48bc8465ea7707ac4e4b0f3ee5a658fba78c582286139b4cddf9051473`  
		Last Modified: Sat, 30 May 2026 02:15:00 GMT  
		Size: 12.5 MB (12532021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1069525c09b762877bad24097062798752ac4213476d2bdc4ab4c61aa2a31d7c`  
		Last Modified: Sat, 30 May 2026 02:15:00 GMT  
		Size: 9.4 MB (9359967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b55f465cd62f7bd63c74c86385d3238b67bf2aaf3fd4e6bb7ce494ad9136c3`  
		Last Modified: Sat, 30 May 2026 02:14:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d308acfe364dba0ed5106f8e61689b0fc362bad8cb3c504e08cc8d68354fa2c5`  
		Last Modified: Sat, 30 May 2026 02:15:01 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:33f03de1d2d38e247ef7ae156f14658672ec6699231855d62251d2cf28a3a2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6258004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea1ad017f5a29ba1367c1af4eee705006700f7a97d0da6d13df8680c6e1f7b3`

```dockerfile
```

-	Layers:
	-	`sha256:4939df5c0047e1431dcc030951c89086df1904a90c7ca2c707e4b9190afc3f00`  
		Last Modified: Sat, 30 May 2026 02:15:00 GMT  
		Size: 6.2 MB (6241715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d35fdb1620568a000b9509d5e2866f511c3a9b0a959adfc5b3f1e8200876fd4c`  
		Last Modified: Sat, 30 May 2026 02:14:59 GMT  
		Size: 16.3 KB (16289 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:205712764b442186ea05da87925e12a9ffe68d2c439ed23a2a0bbd2bb7025681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.3 MB (364272949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84003861e94ec2a80c186b523f4c765090b81421c137bf7aeb764bbc2dfdedfb`
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
# Sat, 30 May 2026 02:14:32 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Sat, 30 May 2026 02:14:33 GMT
RUN yum install -y openssh-clients # buildkit
# Sat, 30 May 2026 02:14:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 30 May 2026 02:14:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 30 May 2026 02:14:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 30 May 2026 02:14:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 30 May 2026 02:14:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 30 May 2026 02:14:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 30 May 2026 02:14:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 30 May 2026 02:14:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 30 May 2026 02:14:34 GMT
ARG USER_HOME_DIR=/root
# Sat, 30 May 2026 02:14:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 30 May 2026 02:14:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 30 May 2026 02:14:34 GMT
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
	-	`sha256:c43e90de91ada36c665c8a59681f4873d71550c80843f5b55e85e9a0fd7f0c66`  
		Last Modified: Sat, 30 May 2026 02:14:53 GMT  
		Size: 120.0 MB (119950241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50a07e43278e07e4fe1a1cc576d7c2a47e72e60709aa692988952ab41db9096`  
		Last Modified: Sat, 30 May 2026 02:14:50 GMT  
		Size: 12.8 MB (12782990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbfeaf2c46e550170219e16e195a6770f305dfa7678bd8b8e2f76739b66c7b7`  
		Last Modified: Sat, 30 May 2026 02:14:49 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11ecf1b77adc6773533b15df528d6466d793e872008c4010ce46d4a2c675eb8`  
		Last Modified: Sat, 30 May 2026 02:14:49 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd0fc725c7d9e42057c7a7636575121bf03305e1c136e4b3e53ec98a038fdc2`  
		Last Modified: Sat, 30 May 2026 02:14:50 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:7db46fbd025aecc66d39267ef3ce92801084013736cb4fe5eaa18d30497a8bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6257085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353f15e2ab4777a9d53019c0aaf7db03da07a1a4e8a50f59705818ef37c337a8`

```dockerfile
```

-	Layers:
	-	`sha256:6e14a4795861e5846f3d93123488fb545bdcf78d67f956373baf593c9fd23855`  
		Last Modified: Sat, 30 May 2026 02:14:49 GMT  
		Size: 6.2 MB (6240649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:121e8ae8fbd6ee16c27ac10f3de7dec8dc0ab73f03e85fdd2e0b36e6a50de6e8`  
		Last Modified: Sat, 30 May 2026 02:14:49 GMT  
		Size: 16.4 KB (16436 bytes)  
		MIME: application/vnd.in-toto+json
