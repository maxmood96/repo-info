## `eclipse-temurin:21-alpine`

```console
$ docker pull eclipse-temurin@sha256:e23a0ed210af78c9e38d97c75be490b1e7bcf274d933d3dd09c7b45276024988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `eclipse-temurin:21-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:09aee388378356dc0d14f48d5685d988d0ecf9bdb4026322a5f9eaae8a7c69c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175159390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e524c4de31fa52ce7e99634e70bb5fe7551d8474fec87f823abd4c0f013e859`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:22:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Mar 2024 03:22:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Mar 2024 03:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Mar 2024 03:24:03 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/*
# Sat, 16 Mar 2024 03:24:47 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Sat, 16 Mar 2024 03:24:58 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ae933ea8eeb4a077f19277842ba95ba93d29177e44d53cec7a98afd3b9abb2c3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|x86_64)          ESUM='f1aef3652dd52778e81eb4897a88a34e38ca0159d22f160f7205e69907a0f14d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Sat, 16 Mar 2024 03:25:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Mar 2024 03:25:00 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Sat, 16 Mar 2024 03:25:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Mar 2024 03:25:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6fa00702eb0aa7934afc50cb28145402935b385451bcb6ae891ecc0d4a9b90`  
		Last Modified: Sat, 16 Mar 2024 03:27:45 GMT  
		Size: 13.1 MB (13136633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d612c1d04b376743b394b68467423c1b2caae2a70e06e7c7ba24e11fbc29ca5d`  
		Last Modified: Sat, 16 Mar 2024 03:28:46 GMT  
		Size: 158.6 MB (158613135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549d9f50a51df057355cfbbaa0f094954f8d8b227b6a91c110bfd718d5410fd7`  
		Last Modified: Sat, 16 Mar 2024 03:28:26 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a33d3f3feeb368051b5b1fb0ca441b7e4369a393131de1c86610a736ff8a6d6`  
		Last Modified: Sat, 16 Mar 2024 03:28:26 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:e8690522b7910c1fd5b5c85cb931780533dea9f2f7a379afed645a9d3da5a24b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173352744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f470669af4674579d1bf81b3328c904d28861a492af118ff575be327f7094c35`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:59:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Mar 2024 02:59:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Mar 2024 02:59:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Mar 2024 02:59:30 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/*
# Sat, 16 Mar 2024 02:59:30 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Sat, 16 Mar 2024 02:59:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ae933ea8eeb4a077f19277842ba95ba93d29177e44d53cec7a98afd3b9abb2c3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|x86_64)          ESUM='f1aef3652dd52778e81eb4897a88a34e38ca0159d22f160f7205e69907a0f14d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Sat, 16 Mar 2024 02:59:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Mar 2024 02:59:41 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Sat, 16 Mar 2024 02:59:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Mar 2024 02:59:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c44d4fdb48b09df8f24503c1c37d34a4c111822cd814c6284a4fa1c69a3528`  
		Last Modified: Sat, 16 Mar 2024 03:01:12 GMT  
		Size: 13.4 MB (13416220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61468841df6d54b5eeb33a27e60b2ad03e9441573419ddd9790233c3c294b9c`  
		Last Modified: Sat, 16 Mar 2024 03:01:21 GMT  
		Size: 156.6 MB (156587916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8d69320f28893a392ebc4217f9872163cbe1b1e7442dbb4354471d823c1847`  
		Last Modified: Sat, 16 Mar 2024 03:01:11 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec6b5f8dbeb3920a8e64ff7eaecc4e79a162e39081411608c28e85d36afefde`  
		Last Modified: Sat, 16 Mar 2024 03:01:11 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
