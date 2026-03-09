## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:0c999595d4f1ec1d3d2078d1dca36289b93ca438e9d2cc850eb5777cbe79cccc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:7cc3576344fa5a76c8111fbf3e83ca764537ca75622677d246e8da53c581e46f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.8 MB (332766960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b7279d63306c5ff51fe0f2e7ed7ab1c68b78b8a72d8a3d625963f52a8bc1d4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:01 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:01 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:11:21 GMT
ARG version=11.0.30.7-1
# Mon, 02 Mar 2026 23:11:21 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:11:21 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:11:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 09 Mar 2026 19:13:39 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 09 Mar 2026 19:13:42 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 09 Mar 2026 19:13:42 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:13:42 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:13:42 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:13:42 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:13:42 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:13:42 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:13:42 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:13:42 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:13:42 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:13:42 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:13:42 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:13:42 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:13:42 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:13:42 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2584a8e504dfaf493eadaafafbabd8b97f7cb5bbe3cb6a319fb37cf3c4335d86`  
		Last Modified: Thu, 19 Feb 2026 02:57:43 GMT  
		Size: 54.0 MB (54032840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bad2af03af5188a3cc6de4fd433994d98208a28c2aadd7bd215b1c171939319`  
		Last Modified: Mon, 02 Mar 2026 23:11:43 GMT  
		Size: 153.4 MB (153362633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a8c53eb578ea24fe1b1013f0cef52e465a0271409f238635e94582364f5566`  
		Last Modified: Mon, 09 Mar 2026 19:14:01 GMT  
		Size: 103.1 MB (103141061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e27e4fc6a547231250f769fed1b19eddf3ee9dd428f5643dec77c465015fbb2`  
		Last Modified: Mon, 09 Mar 2026 19:13:58 GMT  
		Size: 12.5 MB (12531862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bf5ec26ebbd63813f5490b99b222a1a69d5509c9c0b88f957197d7a9569297`  
		Last Modified: Mon, 09 Mar 2026 19:13:58 GMT  
		Size: 9.7 MB (9697522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1679c10b6a53aa6afb38adfc9e09712224265a888074a724147f6b63830f1a`  
		Last Modified: Mon, 09 Mar 2026 19:13:57 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079987ce6db32c05d8c994854e66e956698005f5ea1ede2481b71f916dbb5219`  
		Last Modified: Mon, 09 Mar 2026 19:13:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:29d299f61be352484256e565749e2681001d9c1a15e57ce1abb88966836483ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8960749341429125baa1066ddfae6aacdd138814d2687635afcf41770b1a69e1`

```dockerfile
```

-	Layers:
	-	`sha256:813b603219be052dab4f71434670c3cc478f235aaa7f1dc19f8458bd1f7350e9`  
		Last Modified: Mon, 09 Mar 2026 19:13:58 GMT  
		Size: 6.3 MB (6264082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d8c9806364d0804d98361192350a3be43ad8d5e260bfb60242754116a1d255d`  
		Last Modified: Mon, 09 Mar 2026 19:13:58 GMT  
		Size: 18.3 KB (18290 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:3da749d5557bf873cbc7b62759a928cc26f99bfbb47b5cb6ea94fcdc8829ae94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.2 MB (329220189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955e90f1cfe9af6648eda55e754334b76f198c23063681d534945177788731eb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:04 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:12:32 GMT
ARG version=11.0.30.7-1
# Mon, 02 Mar 2026 23:12:32 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:12:32 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:12:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 09 Mar 2026 19:13:21 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 09 Mar 2026 19:13:24 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 09 Mar 2026 19:13:24 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:13:24 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:13:24 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:13:24 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:13:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:13:24 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:13:24 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:13:24 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:13:24 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:13:24 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:13:24 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:13:24 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:13:24 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:13:24 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9330fae67a20d9aa2569828674140d8b67d50cfd127cb99ba0f9be275d35f976`  
		Last Modified: Thu, 19 Feb 2026 02:57:42 GMT  
		Size: 52.9 MB (52941319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7350756942f6b9b7af025da5fd26f1c03d9276b1ea1bc9aa9432be6e9b01612`  
		Last Modified: Mon, 02 Mar 2026 23:12:53 GMT  
		Size: 151.9 MB (151924448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad275e587755ada61e5eb8b945d63000cfe4a5a87160a669bfbd236debfc9f55`  
		Last Modified: Mon, 09 Mar 2026 19:13:45 GMT  
		Size: 101.9 MB (101859915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bee38f2e8c557d80b3fc68b6acaaffa099f66b50733add69d018981ad735d1`  
		Last Modified: Mon, 09 Mar 2026 19:13:42 GMT  
		Size: 12.8 MB (12795914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7557156500b2c9d43f3d7cbc06ea7b0e781d1a98a23d8f21d580be6acf10b4a5`  
		Last Modified: Mon, 09 Mar 2026 19:13:42 GMT  
		Size: 9.7 MB (9697552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f448cfeed93b20219732adf0520e89f1cc8beddd4046ff29fcc5f8fc9801d522`  
		Last Modified: Mon, 09 Mar 2026 19:13:41 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcefe0681d044754c0b656c29f23529b9c6effbd93aed6e7b17a1771663ddd3`  
		Last Modified: Mon, 09 Mar 2026 19:13:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:e310cf80970aee8fd05cc978ef3701faa5f03310a7eb74601d1c0af90fed0397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b83fdf262d0c16c92bac9cc233cd34b78fd0b319e9676f0680af8cb811db145`

```dockerfile
```

-	Layers:
	-	`sha256:2348d36d84d9c85dd57ff18051d645db6282962dfc31f28fec56f82c35a13dfb`  
		Last Modified: Mon, 09 Mar 2026 19:13:41 GMT  
		Size: 6.3 MB (6263856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2d03fd5103b6acf1eaebe6ed8bde6170922fe971a32a5d513da9ca56a37dd22`  
		Last Modified: Mon, 09 Mar 2026 19:13:40 GMT  
		Size: 18.4 KB (18439 bytes)  
		MIME: application/vnd.in-toto+json
