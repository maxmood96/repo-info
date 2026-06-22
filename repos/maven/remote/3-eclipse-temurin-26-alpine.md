## `maven:3-eclipse-temurin-26-alpine`

```console
$ docker pull maven@sha256:17f5fa1caa0908f91a130d13a54137770e61b2b221220c008a35d86a21666959
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-26-alpine` - linux; amd64

```console
$ docker pull maven@sha256:481ae514e388be53d2881530d46a79b50e0a73bfb4bd871f13b509ec2529b0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125753402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f53e563180c22945e2409990999fedade8d16eb4ef46ddb6a5ae7bdef5edcf2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:57:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:57:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:57:49 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:57:49 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Mon, 22 Jun 2026 19:57:58 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7e32b89349385f10d7805197c7696b46556717d041e681017b12590bae6692ca';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='0c97fe7e503fb6daf36a5e86e8d083b97cc2354cda4d11288e6c3b8ec0818afc';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Mon, 22 Jun 2026 19:58:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:58:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:58:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:58:00 GMT
CMD ["jshell"]
# Mon, 22 Jun 2026 20:27:18 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Mon, 22 Jun 2026 20:27:18 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 22 Jun 2026 20:27:18 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 22 Jun 2026 20:27:18 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 22 Jun 2026 20:27:18 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 22 Jun 2026 20:27:18 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 22 Jun 2026 20:27:18 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 22 Jun 2026 20:27:18 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:27:18 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 22 Jun 2026 20:27:18 GMT
ARG USER_HOME_DIR=/root
# Mon, 22 Jun 2026 20:27:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 22 Jun 2026 20:27:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 22 Jun 2026 20:27:18 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f2fd18a0a9bc0fb03fb517a12431b1bf11c2dd8a300797a70c469eb0573499`  
		Last Modified: Mon, 22 Jun 2026 19:58:15 GMT  
		Size: 14.3 MB (14259370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b896cecc272ef7121da940e2be26998d8de663b31adc1e3e4bb1cbb887ae6c`  
		Last Modified: Mon, 22 Jun 2026 19:58:17 GMT  
		Size: 93.7 MB (93726872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ef27f6a9817fdee68c106972c44385780e41f17b2e0f931781e6e066d03423`  
		Last Modified: Mon, 22 Jun 2026 19:58:14 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f794e94355907e9d4c3b9ac7bf794fdcc22add314a4fcd8d3c9ee0e9afed5a2`  
		Last Modified: Mon, 22 Jun 2026 19:58:06 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ee85750e0911e39d96a5efab3fb509a56764766f2f106216d065e1debb7343`  
		Last Modified: Mon, 22 Jun 2026 20:27:26 GMT  
		Size: 4.6 MB (4559170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ded73eb83fb13dd6173f81fa5ed43cba7f56b32c7e7de15fbb5ffa72eedf1b`  
		Last Modified: Mon, 22 Jun 2026 20:27:27 GMT  
		Size: 9.4 MB (9359964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d869c9bde5615673818f8e7d09a16a8414432f9d6b36b476722dd50c4f2cd91`  
		Last Modified: Mon, 22 Jun 2026 20:27:26 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71cca5d3b1a374d8f701626b2c7a8f361e248450610f2b0eeb4497af84f35f2`  
		Last Modified: Mon, 22 Jun 2026 20:27:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-26-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:aeb6fc2a0819c25bf8e1a35dbb0fac53e97942b7e504474876644b6956fdb58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1138897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa81d8242edd2a8e304af926e7894ec91b0d6625c943a034cd428791f75cd975`

```dockerfile
```

-	Layers:
	-	`sha256:9b6be034d79f62ab03af7b741e8bdaa49e776388c719feb4053f9afb44097232`  
		Last Modified: Mon, 22 Jun 2026 20:27:26 GMT  
		Size: 1.1 MB (1121861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e68e5b2813c772d25d1e1ef9ec281c09b8f1240705845d05b7ae3c2d4b88b4eb`  
		Last Modified: Mon, 22 Jun 2026 20:27:26 GMT  
		Size: 17.0 KB (17036 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-26-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:2bd683b8342144bf2fb23d34fb95c344b6eb4bf5598afdda543525f92f5e54ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125125439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c6444ca78720626037f183f080e89efbedd8f4bb84d02aa2504a2e04b613b9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:58:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:58:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:58:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:58:28 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:58:28 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Mon, 22 Jun 2026 19:58:37 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7e32b89349385f10d7805197c7696b46556717d041e681017b12590bae6692ca';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='0c97fe7e503fb6daf36a5e86e8d083b97cc2354cda4d11288e6c3b8ec0818afc';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Mon, 22 Jun 2026 19:58:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:58:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:58:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:58:39 GMT
CMD ["jshell"]
# Mon, 22 Jun 2026 21:01:39 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Mon, 22 Jun 2026 21:01:39 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 22 Jun 2026 21:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 22 Jun 2026 21:01:39 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 22 Jun 2026 21:01:39 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 22 Jun 2026 21:01:39 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 22 Jun 2026 21:01:39 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 22 Jun 2026 21:01:39 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 22 Jun 2026 21:01:40 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 22 Jun 2026 21:01:40 GMT
ARG USER_HOME_DIR=/root
# Mon, 22 Jun 2026 21:01:40 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 22 Jun 2026 21:01:40 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 22 Jun 2026 21:01:40 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259201305cf66a45c6f9b11bf24d453317731d6a78705f78a399137c52f9e461`  
		Last Modified: Mon, 22 Jun 2026 19:58:54 GMT  
		Size: 14.3 MB (14320313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd1e1a965bbb185d2269d31ef27dc5dbe89fa439f174a8b7bf40b3fc7a4190d`  
		Last Modified: Mon, 22 Jun 2026 19:58:56 GMT  
		Size: 92.6 MB (92617795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ebddc94b4afa6b0f737e5864afd8689f7952438e252acbcc0805bd077e8b6a`  
		Last Modified: Mon, 22 Jun 2026 19:58:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938f966bc6eeccc12781f72ab7be7722b25b9dd4da6076c94fd98a7d26e96618`  
		Last Modified: Mon, 22 Jun 2026 19:58:54 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7ec028788578c043b7fede7feb1a1aacbb7fe6c50c969edceb33720bd8b584`  
		Last Modified: Mon, 22 Jun 2026 21:01:47 GMT  
		Size: 4.6 MB (4641898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b79c140767385d9259f33b99ba6969c5c5dc62b0a0d4dfcc6f198d3143acc2`  
		Last Modified: Mon, 22 Jun 2026 21:01:48 GMT  
		Size: 9.4 MB (9359972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e86bdab683944bd47bccf4f44996d5e156211261e04579698cc1ec1a8ebec`  
		Last Modified: Mon, 22 Jun 2026 21:01:47 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999a40a9d03c64c15bd88c511b76c45b6e00bd6f62e3beb9590752d397822b3d`  
		Last Modified: Mon, 22 Jun 2026 21:01:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-26-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:c34a1469a73c5ea51f3aa73f57714a708b29fdd2e832c05e58568c0fcbb56942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92dfcd1c4a7d1bd347f13117066a06de0a956e74debdd68c2d297a222a03af2`

```dockerfile
```

-	Layers:
	-	`sha256:d9731b95d356d532549cd1fe95b7579bb571234df60109d70e51f045d67a2c37`  
		Last Modified: Mon, 22 Jun 2026 21:01:47 GMT  
		Size: 1.3 MB (1271210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04280a50c060ce72d28962f7f365509577f52ed3b2d4f6de6753b5914f04a2eb`  
		Last Modified: Mon, 22 Jun 2026 21:01:47 GMT  
		Size: 17.2 KB (17169 bytes)  
		MIME: application/vnd.in-toto+json
