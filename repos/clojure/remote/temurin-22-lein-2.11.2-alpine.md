## `clojure:temurin-22-lein-2.11.2-alpine`

```console
$ docker pull clojure@sha256:e1d676fcb6e56a963612e8e48d2c8ff798544a76e2a8da22c9df141c26c247a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-22-lein-2.11.2-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:a9a5c814659a53e2b21e50ef6c11fd32d6abcef3f7519975afda43e004d9b6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194889613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac67d44e18193cd7a5afd289cb4b8ebadafafc04b22d71b9ec90994f870b222`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='86a7b47c9277f2fd063ec910616b3676d86553ab7d23aa3bd365e51a57be1dc5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_alpine-linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|x86_64)          ESUM='d226e44b3513942db855df9a8737d848f64069848970d4cfd35ee3c38f2525c1';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_alpine-linux_hotspot_22.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 15:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fd38fd7cf5b8d60c92e1aa46a24527229fb51b451491d35a7028a8a1d0aba4`  
		Last Modified: Thu, 28 Mar 2024 02:08:23 GMT  
		Size: 13.1 MB (13142803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c16e77c87132dd32f3d6a221cf59225fc030b9895a77d196cd77ff1ac25647`  
		Last Modified: Wed, 24 Apr 2024 19:18:13 GMT  
		Size: 156.9 MB (156934796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae397eb730e1b4d590698ce9937b2e515a07cc0649968abae9742be5bd6386`  
		Last Modified: Wed, 24 Apr 2024 19:18:00 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f95ebed3ed7edeb5b3c167bdfe852d99210fccc2416f5950c1210d610e4914`  
		Last Modified: Wed, 24 Apr 2024 19:18:00 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a1de78b72073181d3ddf474c74566861eac418cdba4e6ebc128930757e5559`  
		Last Modified: Wed, 29 May 2024 19:58:02 GMT  
		Size: 17.0 MB (17003926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac57074d4780d571c777e0a09622b060c825d0313799b02aa37300764ff586d`  
		Last Modified: Wed, 29 May 2024 19:58:02 GMT  
		Size: 4.4 MB (4398008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae202f1b4141b13ce30f2f3efad958c719056bcbf2bf6b891e0af8057972ba8d`  
		Last Modified: Wed, 29 May 2024 19:58:02 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein-2.11.2-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:ce84109d592682021f9cdd7e708ee5cd717f8c9517854a08b0b2bcec3ff807c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1206595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f918e7d9fa60043fb0b089aceabac18699dc00e6acf929a76909f3313cbbd7a`

```dockerfile
```

-	Layers:
	-	`sha256:8d463ce80bcfa3840a08a2b8e49329c298268b846da236c969c5602d64a7b3cc`  
		Last Modified: Wed, 29 May 2024 19:58:02 GMT  
		Size: 1.2 MB (1188449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c9c89bf9ebb22e3540471515e9a714af83f7d72f6b3c5f4202869140df90ae0`  
		Last Modified: Wed, 29 May 2024 19:58:02 GMT  
		Size: 18.1 KB (18146 bytes)  
		MIME: application/vnd.in-toto+json
