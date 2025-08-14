## `eclipse-temurin:24-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:8fdbcb6bc6b846640cea7058e6eeb56c311fae4efaa506a213789134065c6b90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:24-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9dc3c4de908aa35846266d775e171c6061583bb9a33c47bdb01d98e122c15078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (115039366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404fca2a1a114eb997831fc61c25e7020f20595cfe6c4d834de722a00492ef80`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='5563867bf1abfc466c59bf3d08e9957a30666fe96fb8f9c5bae939ab11d262d5';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='947ba234c65cdbd4d852e8f2812334ed093530d86b32cca5d9b45d6672186f77';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5ef2386be4a27ea92a01ef0263a3104d9355ac7f4fb22aa55e2a91eeee344e`  
		Last Modified: Mon, 04 Aug 2025 20:12:09 GMT  
		Size: 21.1 MB (21104348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eae701b9ed8b56a4df38c4ec9b72d1f048c6055ba56cff62e61db3768256810`  
		Last Modified: Mon, 04 Aug 2025 20:12:16 GMT  
		Size: 90.1 MB (90132918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939aba76ded566210b691bda00b92ffc2029071fc4984207e3c7d6dce00328d6`  
		Last Modified: Mon, 04 Aug 2025 19:25:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907d1c29ddd75894bbcf074eab7ed68afbe4634ea810f2cf54368a7eec0eb6bc`  
		Last Modified: Mon, 04 Aug 2025 19:25:57 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:19513098d4de466b9841aecd45d217844b0021959ef267352fb677c7e3b075c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1073260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ad4a0adf97d2ab813932b07802dcaf44f0ac0f61bbdee1d73c662ed4d35f5a`

```dockerfile
```

-	Layers:
	-	`sha256:d4fc0ed71f041d4cd2cd0f9f403a0b2e1dced6aa1c3d58292ff2c3d13a456902`  
		Last Modified: Mon, 04 Aug 2025 21:24:37 GMT  
		Size: 1.1 MB (1051802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cfd0c12b90086ced04deb8a1a2bb26983d5e1deea5abc6cb7ffd4256496a3e1`  
		Last Modified: Mon, 04 Aug 2025 21:24:38 GMT  
		Size: 21.5 KB (21458 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-alpine-3.22` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:7354369a87d89c9a1a1d0539c1c09d24d0b9492365b15416173c0f1020caa383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114398703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8acdeffd78763dc23bea0e2deb83f806a33f2da3592e1ce826bc25565d1032`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='5563867bf1abfc466c59bf3d08e9957a30666fe96fb8f9c5bae939ab11d262d5';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='947ba234c65cdbd4d852e8f2812334ed093530d86b32cca5d9b45d6672186f77';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a495748323e0cdac275f94a75856b53137d10e7dd79d59568fe601407fb00e`  
		Last Modified: Mon, 04 Aug 2025 19:31:51 GMT  
		Size: 21.1 MB (21148725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f503b83c17e606e525a15bdf8c088d8b510866bd192730491923c7e09021b161`  
		Last Modified: Mon, 04 Aug 2025 19:39:38 GMT  
		Size: 89.1 MB (89116820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e121434e3e7ced93721c74730970c4545f0d07a1ab8a3cb707d8d97621657a`  
		Last Modified: Mon, 04 Aug 2025 19:39:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94585305800850d7db8da0cf8b919141fa5eb89e43d0bf4133469159f0960634`  
		Last Modified: Mon, 04 Aug 2025 19:39:33 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c19ac06e5eac0c9662dbb728f1ea5bd1a65616bc27f599afec54e188872fbd87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1223453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194a025884e6f5fe856cc5080a90fb13ca3bcb5ba03208ba7fed384f1e606198`

```dockerfile
```

-	Layers:
	-	`sha256:afc4e973d286fe3aa3ce4342a0577c17c8e815d173dbed6b62e0f86998540a61`  
		Last Modified: Mon, 04 Aug 2025 21:24:41 GMT  
		Size: 1.2 MB (1201837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd256d205b29ccdc9c44e2a1c6c91b2f4c8ce561b500a575fe20b5509fa0fcc5`  
		Last Modified: Mon, 04 Aug 2025 21:24:42 GMT  
		Size: 21.6 KB (21616 bytes)  
		MIME: application/vnd.in-toto+json
