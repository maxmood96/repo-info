## `maven:3-amazoncorretto-24-al2023`

```console
$ docker pull maven@sha256:51dcf026f1f7fd44cb2b347c1a5501745acd72102b3ecd00d20e8f8537676832
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-24-al2023` - linux; amd64

```console
$ docker pull maven@sha256:24d3c55a3126e8a683ffa1723764384c8d3cadfa300783e3e72c51b720e4bd26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.0 MB (345020067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5128c2342838e09fb8767b1731876ae2fa136a0d1b159c977b14ac2f982e8d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=24.0.2.12-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Tue, 29 Jul 2025 19:33:31 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 29 Jul 2025 19:33:31 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 29 Jul 2025 19:33:31 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 29 Jul 2025 19:33:31 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 29 Jul 2025 19:33:31 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 29 Jul 2025 19:33:31 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 29 Jul 2025 19:33:31 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 29 Jul 2025 19:33:31 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 29 Jul 2025 19:33:31 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 29 Jul 2025 19:33:31 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 29 Jul 2025 19:33:31 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 29 Jul 2025 19:33:31 GMT
ARG USER_HOME_DIR=/root
# Tue, 29 Jul 2025 19:33:31 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 29 Jul 2025 19:33:31 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 29 Jul 2025 19:33:31 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:989d4a8a2accd45b05933473a235ea401b52185c3db1c1bf8d953380af6a7341`  
		Last Modified: Mon, 18 Aug 2025 22:37:34 GMT  
		Size: 53.9 MB (53868730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1514838d081fb5e63a66fd4fbb6c3b2e1096e3a522459c8cef3c5e0d4069773f`  
		Last Modified: Mon, 25 Aug 2025 20:54:53 GMT  
		Size: 187.4 MB (187384753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95906a128a8eeedc7facaa6a5e65a4a165fb59dc08ac25c3cefe800044ff910c`  
		Last Modified: Tue, 02 Sep 2025 01:14:23 GMT  
		Size: 94.5 MB (94522963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ecc9379d64f2d67fc7cf5419f5c306390f2e7d8b4eb23e0f87bc82253cb6f5`  
		Last Modified: Tue, 02 Sep 2025 01:14:13 GMT  
		Size: 9.2 MB (9242578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8962954447b87127295552085e39808d6caa429f674dc08e7e12d582aeaad54c`  
		Last Modified: Tue, 02 Sep 2025 01:14:12 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a101a98203fce95521ee118cedcefb688c5f4187a5c101886acbb23899727a`  
		Last Modified: Tue, 02 Sep 2025 01:14:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-24-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:a5c58d8ab1e6de2e23900c82e0d55fe195915bb1a13b090f1e7461effcccd2d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6224086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2209d699c1f7bf9530e178c2d8c3ba751c495ac3882c02c75d251fd15bc20a4b`

```dockerfile
```

-	Layers:
	-	`sha256:71c6a34dde675b54ff510833a1a2cc6a36a5b1bf184d4f7f0e4ae2e60c9ce64b`  
		Last Modified: Tue, 02 Sep 2025 02:28:35 GMT  
		Size: 6.2 MB (6207698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fee6e5b728f8d5bc2d7419d0b5fbec22ed1c17a3ce5dac94c71937f92cedfa3`  
		Last Modified: Tue, 02 Sep 2025 02:28:36 GMT  
		Size: 16.4 KB (16388 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-24-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:1a9c1503eafb7dd7c5c5ff3734a191fcb095fae0a6923c75d0bb3228afaca2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.4 MB (341372002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e553c295b971080ba77afd62c50ca1cbb57aa3056d80ea2321d7cc3b8ab45e8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=24.0.2.12-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Tue, 29 Jul 2025 19:33:31 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 29 Jul 2025 19:33:31 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 29 Jul 2025 19:33:31 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 29 Jul 2025 19:33:31 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 29 Jul 2025 19:33:31 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 29 Jul 2025 19:33:31 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 29 Jul 2025 19:33:31 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 29 Jul 2025 19:33:31 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 29 Jul 2025 19:33:31 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 29 Jul 2025 19:33:31 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 29 Jul 2025 19:33:31 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 29 Jul 2025 19:33:31 GMT
ARG USER_HOME_DIR=/root
# Tue, 29 Jul 2025 19:33:31 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 29 Jul 2025 19:33:31 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 29 Jul 2025 19:33:31 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f0b7d54214a6f9c2c7698f71fb06f2128097c3f9d97269e3d449f7639c142381`  
		Last Modified: Tue, 19 Aug 2025 02:47:54 GMT  
		Size: 52.8 MB (52768497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3757bcfa7490d81cf91f8e40a946b5e9b5fb6ef23be79baf6e450f183a8b11a9`  
		Last Modified: Tue, 26 Aug 2025 00:09:32 GMT  
		Size: 185.4 MB (185426677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db8f347de1d8da8a0f61ed7c886a4153309eedc4f14d96a942d6d3ddf211afe`  
		Last Modified: Mon, 25 Aug 2025 23:40:01 GMT  
		Size: 93.9 MB (93933188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db31b48ada216d506b9c9a9064079bd3f01793f787efa485f1fb53d9f5f7ff9`  
		Last Modified: Mon, 25 Aug 2025 23:39:56 GMT  
		Size: 9.2 MB (9242596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9eb83693e79256f1cb7898caec1b687454e1a4fe9a001ac03281855dd95973`  
		Last Modified: Mon, 25 Aug 2025 23:39:55 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a054e7920c750416b8a2f7e868149d64ba5c113e478119effcc98d0d029df7`  
		Last Modified: Mon, 25 Aug 2025 23:39:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-24-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:1d728dc2bec090a0168bd87a34b2d6e217f753ef8abd7c15c917589186038991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c4e6b98d41eb64010043854bed13be48ab2ce879b747cb9bf4e203e59bd20e`

```dockerfile
```

-	Layers:
	-	`sha256:e549b87ed4e1da90b020e3d13d1f05aeb6675dd018bb630e1aead3eb5aa66699`  
		Last Modified: Tue, 26 Aug 2025 02:28:05 GMT  
		Size: 6.2 MB (6206642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf941552e7c48e5bac4094bd07871baac04a3e2723098fbbd88cb0125d359e7`  
		Last Modified: Tue, 26 Aug 2025 02:28:06 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json
