## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:0861511b0a039c725dd21e4064ea8619d1d4bedc2a2833e85156a9e20eacfec3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:2bb7476e39adbfb26dae8e9bb0db8c7d0f066cf39edaec319c3a34f82925119f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.6 MB (494603855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5fea790be6d14b8e142b7afa576d452384c9d579fa46229dc3ce39e2241d13`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 06 Nov 2025 22:15:48 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:15:48 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 23:12:14 GMT
ARG version=1.8.0_472.b08-1
# Thu, 06 Nov 2025 23:12:14 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 23:12:14 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 23:12:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Sat, 08 Nov 2025 19:24:58 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Sat, 08 Nov 2025 19:24:59 GMT
RUN yum install -y openssh-clients # buildkit
# Sat, 08 Nov 2025 19:24:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:24:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:24:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:24:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:24:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:24:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:24:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:24:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:24:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:24:59 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:24:59 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:24:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:24:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:24:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7857af70cc37714ae4781f1d58242c7667f933ef8be05b0636d2c50e756263b2`  
		Last Modified: Wed, 05 Nov 2025 21:09:20 GMT  
		Size: 54.0 MB (54000503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a466983e04f75b0240d48e3a95c546707491d065df8baa3200522fb42bb1f95`  
		Last Modified: Fri, 07 Nov 2025 00:12:03 GMT  
		Size: 330.9 MB (330868155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4040236c688d2c0727e9bb67d7c490e27b1f70fac7c0c259df2ee8548d480e`  
		Last Modified: Sat, 08 Nov 2025 19:25:45 GMT  
		Size: 95.0 MB (95040838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bfd52c6f322dc49bb4867279a0157d65c9289584f6f8a19c20294df4bd52d9`  
		Last Modified: Sat, 08 Nov 2025 19:25:33 GMT  
		Size: 5.5 MB (5450743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7884dc89f5b9ff034d9c996e8697e9c0e8fde182081765e9bb76905f03abae66`  
		Last Modified: Sat, 08 Nov 2025 19:25:33 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0bb39009c728ae659e3cc32f5e085af838c040277288ba8a2414b8eb5637da`  
		Last Modified: Sat, 08 Nov 2025 19:25:32 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af16f1541933cc27e318633e228461cefa6a582a6207bc5940b266759ede6fc9`  
		Last Modified: Sat, 08 Nov 2025 19:25:32 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:579e1003135ed1eac5ee071a6ff7abe4a70b573d20d78be0f261b72320ee68d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13846475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec38413256964217e2a07bb310f5b8ed02365f385d86fa78f9ff7f4c2cc1c604`

```dockerfile
```

-	Layers:
	-	`sha256:4f171a3d6161a3b4f74f6b6bbc4b850d4bfb1196ae23e5132ffe74b46b118d1b`  
		Last Modified: Sat, 08 Nov 2025 21:30:13 GMT  
		Size: 13.8 MB (13828199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccdb1176590c4c7c6ea2cc9184a1f7cdd6b494239509e3b93d2dc0806850019c`  
		Last Modified: Sat, 08 Nov 2025 21:30:14 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:be8b7439d41c4c00a4786f49c1d42efdf1a38d9a57043b955e54735e846e32e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284571734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e582447203581a20105bce19db7db1f966a7fbb571e38abd48d1c5749ef62567`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 06 Nov 2025 22:01:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:01:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:11:25 GMT
ARG version=1.8.0_472.b08-1
# Thu, 06 Nov 2025 22:11:25 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 22:11:25 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:11:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Sat, 08 Nov 2025 19:24:29 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Sat, 08 Nov 2025 19:24:31 GMT
RUN yum install -y openssh-clients # buildkit
# Sat, 08 Nov 2025 19:24:31 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:24:31 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:24:31 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:24:31 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:24:31 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:24:31 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:24:31 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:24:31 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:24:31 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:24:31 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:24:31 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:24:31 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:24:31 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:24:31 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6d0dad3595837e5d244dadb238b6a2012108ea03c6af3e9c48dc16cad05f98d0`  
		Last Modified: Thu, 06 Nov 2025 01:49:48 GMT  
		Size: 52.9 MB (52901684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d1f499ea2be350aeea557e5a54efc605e09542e2e0eb46c78b5696360c7ce2`  
		Last Modified: Thu, 06 Nov 2025 22:12:07 GMT  
		Size: 118.0 MB (117956781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70df662b14801aa614e4770f12cacbb51431c96307a055ee8ade58ca01ddb07e`  
		Last Modified: Sat, 08 Nov 2025 19:25:08 GMT  
		Size: 91.7 MB (91712253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e0374d68b236fea8bd9f087ea980fa6839814bbeb7c95155d4b46b55e733b`  
		Last Modified: Sat, 08 Nov 2025 19:24:57 GMT  
		Size: 12.8 MB (12757382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e7f9ab7aafbaaed8ec7824de63758804441fd8f08ce3f2f971895e0dd91d94`  
		Last Modified: Sat, 08 Nov 2025 19:24:56 GMT  
		Size: 9.2 MB (9242594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0191cac76cc7718b4d118a731d71e741b4436c89320d1d9d1b0517094755c937`  
		Last Modified: Sat, 08 Nov 2025 19:24:56 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4806793fee9e9134c3d91d8a5e240d27ffa0488498c86579fc6379d1b6707f75`  
		Last Modified: Sat, 08 Nov 2025 19:24:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:165c4ea1135945850c68799b4dd9fc4af75668eedf993db8921ca7aa5bf9a0a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af44ef83ec5aaa3c54713af755971012b2a87abf4753fa8caf98fedc9f21e86`

```dockerfile
```

-	Layers:
	-	`sha256:f7a3e000261125e758eea372617868a86bb9f5a39ad8e15a8ab04dea45ab8c6b`  
		Last Modified: Sat, 08 Nov 2025 21:30:24 GMT  
		Size: 6.6 MB (6609530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20c0194e50166d6aaa46e3dae84827056b6125d3504481da2e161ed1a7b0b263`  
		Last Modified: Sat, 08 Nov 2025 21:30:24 GMT  
		Size: 18.4 KB (18429 bytes)  
		MIME: application/vnd.in-toto+json
