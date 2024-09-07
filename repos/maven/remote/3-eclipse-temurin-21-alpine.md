## `maven:3-eclipse-temurin-21-alpine`

```console
$ docker pull maven@sha256:eabb696bb6a1ba3952d81c0ea3b69acbe4e16d7446da0e7df19930e5a4e5a93b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:a52752c88c84dfd1d1f95efac9148cfc4b8796f14a29fbb289e5423253b88e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189888589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9623bbe7abd4b0e23942f6479102732c5de18117f23c15b9519737eb0341a196`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 19 Aug 2024 08:57:28 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["/bin/sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 19 Aug 2024 08:57:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Aug 2024 08:57:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='849c6d5a62a1f3dc2a3d2d7be07ffda089d35b862f6160b2a288c0408c2d8be8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='8fa232fc9de5a861c1a6b0cbdc861d0b0a2bdbdd27da53d991802a460a7f0973';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["jshell"]
# Mon, 19 Aug 2024 08:57:28 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c34627c847892ee87160ccb0488eb4484039dd04d400e9e86561f15459495`  
		Last Modified: Fri, 06 Sep 2024 22:44:13 GMT  
		Size: 14.0 MB (14032627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf8156c97e09482c8570965c0b9238fec4fef282a569e89f67a4eb990894ee6`  
		Last Modified: Fri, 06 Sep 2024 22:45:05 GMT  
		Size: 158.8 MB (158815391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b0721dd94269153e4f5994aac8f72c2c57e0f1a0a464fa53bee6d993fed5e1`  
		Last Modified: Fri, 06 Sep 2024 22:44:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcd5a714946cb14973166aaf3ad39335cd7fd14cad658b8ceb9026cd7cb72ee`  
		Last Modified: Fri, 06 Sep 2024 22:44:52 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163f4874014ebe477b216f0efc26bfadcb0fe633d2edd77a9c9cffd6341427d8`  
		Last Modified: Sat, 07 Sep 2024 00:11:35 GMT  
		Size: 4.2 MB (4243016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d501889175c54cecf0bb413d8037a8da41ff61083dfa5bd2972c6978c4b67b4`  
		Last Modified: Sat, 07 Sep 2024 00:11:36 GMT  
		Size: 9.2 MB (9170440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64b0f34d2193870e493fd10b9fc7c30d2a1c50b51c2ca85e8d92a7458382730`  
		Last Modified: Sat, 07 Sep 2024 00:11:35 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f307044c19303aa3e7ca10e18451efaf5be2fe77e15ecf5becc5857670c01f9`  
		Last Modified: Sat, 07 Sep 2024 00:11:35 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:1bd8c29f3c3d7f518f494269376f45e228901b9725e989c473b9e22109175e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.8 KB (994840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eaf4db2509491c4e8968b8b4794bb280e37701e53d2415666913a9ec5357c90`

```dockerfile
```

-	Layers:
	-	`sha256:6a27a60cedb9a994efcea59db47c054bd1136cad1a11b8fe3bc332dbbe541f2f`  
		Last Modified: Sat, 07 Sep 2024 00:11:35 GMT  
		Size: 975.5 KB (975482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cac81ac728c411e76c6929be46e85c8f68dcf487fa790b2e0e0289395cb7619`  
		Last Modified: Sat, 07 Sep 2024 00:11:35 GMT  
		Size: 19.4 KB (19358 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-21-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:8fd51092fb78f83dc2b75e59fa77c0ff360050672e4f4a33cbfd002dd60f5fe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188733630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd49e896b863ef6f97649a2afc18b1271b6bcbce1286bbac681cca8f1e5990cf`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 19 Aug 2024 08:57:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Aug 2024 08:57:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='849c6d5a62a1f3dc2a3d2d7be07ffda089d35b862f6160b2a288c0408c2d8be8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='8fa232fc9de5a861c1a6b0cbdc861d0b0a2bdbdd27da53d991802a460a7f0973';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["jshell"]
# Mon, 19 Aug 2024 08:57:28 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
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
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2478f4a9466e915a5997ded853c525c23643a703902fa3b4e95b2c80136f5c87`  
		Last Modified: Thu, 25 Jul 2024 17:46:42 GMT  
		Size: 14.4 MB (14369016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abadc835ffa030fc985e78cb8f354d889f827c5b2839069fedf76f9c6896a83e`  
		Last Modified: Thu, 25 Jul 2024 17:46:51 GMT  
		Size: 156.7 MB (156729061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0158a214eb3542371be651186374a14af2a6fe541da3f11897b547875db9c2f6`  
		Last Modified: Thu, 25 Jul 2024 17:46:40 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593a67afee94d7f74b36753ba56040649cdd97cdc81687b1822dc07ffa806e98`  
		Last Modified: Fri, 23 Aug 2024 19:45:43 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b510fd76d6808194135e60c2a36424cfc76b0b362b851959eb3faf1947e229a`  
		Last Modified: Sat, 24 Aug 2024 03:09:19 GMT  
		Size: 4.4 MB (4374869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc08d0de36b53edb88183a468f6b805847f954be8c12ba7c1d26bbbd4426d63`  
		Last Modified: Sat, 24 Aug 2024 03:09:19 GMT  
		Size: 9.2 MB (9170440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f460aec119b5c9545ac01ac1799bf96ee86e246c2a100d20139e4dd30b8f573d`  
		Last Modified: Sat, 24 Aug 2024 03:09:19 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccd73f97ad101df7754ee17eea2ee4d06198331e0e9dacad9976c8951648ee6`  
		Last Modified: Sat, 24 Aug 2024 03:09:19 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:90f2e4a7b91d902f3a733b4bd137579437ed31990e1be70e5f9d7ebfe49229b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1100798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92740c108dec8b1a7985f6d769084c673fbf2d752c9677382e0d62890792833`

```dockerfile
```

-	Layers:
	-	`sha256:dad575599cd8c495094ea7f8e4c89ee71fbf1b86d56fd9bd9a77635fc3fad21b`  
		Last Modified: Sat, 24 Aug 2024 03:09:19 GMT  
		Size: 1.1 MB (1080782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2f08ebaeb834be6637d562675bcb26c8e1097e2c8fbab5d35fdfd0ab82348c6`  
		Last Modified: Sat, 24 Aug 2024 03:09:19 GMT  
		Size: 20.0 KB (20016 bytes)  
		MIME: application/vnd.in-toto+json
