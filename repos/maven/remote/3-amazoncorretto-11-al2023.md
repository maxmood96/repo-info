## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:bbce76aea17eb0ef0a1a77cc62a02f9d7b743d3967b9a530a9f097738b6534d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:5cd2564a289d08c01e2277ad31988e3349026f9b4fcd1fe9b7e7a080a7742152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.0 MB (338952084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bfd2224002efbc9e22a5ba4f9765b6ae473acdad356c237d43f97505b3a2d15`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:33:19 GMT
ARG version=11.0.31.11-1
# Wed, 22 Apr 2026 21:33:19 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:33:19 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 22 Apr 2026 22:14:34 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 22 Apr 2026 22:14:37 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 22 Apr 2026 22:14:37 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 22 Apr 2026 22:14:37 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 22:14:37 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 22:14:37 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 22 Apr 2026 22:14:37 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Apr 2026 22:14:37 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 22 Apr 2026 22:14:37 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 22:14:37 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 22 Apr 2026 22:14:37 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Apr 2026 22:14:37 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Apr 2026 22:14:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Apr 2026 22:14:37 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a88a81ff0950e289635eefbfbb2c99d4e5fa9802747adfbe0deab3edf23eb`  
		Last Modified: Wed, 22 Apr 2026 21:33:40 GMT  
		Size: 153.5 MB (153477599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8bac55d67bc62ad881707e5c743927f1654b0d3acd598f472151143f22920be`  
		Last Modified: Wed, 22 Apr 2026 22:14:54 GMT  
		Size: 109.1 MB (109057805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68a9a998fc369cf156e258cdc9080affd3f1f66a6b02229bbf4408498930d69`  
		Last Modified: Wed, 22 Apr 2026 22:14:51 GMT  
		Size: 12.5 MB (12532196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5a504afbdd73cff6c2922b4f8b99e4a7f55b9950cb1e427fe9826e9504cb35`  
		Last Modified: Wed, 22 Apr 2026 22:14:51 GMT  
		Size: 9.3 MB (9312218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea009de64fc29f60f4b7d83e64e25341240ad6a98604d5d47ed555bd7cddf3eb`  
		Last Modified: Wed, 22 Apr 2026 22:14:51 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaa4f77fa48ac0bb067d931da9ce146c1f5dbfd96c9e28c07987054178dabdd`  
		Last Modified: Wed, 22 Apr 2026 22:14:52 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:715d21e66a2c67bb0e3945da66f50537a34ff55b405d24368261c7b9e297eaf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6280262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c33ccdae5f2cadfdf85b20fd370bd5670a81949524af5bbc9a0e489e9ee532e`

```dockerfile
```

-	Layers:
	-	`sha256:9fcc78c0b51ccba7a01343df11135b1b83db3fc10b6e40c5fadc5ec9fc109958`  
		Last Modified: Wed, 22 Apr 2026 22:14:51 GMT  
		Size: 6.3 MB (6263977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1f14eef8b4a688d6ee5564de2d678caea81c8060ae6a8ee48f06f49dec8ad19`  
		Last Modified: Wed, 22 Apr 2026 22:14:50 GMT  
		Size: 16.3 KB (16285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:233316ff802cb6034d09658b9651485fe998bd5cb177f243433ad8d7de05b1d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.5 MB (335507226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665ca45871e6fbd75cc9294e8dc7d3e741ccd04c804a6c5231c1243b0f2ccb88`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:33:31 GMT
ARG version=11.0.31.11-1
# Wed, 22 Apr 2026 21:33:31 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:33:31 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 22 Apr 2026 22:14:21 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 22 Apr 2026 22:14:23 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 22 Apr 2026 22:14:24 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 22 Apr 2026 22:14:24 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 22:14:24 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 22:14:24 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 22 Apr 2026 22:14:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Apr 2026 22:14:24 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 22 Apr 2026 22:14:24 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 22:14:24 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 22 Apr 2026 22:14:24 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Apr 2026 22:14:24 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Apr 2026 22:14:24 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Apr 2026 22:14:24 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a1e2a231db3544e8a7929f99d6ce37f195163dc73ffccb051764be2f886290`  
		Last Modified: Wed, 22 Apr 2026 21:33:54 GMT  
		Size: 152.1 MB (152053159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79253c8e319ef6870b8d9b423c986f360f229b6b2ef21af7eb4cea698ba9065`  
		Last Modified: Wed, 22 Apr 2026 22:14:46 GMT  
		Size: 107.9 MB (107905104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4836c84fef10e7343bd5768deb73071fd8bf626a9d41021dbeece6ba32038db8`  
		Last Modified: Wed, 22 Apr 2026 22:14:39 GMT  
		Size: 12.8 MB (12792959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8ff160604ff0285536f921b6c1a352e5ec064466a7c1828a7a9cfdba7a989e`  
		Last Modified: Wed, 22 Apr 2026 22:14:39 GMT  
		Size: 9.3 MB (9312255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a345f6704ff9a60d6f26f11c83ae3f6d724bf16467ab3ad32dea0f538e46a09d`  
		Last Modified: Wed, 22 Apr 2026 22:14:39 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2258fc06f6c0770fa22a7b64498edb5b865bec238f919f68ff3e83c0d1f22c5`  
		Last Modified: Wed, 22 Apr 2026 22:14:40 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:db67f00c24d35e2723fd2dffa047d5367f718542e5fc55e58dafff142a302fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6280188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad63017129a7dbaac2f9b20c4c084882136390bcbb5ca80d197897c4d8bb4f5`

```dockerfile
```

-	Layers:
	-	`sha256:a6099a1c12846087463db846da564f08ed069df042d9d826f02b6c5fb39edec8`  
		Last Modified: Wed, 22 Apr 2026 22:14:39 GMT  
		Size: 6.3 MB (6263751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e01274fe252d650926f6cf16ea2ec196faeefb0562645142f14ce18cbd8cbfb`  
		Last Modified: Wed, 22 Apr 2026 22:14:38 GMT  
		Size: 16.4 KB (16437 bytes)  
		MIME: application/vnd.in-toto+json
