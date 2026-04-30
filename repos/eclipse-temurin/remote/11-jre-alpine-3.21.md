## `eclipse-temurin:11-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:004eb71d32ba3d025f6483aaff73dbdbd8e5b663c76ec7a372c4d118f99e3212
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e758a9b0da2f3a3ed9bbc7824fa314bafd1fcb2e5a3e539ac771f5b215c25ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63551704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13aa21ffff186798ac46bf7e1d0dec7242bc534d55ebfa68a8faff6ab04cd054`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Wed, 29 Apr 2026 22:45:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:45:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:45:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:45:03 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 29 Apr 2026 22:45:03 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='4a1ba44d0b28523ff5b73a5015f3bcc6b9d36f3ac313ffb87762946af7f642ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 29 Apr 2026 22:45:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8535810259eb3348d8380816ff4a8dfe63c2b48e7a533b002927c9a1d517eb`  
		Last Modified: Wed, 29 Apr 2026 22:45:16 GMT  
		Size: 16.2 MB (16198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271b8f6302985d969dee97a30d087ebe9248da205d859e4d888b16f6bd543414`  
		Last Modified: Wed, 29 Apr 2026 22:45:17 GMT  
		Size: 43.7 MB (43703828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2246bf8422231761821743829c6626fb6bdb0c6c8206a0da53afcc1ba63fad8`  
		Last Modified: Wed, 29 Apr 2026 22:45:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baae6ae98f8e47609c60232f260fe73c536262064ee1ee7ad66dfae876070eb1`  
		Last Modified: Wed, 29 Apr 2026 22:45:16 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:35e0b063d5d17ffff9ecbcea39d162148545ab7e01f32411a046447cfb2f1e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **926.8 KB (926786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a485e21b679e99826c0098f0e75ff40ee4d4b349441c48d3a66fb0a1ac7cfc6`

```dockerfile
```

-	Layers:
	-	`sha256:69e0509c695a9bb8e830a74ba8ee91334bccb4a5e5f12dcebf2fb66ded07b4e2`  
		Last Modified: Wed, 29 Apr 2026 22:45:16 GMT  
		Size: 908.6 KB (908562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e73c7140b07ad6171ebf3422827ffcc6de8a34d8e67b43e8fe5165b96ef81db4`  
		Last Modified: Wed, 29 Apr 2026 22:45:16 GMT  
		Size: 18.2 KB (18224 bytes)  
		MIME: application/vnd.in-toto+json
