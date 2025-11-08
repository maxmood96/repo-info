## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:28ae863f789320c4e0cd1554c9157afe25b93b6e95c1aa1c01c579e7781f0b5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:adfe1ec4619612e47a6bb83b8f1fcf9913701d7430219ff164ce58be3ddd9e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325386786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5201fc59cea128dc83a3232afc8f393f7e84cf576ae0c56a0f6f12a5203be5bc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 06 Nov 2025 22:15:48 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:15:48 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 23:12:23 GMT
ARG version=17.0.17.10-1
# Thu, 06 Nov 2025 23:12:23 GMT
ARG package_version=1
# Thu, 06 Nov 2025 23:12:23 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 23:12:23 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 23:12:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sat, 08 Nov 2025 19:23:17 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Sat, 08 Nov 2025 19:23:19 GMT
RUN yum install -y openssh-clients # buildkit
# Sat, 08 Nov 2025 19:23:19 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:23:19 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:23:19 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:23:19 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:23:19 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:23:19 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:23:19 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:23:19 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:23:19 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:23:19 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:23:19 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:23:19 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:23:19 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7857af70cc37714ae4781f1d58242c7667f933ef8be05b0636d2c50e756263b2`  
		Last Modified: Wed, 05 Nov 2025 21:09:20 GMT  
		Size: 54.0 MB (54000503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72fab7e98d79cbd6d7228c28372060c6f33b8a670c5ac74e9a4276a3de3239f`  
		Last Modified: Fri, 07 Nov 2025 00:11:28 GMT  
		Size: 156.9 MB (156930901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153a53cc465ac332ef65eb2752ae0f997d53a0577cad9e836007f2ed01c33ddc`  
		Last Modified: Sat, 08 Nov 2025 19:24:12 GMT  
		Size: 92.7 MB (92691640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5541b6367a4e9e14432c5108bfbe67348f62f7b9ee42b95a348f767cd7debae`  
		Last Modified: Sat, 08 Nov 2025 19:23:46 GMT  
		Size: 12.5 MB (12520134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac11a637e4ca7b9a4fcecc4b3f56d7720b2710dccc016cde8ca79d354786e85a`  
		Last Modified: Sat, 08 Nov 2025 19:23:44 GMT  
		Size: 9.2 MB (9242570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88425822dd0bab5341a883939694cb0e3e34cdd5d8414fc826c5bab1bf337bfb`  
		Last Modified: Sat, 08 Nov 2025 19:23:43 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43126a6ece2a3770cb4a2913e9b6bca8240c73f3f7e1fb5ce25621e6a690bd3c`  
		Last Modified: Sat, 08 Nov 2025 19:23:43 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:7310200bb125284cb4fe8ab252b453e8143fad67cf299a226a00965e61a0f36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e2fc12ce57192667f29007ffdfc7ee352a8c2d631781d768e01f8c3a87c874`

```dockerfile
```

-	Layers:
	-	`sha256:618f3f3841c424bbdda62f06f60088f994df003c24c7c631e11a4af0162ae069`  
		Last Modified: Sat, 08 Nov 2025 21:28:30 GMT  
		Size: 6.2 MB (6232024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:775a634f0e319528466a717c9e0f536c1051c4f44ed89bc614abf9c2487fe5e9`  
		Last Modified: Sat, 08 Nov 2025 21:28:31 GMT  
		Size: 18.3 KB (18285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9641da22747f14507024785774a1c42118ac5cbb02acda37e446b49b822211e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322384184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbac22a08d07fe5b95113b6a60f748f88ae72b1b945390bb673ce005c10b7119`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 06 Nov 2025 22:01:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:01:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:13:29 GMT
ARG version=17.0.17.10-1
# Thu, 06 Nov 2025 22:13:29 GMT
ARG package_version=1
# Thu, 06 Nov 2025 22:13:29 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 22:13:29 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:13:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sat, 08 Nov 2025 19:22:40 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Sat, 08 Nov 2025 19:22:42 GMT
RUN yum install -y openssh-clients # buildkit
# Sat, 08 Nov 2025 19:22:42 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:22:42 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:22:42 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:22:42 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:22:42 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:22:42 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:22:42 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:22:42 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:22:43 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:22:43 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:22:43 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:22:43 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:22:43 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:22:43 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6d0dad3595837e5d244dadb238b6a2012108ea03c6af3e9c48dc16cad05f98d0`  
		Last Modified: Thu, 06 Nov 2025 01:49:48 GMT  
		Size: 52.9 MB (52901684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42206444f43ddda96491ceb64db5c92fe941fa16f8ddf5f9800eaf678742c975`  
		Last Modified: Thu, 06 Nov 2025 23:11:31 GMT  
		Size: 155.7 MB (155740957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d4cef6812c2395b9e42e856fd1cd007b702c9e90a9b812631dbfe1da219d63`  
		Last Modified: Sat, 08 Nov 2025 19:23:19 GMT  
		Size: 91.7 MB (91720092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16c6f464bb82eaf075a7294a9be348dd5cd345ccab6c057775adf04a8c2e826`  
		Last Modified: Sat, 08 Nov 2025 19:23:07 GMT  
		Size: 12.8 MB (12777832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1b90adf840e08598226a7fa8a0d1494586697237db10948836e4077e379bd1`  
		Last Modified: Sat, 08 Nov 2025 19:23:07 GMT  
		Size: 9.2 MB (9242579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed8fc0aba2a1db9122c0e4e355209e8e8d41ca5cb76dba3a580e20fd0f3226a`  
		Last Modified: Sat, 08 Nov 2025 19:23:06 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d93ffd1c8a567b3f5a85852daa2f475b0696399d77cfc525e4a01a00605110`  
		Last Modified: Sat, 08 Nov 2025 19:23:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:783f9f38515b7dc40ef306c125b0cc6fbac49e8a91dc928a963ba5e25b04db7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6249387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad61180a85e38ef905d08abd0fc3cb802cd378a7881b8dd7828d4e12a2860b24`

```dockerfile
```

-	Layers:
	-	`sha256:e1912dced348278aac4a68b794eaea5c3535a85f17211b23d62ba43c4dbb8589`  
		Last Modified: Sat, 08 Nov 2025 21:28:37 GMT  
		Size: 6.2 MB (6230954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093b3540f401137bc0b5d45c4a9dbf7b770998f94f57e8656db7ace85acb6669`  
		Last Modified: Sat, 08 Nov 2025 21:28:38 GMT  
		Size: 18.4 KB (18433 bytes)  
		MIME: application/vnd.in-toto+json
