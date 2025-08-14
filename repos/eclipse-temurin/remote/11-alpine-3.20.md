## `eclipse-temurin:11-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:5de87d07ac3306277a91aa8689f2398878b16700fec0876595d0591d6a2bfc80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:b62f76c1e8677c3dd6471a748eeab5e3d6695b6388a2667b507f406ee957e8e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160476247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cd012e53f396ef54895dcf2e5ea4c87346e114b58685736f322f4527f44879`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
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
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7e9e5241d1378d75ae70e9b216d0d51d3aa2e61e187e92e09d117cb613e16ee4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e28a18dc7e9ff24aebdee2ccffe9159f71f6e508bee69b20d9434f9de78f2f4`  
		Last Modified: Mon, 04 Aug 2025 19:11:26 GMT  
		Size: 16.0 MB (16011729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103175d76b00bc7b2bcccde977f7e5f27e241ea0760284b67d5fb910a3a2ae7d`  
		Last Modified: Mon, 04 Aug 2025 23:04:53 GMT  
		Size: 140.8 MB (140841631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6995e4ea18d5c37fae66155ba9a956d86dcbe6cbbaaa2c646c062408c26a2241`  
		Last Modified: Mon, 04 Aug 2025 19:11:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513a18996127d880ec4a9c31c0ea58c591f5c603202bc41cfc727d82727e22e8`  
		Last Modified: Mon, 04 Aug 2025 19:11:24 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0ad46a4e15ed3c535841fb328d87479c5f4f9272198c0b739931f2901004e38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1008834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cadda31d531e2a3375a08ed5a3c9880f41f22fa7a366d90720ece20206ab84f0`

```dockerfile
```

-	Layers:
	-	`sha256:5f9e5d2e8d605a253acb1024b0628a3c335e4505d2bd0294e7a07959668b8e2c`  
		Last Modified: Mon, 04 Aug 2025 21:12:41 GMT  
		Size: 989.6 KB (989621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83ad3a4b12ada34ca4f3fbaf94d62902cd6c48f785818e77ecaac5787ac7e8a9`  
		Last Modified: Mon, 04 Aug 2025 21:12:42 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json
