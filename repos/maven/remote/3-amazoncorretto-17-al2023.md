## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:69f396497512bc7f910d8638cf43a12a8e71897a6c136be20608924459f15903
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:0282d5f8acb65e837becc579f43d853a4694b3a34777b7770b83bbad65e3324a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (286013040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6226ff7309e4076d7b4ea7d3c8aca2a13bdc0006b65829b9f845a76586b7dd0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.12.7-1
# Tue, 20 Aug 2024 18:12:59 GMT
ARG package_version=1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:9a0f8ca95549caa504c79acef976bd6b204271a0f61eacfa1a045c2ce6bb0d43`  
		Last Modified: Tue, 17 Sep 2024 02:04:40 GMT  
		Size: 52.3 MB (52324958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c81cf3281307c3350c0aa087036997fbd111ab613d9855fd088b8cf9c416c3`  
		Last Modified: Tue, 24 Sep 2024 01:56:54 GMT  
		Size: 157.1 MB (157085539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf10e1d8b80e0ba166479544942adce89fc2e6c403cb2f659524638763e349a4`  
		Last Modified: Fri, 27 Sep 2024 19:56:01 GMT  
		Size: 54.9 MB (54914906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16df7d457ba465bad3ca8eafcef4373a29b985796be12e1243ec3b7084ced2b`  
		Last Modified: Fri, 27 Sep 2024 19:56:00 GMT  
		Size: 12.5 MB (12516157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a43b1ed52c62f5b74e1eaaeb2ecc2f9dfbc844ef5046287b49b05d622bb9c14`  
		Last Modified: Fri, 27 Sep 2024 19:56:03 GMT  
		Size: 9.2 MB (9170441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c911bd5d01c7c274942691a923cd3edb658b00d35020b5db3bc3ac1c2ab623`  
		Last Modified: Fri, 27 Sep 2024 19:56:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af284bdbf3e039bd4bdbd37e0becdede6252d552553852955c5bfdc2bad81b0f`  
		Last Modified: Fri, 27 Sep 2024 19:56:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:598f508db37e15b5c30ddddfe952b43f17f517560fb6b022173bcf4f6ab33e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6244204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0151d42ea3b71c86b0fa9463aa78fbeb2069f104ff075c677a184d1b483a883`

```dockerfile
```

-	Layers:
	-	`sha256:445cdf2017df085708c5dfb3612e027437c03316b5d8b4e163851797f871b480`  
		Last Modified: Fri, 27 Sep 2024 19:56:00 GMT  
		Size: 6.2 MB (6225921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad33f9b19fd9b1bb44b2234f6e57a0483f4ee7fe3c2101d4e2805a275caee05d`  
		Last Modified: Fri, 27 Sep 2024 19:56:00 GMT  
		Size: 18.3 KB (18283 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c753f76501c6d229091dc3675393e6f51dc2abf9c9abe77c3aa9f63391e0c5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283648468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce736b9e62ea602a1eb8087fb03509664a8447a33e859ed45136facb9cd1f41`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /rootfs/ / # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["/bin/bash"]
# Mon, 19 Aug 2024 08:57:28 GMT
ARG version=17.0.12.7-1
# Mon, 19 Aug 2024 08:57:28 GMT
ARG package_version=1
# Mon, 19 Aug 2024 08:57:28 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENV LANG=C.UTF-8
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 19 Aug 2024 08:57:28 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8e0a984b7f222102e6d0bbaa2dac67ec2c00d5735727c1b5e918160055b8f617`  
		Last Modified: Tue, 17 Sep 2024 02:35:27 GMT  
		Size: 51.4 MB (51425992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826c475048ea1b65f38c25b766ec5b7a62d1423fdbbd88c0f57afc100a68f749`  
		Last Modified: Tue, 24 Sep 2024 02:37:03 GMT  
		Size: 155.8 MB (155785983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67057e8c7804ae0beb93207148a0de5b4ef8df6e3a725487a404848582586130`  
		Last Modified: Tue, 24 Sep 2024 03:09:43 GMT  
		Size: 54.5 MB (54476427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ff993acba8b9126d26bddc28033b79d09e5aaa4d8f01f0de6dcb089a1e8c0a`  
		Last Modified: Tue, 24 Sep 2024 03:09:42 GMT  
		Size: 12.8 MB (12788584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfe7ef1d3c013b9fc5284850b71cc35b4a3435628066fff013bfd46863310c1`  
		Last Modified: Tue, 24 Sep 2024 03:09:42 GMT  
		Size: 9.2 MB (9170441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e5427b73d523e5648eeb5dcf2973cec108da063cea73fca31e293850132865`  
		Last Modified: Tue, 24 Sep 2024 03:09:42 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dd344e02c1967bc7eff327cda979396b6115467a4d9dcbdc71cb78804349ee`  
		Last Modified: Tue, 24 Sep 2024 03:09:43 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:a46c21421e691e51fceca56190b64499323fb44add63372c8971781d4f611bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6243843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc79f76429bcfde2e7804316f8e149f35439992aa014dde097d72b29bfacd2b`

```dockerfile
```

-	Layers:
	-	`sha256:975f00478bed4ffc6a2f5d4dd80178e6f24bd98b8b1b5583d8d73c6bdb4939fd`  
		Last Modified: Tue, 24 Sep 2024 03:09:42 GMT  
		Size: 6.2 MB (6224835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02d740b561a89b2c0a657c0ec9d9177eb7b42d8e6695d89c2f7a095ddc2c2810`  
		Last Modified: Tue, 24 Sep 2024 03:09:41 GMT  
		Size: 19.0 KB (19008 bytes)  
		MIME: application/vnd.in-toto+json
