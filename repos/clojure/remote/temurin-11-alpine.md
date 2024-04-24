## `clojure:temurin-11-alpine`

```console
$ docker pull clojure@sha256:df6573c23ce6c9ef37dab83a6edab579b09607752db109c06d70ffb4c6cc5046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-11-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:fc8001a07f3de091c04fd592c2d25dc1eccdbaa2accf669f0b7a64086169a26a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177641326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94a4431cea25ffe72b8676886ded07933722dc94270161072750b9d1a87faa5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b45c467be52fe11ffd9bf69b3a035068134b305053874de4f3b3c5e5e1419659';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Wed, 24 Apr 2024 21:21:39 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:21:39 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:21:44 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Wed, 24 Apr 2024 21:21:44 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:21:44 GMT
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
	-	`sha256:6375d72bd15b0291aaba9d6ead3e6c16979fc8fd322b5b4f95562a2f1bfe11a1`  
		Last Modified: Wed, 24 Apr 2024 19:09:59 GMT  
		Size: 140.7 MB (140685938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f5ef7c6218be43cbec322c87c9bc0bbb141a5b16a3143f142c578f7f46a65b`  
		Last Modified: Wed, 24 Apr 2024 19:09:48 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a23006a5c01a7721ee3675366be401e445e754026e9c495eac262bc32956f6`  
		Last Modified: Wed, 24 Apr 2024 19:09:48 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5627f8fabf37633885fa30863b327da9e20b2c3c41b2dde785f928f8a0682167`  
		Last Modified: Wed, 24 Apr 2024 21:45:33 GMT  
		Size: 25.0 MB (25007727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c10cfd5ce61500970094fce1cdd15447d3a600a7f1da03f474a3fa93a1c06`  
		Last Modified: Wed, 24 Apr 2024 21:45:31 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
