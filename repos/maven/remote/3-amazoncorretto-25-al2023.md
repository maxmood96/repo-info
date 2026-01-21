## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:725d9181b75d47ddcdfb3dab240043b12a1d9370aafb2a64a254cd3ccc786ccf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:aef30f09b1044a8e2916d62d337e1219231b6acefb241dcd4be815500deaa34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.4 MB (361372319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4ed72f1f7d75d7d8161e064c4981f8a1358fbf54e6466e822167588b0d1cce`
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
# Fri, 16 Jan 2026 02:46:17 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 16 Jan 2026 02:46:17 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 02:46:17 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:46:17 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:46:17 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 02:46:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 02:46:17 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 02:46:18 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 02:46:18 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 02:46:18 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 02:46:18 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 02:46:18 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 02:46:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 02:46:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 02:46:18 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:09:37 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d88fe3c4b256f3e9e43b9cb5ec26a56a3f9a83b14d7daf8a3ab39250d61c86`  
		Last Modified: Thu, 15 Jan 2026 22:52:23 GMT  
		Size: 189.1 MB (189137832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76433b2ed5646a0ec3700a629a89b609030af35c87aff44a98de4983b18ec5aa`  
		Last Modified: Fri, 16 Jan 2026 02:46:48 GMT  
		Size: 108.9 MB (108900000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ebb78d5b633280803eb6233298f7d53eef3b264de5b3d0e1a4a4d44f977a97`  
		Last Modified: Fri, 16 Jan 2026 02:46:56 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102837aaa2cef13acb28abd6225bc0ae07b262cde0aef736cda8d56913efe47a`  
		Last Modified: Fri, 16 Jan 2026 02:46:39 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5afddb26672c42763a41c386372d64cf9a760b9a418aa4fe4e1cbc6fa7cc06`  
		Last Modified: Fri, 16 Jan 2026 02:46:35 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:0eb462a82acef21fa2721b5a3fbb093b7ff90752ffb32b27c7d47e2e75619346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6224135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719e040493e11e036d5d55252e6171660f99f67b599bae2b253fe5c9d1b40628`

```dockerfile
```

-	Layers:
	-	`sha256:ea873ab6e3b4c405038f287cc24bfa662a7c195e0192176fbdcddc4a34e9e636`  
		Last Modified: Fri, 16 Jan 2026 03:29:37 GMT  
		Size: 6.2 MB (6207785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f6780aa8ab4c1e6f3a615296095dcc4ad087993d2b8e87d45b5ed5415a159f`  
		Last Modified: Fri, 16 Jan 2026 02:46:39 GMT  
		Size: 16.4 KB (16350 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c366a61be98c1f55ed04b00741cc708caafe375d8f2b61df1b391abe4078a3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.2 MB (357218560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4961f653310a0ab93a8ec9ed76d75ab8ae05a36a6ff59bac73891083acb27265`
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
# Fri, 16 Jan 2026 03:32:43 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 16 Jan 2026 03:32:43 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 03:32:43 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 03:32:43 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 03:32:43 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 03:32:43 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 03:32:43 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 03:32:43 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 03:32:43 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 03:32:43 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 03:32:43 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 03:32:43 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 03:32:43 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 03:32:43 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 03:32:43 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:36 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506418744a0e688a95c939f508921fc21e961eb25ec4bf5c8550b47aee8f9d3e`  
		Last Modified: Thu, 15 Jan 2026 22:10:46 GMT  
		Size: 187.1 MB (187059433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2a68a52fd66f6d2914b0093be80016c2ef74490b0be82320482d6c6783dfaa`  
		Last Modified: Fri, 16 Jan 2026 03:33:03 GMT  
		Size: 107.9 MB (107931478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c87a411c3b6192f4d02ab75b222b479541c085cdb5b706a4bc85b4bbba2a9f7`  
		Last Modified: Fri, 16 Jan 2026 03:33:00 GMT  
		Size: 9.3 MB (9312252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c5b4d6a2522bef592558e8d4fc29f8a44d8c6d56668c04ee5a139d12880ec9`  
		Last Modified: Fri, 16 Jan 2026 03:33:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609064a65cfbbaf1e34d9abe52b9669bc19f1c9ea37ed6c6ad44c3a5e58fe496`  
		Last Modified: Fri, 16 Jan 2026 03:33:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:60098abca6f1c95e65baa2efe2421990df27970a46bdb12947ae9ff043fd53e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a8b68d50df68ecde95fddd21cb2d81c7f796c7d55bb2ff61978305e5150947`

```dockerfile
```

-	Layers:
	-	`sha256:beb6e611d9f9739e12c062c1e7ca22366991c5ae8a7acf1464f9bfe4365d39e3`  
		Last Modified: Fri, 16 Jan 2026 06:28:50 GMT  
		Size: 6.2 MB (6206729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b04a95d103ed8c4424f342c2d443e390fda48203181d40aa9e8e09c33090192e`  
		Last Modified: Fri, 16 Jan 2026 06:28:51 GMT  
		Size: 16.5 KB (16483 bytes)  
		MIME: application/vnd.in-toto+json
