## `eclipse-temurin:11-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:f959aaa5de04b463c5d6f32baec7bc6a86a4f7050519a400bef018001f783264
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:75368056ab5c3c632bdd7b38d0a415602b19e13dbcc1c11c637893ac926b575d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63034059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00958bfd145bf6396eae6093004572861d3ad60522eb33f0b3fe94c4b909732`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:57:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:41 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:57:41 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 17:57:43 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='a37e818c23e19a0f3f6a77827eac9c6dab572c22efafa6c0e888cce2555d39a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sat, 08 Nov 2025 17:57:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:04:22 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9a389154e8b7d03067c3c5dd643ae61b8f75615167c1db6a16f82841a21879`  
		Last Modified: Thu, 08 Jan 2026 07:53:56 GMT  
		Size: 16.2 MB (16174530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c7705cf72d1a7582a49d04b0a5e8bcff4b226a2728ce9bb173dc951fe585b0`  
		Last Modified: Sat, 08 Nov 2025 17:57:54 GMT  
		Size: 43.2 MB (43214554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a31a814e0f244747f68c84375ed2cabd418ea0029cf0410532f7a67fd5a75d`  
		Last Modified: Sat, 08 Nov 2025 17:57:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef645e473b191b53554504ae98fc46d469f50f657d54016ac6ee359ad41ae6e4`  
		Last Modified: Sat, 08 Nov 2025 17:57:53 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4ea56606aea0d4ec26ff6593e1d5a0481eb3257f9ca484435a1dd009247be95f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **926.2 KB (926193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15fca3de157c5ad25fd3f5e3746125e46a5b5d9541f8abfcc54131e6257f3edd`

```dockerfile
```

-	Layers:
	-	`sha256:88c20758a7db1978d04c04a8b82ba008017e88871680ca935c44afa0d23cb10c`  
		Last Modified: Tue, 20 Jan 2026 03:30:19 GMT  
		Size: 908.0 KB (907979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81bfe93d146d636b5ad6736ee37a63ceb92e1a002eefcadc56d0dcdbeb4d56b8`  
		Last Modified: Sat, 08 Nov 2025 17:57:53 GMT  
		Size: 18.2 KB (18214 bytes)  
		MIME: application/vnd.in-toto+json
