## `clojure:temurin-11-tools-deps-1.11.1.1435-alpine`

```console
$ docker pull clojure@sha256:605acdc47c9e458830608d069502ace1e358c944809f27a1c2f3fe4896d89dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-11-tools-deps-1.11.1.1435-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:679d971aaab9333f5c016afd70fa71a23d0ba75c960632f1284d94da405f308e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177444731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1091df390d0421af714b2e7dd1fd08ac3a9a4b4a7479e3233ee454b07664eff1`
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
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b541c99a5de71ebbe53e7815f9222e377b814fa1025f9f5274cb7bad226809f8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 16:26:40 GMT
CMD ["jshell"]
# Thu, 28 Mar 2024 03:03:46 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 28 Mar 2024 03:03:46 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:03:51 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Thu, 28 Mar 2024 03:03:51 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 28 Mar 2024 03:03:51 GMT
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
	-	`sha256:62e821e71d8d63599c03e25acaa57493f1c151dca7cdea91999cc8883003352b`  
		Last Modified: Thu, 28 Mar 2024 02:05:38 GMT  
		Size: 140.5 MB (140489305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609bda70c76d2028175d3b7ef78a71175a915bbeedfd01351b9da4c5e9b04183`  
		Last Modified: Thu, 28 Mar 2024 02:05:27 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186466e209e780b86f3ff83c6bd480c04712356ea99074c42ddc0db13b43fffc`  
		Last Modified: Thu, 28 Mar 2024 02:05:27 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9956b47e4e1391fae5119a235d4f8638ce4092160ab347e7e774c2aee0ff464`  
		Last Modified: Thu, 28 Mar 2024 03:22:04 GMT  
		Size: 25.0 MB (25007766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f969089f5805b769de6326020d1291191f75b2a20402b0a0ab80687bfecbe5`  
		Last Modified: Thu, 28 Mar 2024 03:22:02 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
