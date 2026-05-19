## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:5157b5b1a13b633b08b40a21d3574f7fc522e5678fe6b811ecc1c643d47e8354
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:056f75ebefd2011739612ce3f9d3e31b34dd1c80245ac930db7a1d68d57ab477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345235785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6141650eaad3a4f3148fc946950f37d1cfe010419cf01fbe9350312b19d6d676`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:18:06 GMT
ARG version=11.0.31.11-1
# Sat, 09 May 2026 00:18:06 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:18:06 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:18:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 18 May 2026 22:40:53 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 18 May 2026 22:40:55 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 18 May 2026 22:40:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 18 May 2026 22:40:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:40:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:40:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 18 May 2026 22:40:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 May 2026 22:40:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 May 2026 22:40:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 May 2026 22:40:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 May 2026 22:40:55 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 May 2026 22:40:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 May 2026 22:40:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 May 2026 22:40:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e8ef4b5fb927c0c86de92b3247666810672cabd7e058c5262c750d5d34c79`  
		Last Modified: Sat, 09 May 2026 00:18:27 GMT  
		Size: 153.5 MB (153472393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c8a2ffb732af1d257465165c98c4295ce16ca583a97b3af37b0c4efaa280d0`  
		Last Modified: Mon, 18 May 2026 22:41:16 GMT  
		Size: 115.3 MB (115295700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f27ae4efd65170750d82ce6aa7ef96532ccab2cc098baf3bb772abbc8dd21e`  
		Last Modified: Mon, 18 May 2026 22:41:13 GMT  
		Size: 12.5 MB (12529912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e04d3d7c6a6a8ebbf09ede0556baa11add33a0287a36ee02c0e8429e2aa739`  
		Last Modified: Mon, 18 May 2026 22:41:13 GMT  
		Size: 9.4 MB (9359967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11a54fcf5fcd18e7b58c857060929ba9bd1b1711f86eb1000c73b96d855dec3`  
		Last Modified: Mon, 18 May 2026 22:41:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a487db2eed7e7a19ee1b43cb72715be3c2c430bd2b1bc26837b4c7557866dc`  
		Last Modified: Mon, 18 May 2026 22:41:13 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:2c4ce4bc1f29c8b534a295130ed363b25be0a267a66c5bfde03674d1ad949c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6280269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1a33c93a2bae0b4cf9e229e9fdfa8ff08526ed1a10add1bd63b6c57b2e9f6e`

```dockerfile
```

-	Layers:
	-	`sha256:f497fb40261e180e46ba560a871e5ab8325c81be256e66fdcaafb1c74acb0f3b`  
		Last Modified: Mon, 18 May 2026 22:41:12 GMT  
		Size: 6.3 MB (6263980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bca60e2b29e33bb76bf430f1733ae4bf00200abafe68b00d24823548e1b5576`  
		Last Modified: Mon, 18 May 2026 22:41:12 GMT  
		Size: 16.3 KB (16289 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:673fcd37fdd7cc5865c1efeeca31478c17fe22a53a0613493bf88363a5278c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341711350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ded156957663558f7cbf740d091c5262f833b853a1bdcf7a766ed5afa8e28c4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:15:25 GMT
ARG version=11.0.31.11-1
# Sat, 09 May 2026 00:15:25 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:15:25 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:15:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 18 May 2026 22:40:43 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 18 May 2026 22:40:45 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 18 May 2026 22:40:46 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 18 May 2026 22:40:46 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:40:46 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:40:46 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 18 May 2026 22:40:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 May 2026 22:40:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 May 2026 22:40:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 May 2026 22:40:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 May 2026 22:40:46 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 May 2026 22:40:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 May 2026 22:40:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 May 2026 22:40:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8763299e6b6a5390624676a6a883b80df08afbd0fe328882a6aa37029abd1826`  
		Last Modified: Sat, 09 May 2026 00:15:47 GMT  
		Size: 152.1 MB (152051820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a8664ebfb2c999f0c23ba6e13c2bb56c0cb7c24be9c381c78e1591cdab757d`  
		Last Modified: Mon, 18 May 2026 22:41:09 GMT  
		Size: 114.0 MB (114047422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a281d0116a65379a8cf51977fe7fcbc0751e4904fa67f2054177771ffbe2eeb`  
		Last Modified: Mon, 18 May 2026 22:41:06 GMT  
		Size: 12.8 MB (12794153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ecec540bab7de5b05a5b9c21cf8f10123b15fc0ceaccfdc90ff2161161fc87`  
		Last Modified: Mon, 18 May 2026 22:41:06 GMT  
		Size: 9.4 MB (9359971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317d6e06032894932cc2246052208f3b6d457c4bb1906e29669475eb5ecb9fb4`  
		Last Modified: Mon, 18 May 2026 22:41:05 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2261e1eb111b1df198832cf3054b4916cd71435a5261862660d5b535ec1cbf`  
		Last Modified: Mon, 18 May 2026 22:41:06 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:eb4e5d2222ffeceafbe69a9c3c0545729f221322406e3af5be31bdb1c64c71c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6280191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4516a813193cb7bfa9c5ee82de57857c95d67b5cee13c5f9804749b5bf6854d3`

```dockerfile
```

-	Layers:
	-	`sha256:c3a86651aa094ea168191f9b4fc281ac352db8b4f9fb1dad9e8dfbcdc67b1fdf`  
		Last Modified: Mon, 18 May 2026 22:41:05 GMT  
		Size: 6.3 MB (6263754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac7ab3adffeac1d850ab91718c2998f21c20537cfef3a89c58443af6075a36ec`  
		Last Modified: Mon, 18 May 2026 22:41:05 GMT  
		Size: 16.4 KB (16437 bytes)  
		MIME: application/vnd.in-toto+json
