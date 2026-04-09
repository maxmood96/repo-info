## `eclipse-temurin:26-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:4b869106a967d8bd651c9fba1b2030ea50684ec72739ddaf8a5b728c7dfa7926
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:26-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f6227038f5b89d45a98ebf69c964d689a123baa06dc74247e77b8dfeefabcf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77081841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e810bca45b0cb9306b488358930a95af3e1ce9f70b36bb06794558b900a8828`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 08 Apr 2026 17:28:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 08 Apr 2026 17:28:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:28:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 08 Apr 2026 17:28:17 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 08 Apr 2026 17:28:17 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 08 Apr 2026 17:28:23 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f3c21f425f9e9f53ab8a19aed6a25cedee662be19fa221696c1450eb67470905';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_aarch64_alpine-linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='4f0866bd8aa88eb6dfd0489793f8b2fb3eb0f6c20aadb27cae1b140f10897f8e';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_alpine-linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Wed, 08 Apr 2026 17:28:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 08 Apr 2026 17:28:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:28:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51d2094f1d8911b912045a83521010dbd4740ff7af8e4e5ce65f449ac4cc346`  
		Last Modified: Wed, 08 Apr 2026 17:28:37 GMT  
		Size: 9.4 MB (9449339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45f58e4f10d49978b81fa0fd465bcc8357d52c956091ff027460c7e2ae12fd`  
		Last Modified: Wed, 08 Apr 2026 17:28:38 GMT  
		Size: 63.8 MB (63768273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcae4c7ed942de10754ac110a7fe25b152598ad1e7592a2d5c72c276361f5442`  
		Last Modified: Wed, 08 Apr 2026 17:28:36 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5846886e0654388af39f44eeea4a024d03813905e37009bf8c218c7602ec93eb`  
		Last Modified: Wed, 08 Apr 2026 17:28:36 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3bce7c4adfe8ea6cdc1e0e9f930e5e5b2f1929723d81d07cec87ce260c637246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **821.5 KB (821495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2ac93167c767b307a785dbe9a9dff8ec8f3f7d88e1b35b8600f8427f5ae97a`

```dockerfile
```

-	Layers:
	-	`sha256:9132e15c2c7b62a350fb7b2df74be1bc43c751b099a9e8d1034733075a82ab10`  
		Last Modified: Wed, 08 Apr 2026 17:28:36 GMT  
		Size: 801.8 KB (801752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adeaf6387c590af0ccf6080e8a2843f7114390d388d8063d56f413a887767cbb`  
		Last Modified: Wed, 08 Apr 2026 17:28:36 GMT  
		Size: 19.7 KB (19743 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26-jre-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:ff7c7f2b396864bebe42b0e29b41f4b8023d044179d021a14e9a711a1eb6a6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76320341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b5885d47f223d60b8e96f7e6ea1cf9f8e92957d4ef2732d27f795046eaed3e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 08 Apr 2026 17:28:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 08 Apr 2026 17:28:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:28:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 08 Apr 2026 17:28:16 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 08 Apr 2026 17:28:16 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 08 Apr 2026 17:28:22 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f3c21f425f9e9f53ab8a19aed6a25cedee662be19fa221696c1450eb67470905';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_aarch64_alpine-linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='4f0866bd8aa88eb6dfd0489793f8b2fb3eb0f6c20aadb27cae1b140f10897f8e';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_alpine-linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Wed, 08 Apr 2026 17:28:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 08 Apr 2026 17:28:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:28:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866ef644d8cd6c88393b327babb4c8526d104a9c70741d510a2d3592671faa39`  
		Last Modified: Wed, 08 Apr 2026 17:28:35 GMT  
		Size: 9.5 MB (9469511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a38f1daf72c3b2590d8e8c15e96432d9178f5e7825d8591dfe042b4245f3409`  
		Last Modified: Wed, 08 Apr 2026 17:28:36 GMT  
		Size: 62.7 MB (62651331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e5e0b9415195d727005e2fb6178a195e86ece8c007ca88a29f43e79abcf87b`  
		Last Modified: Wed, 08 Apr 2026 17:28:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c227b65dcc827eec42fa5491bf300eb92ea38417b71e1a3522a8907de3c10a75`  
		Last Modified: Wed, 08 Apr 2026 17:28:35 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a8e5bab31a025ab58a513d92c1a50e855cc132c3357073bdcbb47f7d4b716948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **820.4 KB (820414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36242b30da9ea40f4d5573fff0fe23b46a30dd04d0c6f4920b1fc0f0589b33a`

```dockerfile
```

-	Layers:
	-	`sha256:043d7efa853282a8fb05d21633a7581af8db1546c1525c845bc6b0ec000ba7de`  
		Last Modified: Wed, 08 Apr 2026 17:28:34 GMT  
		Size: 800.5 KB (800537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d00a3d22a6e0305760bb5a139925cbe243be7e5b863e1095a1896577deaf5392`  
		Last Modified: Wed, 08 Apr 2026 17:28:35 GMT  
		Size: 19.9 KB (19877 bytes)  
		MIME: application/vnd.in-toto+json
