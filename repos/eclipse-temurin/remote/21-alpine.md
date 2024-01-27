## `eclipse-temurin:21-alpine`

```console
$ docker pull eclipse-temurin@sha256:6da40af213861c1b9cc475affa011d395d4dbcf0cb031b6a5d05a658fd9e3c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `eclipse-temurin:21-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:82698e23d15ada036bc176f6fb210401e0679cd0a4b1e71d05e7329982d6062c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175160725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13b621e73dc63fb6be52dc6540fb34c92b98a0e85c69dea04289c03aa53d91b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Sat, 27 Jan 2024 00:55:13 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ae933ea8eeb4a077f19277842ba95ba93d29177e44d53cec7a98afd3b9abb2c3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|x86_64)          ESUM='f1aef3652dd52778e81eb4897a88a34e38ca0159d22f160f7205e69907a0f14d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Sat, 27 Jan 2024 00:55:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Sat, 27 Jan 2024 00:55:16 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Sat, 27 Jan 2024 00:55:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 27 Jan 2024 00:55:16 GMT
CMD ["jshell"]
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
	-	`sha256:6b168e20b9f2c7cde9300b36733340d229efb681e7862b716580cdb07cdb572e`  
		Last Modified: Sat, 27 Jan 2024 00:58:54 GMT  
		Size: 158.6 MB (158613083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98795b95bb4830f88ab5d81f355f8a6f3bd833705d858023f9b58c42457db454`  
		Last Modified: Sat, 27 Jan 2024 00:58:42 GMT  
		Size: 179.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4451c8b3dbe1616b4f1d08ac6cbd135f48e3d3393f2c37402ac18b0b845dfdc`  
		Last Modified: Sat, 27 Jan 2024 00:58:42 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:fd28672bba78b9e74f03e7947499d26a52a9af3bd2c5f4615f07a9888d176858
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173354733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209a4b28f887dd7bd6a58734e592ce793782cbd3de053f137a7bbda1fc055f70`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Sat, 27 Jan 2024 03:46:28 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ae933ea8eeb4a077f19277842ba95ba93d29177e44d53cec7a98afd3b9abb2c3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|x86_64)          ESUM='f1aef3652dd52778e81eb4897a88a34e38ca0159d22f160f7205e69907a0f14d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Sat, 27 Jan 2024 03:46:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Sat, 27 Jan 2024 03:46:31 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Sat, 27 Jan 2024 03:46:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 27 Jan 2024 03:46:32 GMT
CMD ["jshell"]
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
	-	`sha256:df9c9e6685a2ae143b5f3b5dd132fb2b8ef01400cdad01451f7b350df8a26e14`  
		Last Modified: Sat, 27 Jan 2024 03:48:12 GMT  
		Size: 156.6 MB (156587800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c74d189328b8c89a0f7b9849b36733dd2e63773868488fcf22bd27afee3656`  
		Last Modified: Sat, 27 Jan 2024 03:48:02 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723b91e6e1a5f23de9319adc2a59541f319806a968315622c47fc39feef24f59`  
		Last Modified: Sat, 27 Jan 2024 03:48:02 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
