## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:7a7371470aec55dd520b2c88a0e5d5d6448386d0db91ddb1228a60c7b204a88e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:8a86ee32347a78b5824c8aea9eeccad8c104d1528cb862cf40a18772cb6a69c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307095268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009fb9558bc63580e3475f5c0140f4b0a45bef583b4adf8321ca7df025358955`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sun, 22 Jun 2025 10:21:55 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN yum install -y openssh-clients # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b32084d69388d1a83137a801da01717a35f31eef39012331796a50e2c2385667`  
		Last Modified: Wed, 11 Jun 2025 22:05:56 GMT  
		Size: 53.6 MB (53570360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e22b7a3e0e2583ad5c1c22f7798d8decd9e006b02396cf14e7e7e6255ef7d8`  
		Last Modified: Fri, 13 Jun 2025 17:12:47 GMT  
		Size: 156.6 MB (156612002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf6515d81f004c6ed21d6d70b1391f361e9b182bd731add123068448ed9727b`  
		Last Modified: Mon, 23 Jun 2025 17:31:24 GMT  
		Size: 75.4 MB (75420195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a012a2003a005a421248eb89e49a643759c2aa75932c4245d9f69e2d420fdb3`  
		Last Modified: Mon, 23 Jun 2025 17:31:19 GMT  
		Size: 12.5 MB (12538265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90afec41e4cd577df148ae45a054f6aa943816be7eb72b416e62525fc7c0b5eb`  
		Last Modified: Mon, 23 Jun 2025 17:31:24 GMT  
		Size: 9.0 MB (8953407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5189954779bbcb03d93f5897ceee44355b422a9e59c0815cf38def83a08dc98b`  
		Last Modified: Mon, 23 Jun 2025 17:31:22 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50d3b753874acd639788ee0e31d9a0a2c2ccf98e38482f7fee1285a29f7ddf1`  
		Last Modified: Mon, 23 Jun 2025 17:31:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:7770cd6e56bcca102436dd643c7a34aa4da9376b3ea5e4605ca33ba59c9ee841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6248408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370b83414d72ad8d295f9ea0ef7a2963566828de89d5c25517b4299845183ce6`

```dockerfile
```

-	Layers:
	-	`sha256:d775e5927177734af6a57f57840a65ad1935578b1a2ec0084f0d1a2427a2951e`  
		Last Modified: Mon, 23 Jun 2025 20:28:19 GMT  
		Size: 6.2 MB (6230080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0f4de9bcd3bb37730fadddaac0afa42b7e24bd3c5ace6cce085f2be1cc6116`  
		Last Modified: Mon, 23 Jun 2025 20:28:20 GMT  
		Size: 18.3 KB (18328 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a22a75b1e9f4c4f742970892fc8c3084466c368bdd89980ad9e5646bb315b6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304273745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3c817de0da73e61e97fa65e2e93dc2041e221026a4694f283e01ab55ae5cb8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sun, 22 Jun 2025 10:21:55 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN yum install -y openssh-clients # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2913b957e7cca1539a6d274307081564a7142eae485bcd51683bbef9106592aa`  
		Last Modified: Thu, 12 Jun 2025 03:47:32 GMT  
		Size: 52.5 MB (52481692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fed9c8d4dec8b3da0af7e313b2d107387b334695977a6d58fdeeb51d8d32ecc`  
		Last Modified: Fri, 13 Jun 2025 21:53:25 GMT  
		Size: 155.5 MB (155473398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd72ebe0ca4bf0cb1a2b2391e4906d144fd9189ef5019a751405f492b6bde967`  
		Last Modified: Fri, 13 Jun 2025 21:23:40 GMT  
		Size: 74.5 MB (74542500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b734c4fd464f76b14bebbf18ee8d940a383ba378d8c48905f7b95b8aa47650cc`  
		Last Modified: Fri, 13 Jun 2025 21:23:36 GMT  
		Size: 12.8 MB (12821713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa41f46776fac465aa8b81d75fdaee45f76cc0fd46cbe3f1d9e6d7690a1f773`  
		Last Modified: Mon, 23 Jun 2025 17:42:15 GMT  
		Size: 9.0 MB (8953404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65d8037640f926b866f76f1baa9e6e684bad00f9d3911579227854f6de08e75`  
		Last Modified: Mon, 23 Jun 2025 17:42:12 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb1a3fc16f527f3d565a9fb4f94431d4f5d5969dfbe5de6686a7741d49b5483`  
		Last Modified: Mon, 23 Jun 2025 17:42:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:d6a7c4ffb8dc174d33862d90d4bbe961f738939fade4a84c85d607b90ab5fb1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6247486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2fc93993c3969ebb405201ac9addb0bf9124969997cb17d2545045a5723f5a`

```dockerfile
```

-	Layers:
	-	`sha256:4f9d68a51a954dc53b96a29e5a3f5a85d3c75d6b67ec09f142fb115b44ec4ce5`  
		Last Modified: Mon, 23 Jun 2025 20:28:26 GMT  
		Size: 6.2 MB (6229010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18cbe630ff54c6ba92959d4403953e6bbe9f7b308585f2ce653bb182a7712122`  
		Last Modified: Mon, 23 Jun 2025 20:28:26 GMT  
		Size: 18.5 KB (18476 bytes)  
		MIME: application/vnd.in-toto+json
