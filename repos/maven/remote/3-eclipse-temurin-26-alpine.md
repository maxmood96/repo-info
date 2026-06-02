## `maven:3-eclipse-temurin-26-alpine`

```console
$ docker pull maven@sha256:7b67df7d8d7ad1980974f0997176f9cf4fe093ee53cba4390d7029276e6cd593
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-26-alpine` - linux; amd64

```console
$ docker pull maven@sha256:ad43c2b6b611305e0a4105ffda8b6b0b7c60dd140c95ef5d358f9317ae5c8f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125820450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752c35e0521366968e12f454d73f3ee28c7dbd1cce16d95dfad4179ea003c26a`
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
# Tue, 02 Jun 2026 10:21:17 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Tue, 02 Jun 2026 10:21:17 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:21:17 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:21:17 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:21:17 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:21:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:21:17 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:21:17 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:21:17 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:21:17 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:21:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:21:17 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:21:17 GMT
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
	-	`sha256:cf5535addaf7621d1bf3ad4fdba59559fefa58e88425cdd1229b03fde96e566a`  
		Last Modified: Tue, 02 Jun 2026 10:21:25 GMT  
		Size: 4.6 MB (4558652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83377ec358d85c12bf549ca8208cf2517234f70dc5b625f62918a3613bcf91f8`  
		Last Modified: Tue, 02 Jun 2026 10:21:25 GMT  
		Size: 9.4 MB (9359953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85bd90adac2127b4e0a8f2ef5ff1852337a8ff34705b7c362e234bff249e234`  
		Last Modified: Tue, 02 Jun 2026 10:21:24 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa2c13628b97aa4634c3c26d700abd58bfdc6797128adb5120b812ac0e56647`  
		Last Modified: Tue, 02 Jun 2026 10:21:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-26-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:fa358a164dbb962506a712c378ca528ed88b143d160c92bfe3b05d4eac346f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1155789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04f18275b23005c7943afc266719085fa8ab455fb32dc8a798cf4301ec786da`

```dockerfile
```

-	Layers:
	-	`sha256:2cf2c54effbc7e89e2c4acfc70b81e2c2667c0091e47d6f747ba1748110aa0f7`  
		Last Modified: Tue, 02 Jun 2026 10:21:25 GMT  
		Size: 1.1 MB (1138753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2af15c2d9a184b54b4008e5d04d1995ad5ebe806904d7277ebae030ef48a9bf`  
		Last Modified: Tue, 02 Jun 2026 10:21:24 GMT  
		Size: 17.0 KB (17036 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-26-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:91fa55c84ba9e4a5a91f164b270b0fd0a0b79f8287d057914a899513cd496430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125190228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0c94fe07794b544945f428baa2e38aad31c803f969324ad341dec194907d70`
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
# Tue, 02 Jun 2026 10:18:42 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Tue, 02 Jun 2026 10:18:42 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:18:42 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:18:42 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:18:42 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:18:42 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:18:42 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:18:42 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:18:42 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:18:42 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:18:42 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:18:42 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:18:42 GMT
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
	-	`sha256:dace5aed29d4a524396bfb1e9863fd7b588c6549679e381be16a74e9719b8972`  
		Last Modified: Tue, 02 Jun 2026 10:18:49 GMT  
		Size: 4.6 MB (4642103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcb4de0e8dfdca7f12da2ef5228605951a001e79904f046db0bb7eb9fd2867c`  
		Last Modified: Tue, 02 Jun 2026 10:18:49 GMT  
		Size: 9.4 MB (9359959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a80e0fbbfd7487a7bc297c363094d3c3b712da20ab191021154910aa1d1065`  
		Last Modified: Tue, 02 Jun 2026 10:18:49 GMT  
		Size: 860.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b2e5b8cdf9684d3b5d21188904cff59f280e161c34946935fa1e364cd43dce`  
		Last Modified: Tue, 02 Jun 2026 10:18:49 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-26-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:3c5475b7cc12b714d0bb026f95318ad240c6be2147409d430cffc674dd292cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1305270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a5527697915b39a9a4c09b3cdff2a6c2ef79e06ea127d637e92ed82cb10545`

```dockerfile
```

-	Layers:
	-	`sha256:21d02f99af83d2faa037295561c04e06ad0acecc67d312972a9dca83b241faa8`  
		Last Modified: Tue, 02 Jun 2026 10:18:49 GMT  
		Size: 1.3 MB (1288102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0458ade230d041cb2175048438d9a336718f959c4cef06ca87c73ac39355a636`  
		Last Modified: Tue, 02 Jun 2026 10:18:49 GMT  
		Size: 17.2 KB (17168 bytes)  
		MIME: application/vnd.in-toto+json
