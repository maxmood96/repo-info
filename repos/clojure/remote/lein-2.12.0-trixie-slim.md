## `clojure:lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:126e25628b305f83f20bd5f294b62ebf2ef5d98b0c6e5fa2a8c07911689d8357
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d6c60d1093f67b351de251b66950aab39385d07867c3b0385515e3e08bf92d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142784450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ff59b187a4e350135103f44fb62dbb08fa157cd63714ded0d195ff3b494dc8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:05:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:05:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:05:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:05:04 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 02:05:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 02:05:04 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:05:19 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 02:05:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 02:05:19 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 02:05:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 02:05:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:05:21 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:05:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513d9bd1b0250d607bbe5958f2ddedae6365c624fb44183e3ea79758dfb8a724`  
		Last Modified: Fri, 16 Jan 2026 02:05:54 GMT  
		Size: 92.0 MB (92045317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf06936e3215be98bc7fc69c78a732d38ec8adbe89c67556362e07094db17d4`  
		Last Modified: Fri, 16 Jan 2026 02:05:47 GMT  
		Size: 16.4 MB (16447282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519f787a2c3b7728b72ffb246a2f13883a0a4adf833083c08adfab6fc3840327`  
		Last Modified: Fri, 16 Jan 2026 02:05:46 GMT  
		Size: 4.5 MB (4517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77825f79024f959e53aa5be1d0069daeda9165aced1bde28a0bd07accb5b1441`  
		Last Modified: Fri, 16 Jan 2026 02:05:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5ce4824c76bfd6e70f685cc95b3bff6e00734e54a6df31875d05d4643ca5a6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58df79a54e692049959c2db6a075970a43b999148da84180c9696980747952d7`

```dockerfile
```

-	Layers:
	-	`sha256:4ba02cfecee5734b56c61a0c6491d2bb49a08a2714c925c86684a3c82482ee25`  
		Last Modified: Fri, 16 Jan 2026 04:36:06 GMT  
		Size: 2.3 MB (2314816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46ae3bb7cd48ebb76a43b9f3cd0650ca078791e55c1eb3674ce1adece9dc6678`  
		Last Modified: Fri, 16 Jan 2026 04:36:06 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:df512d78b45218befd01c7f12fd27fdae8d97da2e39b2edcca7f00634ebed6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142118603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce43cfe9c926b6d15458d2812fa2b910b892ef04732a00737da87c25b0d31da`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:10:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:10:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:10:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:10:17 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 02:10:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 02:10:17 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:10:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 02:10:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 02:10:33 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 02:10:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 02:10:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:10:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:10:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6a0e3c87a32b613f5a9f47ce1800a1b1c51b28ae8a0901d6ccd4ed5fa994e2`  
		Last Modified: Fri, 16 Jan 2026 08:58:45 GMT  
		Size: 91.1 MB (91052460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86b80420568384c81bf59d8a5af5d9f96a05946167a021277038c0c81087e0f`  
		Last Modified: Fri, 16 Jan 2026 02:11:00 GMT  
		Size: 16.4 MB (16413937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afdf5d8f3ac74eb3c19c99d9f7ba23887b2010261ba333d5c0ad52a6feeb688`  
		Last Modified: Fri, 16 Jan 2026 02:10:51 GMT  
		Size: 4.5 MB (4517736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64e6168db5765d5cb17e26531c7d28a3c98fd5356b9b478138fe1b09c9c9bd0`  
		Last Modified: Fri, 16 Jan 2026 02:10:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3b22958fe6547a1860ceb2ea95c261fc93b10ec49d155c96ac9d2242bace4059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4645055d82da55c6e4c31472639f97002663372fcf69ad494ae962d2226cfb9`

```dockerfile
```

-	Layers:
	-	`sha256:33ec3953871cec84ceb8612534e220ce23ec68e95d5d486feeaf13458d6fcd07`  
		Last Modified: Fri, 16 Jan 2026 04:36:10 GMT  
		Size: 2.3 MB (2314455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14b96fda5493ffeda5c83efe07f79383ee2c237ca2f5f733ad41107e3053451b`  
		Last Modified: Fri, 16 Jan 2026 04:36:11 GMT  
		Size: 19.2 KB (19179 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3c9219c8c142a1f110e08a2f9c781eda4aee38ffc6d5ab3b0e0efe6ceb6cb323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146210004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207d080d615907ac0a31e731db4db1057d3a6626c41518950bd189096f1dd0db`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:44:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:44:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:44:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:44:53 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 03:44:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 03:44:55 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:45:58 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 03:45:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 03:45:58 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 03:46:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:46:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:46:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:46:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11e063d257c7fd0378d1844308cea571e43cdc3c6ef2206a9db6629a1520ee`  
		Last Modified: Fri, 16 Jan 2026 03:46:44 GMT  
		Size: 91.6 MB (91610755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2246e2006158f66cdaa3bace84b646348ea88497a12fefad6e2ebd992dc5fa6c`  
		Last Modified: Fri, 16 Jan 2026 03:46:41 GMT  
		Size: 16.5 MB (16485502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00af45bdef0f7e5ee487d595115ee9c3d4330035bc8f19f7b51331818da304d9`  
		Last Modified: Fri, 16 Jan 2026 03:46:50 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afb0817dc0f0ea743dc97f2d9291c0bb28bf08badba082482f92dc1fc050569`  
		Last Modified: Fri, 16 Jan 2026 03:46:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b03653d35b146d75d7dd06769461aef8ee5a80f6e3436b72b921cbf6a984b3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc75237e4a804dffbe74f8429b97d875639aade17bb62f3c4e5a0d2eab236db9`

```dockerfile
```

-	Layers:
	-	`sha256:199b4e9e19ae0d738a6c50d273c8b28f10d00bcd9eb61b19c2915c276d4f0ff0`  
		Last Modified: Fri, 16 Jan 2026 03:46:40 GMT  
		Size: 2.3 MB (2317106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3854a295dd88b74e952f2154ea5ed5fb21c5c6a97d819acd313f80b009a7289`  
		Last Modified: Fri, 16 Jan 2026 04:36:21 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:98bd97f7da94b04c70f5c690248c396909864aaec16cf66e3cda8180b7a537c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139942042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f956d62f96f6c2d1fc7720a5d66542029874f5988cfbd59c269b0bb5c8d142`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 07:30:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 07:30:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 07:30:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 07:30:35 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 01 Jan 2026 07:30:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Jan 2026 07:30:35 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 07:32:04 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 01 Jan 2026 07:32:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Jan 2026 07:32:04 GMT
ENV LEIN_ROOT=1
# Thu, 01 Jan 2026 07:32:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 01 Jan 2026 07:32:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 07:32:21 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 07:32:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:14 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a09886da888ac7f39c6c9f60f721941a5a3cc3ed273e4d20352388b50fb5af`  
		Last Modified: Thu, 01 Jan 2026 07:36:11 GMT  
		Size: 90.8 MB (90752859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809340366dabeee7446bfef1c9430edd6aced6075aa4c14861cdb274ae8b082`  
		Last Modified: Thu, 01 Jan 2026 07:36:01 GMT  
		Size: 16.4 MB (16397836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483da57381707f5798e42be6df179f839c90ea4b2f6c6e7c680e238d5ac7f920`  
		Last Modified: Thu, 01 Jan 2026 07:36:01 GMT  
		Size: 4.5 MB (4517788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b22dcbdce2eb2b0ce5e249fb8a0bd633ba430ee21fcbe4930530bbdbbf8797`  
		Last Modified: Thu, 01 Jan 2026 07:36:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9d9867ffb5eefb293d9df5f02d9d933702431d7a48fa8d9e6b942656429d79d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2325901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375be7215430e83b634b548dab69a401386d0acd9741d530e4c87047dc276285`

```dockerfile
```

-	Layers:
	-	`sha256:95ad62ba696e7ed6b7f904e40f0cec1913376b2bd8da9a29c2c5033bba16aef7`  
		Last Modified: Thu, 01 Jan 2026 07:35:38 GMT  
		Size: 2.3 MB (2306811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c250f59a91d6e671e1acd6d5d3b283c04a8d5528acba645a7704bc27fed7f74`  
		Last Modified: Thu, 01 Jan 2026 07:35:37 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:253703d5c9373cf3b91b49b5d9a0c0a2e9913b8ba4236595ea973dc1c244a196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139045356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ce53171cc49e272907126812140caa0417ba57b838269401cfe5086c38e29a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:23:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:23:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:23:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:23:10 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:23:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:23:10 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:23:23 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 15 Jan 2026 23:23:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Jan 2026 23:23:23 GMT
ENV LEIN_ROOT=1
# Thu, 15 Jan 2026 23:23:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 15 Jan 2026 23:23:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:23:25 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:23:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2b60cbc839537ac9d2d64e95bf99e1c19c3b75f06175e544fbfafc8cc5fea1`  
		Last Modified: Thu, 15 Jan 2026 23:23:51 GMT  
		Size: 88.2 MB (88210671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181ce5dfe9b484262a7d1f2d45a10d603a7e14f778b0f8a489988dd4ce969fad`  
		Last Modified: Thu, 15 Jan 2026 23:24:00 GMT  
		Size: 16.5 MB (16483100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee5d985dfd304bb5400ddfd11aad3324665d74ecb4ed4d0869aeff9c74bd7d0`  
		Last Modified: Thu, 15 Jan 2026 23:23:59 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ce7eddd94e5026e0958fcaa0ab9176e5eda37cac5892f32612ae81c227d5a1`  
		Last Modified: Thu, 15 Jan 2026 23:23:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:28fd4627b2b2576563b1e193e162c2d925fb850bc50927ac5fbdd56d242c6670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2332825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3366679e4c9a570b8896e6ac7411f4ba9ffa8454b161a3f36ec211425481fdfc`

```dockerfile
```

-	Layers:
	-	`sha256:773cbf54d3740f71f4006fde4dc4e34b741c366fde6351013464189f0e00851b`  
		Last Modified: Thu, 15 Jan 2026 23:23:49 GMT  
		Size: 2.3 MB (2313791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14f7230f5a07c1db1f981ab8137b84204c20ec470687f1cc244298f0c620637d`  
		Last Modified: Fri, 16 Jan 2026 01:36:25 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json
