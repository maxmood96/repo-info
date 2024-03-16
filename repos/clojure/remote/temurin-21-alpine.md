## `clojure:temurin-21-alpine`

```console
$ docker pull clojure@sha256:3c64c9c92fb27d00351281f4a0fb580f2d8a49a2283d1528abe80efebb07f56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-21-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:82f2acb29485be523a15ddc98b0caa0cb440c7b2a1d58d23ad2472a68f40a804
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200166739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905a98914a0ae83b601a293ad2da651acb3219280cb03351ef7585cf5d4e26be`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
# Sat, 16 Mar 2024 12:04:29 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Sat, 16 Mar 2024 12:04:29 GMT
WORKDIR /tmp
# Sat, 16 Mar 2024 12:04:34 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Sat, 16 Mar 2024 12:04:34 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 16 Mar 2024 12:04:34 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Sat, 16 Mar 2024 12:04:34 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Mar 2024 12:04:34 GMT
CMD ["-M" "--repl"]
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
	-	`sha256:6041a77b9f2624824f2a09da0102ded6d95a8aba98c986a8a26c10da7de4f54a`  
		Last Modified: Sat, 16 Mar 2024 12:08:26 GMT  
		Size: 25.0 MB (25006320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65279956228fab09a5d1b18e24d152f7ce8e2b45d11897da5cf9d91a6b4f26a`  
		Last Modified: Sat, 16 Mar 2024 12:08:24 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b856178408bfe05c10b17fa465f5eb894b5a8907dba2733230e0c41cc92691`  
		Last Modified: Sat, 16 Mar 2024 12:08:24 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
