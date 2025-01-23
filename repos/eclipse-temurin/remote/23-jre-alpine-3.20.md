## `eclipse-temurin:23-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:8e45e319f105a5cd4e43406ae19045fc109dfa964a924ebf05f9c254c28baabb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:23-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:34edbc7c5e4ed91d765377696dd1c61d8bc9e2c85760004b420966be456eadb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72775432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ceb618f1bc13b200128ab1d32e693186c10a39917260af0247980b0f0c4d05`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Jan 2025 01:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 01:19:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='b56eaedc094cb9107be2d5be9ad34c3dd9492c45aa671d102b5829a488cfc744';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='38a1b20b5ee8869b20e9f9aefdc91eedf245584d35287842a66540f0745dd3d0';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf97c9b3846c4237731ac8d347afd462b262bfb591f5e7f857c325b204a8f3d`  
		Last Modified: Wed, 22 Jan 2025 18:29:00 GMT  
		Size: 16.0 MB (16022224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9833fae3fad23edef423f32b9b200fb06714da5798b1fe8da024b65d0483c13e`  
		Last Modified: Wed, 22 Jan 2025 18:29:01 GMT  
		Size: 53.1 MB (53124540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49747f92db83e58423b17f355e08d2f6c385e652eac821b2eda2ad0aa235c5c3`  
		Last Modified: Wed, 22 Jan 2025 18:28:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3377759dcee75d1f139fb37d8d10a5ceaa62a04d896c4afe40175aa11d201c`  
		Last Modified: Wed, 22 Jan 2025 18:28:59 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5f5720628224400ccdf44428e7e15c7e0d2e091ab93b5704cfd210d7e893df3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **906.2 KB (906171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1244c859faca719c3dd127450f01d0aff3e3a5da2c3bee2920dbad8a50e02d`

```dockerfile
```

-	Layers:
	-	`sha256:a22c5b8f847d855e9e808a13db48629c8a42f211733f1dc5209b201d40846924`  
		Last Modified: Wed, 22 Jan 2025 18:28:59 GMT  
		Size: 887.1 KB (887103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2649ac2293a1869d5999a9d83a9a38de342c44cb3b5ebe914274b4c6ffee661e`  
		Last Modified: Wed, 22 Jan 2025 18:28:59 GMT  
		Size: 19.1 KB (19068 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-alpine-3.20` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:4ddadcd6114ffa43b12d516607314a6e5d7666148bc300aa7fb40b1dd417df17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72357174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa79ad77349e3e2edff91776c6a7b28ec9d38e8b8f6bf63044651fa6be399e91`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Jan 2025 01:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 01:19:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='b56eaedc094cb9107be2d5be9ad34c3dd9492c45aa671d102b5829a488cfc744';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='38a1b20b5ee8869b20e9f9aefdc91eedf245584d35287842a66540f0745dd3d0';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539ef939d4f3419215ec7a0fb03915a0ee2eae3cc91741b20cdc867be6436ac8`  
		Last Modified: Wed, 22 Jan 2025 21:11:39 GMT  
		Size: 16.2 MB (16187864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206c33b8345b81e42a23f2605d61498009d484ea46c026e1379974cfc30adebb`  
		Last Modified: Wed, 22 Jan 2025 21:16:34 GMT  
		Size: 52.1 MB (52076135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fe6c8710d6839af7f8c515b913ca95b550d600068414de19225a67b46c4bbe`  
		Last Modified: Wed, 22 Jan 2025 21:16:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62336ba0fd0ec6a4ebfadfdad3a6aef193b2f591ee91c4061931534697dda397`  
		Last Modified: Wed, 22 Jan 2025 21:16:32 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:71b286886f0af7809fffca01e936b4bffbc4080b87475a3a14720cc222e4a1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **905.1 KB (905074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16918df5f670dd9eaf8c00ac057d7e4a439af2e2584c3e1f191bef77953a5780`

```dockerfile
```

-	Layers:
	-	`sha256:f740cf9485355d4cb4911fb4ad8b635fca912c16e3a243fa5d015ed2ad2b8d10`  
		Last Modified: Wed, 22 Jan 2025 21:16:32 GMT  
		Size: 885.9 KB (885896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91839b9d54034904936383fd3db40ec220c7932d198242738cb300fb56b1f01c`  
		Last Modified: Wed, 22 Jan 2025 21:16:32 GMT  
		Size: 19.2 KB (19178 bytes)  
		MIME: application/vnd.in-toto+json
