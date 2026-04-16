## `clojure:temurin-26-lein-alpine`

```console
$ docker pull clojure@sha256:d9be79f101d9a067b582d23f7369808b07e75f0151f3844b33f712664fd4114c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:48043a381f464876eb11f7364dc73611363380387b27173e1fa8756c083fdfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131510369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39df41deab2b782777c44ea97e87b3b711e259b0c882045e53ec7e74fdd9c17`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:34:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:31 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:34:31 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 15 Apr 2026 20:35:19 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='049027647a2d1cf3b1e3c1e7dad746aa6436928932bbed9130b87a25f585908a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_alpine-linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='c105e581fdccb4e7120d889235d1ad8d5b2bed0af4972bc881e0a8ba687c94a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_alpine-linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 15 Apr 2026 20:35:21 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:35:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:35:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:35:21 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:07:01 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:07:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:07:01 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:07:08 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg # buildkit
# Wed, 15 Apr 2026 22:07:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:07:08 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:07:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:07:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:07:09 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:07:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8bff7045b4dedcda28d3e173f14d1ba10aa99e2d37aca0e2fc2121c2c26408`  
		Last Modified: Wed, 15 Apr 2026 20:35:38 GMT  
		Size: 14.3 MB (14307228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391edefba2e6ae3493026f4fb7364e2b3cfdb3d6f20c95c057a840c7e2a70de4`  
		Last Modified: Wed, 15 Apr 2026 20:35:37 GMT  
		Size: 93.7 MB (93716220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195635ff26dc4127f92b360891f7063894021e91e54110ef34da2c8959f43c67`  
		Last Modified: Wed, 15 Apr 2026 20:35:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3caeef0ce8088f690976509ec2e96ce94d7badc8e863f438892920077dceff`  
		Last Modified: Wed, 15 Apr 2026 20:35:34 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8dce05375835b1100b05b350dbead9b7e9e92be9f2064dd7263f9a348d197e`  
		Last Modified: Wed, 15 Apr 2026 22:07:18 GMT  
		Size: 15.1 MB (15102212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc1aa127c1c5443b660906216988a409d8759e312a2f8d41b04687fdc99c9ea`  
		Last Modified: Wed, 15 Apr 2026 22:07:18 GMT  
		Size: 4.5 MB (4517678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9957a6951aa1d5c08321daf627156bf20a5e05c58d7ceee39d7190f1267a44`  
		Last Modified: Wed, 15 Apr 2026 22:07:18 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:c1662561892807316929a9bab9ec46f10afa2355ba974ef88b188805d86c36ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1046072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df44ce60dea7c6b77bfa227d4630189583687d1ec6382e509d5fc4043c5ff17`

```dockerfile
```

-	Layers:
	-	`sha256:524d7a119cea551738a3eebc130b9247a1302c7b5aec1b454b9ac0aab26ce6f5`  
		Last Modified: Wed, 15 Apr 2026 22:07:18 GMT  
		Size: 1.0 MB (1027872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e97b8730efd31f7a55b7347b8b57cff94fd7a5c58d0609eab747a92ee806b965`  
		Last Modified: Wed, 15 Apr 2026 22:07:17 GMT  
		Size: 18.2 KB (18200 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6d0665887ca347bc615dcee73c4063cd27c20bb37a05a4517b8af6eea00ad625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130876969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6cfb9dcfd68ba6a038bc8035caaf3dc4e75a8ef9bc6e7a3fe6fd39bea093c8e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 08 Apr 2026 17:28:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 08 Apr 2026 17:28:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:28:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 08 Apr 2026 17:28:08 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 08 Apr 2026 17:28:08 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 08 Apr 2026 17:28:18 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='049027647a2d1cf3b1e3c1e7dad746aa6436928932bbed9130b87a25f585908a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_alpine-linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='c105e581fdccb4e7120d889235d1ad8d5b2bed0af4972bc881e0a8ba687c94a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_alpine-linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 08 Apr 2026 17:28:19 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 08 Apr 2026 17:28:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:28:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 08 Apr 2026 17:28:19 GMT
CMD ["jshell"]
# Thu, 09 Apr 2026 23:36:03 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 09 Apr 2026 23:36:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 09 Apr 2026 23:36:03 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:36:09 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg # buildkit
# Thu, 09 Apr 2026 23:36:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 09 Apr 2026 23:36:09 GMT
ENV LEIN_ROOT=1
# Thu, 09 Apr 2026 23:36:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 09 Apr 2026 23:36:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:36:11 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:36:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ccdff04ff7edee57bed94a8c62171239c7b006206fd98ad8e30823b60a28da`  
		Last Modified: Wed, 08 Apr 2026 17:28:34 GMT  
		Size: 14.4 MB (14373265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76800d5cb27e61f1409e0f4507e139c567e21e69c5dc0e321657337875c7d8c`  
		Last Modified: Wed, 08 Apr 2026 17:28:36 GMT  
		Size: 92.6 MB (92608862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcfff75b67965338d8bc778e36ba0902a20b28ed537fc7b19f4041f6c239640`  
		Last Modified: Wed, 08 Apr 2026 17:28:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1827940bcff4b3fffc6024c952b6684419e7a2a77b918483dae0767edb2fc630`  
		Last Modified: Wed, 08 Apr 2026 17:28:34 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0291931fa736c79975e98fb3dcba5f1041a81caf594342c9a2616eb377f13d76`  
		Last Modified: Thu, 09 Apr 2026 23:36:19 GMT  
		Size: 15.2 MB (15177191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0d271d162484331d5ba0f264b484d242d6d2492045ed9670313adf9d01ee83`  
		Last Modified: Thu, 09 Apr 2026 23:36:19 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1988e03a71bd41513f7372ff4b8ba01e7d801247ec80fd618e7433ff3a07729e`  
		Last Modified: Thu, 09 Apr 2026 23:36:18 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:4025d9bd54651c4bb2371c2b0c65cf628e0c5088eabf027f67c808f69d2981e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15beb315bfde5d93fca6c2a10e12a1b35a4e636ac4da6d58836b43b93cf1d8d`

```dockerfile
```

-	Layers:
	-	`sha256:50fddb37ebd7de3f6801da616a0256340ad18183127b66342483e20be2cf4d66`  
		Last Modified: Thu, 09 Apr 2026 23:36:18 GMT  
		Size: 1.2 MB (1177181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:180a28185857f1580caee70155b4c3ca1b5577a5772b7f15031c3cff3cb20789`  
		Last Modified: Thu, 09 Apr 2026 23:36:18 GMT  
		Size: 18.3 KB (18295 bytes)  
		MIME: application/vnd.in-toto+json
