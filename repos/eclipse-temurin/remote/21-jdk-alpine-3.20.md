## `eclipse-temurin:21-jdk-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:108c96f846c4f8affd722908f8392eb15d123b21395616dfbf8b2e6f48db44fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jdk-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2bff8f1646e0b7bae9d9f1f8aaa8d86aa323ee5822d660e6b4eac33ce233125e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182476499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35558f58da1a33eb023693e6417e26283fbc6f24da4f8a521e3ed2c89466f59f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:18:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:18:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:18:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:18:56 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:18:56 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:19:04 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='19eba6c3877612157ef1f46deb92745b4567cfcd64b79f15449c68cd2b7501e3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='8eb39f442c3c603e414af43844b419a9b5d4f3fe221181f323aa4eec1bd20cf8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:19:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:19:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:19:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:19:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35398ed5f265d62ebaf53a3e67aebe99e3930d40789db41d93e703b1095a080f`  
		Last Modified: Thu, 05 Feb 2026 22:19:20 GMT  
		Size: 20.7 MB (20727406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938894ece6ad91873f5011550ff24aafb2f865ced366f21d392b9cd2698a9acf`  
		Last Modified: Thu, 05 Feb 2026 22:19:23 GMT  
		Size: 158.1 MB (158118819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0481d03d4e190421e4c9cc506c8b25cdd785cc9f09791805f3a81557c8e184d`  
		Last Modified: Thu, 05 Feb 2026 22:19:19 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc06e80edc5409ae0929a547d14445d55fa8cfc18a651c949b03b2a234c67eb5`  
		Last Modified: Thu, 05 Feb 2026 22:19:19 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:180309690e235b4c91e7239f514cc65d284a8849507fdfb67273c9aebc33ef42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1093846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a197b677c37d3f38850f4fbf894413f8fde9f2483e40b2c93e57d9fb3ff62cd4`

```dockerfile
```

-	Layers:
	-	`sha256:0f37548ca27fa33e40d73249c5bd6b1b7324befffa83c05734e112bd1218ebc8`  
		Last Modified: Thu, 05 Feb 2026 22:19:20 GMT  
		Size: 1.1 MB (1073424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86f63e355077d235cc156ec07171f9ea81413707672147a3248475dc756fa596`  
		Last Modified: Thu, 05 Feb 2026 22:19:19 GMT  
		Size: 20.4 KB (20422 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-alpine-3.20` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:b66f46cfb4b8bb671fef9c09b0b6d5dcb6172fce867a212951cfb58199c2d81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181332479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae0de3e90e46be5eba6f5b09e2c79ce6e3bb4170b981e2dfa7a5aef0614dcf0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:17:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:17:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:17:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:17:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:17:32 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:17:41 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='19eba6c3877612157ef1f46deb92745b4567cfcd64b79f15449c68cd2b7501e3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='8eb39f442c3c603e414af43844b419a9b5d4f3fe221181f323aa4eec1bd20cf8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:17:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:17:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:17:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:17:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4deb4a15152d5acaee772c53471699fa828bad431802f6decedabbdcda0b1968`  
		Last Modified: Thu, 05 Feb 2026 22:17:59 GMT  
		Size: 21.1 MB (21110124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cab5fd6ca07b1f3a727093b8413c9e1edd372a9b3cdc2be9afe58ecc782056`  
		Last Modified: Thu, 05 Feb 2026 22:18:02 GMT  
		Size: 156.1 MB (156129986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87fbddc51c06224fe49ca57012fb4c34ed5f06d4c43ef0c0dbc16f0e988bf29`  
		Last Modified: Thu, 05 Feb 2026 22:17:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45ebe2b2ea8774cb30fdfc06e6c39e40cc26e5cdb1c15b85a9bd20ee630d4d8`  
		Last Modified: Thu, 05 Feb 2026 22:17:58 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4cb0bb08eaac0e0c2efbed598078c5cfe8583fd05cedc9f1af34812364a65ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1198488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3258280a877316191af0b913107f4699e93552214de489bd456374531a79fd5a`

```dockerfile
```

-	Layers:
	-	`sha256:b9588a87351f76fb1f9ffdbaf57a74284b0892321ba22b941d632938d22ba055`  
		Last Modified: Thu, 05 Feb 2026 22:17:58 GMT  
		Size: 1.2 MB (1177944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72355bbd91af6e25e25b4c0fd2463e96d53177b9914b9f40e5e21323e890024a`  
		Last Modified: Thu, 05 Feb 2026 22:17:58 GMT  
		Size: 20.5 KB (20544 bytes)  
		MIME: application/vnd.in-toto+json
