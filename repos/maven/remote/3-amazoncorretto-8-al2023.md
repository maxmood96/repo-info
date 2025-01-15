## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:fffc994574f0780a15fdeca4d81af5b5710bf85ac46f565a9c27bbaacee282cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:f5cd9500c63d97a6f311cc71a4b60b135536f2c6956f90821cc1b89ecaa3c352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.3 MB (414326124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7ffc5e4434eb6ae69a347ee3d67e9190a029cd9dc965ee88817b365430b9ba`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=1.8.0_432.b06-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
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
	-	`sha256:2d449a9cb20bfb0f76c698e4adb686874f9bd35779c1f8f9d76c5528c87b3366`  
		Last Modified: Wed, 15 Jan 2025 00:43:54 GMT  
		Size: 53.2 MB (53156717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc28606bf023b3c71d1b87f03a79eb281808b8c13245cef74cfa7bda58e6e73`  
		Last Modified: Wed, 15 Jan 2025 18:31:27 GMT  
		Size: 285.7 MB (285683472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d20b4cea094dca22ae7ace1c91c7681637c6dfa6bcf3cabae7c8f7987c15764`  
		Last Modified: Wed, 15 Jan 2025 19:10:24 GMT  
		Size: 61.5 MB (61519055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fa3f80a5764320388f2c179f42e323d8468da535e38f38f38f773bddd5f4e6`  
		Last Modified: Wed, 15 Jan 2025 19:10:22 GMT  
		Size: 4.8 MB (4795394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fa4236fcbf2405ac58ef5e7d3d9e1bdf0d8dd604561c1cc4fcf6483bade2c4`  
		Last Modified: Wed, 15 Jan 2025 19:10:23 GMT  
		Size: 9.2 MB (9170444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fae62dfabf9b86b5f4606b8989451136697b8be9ffd3374bb86e6ed58430a0`  
		Last Modified: Wed, 15 Jan 2025 19:10:22 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca52cff49ccf02d0d1e6c01aa2a1906b97333b79baaf5722ff73d281bc9dce0`  
		Last Modified: Wed, 15 Jan 2025 19:10:23 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:fa3b6a72a8c11baad3599f6b415300d825f9c4c9363f7383a464706a68723887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12718734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5b8513c12d0459fb52870e6ee593b64427acceb9359fd9be38718fe801a72d`

```dockerfile
```

-	Layers:
	-	`sha256:c29cd735005a24dce15c521e12e7ef19509ead3cb94c2b61019dca57a9ec602f`  
		Last Modified: Wed, 15 Jan 2025 19:10:22 GMT  
		Size: 12.7 MB (12700422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38806bc92506bbb247f3949b97daf86aed42154e6b3cdaa15fd45dd26d080d4e`  
		Last Modified: Wed, 15 Jan 2025 19:10:22 GMT  
		Size: 18.3 KB (18312 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:bf2a03e1d539c7c93c243df861eb73d2c1666c5a706f8f4fe67d2ad22ab8e2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252448933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee0cf4d37fb08f76fb13b02e40d1806b58de5cfc84e675896836fa315f82590`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=1.8.0_432.b06-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
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
	-	`sha256:2dc99809e33185161e199db0b479b51cf3fb7470fd27c484aff50bdf9dcb5dab`  
		Last Modified: Fri, 10 Jan 2025 02:14:49 GMT  
		Size: 52.3 MB (52268196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc169d94e6d9cd3a7a940d75bf4eaf25616e38ec662abc4c24c17ff89c4d1b1`  
		Last Modified: Sat, 11 Jan 2025 02:56:35 GMT  
		Size: 118.7 MB (118662341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0b2789b955760046a961407c39ce6fdba458f179231b29b4f674032fce435f`  
		Last Modified: Sat, 11 Jan 2025 04:00:54 GMT  
		Size: 59.6 MB (59557033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ba0e27a24421f6892ab2deeed48e71b93e54c7c456b0ed68fa65844704aa3`  
		Last Modified: Sat, 11 Jan 2025 04:00:53 GMT  
		Size: 12.8 MB (12789892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204f24cd4ae057f45ee6fdf45aec8b0e3423200f77a8482d60c06f51d451ffa1`  
		Last Modified: Sat, 11 Jan 2025 04:00:53 GMT  
		Size: 9.2 MB (9170426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24669ff5c8f1a99ba42304d364768a7ea2e6d7f09bd013fd1d746a0333a229a1`  
		Last Modified: Sat, 11 Jan 2025 04:00:52 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816e67d044baaf6c4f2ca974d3ed97cf2cdb0376ab7206308a113c1ee9d8e721`  
		Last Modified: Sat, 11 Jan 2025 04:00:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:ea6789e35e5de9c6672fa724a94828711e913f51568d61c38e5c3b7ef57043f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6619804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f659332086e550f068b4e9bea7a507804093f45ab7a5d70fb3546d32a8f97bb`

```dockerfile
```

-	Layers:
	-	`sha256:a2596595db0c801d11b22797b4e4a66073882c9063ae6734189c1905f637c9ae`  
		Last Modified: Sat, 11 Jan 2025 04:00:53 GMT  
		Size: 6.6 MB (6601339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8a8d371b7d47bfc9c4ad7260d07e7bdaa53fe37f90250ecf3d67b9f90e74372`  
		Last Modified: Sat, 11 Jan 2025 04:00:52 GMT  
		Size: 18.5 KB (18465 bytes)  
		MIME: application/vnd.in-toto+json
