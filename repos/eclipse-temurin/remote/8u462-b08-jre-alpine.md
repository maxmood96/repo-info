## `eclipse-temurin:8u462-b08-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:963a365705214a3ab2880de348027864b3a2afa4e0f44f62c466c6b8d652e8b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u462-b08-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:5af36ce0b04d7b8e33f0b0745679aab4eb61bc4d0745780a38de94e0ba418b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61920997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955b02db0c1add657917511c2cdeeb00de7240dd69828a2eb01f52a0ad2a19d3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bdf1a8851b43696a9ccfbf69c59d0116574ea989236806249e61534b9b274f`  
		Last Modified: Wed, 08 Oct 2025 23:02:05 GMT  
		Size: 16.3 MB (16289695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae066e7f1dd8898b5f19b8a7f11b401a8153278e38da310ed57c55e28af6ebe`  
		Last Modified: Wed, 08 Oct 2025 23:02:07 GMT  
		Size: 41.8 MB (41826445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d1427eb5d21b45f25dd47537feda0b77fd2eb4397866eabd4dcbc31a7c84c7`  
		Last Modified: Wed, 08 Oct 2025 23:02:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9052c7f8d7ccd05f8651166022c814629d5a8f3b124c01cacadcdd89434bb5`  
		Last Modified: Wed, 08 Oct 2025 23:02:04 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u462-b08-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:89cb03c1c142ceffeaaceae60f71fce415f733e37209eb9bc75f79fb03117462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **948.0 KB (947978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d9e1ce878d63a303f21be50309e8e73ee19dfdbafd1f44ccd43e247dc8599b`

```dockerfile
```

-	Layers:
	-	`sha256:b02f624cd5ae1d4421909d9567a33687abd1a318959c6ca6126ff502357e074b`  
		Last Modified: Thu, 09 Oct 2025 00:18:46 GMT  
		Size: 929.1 KB (929076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33172c7a7dfc65ff1efaac93945cf7df95d895e874a9ed34a0e698774025e603`  
		Last Modified: Thu, 09 Oct 2025 00:18:47 GMT  
		Size: 18.9 KB (18902 bytes)  
		MIME: application/vnd.in-toto+json
