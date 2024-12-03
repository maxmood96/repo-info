## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:91373ab3577e75eb737d2bf5d37a428023207bc3e1f222e61d4b4f99206043e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:66ba91a8ec2aa45944dd8f37eb4cb06fa3ef257bc100afa05f1782f7e8c2bb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288845069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d76050b009c9006bee389fd98a2f5f29fe5668245db47d9ca19c7daa9cbb76`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.13.11-1
# Tue, 20 Aug 2024 18:12:59 GMT
ARG package_version=1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:4a665eb63bc8cddb90e1e74e3ec745a1bab733c919dc4b2d648b43459295464a`  
		Last Modified: Sat, 23 Nov 2024 01:38:06 GMT  
		Size: 52.4 MB (52377532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7b7b0b3977758d91493f98bedfe248b3374bb1cd3b93a7b84673eaf885f0cf`  
		Last Modified: Mon, 02 Dec 2024 23:23:31 GMT  
		Size: 156.5 MB (156452988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3952ebbdf54a04ecef950ec6501fa9c9f8613606938e07733e9c9a4897ff2043`  
		Last Modified: Tue, 03 Dec 2024 04:33:38 GMT  
		Size: 58.3 MB (58299711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d45cf60eadbac690dd87f6749bfe52809c91d72d40cc33f8dca043745e92eb8`  
		Last Modified: Tue, 03 Dec 2024 04:33:37 GMT  
		Size: 12.5 MB (12543359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155e60a81f0c541aafb583b0ee789d6502a98fa65c55f40fbe0eeb037296e957`  
		Last Modified: Tue, 03 Dec 2024 04:33:37 GMT  
		Size: 9.2 MB (9170440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59bb4fda07cbb589c6a1d47d2f0bac1e8bb89dfbfcc726698921c7c440dbdd6`  
		Last Modified: Tue, 03 Dec 2024 04:33:37 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2d0c8a794bc6ee7648f04271e951b12341be3c1aa1ad9f3ed1e816c944034a`  
		Last Modified: Tue, 03 Dec 2024 04:33:38 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:616e84b6e981bff2ce8815f80ff9a02b8c8e6be13c3c83ac09c8232078ea4f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218ac5ada692fe48c04f346f6f8aafa5117a21dbf4422343dcbfed5cd4dc0329`

```dockerfile
```

-	Layers:
	-	`sha256:778172f81894279e93fdbdf62bc57ff2af43be822a7fa9df9f53b25de4f690fa`  
		Last Modified: Tue, 03 Dec 2024 04:33:37 GMT  
		Size: 6.2 MB (6231994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fdbf719a98ec34d4e01bded8520b54ea716013e156e7ec91067fcb986aaa8e6`  
		Last Modified: Tue, 03 Dec 2024 04:33:37 GMT  
		Size: 18.3 KB (18317 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:8005588fd74449d43b6e7fda26b67461ca1c0dba3270a8ae0a8b7e3f862568dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286480629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e1feb8c2806a8de1a64195178348d4d235b1f3dcf02a9caed07078d1419725`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.13.11-1
# Tue, 20 Aug 2024 18:12:59 GMT
ARG package_version=1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:aa4cd91a180503f7c5ac34b85fdd22c27356599a1d700f978c6d2fa5858867fd`  
		Last Modified: Fri, 15 Nov 2024 02:20:08 GMT  
		Size: 51.5 MB (51456561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761998b03c3af02384f348b6aa4ba3c4c3baedacf29f61695f06b5ce94d52b38`  
		Last Modified: Sat, 16 Nov 2024 00:59:23 GMT  
		Size: 155.3 MB (155267071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbfd16c503a111e478239c79ccd9c77c6d95277855a5952acfa28d2c339cbc5`  
		Last Modified: Sat, 16 Nov 2024 07:47:46 GMT  
		Size: 57.8 MB (57774863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2208744e094c99896d0fdbe8cca25e81114ea4772ef01764fbfdb8e99b6b98`  
		Last Modified: Sat, 16 Nov 2024 07:47:44 GMT  
		Size: 12.8 MB (12810657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542fa4e1d32bd7562b41415bc01edb00ecbb1819917824dc5a9f54c69ee3fc6a`  
		Last Modified: Sat, 16 Nov 2024 07:47:44 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925229f5463f92ed53237a086997c5897678ba0abf03c97943bc2d5ffd7cb798`  
		Last Modified: Sat, 16 Nov 2024 07:47:44 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6770427d9eaa7b8eeda08d67ba358735dfb6cf9cd6357d6fa269c659f174367`  
		Last Modified: Sat, 16 Nov 2024 07:47:45 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:07ec7156e17ced5db87adfd32807238fc494be67666b9865526497683c201f4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6249387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da74668286171e3521e25f4d34f3c213d1e4964062ccba6b9c374e99819806eb`

```dockerfile
```

-	Layers:
	-	`sha256:5361a0c726dcecf94f2da2eb8be92cd2297b6ef3f7a207c90f59b46257fd2f5e`  
		Last Modified: Sat, 16 Nov 2024 07:47:44 GMT  
		Size: 6.2 MB (6230922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6f96ea729f87e399b66a1c9528e47d345e720873b50d57d62f6aaa0888bcff1`  
		Last Modified: Sat, 16 Nov 2024 07:47:44 GMT  
		Size: 18.5 KB (18465 bytes)  
		MIME: application/vnd.in-toto+json
