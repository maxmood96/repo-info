## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:9688db93f403b629623d86168693cc8f35b4d5a69119ff07c0fdab1ecb1be404
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:d5d1c19f52541b6f9b345dae59691abaf8eceffdd0b0f103cefc7c32fa6062d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.9 MB (365864454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a64ebf2b3bbbfb8ee7a01c1f692fc3f7036fb88dce2bee0b6e58445ea778781`
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
# Mon, 09 Mar 2026 19:14:36 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 09 Mar 2026 19:14:36 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:14:36 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:36 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:36 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:14:36 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:14:36 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:14:36 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:14:36 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:14:36 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:14:36 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:14:36 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:14:36 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:14:36 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:14:36 GMT
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
	-	`sha256:7849487219dde225cf6e98e1d17758ee11c8ee484e9ce737082c578cb5da5167`  
		Last Modified: Mon, 09 Mar 2026 19:14:55 GMT  
		Size: 112.9 MB (112946962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba34b97463376aa022ffad9a9b0a8770c09b6672b7a479cad0d63d998c53468`  
		Last Modified: Mon, 09 Mar 2026 19:14:53 GMT  
		Size: 9.7 MB (9697521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706e6a37a13efd29e1fd368705cb1275a6232229b848673a63fc9d2ddae735ab`  
		Last Modified: Mon, 09 Mar 2026 19:14:52 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6261f218d7783d70e14089e3382f40904976596134f1593abf59732e8f55bb49`  
		Last Modified: Mon, 09 Mar 2026 19:14:52 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:9e0cdcb0cfc2787a7468e395a7dd0fa2541e62e7ff38c3ddc0e0809617eb9349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6230692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b008d1e213c6dd6d402e5f2e590be583b48e46bcb8e0a0b213835b43fa05f7f9`

```dockerfile
```

-	Layers:
	-	`sha256:34a1dd176297b1149b7dfdaec70dffa8887f383d4bc06374d8edb12aacc18d0a`  
		Last Modified: Mon, 09 Mar 2026 19:14:53 GMT  
		Size: 6.2 MB (6214342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fdf26bbabac7f9ad15294d9a666e87316d94e4f60c2889bbde75e101f4e6b45`  
		Last Modified: Mon, 09 Mar 2026 19:14:52 GMT  
		Size: 16.4 KB (16350 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:25a20cfea90b4657c153179e91c7b1b12e56ad36642831438196220996d1b56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.7 MB (361670560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8258f5203c5c0033d6d4f41a7521fc1d8911764e1ac3ac7910ff5638ec950f11`
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
# Mon, 09 Mar 2026 19:14:30 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 09 Mar 2026 19:14:30 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:14:30 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:30 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:30 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:14:30 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:14:30 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:14:30 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:14:30 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:14:30 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:14:30 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:14:30 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:14:30 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:14:30 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:14:30 GMT
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
	-	`sha256:7b0231f2f077080f9c70d37bedbbc72056f5500dfbd2795bd6921b3dfee45ad0`  
		Last Modified: Mon, 09 Mar 2026 19:14:51 GMT  
		Size: 111.9 MB (111942390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5083b821d05054d28be8a89b2880a472fe4bf9be5963f4e27b12ff8fd23d8b53`  
		Last Modified: Mon, 09 Mar 2026 19:14:48 GMT  
		Size: 9.7 MB (9697557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7274913118d0b588cbbf247391c37656623d8fc2b9875ccccf4e044f2b9444f8`  
		Last Modified: Mon, 09 Mar 2026 19:14:48 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4935f7c71abe0fa301d41a159d3ad8048e3a569c393d23edc398a2d7e1bbf8`  
		Last Modified: Mon, 09 Mar 2026 19:14:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:06f865f2a263bff4ffea9dbd8acf28ca7364740f435235ac2e6e0a74570526c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6229769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1af6cf1220827d054276efaa3387d6375bf9e094cf20fa5f039fd6854965d0c`

```dockerfile
```

-	Layers:
	-	`sha256:c3ed146f12d03d8808aebfacb59c313aa2ee1ae6413c04418ec11e66454de6f6`  
		Last Modified: Mon, 09 Mar 2026 19:14:48 GMT  
		Size: 6.2 MB (6213286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34fa3d2474f0de1ef89a9cc5fcab4d17d1c02d18f5e4cb8f9aa40269df06c404`  
		Last Modified: Mon, 09 Mar 2026 19:14:47 GMT  
		Size: 16.5 KB (16483 bytes)  
		MIME: application/vnd.in-toto+json
