## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:2d2cebcb39a6fc4bd2fb4b7315eac6c66b6fb2456c7935eb0e333cb3ab33626d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:bc36e389dbfff0913ee3bd83a66768a85c7804f23ee31035dae504fc312f321d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304411790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416eab93eca5c3ff973e47634b8090837e9efcde6f7042d0cd5fb9f145e8d4a6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sun, 22 Jun 2025 10:21:55 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN yum install -y openssh-clients # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b32084d69388d1a83137a801da01717a35f31eef39012331796a50e2c2385667`  
		Last Modified: Wed, 11 Jun 2025 22:05:56 GMT  
		Size: 53.6 MB (53570360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708f6522ceeab5915afc29985d74cf7077875a98f799786146a2c56ccf4c5366`  
		Last Modified: Fri, 13 Jun 2025 17:12:51 GMT  
		Size: 153.9 MB (153920803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809a6b37e1d03bbf3d46a4d0f59ef7745637a73d1cada3afad45b19154aba12d`  
		Last Modified: Wed, 02 Jul 2025 09:49:16 GMT  
		Size: 75.4 MB (75424248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c901cd25fff769af583f4aaded5208c2358163009f3416d5f96e99e96a6b4de8`  
		Last Modified: Wed, 02 Jul 2025 05:13:01 GMT  
		Size: 12.5 MB (12541961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef98b1bbeaf40d270293cd3be0a4826a1b81dd40f8719db1124fb3bf57361186`  
		Last Modified: Wed, 02 Jul 2025 05:13:02 GMT  
		Size: 9.0 MB (8953378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49371b00fb7fcb54ae2b6d5e4034ea9e30aabb0c81eb2fea93d2fb1886de6601`  
		Last Modified: Wed, 02 Jul 2025 05:13:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502526ff1823225b06b7f3df69222818ac4ac9a82f590a393f9b9ac9d9d886bc`  
		Last Modified: Wed, 02 Jul 2025 05:13:00 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:cb71c6b4e7758973b9ced20a5884932b41c8eee9c00b7f56bcf159fc791c0df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6273918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ee750e51d7f4398545068ebbd7e3249157c047d3c46579e692a839560477ac`

```dockerfile
```

-	Layers:
	-	`sha256:34c54c844d5ae0ea79b8e8711d2e131a9781cebe0c83c1a2336914b5604565e5`  
		Last Modified: Wed, 02 Jul 2025 08:27:33 GMT  
		Size: 6.3 MB (6255590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3abe278de796c8ddf6af7a6a56fcd1cf4c44db58ad4b3c87d038b07756250ca6`  
		Last Modified: Wed, 02 Jul 2025 08:27:34 GMT  
		Size: 18.3 KB (18328 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:dad2cb6cdb4e94c8795a1d55a50cad5c9872ad0442deef6af0e6c45c2e004017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.2 MB (301246230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4a6d0cfa2afa84593adb7a67492d5834e8cf60f7b54f38b08025689511c60f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sun, 22 Jun 2025 10:21:55 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN yum install -y openssh-clients # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2913b957e7cca1539a6d274307081564a7142eae485bcd51683bbef9106592aa`  
		Last Modified: Thu, 12 Jun 2025 03:47:32 GMT  
		Size: 52.5 MB (52481692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0c519f05c9a0dd0a67d373078abf3f9e9c77775616f0ab4dacd5b6eaa84d0c`  
		Last Modified: Fri, 13 Jun 2025 23:40:30 GMT  
		Size: 152.4 MB (152439882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf9c44b4cf9d648945678973fb89afcd8d50714fcd73a33d5142f4d8849a8a9`  
		Last Modified: Fri, 13 Jun 2025 21:22:06 GMT  
		Size: 74.5 MB (74544267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3bbfb67b305408eb306f18f8f4b1709e611fd9272877617c18dcedd0fe4009`  
		Last Modified: Fri, 13 Jun 2025 21:22:03 GMT  
		Size: 12.8 MB (12825963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaf2c3ce216f65770b5e0415ad6d5046ae026af1a566f271429cacc72050a0f`  
		Last Modified: Mon, 23 Jun 2025 17:39:47 GMT  
		Size: 9.0 MB (8953388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e000efe9fee76502612b872a6d90fbe21e9fd10ecd14a03a7f2170dc5b925f`  
		Last Modified: Mon, 23 Jun 2025 17:39:45 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c26b0dd31f136ce7970fea87c95509625627940275aa8f72e6e2a78152cc026`  
		Last Modified: Mon, 23 Jun 2025 17:39:45 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:34f968c7ed78c1581b71d90b5ed50394ba08eeb69313936f68d2f04b57cc7d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6273840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806cf8b0c133e7a01715003c047bd8a466b05dcb626f106328d1484f8859de89`

```dockerfile
```

-	Layers:
	-	`sha256:0369c9d08497b60deab6fb28386aba7f105829b1752a1f731fa7413ae142bc06`  
		Last Modified: Mon, 23 Jun 2025 20:28:02 GMT  
		Size: 6.3 MB (6255364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8281f5095f8b35cca8c28a6523026541441c3df146fdfbda4244c762be7b7ee1`  
		Last Modified: Mon, 23 Jun 2025 20:28:03 GMT  
		Size: 18.5 KB (18476 bytes)  
		MIME: application/vnd.in-toto+json
