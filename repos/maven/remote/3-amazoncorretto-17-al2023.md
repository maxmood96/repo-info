## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:b8979f52f6e42df40aab1c8035ddde9fa291ad2c59032ab4f581efa6c31f5359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:0ee3c32c79e039b232a3e4f3dfb38ba2839451d27ab890100a7ee52caaa76ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265635614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6df3ea35683185c56ee2ad3e2fce93d33ba547192accb333601de1b3fcf003`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Apr 2024 22:25:10 GMT
COPY dir:c7d5463abe17dfd3879bd12c94f31ebdaedb939167b5199c40650e35e379f334 in / 
# Fri, 19 Apr 2024 22:25:10 GMT
CMD ["/bin/bash"]
# Fri, 19 Apr 2024 22:56:23 GMT
ARG version=17.0.11.9-1
# Fri, 19 Apr 2024 22:56:23 GMT
ARG package_version=1
# Fri, 19 Apr 2024 22:56:46 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 19 Apr 2024 22:56:47 GMT
ENV LANG=C.UTF-8
# Fri, 19 Apr 2024 22:56:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 27 May 2024 15:57:48 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 27 May 2024 15:57:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 27 May 2024 15:57:48 GMT
ARG MAVEN_VERSION=3.9.7
# Mon, 27 May 2024 15:57:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 27 May 2024 15:57:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 27 May 2024 15:57:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6f59c9417334b7a9eb6449cc09a14d6738ae8afbfb25d681f2c27740e7d4856c`  
		Last Modified: Fri, 19 Apr 2024 22:25:53 GMT  
		Size: 52.3 MB (52323609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7faae36eec06ab9002b453e309f1efbfb1c1b6ca3ad60cebefee42df6aac9dc3`  
		Last Modified: Fri, 19 Apr 2024 23:09:57 GMT  
		Size: 157.1 MB (157050137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c97985d3eb27479493ce6edd8cbc42c44b594b6c22779755a2b62b0933fded`  
		Last Modified: Tue, 28 May 2024 19:56:11 GMT  
		Size: 46.6 MB (46612928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe51cd8a4e1349071c4a7d8897120c1a534cd58cff35f5f92263e485d5a6f14`  
		Last Modified: Tue, 28 May 2024 19:56:08 GMT  
		Size: 9.6 MB (9647563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4004777c17cf29165e25f7a4a301ddb4f00320f843e58e547b39fefb7f7673`  
		Last Modified: Tue, 28 May 2024 19:56:08 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff19cce96269c061e4797ae381daa088455a00b9b68c8844c7dd3c25ffe9218d`  
		Last Modified: Tue, 28 May 2024 19:56:08 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72e30343224eaa7d4f57e6b85102d82c44cf5e6c99767cff73e57ca24c794bb`  
		Last Modified: Tue, 28 May 2024 19:56:08 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:8dd2ded7012132c497bdb447051602bbed0dc2115321098e985cb93186461be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263053166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8334c6dcb4b3500af4cdaf330cfaa943293d3f80573b9c020667238f9bf020a2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Apr 2024 22:10:28 GMT
COPY dir:e8d306065b89c24e8d7ed76b1f4a499224cd18e3ec44dc6823b5d039220ebc19 in / 
# Fri, 19 Apr 2024 22:10:29 GMT
CMD ["/bin/bash"]
# Fri, 19 Apr 2024 22:33:17 GMT
ARG version=17.0.11.9-1
# Fri, 19 Apr 2024 22:33:17 GMT
ARG package_version=1
# Fri, 19 Apr 2024 22:33:34 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 19 Apr 2024 22:33:36 GMT
ENV LANG=C.UTF-8
# Fri, 19 Apr 2024 22:33:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 27 May 2024 15:57:48 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 27 May 2024 15:57:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 27 May 2024 15:57:48 GMT
ARG MAVEN_VERSION=3.9.7
# Mon, 27 May 2024 15:57:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 27 May 2024 15:57:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 27 May 2024 15:57:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0fff0db406e493d5737bccd8db4b9460e6d6c5e6d45f62e14ae7cb208fcc984a`  
		Last Modified: Fri, 19 Apr 2024 22:11:04 GMT  
		Size: 51.4 MB (51413307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72acd7cc9362d6ace48a6a40a6b1d145996c0e0b5cbec014657020019ae1ca77`  
		Last Modified: Fri, 19 Apr 2024 22:44:35 GMT  
		Size: 155.8 MB (155759068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20717d81baaaf2d884d5ffc1c07e64c30dc0be3fa35a7d25c5d62a184a14236a`  
		Last Modified: Tue, 28 May 2024 20:36:34 GMT  
		Size: 46.2 MB (46231854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d1b659193e0ad9d8a93adbe456733f8f380f61a5b9a5ee8cf7c5acf2c85ae3`  
		Last Modified: Tue, 28 May 2024 20:36:32 GMT  
		Size: 9.6 MB (9647556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4efe1332672a7464ea4c1561c84c3777d1ed47ee1b5e8cfb32f4bba21a9c1d`  
		Last Modified: Tue, 28 May 2024 20:36:31 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cbce36c3bcff5e15b442f5a42b8aa22bad9e16aa550ab28aceb1c686a5a8d5`  
		Last Modified: Tue, 28 May 2024 20:36:31 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c8507057becf06ea43761a5b5ab87df96c1f2051223f590988ca737f584fa4`  
		Last Modified: Tue, 28 May 2024 20:36:31 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
