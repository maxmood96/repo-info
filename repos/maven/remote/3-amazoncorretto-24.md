## `maven:3-amazoncorretto-24`

```console
$ docker pull maven@sha256:7e48200b86af570214a4a9fa3d045475df28edd9532a7420a8ecc0c6a0174bb7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-24` - linux; amd64

```console
$ docker pull maven@sha256:68f6e41d34bfb1dccd117312737f4440ca3d402ad2ea6f6c5c00f93d02d20f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.8 MB (349752743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1f59053a8f5200d99e1770340364326bceb0f3526016d48e721d070f8fbebb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=24.0.2.12-1
# Wed, 16 Jul 2025 06:51:38 GMT
ARG package_version=1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b659529362324a4924ebe72940d12aa052ab5c84a979e7141ba538d8f4cbf4`  
		Last Modified: Mon, 06 Oct 2025 22:59:30 GMT  
		Size: 187.4 MB (187394702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bde25b94f337439c541e25876d3c8240702eb2c9f0ad7aaa696291f1a88ff4`  
		Last Modified: Mon, 06 Oct 2025 22:15:18 GMT  
		Size: 99.1 MB (99109271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892903172c8eebb5a9d8a7c5753a3edf5b033539c4d6196a166f78804cc20d75`  
		Last Modified: Mon, 06 Oct 2025 22:15:05 GMT  
		Size: 9.2 MB (9242596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3589d3b726b6d10e3ab029e7c1bc46be92beee23a6030a76d6a49f4b93a3dc5e`  
		Last Modified: Mon, 06 Oct 2025 22:15:05 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9753216c28e6cccbff15c1fcd20e614032092cd6a7df3cbafb84794e83fcb0`  
		Last Modified: Mon, 06 Oct 2025 22:15:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-24` - unknown; unknown

```console
$ docker pull maven@sha256:e835fb32be6906d8dea0de0ea9bdf8e7f9a2057263c46c2a9721cac293413c8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae4fad3d4b4ec0604d552cdc9c5e4e4f6a49ce13c3fb925fcae9e20e7ef75da`

```dockerfile
```

-	Layers:
	-	`sha256:8be8b8e5f0dd19ce8fbb8025e10e38289367be4b5bb2499d83a05610a1d4b02b`  
		Last Modified: Mon, 06 Oct 2025 23:28:29 GMT  
		Size: 6.2 MB (6207656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f89437dd0b09cb68e460624a140257acbbab12a5c87c84aa8973fca2bf7eed43`  
		Last Modified: Mon, 06 Oct 2025 23:28:30 GMT  
		Size: 16.3 KB (16313 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-24` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:1d0c93c00e8be9ce14e17fee74f17876446f95c2d3ed3ec12634aa8771935214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346058401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b17a266341f14ef79e548fc8ddc9b1f340bf4f5c3e5f840b27961afd6bd13a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=24.0.2.12-1
# Wed, 16 Jul 2025 06:51:38 GMT
ARG package_version=1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f92cd41b876f74ccba948207ca3ad51dc368e3be89f4da98af7d370eadeff0`  
		Last Modified: Mon, 06 Oct 2025 22:11:46 GMT  
		Size: 185.4 MB (185439334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8427c7cdcdb70369a8185054f6ccffda7f8a487b8af14a20043329b3abbecd07`  
		Last Modified: Mon, 06 Oct 2025 22:15:22 GMT  
		Size: 98.5 MB (98484244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4dd285b5cfb9b4d89f84683d41729f6ea26db74fc7821f3f1bd5a11b754d03`  
		Last Modified: Mon, 06 Oct 2025 22:15:27 GMT  
		Size: 9.2 MB (9242576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2efc62f60ca01e783dd1e12224bead7e2bfa6f17a46025b809fa33bcd774f9`  
		Last Modified: Mon, 06 Oct 2025 22:15:27 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d040d116478a1369a00698b0fa46657f146795150f3bae020ab359cf31de32`  
		Last Modified: Mon, 06 Oct 2025 22:15:27 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-24` - unknown; unknown

```console
$ docker pull maven@sha256:639eba8b0a616e4cefe3e658e0032658cd9bf85ce8a42911b4955d965cd1b3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76ec333fab63d75b8ee392ebd4fcb4c5cb7a49b61058e0672d183233d50a4c6`

```dockerfile
```

-	Layers:
	-	`sha256:fca0bc76b8aa00b6560a3b901f629fecfde50352f214cd0bbda36ab08c37e6a1`  
		Last Modified: Mon, 06 Oct 2025 23:28:36 GMT  
		Size: 6.2 MB (6206600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c78be42cf7431586cf19e4425dda2ab5abfb2b52483de1e5983b1b81d18017cf`  
		Last Modified: Mon, 06 Oct 2025 23:28:36 GMT  
		Size: 16.4 KB (16446 bytes)  
		MIME: application/vnd.in-toto+json
