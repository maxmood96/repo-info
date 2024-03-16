## `clojure:temurin-17-tools-deps-1.11.1.1435-alpine`

```console
$ docker pull clojure@sha256:4e8b68225dd68160a2d3bc51bc92179747ffb55834d0b481a9b3eca66f0ea305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-17-tools-deps-1.11.1.1435-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:208b53605afa88bb0d545dbda024ccd4a19833340f39f0f4a381732573caebc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.7 MB (185696045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04aeb3083b5f6881de1d98baad7d7efdd8385132b491adf9119032f6568506c8`
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
# Sat, 16 Mar 2024 03:24:03 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Sat, 16 Mar 2024 03:24:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ce4085548f73ec97fa870de3f7da87634b4cbbf9753600365e2e0b255585e7e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Sat, 16 Mar 2024 03:24:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Mar 2024 03:24:14 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Sat, 16 Mar 2024 03:24:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Mar 2024 03:24:15 GMT
CMD ["jshell"]
# Sat, 16 Mar 2024 12:03:39 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Sat, 16 Mar 2024 12:03:39 GMT
WORKDIR /tmp
# Sat, 16 Mar 2024 12:03:44 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Sat, 16 Mar 2024 12:03:44 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 16 Mar 2024 12:03:44 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Sat, 16 Mar 2024 12:03:44 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Mar 2024 12:03:44 GMT
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
	-	`sha256:dc145c2c40b090019607ad8d5618e1026c57507c6622d156be1870fa790a7339`  
		Last Modified: Sat, 16 Mar 2024 03:27:56 GMT  
		Size: 144.1 MB (144142428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65413771e18cd2c82e4675596f5160e42af611ff7d9eabbe7621c2d626bd9b6b`  
		Last Modified: Sat, 16 Mar 2024 03:27:44 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f39855dd57cb06f224fd5f6e6327f6551e336425c751b77c2f53f11ba7ce94`  
		Last Modified: Sat, 16 Mar 2024 03:27:43 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba21eb07ffb6d9238c53980b1761349f5dfb7e5bc01cf89e9988f1fe34a74441`  
		Last Modified: Sat, 16 Mar 2024 12:07:53 GMT  
		Size: 25.0 MB (25006333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ab4bbc3b6202ed37018a406bf397605ca2d3f85bc3c21cd907742754fe3816`  
		Last Modified: Sat, 16 Mar 2024 12:07:51 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21bc9ad1a783cdabdd5ae79393cf3b5f160871bb65e2941ec24c33bc2764a31`  
		Last Modified: Sat, 16 Mar 2024 12:07:51 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
