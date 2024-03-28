## `clojure:temurin-8-tools-deps-alpine`

```console
$ docker pull clojure@sha256:1dd4a2fa879c89a2ba22577f3be59be931c3b951cdaad49442c50f04340f9a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-8-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:6d66f8e9ef5941658ca02145c6577ea9183a64b04d45b43e96c28a24e94ce063
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138459185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f82713e261f3016ffca91cee04fb845177ca007fa827ab4934ab3a95a49bd1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2024 16:26:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 16:26:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 16:26:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c911fc057440f48c95f3eea8ec688732f43584e93fc0b090f5a361b2b6a64b71';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 28 Mar 2024 02:56:36 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 28 Mar 2024 02:56:36 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:56:41 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Thu, 28 Mar 2024 02:56:41 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 28 Mar 2024 02:56:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21a63612cbe8d148f75173be90696fbe03e2a6e9c901e2c039bcf1bcdeec0b9`  
		Last Modified: Thu, 28 Mar 2024 02:02:51 GMT  
		Size: 8.5 MB (8537401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b162d0e8210020d02e7636ec080e501544c8d98eee3cd62071575a779c741f`  
		Last Modified: Thu, 28 Mar 2024 02:02:58 GMT  
		Size: 101.5 MB (101503811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b33121868620153f81916270d545ef9ca6f753facd5958471db160fcc61c840`  
		Last Modified: Thu, 28 Mar 2024 02:02:49 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298ffa9577066ffef5d839c2df4a401e0e2199cf4b609ea7e5a4e86d8dce0db1`  
		Last Modified: Thu, 28 Mar 2024 02:02:50 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c347c27505a9be359278b0d6a68174d56484e0997ce1851920ad21884ce15a95`  
		Last Modified: Thu, 28 Mar 2024 03:18:06 GMT  
		Size: 25.0 MB (25007733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab6418d4dfd33af147643d9b6b3100c7ee88665d89c308caff8842676ea85ba`  
		Last Modified: Thu, 28 Mar 2024 03:18:04 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
