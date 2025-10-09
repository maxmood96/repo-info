## `eclipse-temurin:8u462-b08-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:9c5c91af7816f248a63272d4848634d9f5e3685df0a9e8153b21865fc494c5b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u462-b08-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:4ec8a80241d1d237abc86e1cbb6c81d3fafd6df0ee18c3e6ed235d6a38650e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61479353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243a3b4b1402c2c43f951f3fffc2b5e10c91a5a034a5b03ac82bff1a655aaba0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='fb10b6185c76cb48bdcbb76e466adc319b37ffc0b1cf89708a1f13e94adcc12c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb91ff3d5572bfeea2653bf20cb06d848490b3143f60d9637be51acaf61d98c`  
		Last Modified: Wed, 08 Oct 2025 23:01:34 GMT  
		Size: 16.0 MB (16023431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed3794b043573068e0916bfe7dadbbba28d0605e1b0770289f647349f9eb61e`  
		Last Modified: Thu, 09 Oct 2025 05:00:33 GMT  
		Size: 41.8 MB (41826458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5292599915fb16a0e22aef9803b3d62eb3bfe0075a58badc3e9e2ee21ee4ddba`  
		Last Modified: Wed, 08 Oct 2025 23:01:33 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6831a4c1211943955f8f1e8565ae111eb99312577e568b1ca97f4a15f9896e`  
		Last Modified: Wed, 08 Oct 2025 23:01:33 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u462-b08-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a275e5ff009b700ad68c93f3c8825db25bb5ab51ece981300775ab451e881a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **937.8 KB (937826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4073f332c2c6be5019b4d8edf2cfd190173195ac56f633730f66f248ebcbe761`

```dockerfile
```

-	Layers:
	-	`sha256:d436203b67ea3b2489578f6d8c2f2d86ac7a93081217ed6acaa7c96a32a55582`  
		Last Modified: Thu, 09 Oct 2025 00:18:51 GMT  
		Size: 919.6 KB (919596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e5b0e83191dc54e171cd879a3816bc27fdd010d30de618ae6266e1e8153b15a`  
		Last Modified: Thu, 09 Oct 2025 00:18:53 GMT  
		Size: 18.2 KB (18230 bytes)  
		MIME: application/vnd.in-toto+json
