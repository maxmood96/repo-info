## `eclipse-temurin:21-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:9a21ac97b76e52f4b58d5d6c7fdd459cd600cce8724a31fc0a2b4346b35bced2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `eclipse-temurin:21-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:98963ed09c4fd82e128c6cc9e64d71798239b824164276626d79b8f9e666ac0e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69652231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4914e3ddb9fa05c8af3baf74fbaef1144b3a122bb31e75a4d0cccf10c8b5a87`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Fri, 01 Dec 2023 07:13:43 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2898ea1ddf6f70f09b09cf99d928f6d4c862f78f81104f5dce3e44a832b8444a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.1_12.tar.gz';          ;;        amd64|x86_64)          ESUM='a8fcc43927664ba191c9a77d1013f1f32fec1acc22fe6f0c29d687221f2cc95d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 01 Dec 2023 07:13:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 01 Dec 2023 07:13:44 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 01 Dec 2023 07:13:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:7eb0e0966f8cc835f3d3a483b71a14d7d77316b572590eb5939f666628f4a6eb`  
		Last Modified: Fri, 01 Dec 2023 07:17:12 GMT  
		Size: 53.1 MB (53107853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c432e8ceb055226cee91abbb52b686f14a2844a21e0581121ea7d326eb0e4793`  
		Last Modified: Fri, 01 Dec 2023 07:17:05 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f9f010fdd74178cb5351c8cd057c6887939fa59c631e03ede532a24ce09a2a`  
		Last Modified: Fri, 01 Dec 2023 07:17:05 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:50de1de903365a5ab21ae15213335962a1949027a54b3f1e72798ae584d42e66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69028054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92673ef1efd5b9ddba371b13226ac2abb5d768e45bed838c7d8c0794904f7db`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Fri, 01 Dec 2023 03:27:03 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2898ea1ddf6f70f09b09cf99d928f6d4c862f78f81104f5dce3e44a832b8444a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.1_12.tar.gz';          ;;        amd64|x86_64)          ESUM='a8fcc43927664ba191c9a77d1013f1f32fec1acc22fe6f0c29d687221f2cc95d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 01 Dec 2023 03:27:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 01 Dec 2023 03:27:05 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 01 Dec 2023 03:27:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:bb31aaab2e29fd9e25abe4c69c397fdf53b9f9d8ce194b9511191e9f47fbfba2`  
		Last Modified: Fri, 01 Dec 2023 03:28:50 GMT  
		Size: 52.2 MB (52178448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8832e434f7b1f89f69629d6902cae47e8a8cb294ff631c23474e7d4b02f5b025`  
		Last Modified: Fri, 01 Dec 2023 03:28:45 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fc4700aeebcd0229473c351033e36b1ecdf21a8972a097c43a6aa2a1649c47`  
		Last Modified: Fri, 01 Dec 2023 03:28:45 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
