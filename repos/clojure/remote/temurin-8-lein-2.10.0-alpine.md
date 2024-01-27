## `clojure:temurin-8-lein-2.10.0-alpine`

```console
$ docker pull clojure@sha256:92992db48a3e933dc84ea659d182128e7e2bbc20d691b8c61856bbf80a3ba09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-8-lein-2.10.0-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:1f5bb7c5963821bebd5d13754e670ade5ef38201ff6fcaf8f9d986bb387aa142
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130156119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ad9c1ba86e180085c3b2dee1a7de9f6b1676a4dfa36ee94626db06fded49c1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["lein","repl"]`

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
# Sat, 27 Jan 2024 00:53:00 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/*
# Sat, 27 Jan 2024 00:53:00 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Sat, 27 Jan 2024 00:53:07 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c911fc057440f48c95f3eea8ec688732f43584e93fc0b090f5a361b2b6a64b71';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Sat, 27 Jan 2024 00:53:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Sat, 27 Jan 2024 00:53:08 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Sat, 27 Jan 2024 00:53:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 27 Jan 2024 09:50:27 GMT
ENV LEIN_VERSION=2.10.0
# Sat, 27 Jan 2024 09:50:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 27 Jan 2024 09:50:27 GMT
WORKDIR /tmp
# Sat, 27 Jan 2024 09:50:34 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Sat, 27 Jan 2024 09:50:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 27 Jan 2024 09:50:34 GMT
ENV LEIN_ROOT=1
# Sat, 27 Jan 2024 09:50:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Sat, 27 Jan 2024 09:50:39 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d043da2becbad64efc04c3177047b954002aa6a615a5716af19ecff2d3ff3ed0`  
		Last Modified: Sat, 27 Jan 2024 00:56:34 GMT  
		Size: 8.5 MB (8528146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8741ab9a3e5ee73cb0206f307b55a2726315260f8528cc938ff34f1c8e5d80b`  
		Last Modified: Sat, 27 Jan 2024 00:56:42 GMT  
		Size: 101.5 MB (101503872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7b717201f1ef54e5e4ba0b7f4e7bddef76d7bd0f701ef6da06fd4fed273681`  
		Last Modified: Sat, 27 Jan 2024 00:56:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8943f3da6bd76aaf14fa268110c75319364884fadf5883dfd91ca31e52f5e74`  
		Last Modified: Sat, 27 Jan 2024 00:56:33 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a3222bbf268aa70db4f33aad1a2ecde0519fd4936260d116cb9b6d40580c87`  
		Last Modified: Sat, 27 Jan 2024 09:56:03 GMT  
		Size: 12.3 MB (12315208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdde6fa0225615f3d3ce2f1f08755b03cb1aa1adf9f34a1daa4a4d41503850f`  
		Last Modified: Sat, 27 Jan 2024 09:55:58 GMT  
		Size: 4.4 MB (4399290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
