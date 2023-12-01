## `eclipse-temurin:21-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:075f8207cbfecf7e509e2d93e2ffc36c097b52a8109a9bfd40326fa12bd5c438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `eclipse-temurin:21-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:7e1c2f37fffae18238a4bb018080a0a46d23bfe646d0e1eaacb35a4fdf383a2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174209390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9017e7c8441517b002e05be8e72b0032d6d55e108e720c8ac6a5255d5611baa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:11:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Dec 2023 07:11:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Dec 2023 07:11:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Dec 2023 07:12:38 GMT
RUN set -eux;     apk add --no-cache         bash         fontconfig ttf-dejavu         java-cacerts         libretls zlib         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/*
# Fri, 01 Dec 2023 07:13:19 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Fri, 01 Dec 2023 07:13:28 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='77006c0a753808c2a6662007906eb6eb230f2fb6eb9d201a39cc46113e68f82c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.1_12.tar.gz';          ;;        amd64|x86_64)          ESUM='422f23f5109056cacb9227247bebf8532e2dc3c9d505e71637ba610569d6b3ff';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 01 Dec 2023 07:13:30 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 01 Dec 2023 07:13:30 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 01 Dec 2023 07:13:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Dec 2023 07:13:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5820a814e8c90e2b86457ad1da29a79516ae242489d7bf67ea216d150c1efdc`  
		Last Modified: Fri, 01 Dec 2023 07:15:58 GMT  
		Size: 13.1 MB (13141060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0a188ff282b81403d8a726aacd5d985ef4761a8a8f5c876dea381e7a9337a2`  
		Last Modified: Fri, 01 Dec 2023 07:16:52 GMT  
		Size: 157.7 MB (157664998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1103e3032e0ab2751fa60d490107a4b908c287ed9264496a5285c5127ba8a8b1`  
		Last Modified: Fri, 01 Dec 2023 07:16:39 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab03e20f0bc9420a8ab17a6aa1f2cad9ff28b9394902fedb9e44ef361a7edca`  
		Last Modified: Fri, 01 Dec 2023 07:16:39 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:768908667a4899249022fc59fc9c2d86e14565d498655eda063428301ad54ed7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172523877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a24cbf090ca23a29b38828d7e5c16dabd14387b9b26465446adead71bd286d2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:26:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Dec 2023 03:26:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Dec 2023 03:26:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Dec 2023 03:26:43 GMT
RUN set -eux;     apk add --no-cache         bash         fontconfig ttf-dejavu         java-cacerts         libretls zlib         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/*
# Fri, 01 Dec 2023 03:26:43 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Fri, 01 Dec 2023 03:26:51 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='77006c0a753808c2a6662007906eb6eb230f2fb6eb9d201a39cc46113e68f82c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.1_12.tar.gz';          ;;        amd64|x86_64)          ESUM='422f23f5109056cacb9227247bebf8532e2dc3c9d505e71637ba610569d6b3ff';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 01 Dec 2023 03:26:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 01 Dec 2023 03:26:55 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 01 Dec 2023 03:26:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Dec 2023 03:26:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44021108607f2b7d09544b8ac8de2c0e834ae38973587f6926bb5bb3adb965cf`  
		Last Modified: Fri, 01 Dec 2023 03:28:23 GMT  
		Size: 13.5 MB (13515679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0494811225c212d40527e810cdcd91c8dc2912553e44fa5225e42ae8b87f7657`  
		Last Modified: Fri, 01 Dec 2023 03:28:32 GMT  
		Size: 155.7 MB (155674255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53980a556110a0b82ea03d71034d2ef199e5025d24d6aeeb87bf90e290c22f55`  
		Last Modified: Fri, 01 Dec 2023 03:28:21 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4d2d03fb1bdd8b5b90a0605efe17ba79e0bea7c57e87fb989fb645490c8fcb`  
		Last Modified: Fri, 01 Dec 2023 03:28:21 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
