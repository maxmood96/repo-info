## `eclipse-temurin:26-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:67d858361411ee84a1510f560757b188a85349d62895767ea05dcf4fb0a9a285
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:26-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:81821a86c061a7602c93a7f447e1e6877321b3306490126fd025e6bd947b28dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111900832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760911c319129dff8d2ba4ac1575d292c35748cd3a2866ea743f1b30d2b54799`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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

### `eclipse-temurin:26-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:fba08d94a883b050d01fe50f4ff1e961e900a28ed18acdae8738ccaf98f18ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.6 KB (986590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205ead85a0027ac4d44b8be76149d2f58d0d0d062329e32f40d0f6c09762ea95`

```dockerfile
```

-	Layers:
	-	`sha256:accb4c73fb70d53f6a42f783632d6e61a283f0e0e84d0ee7de81e5640d7ed785`  
		Last Modified: Fri, 15 May 2026 20:29:20 GMT  
		Size: 965.1 KB (965077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e27f2034cda8e340949c300973e626cd1b282e57bdc9fb6e278585c38183689`  
		Last Modified: Fri, 15 May 2026 20:29:19 GMT  
		Size: 21.5 KB (21513 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26-alpine-3.23` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:048e4cfc893da1d2f7424dd510bd2ebf34b91391916f25a57f6facf42d7a3add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111187153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6a7a391510a556a80d84e83a70380c469bd0f92dab2b236bda424c3f1c76df`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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

### `eclipse-temurin:26-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5a208788d13758a2a17b2e0547ef30b396b556ed31d0fd68aa2a2a8fd0c8ca20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1136133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88be39c6b887c0ceb518282fc855a509420a8bdd639c06e9085f95e5e651af71`

```dockerfile
```

-	Layers:
	-	`sha256:04daee4ad56596d73d677bfa3393a46b1bbcec94c2b5afafc1ef04ca149de488`  
		Last Modified: Fri, 15 May 2026 20:28:59 GMT  
		Size: 1.1 MB (1114462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:185c612bb65928d0c8f4e6cf637dd0d048f759489a6a56d80966c4900a44e9dc`  
		Last Modified: Fri, 15 May 2026 20:28:59 GMT  
		Size: 21.7 KB (21671 bytes)  
		MIME: application/vnd.in-toto+json
