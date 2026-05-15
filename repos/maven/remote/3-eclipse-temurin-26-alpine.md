## `maven:3-eclipse-temurin-26-alpine`

```console
$ docker pull maven@sha256:9b0bc1420b93f3eafb7401dc3030eac01e773d8d709686d3c4ac351fcf6f9f42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-26-alpine` - linux; amd64

```console
$ docker pull maven@sha256:f3f7f752accbff22aa3c9df68368ea270fe9ba9506ac9cb12ad0c46c0bf4b264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125772751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb49520935d106525a60cbc2cf1469d16ad7066ea2b45a2c9106bd019f20d3c4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 20:28:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:28:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:28:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 20:28:55 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 15 May 2026 20:28:55 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Fri, 15 May 2026 20:29:03 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7e32b89349385f10d7805197c7696b46556717d041e681017b12590bae6692ca';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='0c97fe7e503fb6daf36a5e86e8d083b97cc2354cda4d11288e6c3b8ec0818afc';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Fri, 15 May 2026 20:29:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 20:29:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 20:29:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 20:29:04 GMT
CMD ["jshell"]
# Fri, 15 May 2026 20:37:53 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Fri, 15 May 2026 20:37:57 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 15 May 2026 20:37:57 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 15 May 2026 20:37:57 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 15 May 2026 20:37:57 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 15 May 2026 20:37:57 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 15 May 2026 20:37:57 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 15 May 2026 20:37:57 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 15 May 2026 20:37:57 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 15 May 2026 20:37:57 GMT
ARG USER_HOME_DIR=/root
# Fri, 15 May 2026 20:37:57 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 15 May 2026 20:37:57 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 15 May 2026 20:37:57 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e081e96822532a01c7bb1e027265fed4b4c27a2e1d696c326f173f3cc1223765`  
		Last Modified: Fri, 15 May 2026 20:29:20 GMT  
		Size: 14.3 MB (14307105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbaa5d5be003b1eed063c02fb86d96eed583ae248613b526315e1da79db26c33`  
		Last Modified: Fri, 15 May 2026 20:29:22 GMT  
		Size: 93.7 MB (93726947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e549ff0e96b732aa8f90eae5e53676271da5ac10a0fd38c6b26da9ff83ce4aae`  
		Last Modified: Fri, 15 May 2026 20:29:19 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521a9ec0292e87558350138ddd287318bfa3975e6531bc92f1c86438baf45fe9`  
		Last Modified: Fri, 15 May 2026 20:29:20 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1308bbeed518480b88f3b731c588ba3c0385a366d132329a29819e6f01485804`  
		Last Modified: Fri, 15 May 2026 20:38:06 GMT  
		Size: 4.6 MB (4558655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f724dde8681ae1a131a9daf0757d0adced0da57744079b24bdf4cc4a4500f9`  
		Last Modified: Fri, 15 May 2026 20:38:06 GMT  
		Size: 9.3 MB (9312252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d19c010610345698c1c102b2e86b9aed2e96fc472a95fb4f1232e04ab367b5`  
		Last Modified: Fri, 15 May 2026 20:38:05 GMT  
		Size: 860.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4cad0399804d2ad4a6a124c7d68166f2946cf19549136ae9e948f4af0ce7c6`  
		Last Modified: Fri, 15 May 2026 20:38:05 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-26-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:970c470ea218377a7d07b8e36fdde9f61f7c4e4f2372c931b6d03f270f9cc970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1155940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c6349d27a1323d92ecd8c55fe20198756e4e5ac9808a7b7a4d3f7c53f10038`

```dockerfile
```

-	Layers:
	-	`sha256:8d2cf547081d205a494f9c2a4203a179511c1302881adfca530169fb9662c5aa`  
		Last Modified: Fri, 15 May 2026 20:38:05 GMT  
		Size: 1.1 MB (1138750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:817489f577a2996acb4fa2eb626bfc0e5475b6552ffadd4bb70b76ef03235d14`  
		Last Modified: Fri, 15 May 2026 20:38:05 GMT  
		Size: 17.2 KB (17190 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-26-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b538b5598cf0395d00845ffe1702a3f21deccd950cabdecbecd26f31efbe2249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125142526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a26beb9e3566c14a8c50b568b60715cfaaaf048a64ed29fe6e0e00184ce1a09`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 20:28:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:28:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:28:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 20:28:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 15 May 2026 20:28:32 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Fri, 15 May 2026 20:28:42 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7e32b89349385f10d7805197c7696b46556717d041e681017b12590bae6692ca';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='0c97fe7e503fb6daf36a5e86e8d083b97cc2354cda4d11288e6c3b8ec0818afc';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Fri, 15 May 2026 20:28:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 20:28:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 20:28:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 20:28:43 GMT
CMD ["jshell"]
# Fri, 15 May 2026 20:37:34 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Fri, 15 May 2026 20:37:41 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 15 May 2026 20:37:41 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 15 May 2026 20:37:41 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 15 May 2026 20:37:41 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 15 May 2026 20:37:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 15 May 2026 20:37:41 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 15 May 2026 20:37:41 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 15 May 2026 20:37:41 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 15 May 2026 20:37:41 GMT
ARG USER_HOME_DIR=/root
# Fri, 15 May 2026 20:37:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 15 May 2026 20:37:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 15 May 2026 20:37:41 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663c281b02178500cc2405957896cb4b2c901f353ce59d8c702000b44a4eb4cb`  
		Last Modified: Fri, 15 May 2026 20:28:59 GMT  
		Size: 14.4 MB (14365440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8478f678d308c7c3dd2a812916604bc76952d2cbdd6cbfed048df7d43bd35b55`  
		Last Modified: Fri, 15 May 2026 20:29:01 GMT  
		Size: 92.6 MB (92619253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36508231094e13df0969686478e5f11986327f94f6c60eac3a91ccd402da86b`  
		Last Modified: Fri, 15 May 2026 20:28:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd0378873387f971dd8030f59afc279b6de616979cc085f74c1a3b2f5bde1dc`  
		Last Modified: Fri, 15 May 2026 20:28:59 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c270e387b8590f5a5c8079e00c029090b70c35accdc65ade99c20e4e71c31fd5`  
		Last Modified: Fri, 15 May 2026 20:37:45 GMT  
		Size: 4.6 MB (4642104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c925cf3d9dc06e9be398d20492f08ae5f00de3e1a2a94d6b3a58c3182cf3f4fa`  
		Last Modified: Fri, 15 May 2026 20:37:48 GMT  
		Size: 9.3 MB (9312258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf1fc8bd20bfd53ae1fb6799b21a76e125df25c81f20541254be13f436b6c04`  
		Last Modified: Fri, 15 May 2026 20:37:48 GMT  
		Size: 860.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448c2c0694582f6f93147c0821d27ca8bd5408e4e06bc25f4a8f7d2267789ffa`  
		Last Modified: Fri, 15 May 2026 20:37:48 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-26-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:f13a40950f7f3aa1c464c27f626b2187c54b36dd7c9ca5ef4181494703e291bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1305422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c0f1a3ebb0a153930cd9252867afa7f0cfa861182a9a334df6b1dde763a28a`

```dockerfile
```

-	Layers:
	-	`sha256:bd30374412d177fbc7ba08e7ace42d3e3c1bf3457a4fc426b4989c8f830320da`  
		Last Modified: Fri, 15 May 2026 20:37:48 GMT  
		Size: 1.3 MB (1288099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0453bd05a2ba60ed01128bf16c05acc13e04e3e4fdc5a65b165d392c41f57a4e`  
		Last Modified: Fri, 15 May 2026 20:37:48 GMT  
		Size: 17.3 KB (17323 bytes)  
		MIME: application/vnd.in-toto+json
