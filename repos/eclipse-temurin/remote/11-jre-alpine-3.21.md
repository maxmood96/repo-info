## `eclipse-temurin:11-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:e07342fae63cfa1fa1018c364f72ed31a5f660b90c2c9188a013344b058a80e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:57d2de111ff18340d8be2a246ac59521ccaaa5065d79d4d431becb9b1b6a00a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63414103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2c5c8b6ea1d16cff711f56c8e0321f5ce5de9ac0c7560730de8c8ee5e97d28`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
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
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='b0092a3f753beb13221fab3a1ce713390809b4841b4a5eb407f9819d628c8856';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cc19ef16fe2e1e96f066552c60478d848ffcbefd7fd96beda65fbea519f397`  
		Last Modified: Wed, 08 Oct 2025 23:02:04 GMT  
		Size: 16.2 MB (16174562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a03a8bdc0f84144147f010b958cc5a2c2ad050590e89453838a9c5e230adb65`  
		Last Modified: Wed, 08 Oct 2025 23:02:07 GMT  
		Size: 43.6 MB (43594562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189a0d017bd2ebe27d51f6ca250f8f3b845a4eaa6b7ade9d99f9a90a3e6259b2`  
		Last Modified: Wed, 08 Oct 2025 23:02:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c15ddc1ae9a8cfd97e05c5cb19dd614f5ec8ecc4da79d4d8f82940f5a633769`  
		Last Modified: Wed, 08 Oct 2025 23:02:03 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:01fbb9cce32e00c82bb3457c610bba88141d14f17903fbe77c314aaf2c4ed32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **926.2 KB (926236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f038da74a5ac2850998c7d75ba2f4be54a8bf6321af1c57686aa70e03029ec0f`

```dockerfile
```

-	Layers:
	-	`sha256:9e9de7d97ff23a2d720c789ea9c070bd2689a8cd115e2d54767e0c4db625cefe`  
		Last Modified: Thu, 09 Oct 2025 00:13:01 GMT  
		Size: 908.0 KB (907979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cd450bb2861521b555525be35ac2543e80e9914484df9f5330464509f3e8169`  
		Last Modified: Thu, 09 Oct 2025 00:13:01 GMT  
		Size: 18.3 KB (18257 bytes)  
		MIME: application/vnd.in-toto+json
