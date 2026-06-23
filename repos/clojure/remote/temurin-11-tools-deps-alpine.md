## `clojure:temurin-11-tools-deps-alpine`

```console
$ docker pull clojure@sha256:c0478290aa7a3edf9db700a7cdaf07f8a2286d0aaf479490d7a93158605f363c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:52882e34ec4f576bc2f85f88510c92ae1495910217644b774287a99c767aeee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.0 MB (184034627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc2d36203250d5ccb2054636a136d581e0183f4ee9a8f193fe0f6ccce8c9819`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:56:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:56:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:56:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:56:34 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Mon, 22 Jun 2026 19:56:41 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='ed06a4b8381786a6e8091c10539856675497d2b821cd2d0200cc5b65f453b982';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 22 Jun 2026 19:56:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:56:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:56:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:56:43 GMT
CMD ["jshell"]
# Mon, 22 Jun 2026 20:24:41 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Mon, 22 Jun 2026 20:24:41 GMT
WORKDIR /tmp
# Mon, 22 Jun 2026 20:24:45 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Mon, 22 Jun 2026 20:24:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Jun 2026 20:24:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f9b522ef6226b5e762f07b84e312e749c4ff9762d64fb0a0e6a0f08d3dadc9`  
		Last Modified: Mon, 22 Jun 2026 19:56:57 GMT  
		Size: 16.8 MB (16815695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82edf31c58962a79b82269852db50864e5e46165fd344f4918a80796db584951`  
		Last Modified: Mon, 22 Jun 2026 19:57:00 GMT  
		Size: 141.1 MB (141074581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6857b309472f9776411dbc577858d377ec37fa81f85b3d973ce4c495a1a72e`  
		Last Modified: Mon, 22 Jun 2026 19:56:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2ca25c879ff73f76024b21ff3fcdcae040cc01923ae1d2bf184bd72f35d3bf`  
		Last Modified: Mon, 22 Jun 2026 19:56:57 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63c17f27dc355d8fdd3a9d39c20633a92f52ee751af21ba295fa5a6a0a744c4`  
		Last Modified: Mon, 22 Jun 2026 20:24:55 GMT  
		Size: 22.3 MB (22296873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58a6ff9701e4bc087b20a91da1811cf2c96ad31d58899c57a1196e0f68cbb85`  
		Last Modified: Mon, 22 Jun 2026 20:24:54 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:be1f55fd0ccec6c3c77fcc9c2b6f2b492c0aa55ab7ac93cf137396a8ce92e16e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1204481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed48faca8fd3fd31060531b4cca5c052274f3281e48c16bd4bbcb74a1df73a75`

```dockerfile
```

-	Layers:
	-	`sha256:f34a31bd15b65450688093383d740453de263a72d58f0ef261838f8fe7f90d42`  
		Last Modified: Mon, 22 Jun 2026 20:24:54 GMT  
		Size: 1.2 MB (1191085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ff3ec6d1b16d0a36555541f4806eae8e399ad00365cebaf16ce158f574c2f7d`  
		Last Modified: Mon, 22 Jun 2026 20:24:54 GMT  
		Size: 13.4 KB (13396 bytes)  
		MIME: application/vnd.in-toto+json
