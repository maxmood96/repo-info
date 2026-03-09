## `maven:3-amazoncorretto`

```console
$ docker pull maven@sha256:4198fac7711f1ef8405baaa28fae7d363b4ef30ccee1a677b8e036f564ad98b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:af6a88b4da461121ecf572eedbfe8b87aeb0d232e29c6d3e37364c53dc322493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.9 MB (365864230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0831890e795f28c81b9a289272797afa356b0f0b9a784cd541b90b9614d1242`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:01 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:01 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:15:42 GMT
ARG version=25.0.2.10-1
# Mon, 02 Mar 2026 23:15:42 GMT
ARG package_version=1
# Mon, 02 Mar 2026 23:15:42 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:15:42 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:15:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 09 Mar 2026 19:14:25 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 09 Mar 2026 19:14:25 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:14:25 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:25 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:25 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:14:25 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:14:25 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:14:25 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:14:25 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:14:25 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:14:25 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:14:25 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:14:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:14:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:14:25 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2584a8e504dfaf493eadaafafbabd8b97f7cb5bbe3cb6a319fb37cf3c4335d86`  
		Last Modified: Thu, 19 Feb 2026 02:57:43 GMT  
		Size: 54.0 MB (54032840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bde93536aea729dc60831121cc5de0581f15b1e2767f2b7a4b932e58ca2b0d`  
		Last Modified: Mon, 02 Mar 2026 23:16:07 GMT  
		Size: 189.2 MB (189186090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76983481fb71a4555d82e8243b6810f7e4c0784a1c1a5d1220bbc0e80ae8d14`  
		Last Modified: Mon, 09 Mar 2026 19:14:44 GMT  
		Size: 112.9 MB (112946736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471ec7ec85befd60fe2b8ed2dcb7e2727d081f43aa25fcf28d9dd4b4d840f4a8`  
		Last Modified: Mon, 09 Mar 2026 19:14:42 GMT  
		Size: 9.7 MB (9697521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a5cf1f4391563a1c135215f52ca30516090180c8701f3939d49a44d704cfaf`  
		Last Modified: Mon, 09 Mar 2026 19:14:41 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a62df827a31e4ec0227bf0ba6696a815b05346046c0d9bc8e12d57fbf183ff`  
		Last Modified: Mon, 09 Mar 2026 19:14:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:4d966eb1c5db3082c03c28563034b2c191a5e254c193d914b5d65c2acf2ea1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6233123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c10d2cdb686eaad5da612863bccd2dbceb7cf10acbb19a6b95d7713b36e15dc`

```dockerfile
```

-	Layers:
	-	`sha256:a981f9c67c4782581c3e68c1100d53f62677ee9037984d8de74dca9003ba8906`  
		Last Modified: Mon, 09 Mar 2026 19:14:41 GMT  
		Size: 6.2 MB (6215574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f74069f841071591e1eaced48c38f62737cead680e4db750026d8581b18aeaf7`  
		Last Modified: Mon, 09 Mar 2026 19:14:41 GMT  
		Size: 17.5 KB (17549 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:0567dd8fd7fd196e224cbf4571b6d715795ee8c5126843568e6d8b0fc822be41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.7 MB (361670071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a952adda44b102e9738628c3e459a5c506baa3facd54f52227aad244c8bf6a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:04 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:15:32 GMT
ARG version=25.0.2.10-1
# Mon, 02 Mar 2026 23:15:32 GMT
ARG package_version=1
# Mon, 02 Mar 2026 23:15:32 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:15:32 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:15:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 09 Mar 2026 19:14:22 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 09 Mar 2026 19:14:22 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:14:22 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:22 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:22 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:14:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:14:22 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:14:22 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:14:22 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:14:22 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:14:22 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:14:22 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:14:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:14:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:14:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9330fae67a20d9aa2569828674140d8b67d50cfd127cb99ba0f9be275d35f976`  
		Last Modified: Thu, 19 Feb 2026 02:57:42 GMT  
		Size: 52.9 MB (52941319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67cff3cdc82a1cc3dfd577220fec650c7345cfda2ba30437cb1b29e26e1b2fe`  
		Last Modified: Mon, 02 Mar 2026 23:15:58 GMT  
		Size: 187.1 MB (187088252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef65d901fc85327fd9e40d417712624bfaf950ef1754ff0e8e03fb78df3624a`  
		Last Modified: Mon, 09 Mar 2026 19:14:42 GMT  
		Size: 111.9 MB (111941901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01292db7664688491de79c4d1ab658409d9668d5bb041ff72f04cdb9a9f2b4d`  
		Last Modified: Mon, 09 Mar 2026 19:14:40 GMT  
		Size: 9.7 MB (9697557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ed519a3d2145e9639e3a41802d052f48a81254e8941570d982477bfa065be7`  
		Last Modified: Mon, 09 Mar 2026 19:14:39 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d83eb70acc58897ab4dcc8015287c7be92f0ca00b3f766235ef69ea8fbd8b3`  
		Last Modified: Mon, 09 Mar 2026 19:14:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:0be26109a737e0b6dba981183b87e330dae6087355b0fece6473870b1fc2f4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6232296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:debf650890a3a307f146e704980266eb5ed81e995f929cb20f3344c0f298efe0`

```dockerfile
```

-	Layers:
	-	`sha256:28d0e558bd239b43a71b4e0cd4d4eccd8e7abf3c2c47805d27315d5db52aab54`  
		Last Modified: Mon, 09 Mar 2026 19:14:39 GMT  
		Size: 6.2 MB (6214566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ef1530ece8b2a347d817e28b8a7eb8c62f14f6b76a596808efb6620ba070b0`  
		Last Modified: Mon, 09 Mar 2026 19:14:39 GMT  
		Size: 17.7 KB (17730 bytes)  
		MIME: application/vnd.in-toto+json
