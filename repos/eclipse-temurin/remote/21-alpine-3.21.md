## `eclipse-temurin:21-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:203eeb35b27ed4e049275946f4b4b241fcdde6b67d31e91925fab61bcf622575
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:27ed194db54cf8f64bfda3c3332541087d87200ef9734c48b02a98d38357870e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182622684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319d1b2f48509f8db16eefd9b3013841ba296f29f422cde5991e2aeb79442667`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ccc8482f6c13e77be9f93f7e9cf0ada6c78ed617011fd06e5f0e2e5ef737c7`  
		Last Modified: Wed, 08 Oct 2025 23:36:13 GMT  
		Size: 20.9 MB (20948581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907b901ad5ce977d6da31849f702f3702b8ce2bc9dd3241ba04487acc91c7af3`  
		Last Modified: Thu, 09 Oct 2025 00:37:12 GMT  
		Size: 158.0 MB (158029125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee360a53992c0547252093f0d28fd3ae0619918c2efb7a4a0a9e83b78dd364b0`  
		Last Modified: Wed, 08 Oct 2025 23:36:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efd55cafaeaa3b7920966b500bbb2e65082bfe101f587b65bbb4284bd821521`  
		Last Modified: Wed, 08 Oct 2025 23:36:12 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:cd57c97ee4dfcadfa900af2e72be9e83d5f48ed291d81f43f309d0f5a28bcb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1124767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9171b2d583587ab740eee79bcb3c4288d4741f749985b3bc2dfcde191099a4bf`

```dockerfile
```

-	Layers:
	-	`sha256:f476d3584231c62e2dbca170529dc9c3937923eef15ec5dcc31621d18189d38e`  
		Last Modified: Thu, 09 Oct 2025 00:15:26 GMT  
		Size: 1.1 MB (1104318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13c861b507cdb1fd98261cb2571c52fe3a85dd5b24d79a28a85a4708c0ce111f`  
		Last Modified: Thu, 09 Oct 2025 00:15:27 GMT  
		Size: 20.4 KB (20449 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-alpine-3.21` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:023aad9485ed27cb55c6011924a3beb787b6d70e5b12fe2ae70b3157bd651392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181020391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac2e5617ca5dbb8852eda1f195f521849a0c665677787b7b5bb8c88f6cbef4a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bb73b098c9b830a91c4843a949ae810f9f55fd762d7d66533dba0e7c07e38d`  
		Last Modified: Wed, 08 Oct 2025 21:48:26 GMT  
		Size: 21.0 MB (21002961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa56154b3751608127d028a0ed0e3e0df766f3f8801ba4fd44156c0ffd4d83c`  
		Last Modified: Wed, 08 Oct 2025 21:48:30 GMT  
		Size: 156.0 MB (156022669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a7b4572d40ef82d24c9a7e71a784099a730ca6b4942aca1e655d8eb4bbacff`  
		Last Modified: Wed, 08 Oct 2025 22:37:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a291b36683dbfdb219728a3c1451396b88e4cfaf825843be4e6ffe40b60be294`  
		Last Modified: Wed, 08 Oct 2025 22:41:12 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:65a933ecc0bf65b8d9678704830f020b757d2c568fcd57284b18f4151c04e99a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1274891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2008a4c5ad3255f2fc56224f67a61cebad8ab79340809714db15b3999e9cb23`

```dockerfile
```

-	Layers:
	-	`sha256:adb438d3118122ca76847354b07e9357565db6462cffbd647ea1f0372243aa74`  
		Last Modified: Thu, 09 Oct 2025 00:15:31 GMT  
		Size: 1.3 MB (1254320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6edef630fbf1789dba8e41063e5b00cb37fe3b6069b44da609baa5d52bd68d3e`  
		Last Modified: Thu, 09 Oct 2025 00:15:32 GMT  
		Size: 20.6 KB (20571 bytes)  
		MIME: application/vnd.in-toto+json
