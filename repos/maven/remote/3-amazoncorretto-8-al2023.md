## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:95de6272851fe6dde7aa6bdd12beb15d8536de95a33191b574fe5eb9dc379c7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:c9a1229196e6dd187aa2b6e979401272d66c2baea5b11d70632008585a7b5dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **497.9 MB (497920190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247a43e99728869d903f0d6015f92e192e74c18419d5462bbcbe632b70fa9465`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:17:48 GMT
ARG version=1.8.0_472.b08-1
# Thu, 18 Dec 2025 01:17:48 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:17:48 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:17:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 18 Dec 2025 02:23:05 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 18 Dec 2025 02:23:05 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 18 Dec 2025 02:23:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 18 Dec 2025 02:23:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 18 Dec 2025 02:23:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 18 Dec 2025 02:23:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 18 Dec 2025 02:23:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 18 Dec 2025 02:23:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 18 Dec 2025 02:23:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 18 Dec 2025 02:23:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 18 Dec 2025 02:23:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 18 Dec 2025 02:23:06 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 18 Dec 2025 02:23:06 GMT
ARG USER_HOME_DIR=/root
# Thu, 18 Dec 2025 02:23:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 18 Dec 2025 02:23:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 18 Dec 2025 02:23:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e34bac1605a4e3c5373bbcccfc49cb6f259622f2e93d19c2553d6de26db99f5`  
		Last Modified: Thu, 18 Dec 2025 01:18:53 GMT  
		Size: 330.9 MB (330887757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f75f538a25cd404c91fd0599e2aa2ed00dc2d9f2f53746f134f69b2ac3a3dab`  
		Last Modified: Thu, 18 Dec 2025 03:20:31 GMT  
		Size: 98.3 MB (98312532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4cf070692c16a8036485d6e16eb3c8ef5261c512c5aafc68887c371d9a57ba`  
		Last Modified: Thu, 18 Dec 2025 03:20:15 GMT  
		Size: 5.4 MB (5418155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c4e3660aa6c11d5ba6838a0d5e204604f1597b44525554827f0b5bef7ec589`  
		Last Modified: Thu, 18 Dec 2025 02:33:35 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd060f2d18a72b6d7e81808b9ada004ca69c03f73fb1c5b8fad2d59a45721e70`  
		Last Modified: Thu, 18 Dec 2025 02:33:44 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f42901fe56640a7896addfc6a3044c3b341d30b09c8ef58d884c5334d18b059`  
		Last Modified: Thu, 18 Dec 2025 02:34:07 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:841d97a9abf8ecbdf83457575144567da8e220013ac1eaee4be4188375ff2a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13846492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0e3fe8eae159a5e642fbf71d9743d389eeeff6c67a806262610b175afb9907`

```dockerfile
```

-	Layers:
	-	`sha256:8b2471a3ecc3d8c62b451d552e760b5260bbf02a686f9df241c52b859deabde5`  
		Last Modified: Thu, 18 Dec 2025 03:28:51 GMT  
		Size: 13.8 MB (13828216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c6edf94d3823822eb307b2e1e171647bf5d581a04c35f3713589efc1110b67d`  
		Last Modified: Thu, 18 Dec 2025 03:28:52 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:853493a1ab4303cc4b51bd696f120e183554527849575ef23bf06c25a138e98c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.8 MB (287829482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8280968dee14256276aaa832814a1be16038c1a7aed1184701b6ffe64d72d8b6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:05 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:05 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:25:23 GMT
ARG version=1.8.0_472.b08-1
# Thu, 18 Dec 2025 01:25:23 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:25:23 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:25:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 18 Dec 2025 02:23:44 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 18 Dec 2025 02:23:46 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 18 Dec 2025 02:23:47 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 18 Dec 2025 02:23:47 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 18 Dec 2025 02:23:47 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 18 Dec 2025 02:23:47 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 18 Dec 2025 02:23:47 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 18 Dec 2025 02:23:47 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 18 Dec 2025 02:23:47 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 18 Dec 2025 02:23:47 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 18 Dec 2025 02:23:47 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 18 Dec 2025 02:23:47 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 18 Dec 2025 02:23:47 GMT
ARG USER_HOME_DIR=/root
# Thu, 18 Dec 2025 02:23:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 18 Dec 2025 02:23:47 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 18 Dec 2025 02:23:47 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de3320244c0c5e8689ab3369d4e7efe9e9c7b32724b174d2d0f966d353d04e2`  
		Last Modified: Thu, 18 Dec 2025 01:25:58 GMT  
		Size: 117.9 MB (117927137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73768a15452176df3a7eaca650972d27aab3762fbd4b7d186d9482337903246`  
		Last Modified: Thu, 18 Dec 2025 02:24:34 GMT  
		Size: 95.0 MB (94986035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1beadf67274670bdfa0d8ee4989022e1aebf95e0fee5c0e5fb5220ed834ff7`  
		Last Modified: Thu, 18 Dec 2025 02:24:13 GMT  
		Size: 12.7 MB (12729570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91234335f959560dc6b713b3471161b2ab6669b7f0836090da19c0b94515d0a`  
		Last Modified: Thu, 18 Dec 2025 02:24:12 GMT  
		Size: 9.3 MB (9312248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9beab7d49df0c3de07da38e215e1f718dac074bbaede31000f7ff5c52e0983d7`  
		Last Modified: Thu, 18 Dec 2025 02:24:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2754e19f1967fbcf9205292a4c4afa91a407c39d48d6cf9e79b2d700d2fa6f02`  
		Last Modified: Thu, 18 Dec 2025 02:24:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:3210fea03dee45c9a435deef47a7fef27393e7cafd44731833b7dce7776cc9c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5203bdfd11890450e6c473d8fe4335d4f7338b64c77a22baa9d29db303b81b76`

```dockerfile
```

-	Layers:
	-	`sha256:2093d999fcbc6edd91cc2cc3cc02f804055901a8c55201fa9b0e4240fd857f53`  
		Last Modified: Thu, 18 Dec 2025 03:29:03 GMT  
		Size: 6.6 MB (6609537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2573f9f392685518c5b69f5980eef709cb9b20d45888455cfad52088d57bd6eb`  
		Last Modified: Thu, 18 Dec 2025 03:29:04 GMT  
		Size: 18.4 KB (18429 bytes)  
		MIME: application/vnd.in-toto+json
