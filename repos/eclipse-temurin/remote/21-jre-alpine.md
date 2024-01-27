## `eclipse-temurin:21-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:fb4150a30569aadae9d693d949684a00653411528e62498b9900940c9b5b8a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `eclipse-temurin:21-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:8535a86d923e1e5ce62c67c53cf7699567ed228b23a7e52cd0c0ad68aafd1cd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70133445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1a3e2315a5fb8083fdfc250c4d79f76e1e2184a925a25a5dab481c457c757e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:52:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 27 Jan 2024 00:52:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Jan 2024 00:52:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 27 Jan 2024 00:54:20 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/*
# Sat, 27 Jan 2024 00:55:02 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Sat, 27 Jan 2024 00:55:30 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e961c43fa418a74d5349d519d4f05b70f2017b13420812946be88349729c8ff3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|x86_64)          ESUM='7077b9e42b40f1ed8d59a71ae59a57d5d55de2685cc5efd70a0405618da616d7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Sat, 27 Jan 2024 00:55:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 27 Jan 2024 00:55:31 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Sat, 27 Jan 2024 00:55:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59648cfc069f04a8d0eece9cae80e25155888dc9b5de722b58603efafaa0d78b`  
		Last Modified: Sat, 27 Jan 2024 00:58:00 GMT  
		Size: 13.1 MB (13138018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35c9fa25004890ec768946e87ce0d755c34bfd07e27d8bae379f20c6aee6b21`  
		Last Modified: Sat, 27 Jan 2024 00:59:13 GMT  
		Size: 53.6 MB (53585825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50073880371c033c1bdb5aa4e8a7fe527f86db249102e38705f0fa07b3f45e`  
		Last Modified: Sat, 27 Jan 2024 00:59:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c757a5f69f5e65ef6edb55386945661bfb4ccd7d449eaadcb8f28c7ceddeac0`  
		Last Modified: Sat, 27 Jan 2024 00:59:06 GMT  
		Size: 714.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:db8bb539babd307d430b0fbc5dfd1036939d45a105aadaa9def58ce2c7693d3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69411388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a65e82c70a681c104cdf5981e9e4c78588be6a53c082a6284d575a3b32588b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:46:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 27 Jan 2024 03:46:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Jan 2024 03:46:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 27 Jan 2024 03:46:19 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/*
# Sat, 27 Jan 2024 03:46:20 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Sat, 27 Jan 2024 03:46:43 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e961c43fa418a74d5349d519d4f05b70f2017b13420812946be88349729c8ff3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|x86_64)          ESUM='7077b9e42b40f1ed8d59a71ae59a57d5d55de2685cc5efd70a0405618da616d7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Sat, 27 Jan 2024 03:46:45 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 27 Jan 2024 03:46:45 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Sat, 27 Jan 2024 03:46:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945f0fd92e41144cd3d23a1785f5f548e99135347bb7d1d96ff2206ff016a0e3`  
		Last Modified: Sat, 27 Jan 2024 03:48:04 GMT  
		Size: 13.4 MB (13418324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8171aedde9885cca1000acf9c5a3cc796a977f33a4260a723ed6563c5be0dc97`  
		Last Modified: Sat, 27 Jan 2024 03:48:31 GMT  
		Size: 52.6 MB (52644473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dffde875525b04c8ae791154d48ee6c1da693b76345e13ad8a2cee8ff903a9e`  
		Last Modified: Sat, 27 Jan 2024 03:48:25 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e9f0fb1d0a45eb956b8d3f94099f313b01c4b327abd95e97960c33479a72ae`  
		Last Modified: Sat, 27 Jan 2024 03:48:25 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
