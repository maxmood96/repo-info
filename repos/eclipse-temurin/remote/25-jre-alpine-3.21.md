## `eclipse-temurin:25-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:6fe7e033a984064edc91bc53d25e1ca342bd6e80cfb9a06ce9d54c0b2c8eb9e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:25-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:b0c1d742383b3dbb57f32806bd155031a355d39fb7fea48b8e79aa20a8aa4057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75030811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd818ecf71f3ff74e2e129d045302e20b27236e0ab85bfdfde78f25c4f365ec`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:24:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Apr 2026 00:24:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:24:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 17 Apr 2026 00:24:40 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 17 Apr 2026 00:24:40 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Fri, 17 Apr 2026 00:24:44 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='159099235c536b152f86111a694a8a03392948924736f354c79e95532dcfc1f8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='2cbb356c6923f89814b892561e6f0377ecf035ab0577e3162d2cf4e202d38ee7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Fri, 17 Apr 2026 00:24:44 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 17 Apr 2026 00:24:44 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:24:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53c129b148106e02243400eec07297a1b69d1e6f1ee5b968439e27e3697447`  
		Last Modified: Fri, 17 Apr 2026 00:24:55 GMT  
		Size: 9.4 MB (9390651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fbe84eb541ba4fa53d3c49a12185803b31e2df9c3c0720ed633e0135d7ee36`  
		Last Modified: Fri, 17 Apr 2026 00:24:57 GMT  
		Size: 62.0 MB (61990877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f54da5839633bbed05f5605c4a3e7ffe2feeefd559580b280223f7bb3a9353`  
		Last Modified: Fri, 17 Apr 2026 00:24:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2aa7e11bab7d27ce8bf62896e35c4e7ec20b609fb0ccf8633b0ccb288508f05`  
		Last Modified: Fri, 17 Apr 2026 00:24:55 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7bb833b68200505f8a96a483b6e8f4ad0e9a0e824b660b18f926cb957f31bb90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **817.5 KB (817495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ede842ef359a454596f617721f9b1aba8eae0f84b88462bc8a9a9657a6d1f82`

```dockerfile
```

-	Layers:
	-	`sha256:59a474d33482a494be2f10aa80a56dd740269aa9496e9672301cea465295c498`  
		Last Modified: Fri, 17 Apr 2026 00:24:55 GMT  
		Size: 798.4 KB (798358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eb3987bc1c720d6fb8dfdb28b67e5087d1c5eea8848fb346873615c255ab6b4`  
		Last Modified: Fri, 17 Apr 2026 00:24:55 GMT  
		Size: 19.1 KB (19137 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-alpine-3.21` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:334c6f42cf9435fc0a1f1faaec8d1601ad314f4ab24c15e8dbc24a0dcc9815c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74323234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff109f8b06d423f37cab7c2f6cdda5caf5f366a262cd0e83df94668a2e7bc41f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:26:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Apr 2026 00:26:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:26:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 17 Apr 2026 00:26:16 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 17 Apr 2026 00:26:16 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Fri, 17 Apr 2026 00:26:21 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='159099235c536b152f86111a694a8a03392948924736f354c79e95532dcfc1f8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='2cbb356c6923f89814b892561e6f0377ecf035ab0577e3162d2cf4e202d38ee7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Fri, 17 Apr 2026 00:26:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 17 Apr 2026 00:26:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:26:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a699a7218c9173571e6fd4d5daf2abf037e877969ee5d5da9062cc87947739`  
		Last Modified: Fri, 17 Apr 2026 00:26:34 GMT  
		Size: 9.4 MB (9414554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5c8532be79d31e4e72c3905982c32d62990b958dee66348f42d71151e1fbf3`  
		Last Modified: Fri, 17 Apr 2026 00:26:35 GMT  
		Size: 60.9 MB (60911805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e30d9a69a42adb86c7a934a228d3debaffd0e3ac83e10f317c5062d57c51bf`  
		Last Modified: Fri, 17 Apr 2026 00:26:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78757a844887349889703c066c8cf336f1835424c0061d12d66f436ceb95392`  
		Last Modified: Fri, 17 Apr 2026 00:26:33 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d3d1b181f461f0633c9c1faa06ab036092944a3a4ae4d309566fc523e8984bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **817.0 KB (817016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b7bc96e873b8c2ea03ef1044501c116338aeac3a4df57f3ef3c7f43ddfdf7d`

```dockerfile
```

-	Layers:
	-	`sha256:cd572c5944c382b9ecf84dc38d3a0ee803fa19d465ba61874e2dcee770cc3dd0`  
		Last Modified: Fri, 17 Apr 2026 00:26:33 GMT  
		Size: 797.8 KB (797769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b6cce3482f465f280a4dcc0017d66197060649aca65502cc7b88fe7216926b9`  
		Last Modified: Fri, 17 Apr 2026 00:26:33 GMT  
		Size: 19.2 KB (19247 bytes)  
		MIME: application/vnd.in-toto+json
