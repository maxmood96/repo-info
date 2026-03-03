## `maven:3-amazoncorretto-25`

```console
$ docker pull maven@sha256:a8e537fe5eba990b340f0d24b1a5399d6dc15323e8eb25e6eed11e5191723ade
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25` - linux; amd64

```console
$ docker pull maven@sha256:804579bc9656d9ec2b555ad7c5cf86cb170fb19076d01cda649b653e65a63c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.5 MB (365479103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c5257ae796b944f0727a6e856826483af260317253ad93266ed0a7bc57ce64`
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
# Tue, 03 Mar 2026 00:15:02 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 03 Mar 2026 00:15:02 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 03 Mar 2026 00:15:02 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 03 Mar 2026 00:15:02 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 03 Mar 2026 00:15:02 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 03 Mar 2026 00:15:02 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 03 Mar 2026 00:15:02 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 03 Mar 2026 00:15:02 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 03 Mar 2026 00:15:03 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 03 Mar 2026 00:15:03 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 03 Mar 2026 00:15:03 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 03 Mar 2026 00:15:03 GMT
ARG USER_HOME_DIR=/root
# Tue, 03 Mar 2026 00:15:03 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 03 Mar 2026 00:15:03 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 03 Mar 2026 00:15:03 GMT
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
	-	`sha256:d4a2ace636bec76db57e6b7956a8f7a98d322919cda209bd8af59989d5c8e4cc`  
		Last Modified: Tue, 03 Mar 2026 00:15:22 GMT  
		Size: 112.9 MB (112946892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b486b6a28706ad825b1ad8e5f832c815dd0e02c6ad56f42252d16abd8b82af8d`  
		Last Modified: Tue, 03 Mar 2026 00:15:19 GMT  
		Size: 9.3 MB (9312236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc599583f16dab83420eb15196a3cbf0b8417b5584bb87cf5e9b0e461b99273`  
		Last Modified: Tue, 03 Mar 2026 00:15:19 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5308f8f83e4c68e0806eee8454ea97b2826f13e75e4c6d7266feeb377389dbb0`  
		Last Modified: Tue, 03 Mar 2026 00:15:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25` - unknown; unknown

```console
$ docker pull maven@sha256:2b0f0ae71588e2d80dc76f068445b4ce10c95c2d9e933375105346d278d5bd56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6226646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5416fb99b4f6349d96f1d1ceb168807cc24f76a94ccedd2444803c41c735c5a`

```dockerfile
```

-	Layers:
	-	`sha256:dfb4cc8b59807b7918df81cd2cf13a6c1c263fdfeabd1dd8ebcb498af324e31b`  
		Last Modified: Tue, 03 Mar 2026 00:15:19 GMT  
		Size: 6.2 MB (6209097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:884d5f0ecc5ed0335f4362da768ef77c6da73b6962fbd37fc5f5a7d295ce4724`  
		Last Modified: Tue, 03 Mar 2026 00:15:19 GMT  
		Size: 17.5 KB (17549 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e646bd0e7c7d918537ef4cceaf4e50451325c8e5e34dad7210d7c7ad7947abc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.3 MB (361284719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2021414b5509781f20c14bd0535d9687f567d13fa89fff04fa21811ec72ae239`
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
# Tue, 03 Mar 2026 00:15:38 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 03 Mar 2026 00:15:39 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 03 Mar 2026 00:15:39 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 03 Mar 2026 00:15:39 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 03 Mar 2026 00:15:39 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 03 Mar 2026 00:15:39 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 03 Mar 2026 00:15:39 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 03 Mar 2026 00:15:39 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 03 Mar 2026 00:15:39 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 03 Mar 2026 00:15:39 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 03 Mar 2026 00:15:39 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 03 Mar 2026 00:15:39 GMT
ARG USER_HOME_DIR=/root
# Tue, 03 Mar 2026 00:15:39 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 03 Mar 2026 00:15:39 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 03 Mar 2026 00:15:39 GMT
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
	-	`sha256:0bffd0a5d9ba0e1a6aa5456db70c65617f1c7bb54a20cad68d9a622ec70ab1e4`  
		Last Modified: Tue, 03 Mar 2026 00:16:01 GMT  
		Size: 111.9 MB (111941849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1a66c83f50d87ece5cfbe52c4ceea6feb70729987468cabc02f87edf80efa9`  
		Last Modified: Tue, 03 Mar 2026 00:15:57 GMT  
		Size: 9.3 MB (9312254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362473ef8e436e71ce66753e3caefb51f88740669f3f570961ebf2c6b92baa93`  
		Last Modified: Tue, 03 Mar 2026 00:15:56 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd0a28c856483f5ed8908a3880a7d340a069cff7f71c5c7d6024035df25dd5c`  
		Last Modified: Tue, 03 Mar 2026 00:15:56 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25` - unknown; unknown

```console
$ docker pull maven@sha256:d984aa6d32a3706c80877ae2a5843de74810d9e8e8006d7559183a5bd4f284c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6225818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3221a78d2cfe56bc64061599196a22d564cb1b9bd4f2e194350a1dd5af97e56e`

```dockerfile
```

-	Layers:
	-	`sha256:bfd351499ef447fcbde2bf2aa2ad83837db508132ce91dd98f1fa5b7e2e317d1`  
		Last Modified: Tue, 03 Mar 2026 00:15:57 GMT  
		Size: 6.2 MB (6208089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7320011d992d29e9091ffe795a386aae48897efec1d1c24428111ffaa1d858e`  
		Last Modified: Tue, 03 Mar 2026 00:15:56 GMT  
		Size: 17.7 KB (17729 bytes)  
		MIME: application/vnd.in-toto+json
