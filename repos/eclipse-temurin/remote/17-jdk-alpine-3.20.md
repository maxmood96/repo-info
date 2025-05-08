## `eclipse-temurin:17-jdk-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:f328427edb370072de4aeea45436c55483b8005e329d6730f60762017207ab68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jdk-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:b91b4d4d2a4b9aace37b1b7c582d8a726a6b75a5c654657b1dea00d4a4e55917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168075623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21557b0db92fbf4639a57159d266315d1d7f72f67d7df8a9e724a6db8dcf9633`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='c596f5c627f84cd801bd7a443cd0743304a6aabb7397e0fdbfad16a9517f7f98';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77a932d4b40d745386615a4774f59b4c106aa0a2f59796abf74dc2929cb8e47`  
		Last Modified: Wed, 23 Apr 2025 16:31:39 GMT  
		Size: 20.7 MB (20670483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acf4c06204a0f3155c546ceb2d4ea7fdc97313c23e5d1225abc3d2889ae0f42`  
		Last Modified: Wed, 23 Apr 2025 16:31:41 GMT  
		Size: 143.8 MB (143775833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c69bdf7cc32d38a74414caab9c00fd23e04e550935d02c00070c69770cab1a`  
		Last Modified: Wed, 23 Apr 2025 16:31:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7df3467295ef07db8da6b3faa64646460a513d80d1114bf8fa3d58c17baa05`  
		Last Modified: Wed, 23 Apr 2025 16:31:38 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:03b6f288cd0cdaba0c1e2b7b580db4bd54a99a06aa7bc72654c7214d89d0fad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1084400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abed74b62b6da765abf1925695be03e24ab1728dacba25d66d4c4e343a5b7bd`

```dockerfile
```

-	Layers:
	-	`sha256:bca5be907c6f2a37207c923def7417ed25392a9d8550c3897ee87e5c92454854`  
		Last Modified: Wed, 23 Apr 2025 16:31:38 GMT  
		Size: 1.1 MB (1064746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:685bbd9b657b1583682ff02a2c6cce0b6f8b4928e12bcf8a53e0ea975946920f`  
		Last Modified: Wed, 23 Apr 2025 16:31:38 GMT  
		Size: 19.7 KB (19654 bytes)  
		MIME: application/vnd.in-toto+json
