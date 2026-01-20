## `eclipse-temurin:21-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:28ed6e1a345d150234c2a613a78196b73bb7dd34691f33032845f0b67202e321
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:09c8660e42ab2a57622e65c5e4af717b0aa1cf74acbf2512419625cd610a2bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183281529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8404114f76913e99459f53020efc2669c2195a7822bc62ae6447785569e5eb9d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 17:28:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Dec 2025 17:28:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Dec 2025 17:28:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Dec 2025 17:28:36 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 19 Dec 2025 17:28:36 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Fri, 19 Dec 2025 17:29:17 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6d3c2b956d6b837bfdc992e58488fb16c96e5852820e9feaa42a8672bbca9c7b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='52e30d3157432e87ee464b656f776f0a22946f1f3182eea779258284bc6f55da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 19 Dec 2025 17:29:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Dec 2025 17:29:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Dec 2025 17:29:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 19 Dec 2025 17:29:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2232d994f359616fc37802f318a1f2070d94a025888d07995589c780243827e2`  
		Last Modified: Fri, 19 Dec 2025 17:29:11 GMT  
		Size: 21.3 MB (21316021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a1d19d3786d967c9b0cf06b141e456299c1ee0a25b1475c31a7cb569db4176`  
		Last Modified: Fri, 19 Dec 2025 17:29:56 GMT  
		Size: 158.1 MB (158102995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b555e94649d12f3c5e3a4c245b010bbb0fd9cc46cf88a070f382aeaefd9985`  
		Last Modified: Fri, 19 Dec 2025 17:29:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7f63db9ee1f615ab54b00d117ebfe96a78619f45952995c5dc2a35a38b58e2`  
		Last Modified: Fri, 19 Dec 2025 17:29:42 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:02c79d4b4903ba1ca59efbe379aa4c0e66006f04c9533e246d8402e3aa0a5612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1128864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9655da02df708627313fd0d28f9dc9580f4a5c33b8bf6e42752dffb80f3d807c`

```dockerfile
```

-	Layers:
	-	`sha256:685f0db62abb88fa0fbb476014f1e90f2bf3b71f1017bf4a2c52b9405c57a26a`  
		Last Modified: Fri, 19 Dec 2025 19:14:14 GMT  
		Size: 1.1 MB (1108443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7634c5de6810c19a8555235cdb68f995c724938dcf4b828fa1672ed5ea4566f5`  
		Last Modified: Fri, 19 Dec 2025 19:14:15 GMT  
		Size: 20.4 KB (20421 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-alpine-3.23` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:62d589b14f5347de0712b7ef6db8f809e6858d13ab6854ee94cadd507d42be40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181607799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bafdd7e1a9430ce600cd394d09e78404846e8251677c33b7290c6eab4b0a0c2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 17:28:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Dec 2025 17:28:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Dec 2025 17:28:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Dec 2025 17:28:19 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 19 Dec 2025 17:28:19 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Fri, 19 Dec 2025 17:28:27 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6d3c2b956d6b837bfdc992e58488fb16c96e5852820e9feaa42a8672bbca9c7b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='52e30d3157432e87ee464b656f776f0a22946f1f3182eea779258284bc6f55da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 19 Dec 2025 17:28:29 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Dec 2025 17:28:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Dec 2025 17:28:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 19 Dec 2025 17:28:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a6a3459c291403c5a68a32dbf6a16e15581e4c8bb5747a835819efbf6f34f1`  
		Last Modified: Fri, 19 Dec 2025 17:29:05 GMT  
		Size: 21.3 MB (21312166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90371aeefd371c92f76eff1d58d3be778b2791f394b4ef6a32acd4975a4bdf8e`  
		Last Modified: Fri, 19 Dec 2025 17:28:49 GMT  
		Size: 156.1 MB (156097484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a8a1fd74d507b6062a3ab22279e1b644919ec1741d041a3c5f2e5b05d597ae`  
		Last Modified: Fri, 19 Dec 2025 17:29:03 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eae93fca4a4177c7877ebf535288042cee517af8a199f7123a91bb4c55e3600`  
		Last Modified: Fri, 19 Dec 2025 17:29:03 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7fcddf6cc2180d4e786653c7d1bcabc589f9bb8a9304aaf342743093dde4b7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf7ec9dcf5cd02e7c72e282a6a4db8a54d827ad612a269e3766e8dcb444317f`

```dockerfile
```

-	Layers:
	-	`sha256:788912166ee1b21c57febbc2ba0e99e4b3d1bd2b7a259f650030029e91a6b945`  
		Last Modified: Fri, 19 Dec 2025 19:14:18 GMT  
		Size: 1.3 MB (1257795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35099086dbe0731aa0104bdfb6f8ecd78b394ea7fb27086ebddc967e96e7f249`  
		Last Modified: Fri, 19 Dec 2025 19:14:19 GMT  
		Size: 20.5 KB (20544 bytes)  
		MIME: application/vnd.in-toto+json
