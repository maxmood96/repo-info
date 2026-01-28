## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:04509333b0bdfd6b57c5e41c34526ba43c56966417e2d6ab4726e867e6373a06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:ccbbffea4673c86e33bc043a3017050a21bb4879f66dab0d603924b418477def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.5 MB (332537524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:215677c04d606cab3ad1309d63101ea9a2025f8397bdc5354d1491ac5778b29b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:39 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:39 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:11:19 GMT
ARG version=17.0.18.8-1
# Tue, 27 Jan 2026 22:11:19 GMT
ARG package_version=1
# Tue, 27 Jan 2026 22:11:19 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:11:19 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:11:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 27 Jan 2026 23:14:53 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 27 Jan 2026 23:14:56 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 27 Jan 2026 23:14:56 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 27 Jan 2026 23:14:56 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 27 Jan 2026 23:14:56 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 27 Jan 2026 23:14:56 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 27 Jan 2026 23:14:56 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 27 Jan 2026 23:14:56 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 27 Jan 2026 23:14:56 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 27 Jan 2026 23:14:56 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 27 Jan 2026 23:14:56 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 27 Jan 2026 23:14:56 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 27 Jan 2026 23:14:56 GMT
ARG USER_HOME_DIR=/root
# Tue, 27 Jan 2026 23:14:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 27 Jan 2026 23:14:56 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 27 Jan 2026 23:14:56 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74463adce1e4f57125e9fd9cff6d1ee4e60a88fd9a1be6afad902b0f8a66863a`  
		Last Modified: Tue, 27 Jan 2026 22:11:41 GMT  
		Size: 156.9 MB (156915298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726c8f24e563cd3bdeb268066fb6f88322a426a5a1caaeb90a862c28bd021e94`  
		Last Modified: Tue, 27 Jan 2026 23:15:15 GMT  
		Size: 99.8 MB (99788141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b9e6fcf2b9afb5b2b1c2896d9e53754eafe8d0ee9ab2bf60b4fe7d90ad5b7b`  
		Last Modified: Tue, 27 Jan 2026 23:15:13 GMT  
		Size: 12.5 MB (12496953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e20afe72f55c8e5d45a7a1a47a4a3a2be3a212f3e223a8983eeea2aac8df13f`  
		Last Modified: Tue, 27 Jan 2026 23:15:12 GMT  
		Size: 9.3 MB (9312251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227693a77c601d14bcf676da64380f4be156000630abd1ad175a4b03bf6651fb`  
		Last Modified: Tue, 27 Jan 2026 23:15:12 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2292b7b08a5e22c06fa60d96759377876966bfe880ee1407d22c493a6b5a24d`  
		Last Modified: Tue, 27 Jan 2026 23:15:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:afc2d9c7f6f29aacdc6bbe55a534cad2dded07a1db3df6ef33aec01bf50885cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e31ae66577460cae187f493078aac4a69110c48ba92b9c247fa4ac92a318746`

```dockerfile
```

-	Layers:
	-	`sha256:c0e412802a1dcd23a6a9775ec06572d58df61d2dfaaf75d14e9806bb048a567d`  
		Last Modified: Tue, 27 Jan 2026 23:15:12 GMT  
		Size: 6.2 MB (6232025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe2f98900b83fae606eac9a2115929e88e5a824a0b2a2213d3d6fcf8bd4dc448`  
		Last Modified: Tue, 27 Jan 2026 23:15:12 GMT  
		Size: 18.3 KB (18285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e42296428ec42461cd225e1b297a4317f467a1abe361418741cc0efbab94e828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.5 MB (329504042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9423b1a32b1381d0e57a6681af1fe0ff3f116124ee3e450a84fb2d25946f19b6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:02 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:28:33 GMT
ARG version=17.0.18.8-1
# Wed, 28 Jan 2026 04:28:33 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:28:33 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:28:33 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:28:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 28 Jan 2026 05:41:49 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 28 Jan 2026 05:41:51 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 28 Jan 2026 05:41:51 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 28 Jan 2026 05:41:51 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 05:41:51 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 05:41:51 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 28 Jan 2026 05:41:51 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Jan 2026 05:41:51 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 28 Jan 2026 05:41:51 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 28 Jan 2026 05:41:51 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 28 Jan 2026 05:41:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 28 Jan 2026 05:41:52 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 28 Jan 2026 05:41:52 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Jan 2026 05:41:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Jan 2026 05:41:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Jan 2026 05:41:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0aad64ff72b39223fe7c89c4c32e0df701234a6d10e6450afd2c590b69880b`  
		Last Modified: Wed, 28 Jan 2026 04:28:55 GMT  
		Size: 155.7 MB (155720069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38dc55c94e17112438acb6ed9e7a4cc61a121725244c25bd36cf8328d9f1aa2b`  
		Last Modified: Wed, 28 Jan 2026 05:42:09 GMT  
		Size: 98.8 MB (98795251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d78993afb086791c269fce7f7d30bce27d4f2f283399491c3d531a6fe11ba8`  
		Last Modified: Wed, 28 Jan 2026 05:42:07 GMT  
		Size: 12.8 MB (12758799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7362acf6b6a8551f17ec79a4c25ef6fff8c9f7bc9a4bad35669fabd41a519932`  
		Last Modified: Wed, 28 Jan 2026 05:42:06 GMT  
		Size: 9.3 MB (9312241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1ea98136ed4751335f35eb2a7ffb33d20e67cd469a36dfac4d95334bc9403b`  
		Last Modified: Wed, 28 Jan 2026 05:42:06 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a130fc08bda695e265857324b24d9a9f328fea476d2aa454b90efa6dd205145d`  
		Last Modified: Wed, 28 Jan 2026 05:42:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:dbb3fc2924b04f4bf27c1cbfa0c72a0a2d0490dac8d8459fc0001012385ec1e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6249387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d144a1f2bc37125443741472714c5f716e98daf33e451c9b2d0e83372bf5002`

```dockerfile
```

-	Layers:
	-	`sha256:9afed08a335b6330be1483d19f17ee2c875272fded8ae73e0fa25b531f1009ec`  
		Last Modified: Wed, 28 Jan 2026 05:42:06 GMT  
		Size: 6.2 MB (6230955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbf18a2dc8443c39d9f5a86803eaccd7c96a0ad4bef49bcc3fd66aa71759a7a9`  
		Last Modified: Wed, 28 Jan 2026 05:42:06 GMT  
		Size: 18.4 KB (18432 bytes)  
		MIME: application/vnd.in-toto+json
