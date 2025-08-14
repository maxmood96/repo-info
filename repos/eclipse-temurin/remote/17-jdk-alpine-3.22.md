## `eclipse-temurin:17-jdk-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:c0dfec8fb4aec4adad2d00d267c5cb5348465d77f087e455d2905fb180ce27d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jdk-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:818e8f70d78a2be3ef70e42c3fec4820d1ba2346b0f73897d88c640c4fe8d4ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168755718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d83145c93bb23306382c14e5390c60e7368cf12116f26337c3ed0d1149b29f8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='2e83ac152fb315db0d667761f2120b64504800f641a513044e834a1a41f29bc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d125b9b630f45fe9fdd3dc16a36920f92fa7c1e01344de92d6b6e6f6b50c5db`  
		Last Modified: Mon, 04 Aug 2025 19:11:32 GMT  
		Size: 21.1 MB (21104306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889e463e11980d977e77842be54e94ad63e877ec78f1f31eb301c571bf31e842`  
		Last Modified: Mon, 04 Aug 2025 20:12:08 GMT  
		Size: 143.8 MB (143849315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5491fe72c6c247575080814d36438026b9d982ae49ccfcf86ff607e533f3b376`  
		Last Modified: Mon, 04 Aug 2025 19:11:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bb5da1a24523a0af1966f13d7bc9ffb567c894c91c19968adcfc1fe0ea1653`  
		Last Modified: Mon, 04 Aug 2025 19:11:18 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e59fd2de36eaad3fefc4baa77e206c1f077330f92adac863ed9d879b874d30b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1121804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57edbd040214fc6cd9ebbed9efeffc7b55e6d2f1f626b3cc5e763b21e22d8b63`

```dockerfile
```

-	Layers:
	-	`sha256:c3e05706e8a8eeb1a78e6ab790e4cdb38c14fca95a4c8c76bf2b9110b29d8241`  
		Last Modified: Mon, 04 Aug 2025 21:16:24 GMT  
		Size: 1.1 MB (1101154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b352d12fddb34389047a01691dfab1e592a4858929d8ca7dafa72e536b3564`  
		Last Modified: Mon, 04 Aug 2025 21:16:25 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json
