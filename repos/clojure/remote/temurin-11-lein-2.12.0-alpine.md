## `clojure:temurin-11-lein-2.12.0-alpine`

```console
$ docker pull clojure@sha256:f2bf477e28bf5084ad93bbd9fca4247d2d20219b9402e5cdd25a4a951a5a0698
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-11-lein-2.12.0-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:6e9fdbb1659f4a260cf6ec4c5323851b85531204ab4f10e5709bc688b005e873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179585751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8262598e0486b3ea4d39b289b647133195858119582b668a085daa795a30b014`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:57:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:13 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:57:13 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 17:57:18 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='c7b58655ffde7b5e6fce4a32fdcd21be5745b3bb64ee2bc723fcf55eae720ebe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:57:19 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:57:19 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 18:40:28 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:40:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:40:28 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:40:35 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg # buildkit
# Sat, 08 Nov 2025 18:40:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:40:35 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:40:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:40:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974df0e0eb67fd6fa35aefb5620f2d84f013b3e0b11b4c38737099a86303d60b`  
		Last Modified: Sat, 08 Nov 2025 17:57:33 GMT  
		Size: 16.3 MB (16289652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b829ff2503da3447968682832d5a69ea284ba1d657a4f8e58d4c799c8c348e`  
		Last Modified: Wed, 07 Jan 2026 18:59:59 GMT  
		Size: 140.1 MB (140102363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a217f6eeaed3b8ab583b886e8495c9ca0664bb21717752475480bc1453bb07d2`  
		Last Modified: Wed, 07 Jan 2026 18:59:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea81eccc49bc152ef173ac2d3a5ac97163278251fda36902720deae5aa454418`  
		Last Modified: Sat, 08 Nov 2025 17:57:33 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20537de2fd7fb6f34b56868e933171e286e83e77ecaa6a299c4b08f584534d8e`  
		Last Modified: Sat, 08 Nov 2025 18:40:44 GMT  
		Size: 14.9 MB (14871156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec41c0b870d09247d69e2e8c6c79a9eda42575aaec40e5424da274486f8dec`  
		Last Modified: Sat, 08 Nov 2025 18:40:44 GMT  
		Size: 4.5 MB (4517688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:f4815dd43019de57cecc0573995bea3ece2cedc1898abc0e8b190a5403715d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **971.4 KB (971430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b080383279d54606ea6f9f6b146e746ecbad996fc4f8c51e7eb231ebf0431b`

```dockerfile
```

-	Layers:
	-	`sha256:85641edf598a59cf54695a7d01b7c9c03278dab0f95d667be95f7066944071b9`  
		Last Modified: Sat, 08 Nov 2025 18:40:44 GMT  
		Size: 955.7 KB (955681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acb83dcaa8643edce5134f7c2206d748f668a5a1346665a27e442d99f798843f`  
		Last Modified: Sat, 08 Nov 2025 18:40:44 GMT  
		Size: 15.7 KB (15749 bytes)  
		MIME: application/vnd.in-toto+json
