## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:06621d3eee441c7b3e6c1e7205bd2f98a3cb295ca1d937a358b903e1f9f77a40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:5b4c168fae7947be5938ad996634b6c795d675e5c429c6aadda6b984908af017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.7 MB (511664871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1856dc06a6a789b7e8bb868d609c94df83fceafa59685f3f789adef6bd76266d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:24:08 GMT
ARG version=1.8.0_482.b08-1
# Wed, 15 Apr 2026 21:24:08 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:24:08 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:24:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 15 Apr 2026 22:52:43 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 15 Apr 2026 22:52:44 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 15 Apr 2026 22:52:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 22:52:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:52:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:52:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 22:52:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 22:52:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 22:52:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 22:52:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 22:52:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 22:52:44 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 22:52:44 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 22:52:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 22:52:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 22:52:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d865abc8958d904089134e6afbdd634333b4eafd515c4ac99168fa07172cc37`  
		Last Modified: Wed, 15 Apr 2026 21:25:04 GMT  
		Size: 330.9 MB (330924355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423fec443655fe616251b4a093af1c0a21808e021f6c0cc09c79ae830107e576`  
		Last Modified: Wed, 15 Apr 2026 22:53:15 GMT  
		Size: 111.4 MB (111401066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beef259f926aa67eedd8e3b20d022102dd79f974d2ca6a208684f4a3c97f97b0`  
		Last Modified: Wed, 15 Apr 2026 22:53:13 GMT  
		Size: 5.5 MB (5455960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a78a38b7f13a069e759de76f4ef7af17cf4430bc708e5267ad0abe9c2a8b05`  
		Last Modified: Wed, 15 Apr 2026 22:53:13 GMT  
		Size: 9.3 MB (9311195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295c7311102283438cb4cf5f3388fcc5ceb697ad8d7701a0291f11b25434a796`  
		Last Modified: Wed, 15 Apr 2026 22:53:12 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39cdce144aebb77673cb71f11b41b87f0f7c6e9139f0b249ce594ebc804c9fa`  
		Last Modified: Wed, 15 Apr 2026 22:53:14 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:4a2de83c64243bb233550dbc782aff14a433a1ea50f0e435260cbd97b17b4c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13852933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ad0380903be219c3165232ed8649d1913583516e46faf01a470f4bdd89c256`

```dockerfile
```

-	Layers:
	-	`sha256:58b0472686665d5c12b0642ef9d84fc14688153432ebee349334e7368ac75f30`  
		Last Modified: Wed, 15 Apr 2026 22:53:13 GMT  
		Size: 13.8 MB (13834652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15cde058ce40e1b70d8cfa750445d75ebc3809d20cb3c1fbccef5bb59e91f043`  
		Last Modified: Wed, 15 Apr 2026 22:53:12 GMT  
		Size: 18.3 KB (18281 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4de552c1f24ea7daabd4e91ae8cd764276410ec9602cf12e11c5d4a234d7ea98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301387019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4916853fd3b04a968393af98a6dcc0205c89acc764fc860c92f3b1b851aa3b3c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:38:18 GMT
ARG version=1.8.0_482.b08-1
# Wed, 15 Apr 2026 21:38:18 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:38:18 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:38:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 15 Apr 2026 23:19:03 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 15 Apr 2026 23:19:05 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 15 Apr 2026 23:19:05 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 23:19:05 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 23:19:05 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 23:19:05 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 23:19:05 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 23:19:05 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 23:19:05 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 23:19:05 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 23:19:05 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 23:19:05 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 23:19:05 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 23:19:05 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 23:19:05 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 23:19:05 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f5d61b99295ea1fb2b1e68202646ef07a17e94b3434367d80f0334607aa4c4`  
		Last Modified: Wed, 15 Apr 2026 21:38:39 GMT  
		Size: 118.0 MB (117961731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce393b02b53a9d59748c770e0a06f4fed1a1e35fec047116992dfcff68016575`  
		Last Modified: Wed, 15 Apr 2026 23:19:25 GMT  
		Size: 107.9 MB (107895891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a28f066b03a07ecac40d05b855ec23b298ec7fbda3521aab20dbf6f9e82c81d`  
		Last Modified: Wed, 15 Apr 2026 23:19:22 GMT  
		Size: 12.8 MB (12774421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9d178bdbcc6455d5ebdb7064225927d48df20aa7c4b04cdb7809c8a2beca28`  
		Last Modified: Wed, 15 Apr 2026 23:19:22 GMT  
		Size: 9.3 MB (9311195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183154482c51e95d384e9b1335c24cdef0d7e691f1838d2c0620f58b4d1491ad`  
		Last Modified: Wed, 15 Apr 2026 23:19:22 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5dfbd9c622f1eb0adcf72e3a2563f6f8a3f8f30f3ac9dded8e5e6488aedf9a`  
		Last Modified: Wed, 15 Apr 2026 23:19:23 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:cadad3338762baadeda903cab6a8226e4036d146294ac99cab852ee191168585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6634408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b841dfded155d8aa1150162cea746e5996a678bd4502fde7c3b15502d932ba`

```dockerfile
```

-	Layers:
	-	`sha256:5694b4551343178bff75c100de300e72c2d9f7f21e1b6474b9036b9cad65fe42`  
		Last Modified: Wed, 15 Apr 2026 23:19:22 GMT  
		Size: 6.6 MB (6615973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97785628c747de7067c99d9cb892d6f8ad9f5f44f8b3932759ab5857ad42d12`  
		Last Modified: Wed, 15 Apr 2026 23:19:22 GMT  
		Size: 18.4 KB (18435 bytes)  
		MIME: application/vnd.in-toto+json
