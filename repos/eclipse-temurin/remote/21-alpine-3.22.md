## `eclipse-temurin:21-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:e5138ee5faa9ef7cdbd5503b9147e618ba8c8301a88bef40ea6dc426ac7cfe63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d5b8a88ea0f5236def9e92bf5bd7edc47e7e8c3a17d0081eefb4d2d727645505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (183042122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a778dfcb4bd8bbb45023230af818b9b4aa3fc5a7f518e816f3bd8d8ef9b39c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:19:06 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:19:06 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:19:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='19eba6c3877612157ef1f46deb92745b4567cfcd64b79f15449c68cd2b7501e3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='8eb39f442c3c603e414af43844b419a9b5d4f3fe221181f323aa4eec1bd20cf8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:19:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:19:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:19:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:19:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db1e60010c33395a1d02c9032689f14d99d4fe3a0ec1e68c4dabecd0c7afc4d`  
		Last Modified: Thu, 05 Feb 2026 22:19:30 GMT  
		Size: 21.1 MB (21115934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef28a5fdeefe4e8e19b01ebefe5dda51a8da5b502f80a427155bc43f7a755053`  
		Last Modified: Thu, 05 Feb 2026 22:19:33 GMT  
		Size: 158.1 MB (158118902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949c18c5c665c511c8b79742ebdc6bf820c05aa9c6b4a56fd498ba05799470a4`  
		Last Modified: Thu, 05 Feb 2026 22:19:29 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2de15b7359a67bc9f936d3a002d8ce8a9a1763a9561817f9369e7e48ebdab`  
		Last Modified: Thu, 05 Feb 2026 22:19:29 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:cd38b603fa12138ba769de3a8f42c4a74dbbd35ab00be769aad46943552a8f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1126298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4e0ee0b14742d41857347f41fdbd758b6544e0c85c4b83542d9439db10369b`

```dockerfile
```

-	Layers:
	-	`sha256:f4f7f33318b71e6e31346fec8274871a29a2b416de5e2ac2e78fc2e3032ac9f2`  
		Last Modified: Thu, 05 Feb 2026 22:19:30 GMT  
		Size: 1.1 MB (1105877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:256f6b9348acf2a26a6d43c92d32681cacd7a5b39540869dbf6839c73162c140`  
		Last Modified: Thu, 05 Feb 2026 22:19:30 GMT  
		Size: 20.4 KB (20421 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-alpine-3.22` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:72e064c69d9cb8de29b6d625ba553d41d045c07ad9d7d9927247d8113c70a789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181437842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a554de7813fe12cbe06b09063b952fff29245074ee75aacb80c81b18d9322a26`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:17:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:17:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:17:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:17:36 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:17:36 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:17:43 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='19eba6c3877612157ef1f46deb92745b4567cfcd64b79f15449c68cd2b7501e3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='8eb39f442c3c603e414af43844b419a9b5d4f3fe221181f323aa4eec1bd20cf8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:17:45 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:17:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:17:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:17:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eec8518b54b00a58837397612743e46696fba163394def84ec5bae0150c153c`  
		Last Modified: Thu, 05 Feb 2026 22:18:01 GMT  
		Size: 21.2 MB (21165905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8488404df12318c7175633932a7778c1225055b7808c6c020bd8dc398f881ca7`  
		Last Modified: Thu, 05 Feb 2026 22:18:04 GMT  
		Size: 156.1 MB (156130008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb445f8698f0686570ebd4b081d1774fe82b2e0e9dece90f3ef462ea794fbd69`  
		Last Modified: Thu, 05 Feb 2026 22:18:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12dd9c45b4dd3b7ddcb06bee37944e9923d7b11ebf668f41f76adca96bc2762a`  
		Last Modified: Thu, 05 Feb 2026 22:18:00 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b86c9c63f0be59a8e7ff8e50c6b09cd90fb39c384bf6c93460968effd84e79c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1276423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a828d44ccb6e3eb3e28f40d9a02d3406430903737420dcbf2cde0ebe847767`

```dockerfile
```

-	Layers:
	-	`sha256:66f1bdefc178e72a3eb64eb293992cc43922b63251cb9204f0738ed29748be95`  
		Last Modified: Thu, 05 Feb 2026 22:18:01 GMT  
		Size: 1.3 MB (1255879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41f2f100c2e3f2761339eacef38f816f817a11ad3bba87e6c06fd6c8831f732d`  
		Last Modified: Thu, 05 Feb 2026 22:18:00 GMT  
		Size: 20.5 KB (20544 bytes)  
		MIME: application/vnd.in-toto+json
