## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:75db7f44f4c4682760022addcb084b0dcbba555593fc045ab083431bc92cbb4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:209fe6e10260608e19048904437ebd333b489fb0131b8b73a515ad029074c371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354745695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b303636850ddd361f035546665a5f9dd6e217168043d77364c3beffccc5ac536`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:49 GMT
ARG version=25.0.1.8-1
# Fri, 31 Oct 2025 00:12:49 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:12:49 GMT
# ARGS: version=25.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:12:49 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 31 Oct 2025 01:15:44 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 31 Oct 2025 01:15:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 31 Oct 2025 01:15:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:15:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:15:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 31 Oct 2025 01:15:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 31 Oct 2025 01:15:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 31 Oct 2025 01:15:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 31 Oct 2025 01:15:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 31 Oct 2025 01:15:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 31 Oct 2025 01:15:44 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 31 Oct 2025 01:15:44 GMT
ARG USER_HOME_DIR=/root
# Fri, 31 Oct 2025 01:15:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 31 Oct 2025 01:15:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 31 Oct 2025 01:15:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cad330e08d585bcff7ce7b398a5a2dbb684e338ae4fe298f9dca43f057f4b8c`  
		Last Modified: Fri, 31 Oct 2025 01:10:53 GMT  
		Size: 189.2 MB (189165602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5023f98495d488c31436ca8260eb3986a6c2b05980be74a1334eed5eca4a6d90`  
		Last Modified: Fri, 31 Oct 2025 01:16:23 GMT  
		Size: 102.3 MB (102335230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb5600b00cb0bd8f779f301a9166297ea6284ebc14cadd40136fb88325dcb88`  
		Last Modified: Fri, 31 Oct 2025 01:16:11 GMT  
		Size: 9.2 MB (9242587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fe1ca93dd620b2bddad7f63aae1a6c1540e703ed7ef19594a1a72932e5a87c`  
		Last Modified: Fri, 31 Oct 2025 01:16:09 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44096dca29d8de777dbee048065706543e639bd46d7a71b20eea43c84c03da3f`  
		Last Modified: Fri, 31 Oct 2025 01:16:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:c3e104c4bf2e37d92fb38bec6c99697f83fb1988f0a8d12e1381742aa03b0e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6224124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2b28d48cbd8950be34151fe7808731d4eefb173574a0f5c30c92cac3048690`

```dockerfile
```

-	Layers:
	-	`sha256:9c55a6d9247da1441e282a5ce40c3aede8df8719ee71a70cf1c4ca99b6dceaaf`  
		Last Modified: Fri, 31 Oct 2025 02:28:30 GMT  
		Size: 6.2 MB (6207774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:302db093c1d0043e3a510db442690ec2de5732ed9b2d401433dc8caf6bcdb169`  
		Last Modified: Fri, 31 Oct 2025 02:28:30 GMT  
		Size: 16.4 KB (16350 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:992f267e3eb1905884caf4fc5384522a98f2a95d020267e5764ed1b334f2306a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 MB (350891131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeda1232dd5c7ffe42e6353d013175d4f3c99d0813a2b0269fa1ebf85123a05d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:13:18 GMT
ARG version=25.0.1.8-1
# Fri, 31 Oct 2025 00:13:18 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:13:18 GMT
# ARGS: version=25.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:13:18 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:13:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 31 Oct 2025 01:15:38 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 31 Oct 2025 01:15:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 31 Oct 2025 01:15:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:15:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:15:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 31 Oct 2025 01:15:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 31 Oct 2025 01:15:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 31 Oct 2025 01:15:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 31 Oct 2025 01:15:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 31 Oct 2025 01:15:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 31 Oct 2025 01:15:38 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 31 Oct 2025 01:15:38 GMT
ARG USER_HOME_DIR=/root
# Fri, 31 Oct 2025 01:15:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 31 Oct 2025 01:15:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 31 Oct 2025 01:15:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57b7d335691ba03f63339309551160b358c13633bf8b3ed736c5fb71399b7e5`  
		Last Modified: Fri, 31 Oct 2025 01:11:07 GMT  
		Size: 187.1 MB (187089365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093b2189a6dff74126bca3ef04c073be1e58ff90638e18309ee4800908a82965`  
		Last Modified: Fri, 31 Oct 2025 01:16:20 GMT  
		Size: 101.7 MB (101656286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05326974fa10459860bb26913d629a1c1d633ebd4c277164e37f177eb6d65b9f`  
		Last Modified: Fri, 31 Oct 2025 01:16:04 GMT  
		Size: 9.2 MB (9242588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7645a3af0b82e3a61860a2ec78bfb85e5263c67cf2cdfd7005cff0e8a78ea906`  
		Last Modified: Fri, 31 Oct 2025 01:16:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07423c2e76164aa41f70a8e811c050ff42d61a6bc134dde3d4f1e972cc2d058`  
		Last Modified: Fri, 31 Oct 2025 01:16:04 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:1caf6b82d79f022363b31ae638c1ea9032651a1a5cf54c70918b40584814b534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623564e3e18545d0810f04a998520995ecc1cda240033e478b55dadac221b6da`

```dockerfile
```

-	Layers:
	-	`sha256:beba4b8204f65fe5c49f355a1deb4b221ec92e6d5dc3510be59be12e9233b2a0`  
		Last Modified: Fri, 31 Oct 2025 02:28:36 GMT  
		Size: 6.2 MB (6206718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ac0db59bf943efe9215d5d04c266504771c2525f0246b03af537db27246283`  
		Last Modified: Fri, 31 Oct 2025 02:28:37 GMT  
		Size: 16.5 KB (16483 bytes)  
		MIME: application/vnd.in-toto+json
