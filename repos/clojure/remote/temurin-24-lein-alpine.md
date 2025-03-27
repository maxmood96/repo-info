## `clojure:temurin-24-lein-alpine`

```console
$ docker pull clojure@sha256:39805d626ddd854aa4b96463fa436ee253b6c6ad262ca904b760aeefe8ef6e1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-24-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:fb454aa0cd0ca5c4f74445369a2ef0e796b1cd9339331d1d13cfef14c24d207d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138172732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235084ddbca3fb995cd9458c915c514b1d567fd9f2840bc47b17f379ae6beca7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='4a673456aa6e726b86108a095a21868b7ebcdde050a92b3073d50105ff92f07f';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='a642608f0da78344ee6812fb1490b8bc1d7ad5a18064c70994d6f330568c51cb';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl git gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da9e4e6bbb3d8fe7ba4feb76b9f85cc591b594ed37c725031140c217b982045`  
		Last Modified: Tue, 25 Mar 2025 21:57:50 GMT  
		Size: 21.0 MB (20950921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09b1f076e8ade81f12374738d4768afffa7e33753b8e5edec2e7165fd328397`  
		Last Modified: Tue, 25 Mar 2025 21:57:52 GMT  
		Size: 90.1 MB (90074010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fee87929fdd34f08d09385a3965e44dcfaa3724ce5f1a2515708890b07049e`  
		Last Modified: Tue, 25 Mar 2025 21:57:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d237c308bf2aec9726a2aad84026d710a041c7de9ee1603fe9726cd1491bed2`  
		Last Modified: Tue, 25 Mar 2025 21:57:49 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a2e6fc065acd07680c49c22223f8dbe9faad5e211618ced5b547104349dab6`  
		Last Modified: Thu, 27 Mar 2025 17:53:04 GMT  
		Size: 19.0 MB (18988596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5a6edc172661d6e24ff3bf8fdf5e5ca2a1364035e802e880624e2991a8b598`  
		Last Modified: Thu, 27 Mar 2025 17:53:04 GMT  
		Size: 4.5 MB (4514110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6b49977bd1291637de306e74470e02786c929e27b55a258b50eb25eb64c2c7`  
		Last Modified: Thu, 27 Mar 2025 17:53:04 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:abeef6396d374930c2071f8c0c58e1eb136c2fdf1620d9a84c193b0f7d30ae58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1056872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55753360cc501bbc62ea0912459034f9b4806dc32c2d862f513f6061d77b5170`

```dockerfile
```

-	Layers:
	-	`sha256:ad05873622c7b69f633e280a4a744c62b9e4b51a27fc3a3dbe91fe1e7e3b2b8b`  
		Last Modified: Thu, 27 Mar 2025 17:53:04 GMT  
		Size: 1.0 MB (1038617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a0f09959dac09245c6c76c382f6388795c7dd91fb5a5f6faf17cb41ffecf6b`  
		Last Modified: Thu, 27 Mar 2025 17:53:04 GMT  
		Size: 18.3 KB (18255 bytes)  
		MIME: application/vnd.in-toto+json
