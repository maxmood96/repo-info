## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:675bd960d8cb76a1e9b4d77769bf984ea81fadb9f3f788655c99fd0d6e85c8ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:e0dceed4578969f4a1fc6c27abccb6e35f5b2193237271cb3e60cd6cd767e8e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363853455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365fcd3fef596ea3975054031e7ed8203dcb77ca3fc1eaadb89d8e5f49b3d098`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:49 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:32:24 GMT
ARG version=25.0.2.10-1
# Tue, 10 Feb 2026 18:32:24 GMT
ARG package_version=1
# Tue, 10 Feb 2026 18:32:24 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:32:24 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:32:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 10 Feb 2026 19:11:00 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 10 Feb 2026 19:11:00 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 10 Feb 2026 19:11:00 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 10 Feb 2026 19:11:00 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 10 Feb 2026 19:11:00 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 10 Feb 2026 19:11:00 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 10 Feb 2026 19:11:00 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 10 Feb 2026 19:11:00 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 10 Feb 2026 19:11:00 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 10 Feb 2026 19:11:00 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 10 Feb 2026 19:11:00 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 10 Feb 2026 19:11:00 GMT
ARG USER_HOME_DIR=/root
# Tue, 10 Feb 2026 19:11:00 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 10 Feb 2026 19:11:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 10 Feb 2026 19:11:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3ffbc2e8833044834ccfc60c99f6275f3632718226c6ef0c9706b41890795123`  
		Last Modified: Mon, 09 Feb 2026 18:58:55 GMT  
		Size: 54.0 MB (54038228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161b81996e3b0e5e4ba9a4cc5fbc9979cd889a255b08bc1d9d4e0dc355bca0f3`  
		Last Modified: Tue, 10 Feb 2026 18:32:49 GMT  
		Size: 189.2 MB (189187292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9f472897e08cc0fc23fd629cc0495e3653a1f1cc8207893a7e49438a46d8c3`  
		Last Modified: Tue, 10 Feb 2026 19:11:18 GMT  
		Size: 111.3 MB (111314652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d977d12a0636f3a2f222f88ab6d20fd0c542153851aa76511f7cc1ac96cde9e1`  
		Last Modified: Tue, 10 Feb 2026 19:11:16 GMT  
		Size: 9.3 MB (9312242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181768b6adfd09e55d7f4dee85085a8208ba3149d7a0650e834c89171c7a3ce3`  
		Last Modified: Tue, 10 Feb 2026 19:11:15 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fc8a54af2784f9258f76b9b3ca1ae054b718d84cebcc0e89d0a92472a021c4`  
		Last Modified: Tue, 10 Feb 2026 19:11:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:551b6431d4eaa9508663e488bdb11aec020daa160b769689e08c21ff8c2e80f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6224145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0d1dbf8c1a19fd8c8db80528ee60356dcc8f92665ee0357bc690d55fe8267a`

```dockerfile
```

-	Layers:
	-	`sha256:955095efa65e65865bf5bd46b616c4695f9e1abf08abfe5cb19c19ce17d153ce`  
		Last Modified: Tue, 10 Feb 2026 19:11:15 GMT  
		Size: 6.2 MB (6207795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a98085c68916e9548b7018ca30ec350ad7c152e55b9980cf8447e43c6bfc2da`  
		Last Modified: Tue, 10 Feb 2026 19:11:15 GMT  
		Size: 16.4 KB (16350 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:bf6078228d96aab0712b32a2328f822863721eb0889896bd215e59a6c8e07fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359745151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746f87d6bfe0c6e26daaefc84292a7412e54f0cbdec25786e944537aff54aac9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:36 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:36 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:32:12 GMT
ARG version=25.0.2.10-1
# Tue, 10 Feb 2026 18:32:12 GMT
ARG package_version=1
# Tue, 10 Feb 2026 18:32:12 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:32:12 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:32:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 10 Feb 2026 19:13:32 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 10 Feb 2026 19:13:32 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 10 Feb 2026 19:13:32 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 10 Feb 2026 19:13:32 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 10 Feb 2026 19:13:32 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 10 Feb 2026 19:13:32 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 10 Feb 2026 19:13:32 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 10 Feb 2026 19:13:32 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 10 Feb 2026 19:13:32 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 10 Feb 2026 19:13:32 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 10 Feb 2026 19:13:32 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 10 Feb 2026 19:13:32 GMT
ARG USER_HOME_DIR=/root
# Tue, 10 Feb 2026 19:13:32 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 10 Feb 2026 19:13:32 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 10 Feb 2026 19:13:32 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:72831a4cffd207c00f002b53208af67cc59cf3af51b98b118c11c230a7926a2d`  
		Last Modified: Mon, 09 Feb 2026 20:01:25 GMT  
		Size: 52.9 MB (52918211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098ac51664cc3ecb50ec7d80c5020cda656bac5f9d79fc5f5a1093c71586c098`  
		Last Modified: Tue, 10 Feb 2026 18:32:37 GMT  
		Size: 187.1 MB (187088942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb02ad52d363c1237965007d19780e65b34906ac5201815ca7ee3e9cc401dae2`  
		Last Modified: Tue, 10 Feb 2026 19:13:52 GMT  
		Size: 110.4 MB (110424717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d02705262f9b9dfe05fdc413aa5cd3175f2d93231f00697a964b249f1e5cc1`  
		Last Modified: Tue, 10 Feb 2026 19:13:50 GMT  
		Size: 9.3 MB (9312239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5f7190ae3faa4b8f0d7e4658f7417618a347b429b94f0d72c25ff6c681b849`  
		Last Modified: Tue, 10 Feb 2026 19:13:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f33686d50419d59d229043b90e70243e00ab1b79fbea8626c6c68c488c12f21`  
		Last Modified: Tue, 10 Feb 2026 19:13:49 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:0609119dd67be2b55b9fc45a94920d7704e84d3c821c2f965744dd0248540650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e950eeb0cef42cf718b44bb2291b2d1e8f3cacf1ad4d7251b184b806feb588`

```dockerfile
```

-	Layers:
	-	`sha256:aa9d73607cefb0207ff696294c85394726117f2d27a41df9027e2754927309e1`  
		Last Modified: Tue, 10 Feb 2026 19:13:49 GMT  
		Size: 6.2 MB (6206739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417954ea01f473b1a4470bea477fa8df9f89f61f3f728cd7a3501344b7c42058`  
		Last Modified: Tue, 10 Feb 2026 19:13:49 GMT  
		Size: 16.5 KB (16482 bytes)  
		MIME: application/vnd.in-toto+json
