## `eclipse-temurin:21-alpine`

```console
$ docker pull eclipse-temurin@sha256:89517925fa675c6c4b770bee7c44d38a7763212741b0d6fca5a5103caab21a97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:59477b37bc856b1639ec73a5abe5b278699b3452ad78323b6f909317308a0e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182946046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac485c3dab1d017bdbc50ed41a74b79ed085ac7e20609665479d1a588ab650bc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='4773cfdc59d66b75f4a68ac843b2b5854791840114cf8bb1b56fb6f7826ae498';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='73c4cbe10f4f385383d9cb54d34f2bee2c68b5265f9e3d954f3326948c40c0be';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2a5ff902df392c9f6430cfcee73bfa86c2856161d3162cbe1ec519b6da89a1`  
		Last Modified: Wed, 08 Oct 2025 23:34:06 GMT  
		Size: 21.1 MB (21112159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ef1487a229d2c2defc8ef70f98308c6bb819c1ee443e3f4d90d7399d6edd29`  
		Last Modified: Wed, 08 Oct 2025 23:36:49 GMT  
		Size: 158.0 MB (158029025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede95b48c87bb31f7470a39694663bb7da86718f456e8968ca1fb4e0f2661f20`  
		Last Modified: Wed, 08 Oct 2025 23:34:03 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64da9540a58e0598f9af16f6180d6ca8a17f6b7ec33c0b9b6c94ac191adf2cbc`  
		Last Modified: Wed, 08 Oct 2025 23:34:03 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:34c29d7b466de247e321e5d2614463164c8f9744fb7600539c4be30d9e8027a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1128308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b6fef223653d7f8485ca9a5c39c467665a69f1b95b908ccb464525491fcbfb`

```dockerfile
```

-	Layers:
	-	`sha256:a7509781589177d4ebb1364b689cce376d192c32cc0f43a05c64122a708d0bde`  
		Last Modified: Thu, 09 Oct 2025 00:15:10 GMT  
		Size: 1.1 MB (1106865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a14db1b6a71fd3bed429eb6cfc2cdda3bcfe208d2c4b2ea7c6834c133f3b3a3`  
		Last Modified: Thu, 09 Oct 2025 00:15:11 GMT  
		Size: 21.4 KB (21443 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:b0d74c873f45169812fe70fa41e1891c02ae70ebd1a2ae562a8d2a1cc81a2642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181327209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552d26c7e3f17d30ffe5118e7b3a626988d324b605394c294d93e73f919b1a51`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
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
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='4773cfdc59d66b75f4a68ac843b2b5854791840114cf8bb1b56fb6f7826ae498';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='73c4cbe10f4f385383d9cb54d34f2bee2c68b5265f9e3d954f3326948c40c0be';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bd7b864b4356da2df87ea4d5d6475aef6137a29351c1d3ecbe0d04706b6d89`  
		Last Modified: Wed, 08 Oct 2025 22:58:01 GMT  
		Size: 21.2 MB (21164177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cfca150e78f40166bc18346742bcdc896b85bc86876b839dd2bdecfeea4222`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 156.0 MB (156022554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b39e649c1874eec7c8c7e132fd4b4a84d5e2a481d34f6e6b71626cda96acc6`  
		Last Modified: Wed, 08 Oct 2025 22:48:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cee7d7d88a0fa09b65df9709dead73cd3ea73a09c5d71cf396727d3453ff025`  
		Last Modified: Wed, 08 Oct 2025 22:47:59 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:dc81083107d9d8c5238ae550ac311c5f85b03e584a78ca5f3d2b497e8f8e7041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633ad221d630bc2f048a676264577e66f65061a7d70cd39053b13857defef923`

```dockerfile
```

-	Layers:
	-	`sha256:a30d98f3473586c23bd14d36aa7b80ee2b77bfff7ca4d726aa929b6a02cf7d3a`  
		Last Modified: Wed, 08 Oct 2025 23:22:21 GMT  
		Size: 1.3 MB (1256903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47fe01fabddb307bdec2ef36e7b5b7c2bd2ecb0b4c84e55af313fd9126351207`  
		Last Modified: Wed, 08 Oct 2025 23:22:23 GMT  
		Size: 21.6 KB (21601 bytes)  
		MIME: application/vnd.in-toto+json
