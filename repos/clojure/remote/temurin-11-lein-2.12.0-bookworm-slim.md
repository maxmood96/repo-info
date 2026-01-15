## `clojure:temurin-11-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:e9e8b9bc97412d4e1283b9501c5033dc1b530e51a936dfc0ea49ef41b32eb6c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:02d6a622df699bebf5d7dd71d489a6d60e03e0e67cacfbebf72878cfd61944f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195471441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd1b88aa1f8bfae6dd52df6a4575359961454c18eb69e75bb8861dd54a8d439a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:23:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:23:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:23:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:23:38 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:23:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:23:38 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:23:51 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:23:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:23:51 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:23:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:23:53 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b03ac94e93ce5604e190a298621555423cbb379a3190cf61a7755de240cc03`  
		Last Modified: Tue, 13 Jan 2026 21:04:01 GMT  
		Size: 145.0 MB (144966652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528668191baf2e79192b634d7a305d195e76a84601ed197bf78bc1033fd22870`  
		Last Modified: Tue, 13 Jan 2026 03:24:21 GMT  
		Size: 17.8 MB (17758451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b233759725d068c06bc8f710e80cb0202e204c462583300986b02c62555e2dd5`  
		Last Modified: Tue, 13 Jan 2026 03:24:19 GMT  
		Size: 4.5 MB (4517734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9bec899c35f0b5401a62dfb671160ebe3d824816bb13cb130bced661befcd13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2765349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2ccf6d9ad796812e3a74dc1e64263dc435ef25c3d580557edd7f94ef63aaf4`

```dockerfile
```

-	Layers:
	-	`sha256:0103402b4bbf3e6cc1d38721ccd057913387cd175b8b7238f2df6a9b31e3ac90`  
		Last Modified: Tue, 13 Jan 2026 07:37:19 GMT  
		Size: 2.7 MB (2748937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67c7737f68003158eee4a057bab7dfcb950d4050c803930c57282512df5aef5`  
		Last Modified: Tue, 13 Jan 2026 07:37:19 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6591f3e4641be684322df9342b2edc9cee6b4fb8edb62471c26ce1cd962b64bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191949280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7baf1f6af77d53763582645e2a2b941e7c30a041e6b699a5c658529e131faee`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:29:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:29:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:29:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:29:38 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:29:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:29:38 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:29:51 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:29:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:29:51 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:29:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:29:53 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531d68848bcefc3a79fa28477f11fa352dfb2796ede671ae9051df27d00ef939`  
		Last Modified: Tue, 13 Jan 2026 03:30:44 GMT  
		Size: 141.7 MB (141731552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca0a28d429a7dd3327e38b4faa2b3a998d26245df05bd6f4cd31df8c71de772`  
		Last Modified: Tue, 13 Jan 2026 03:30:20 GMT  
		Size: 17.6 MB (17592088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef62716a8e895e74e70c6b1e8088dce76f89eb640c39136527e45421670782c`  
		Last Modified: Tue, 13 Jan 2026 03:30:09 GMT  
		Size: 4.5 MB (4517719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cd837a2fecef61d75e6268cc95a1f944e68d146f62adb14d3d836d520d98b0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2765703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3644e2581d4609412c6657759aa26eb439b3bfa07f3685de4e3738d24a5a7e`

```dockerfile
```

-	Layers:
	-	`sha256:7ee34c272d557bc4cfd4a08b382f004d1703be55f3ae64c5476bb0cff5efd8e3`  
		Last Modified: Tue, 13 Jan 2026 07:37:23 GMT  
		Size: 2.7 MB (2749170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f85fcc2ee1f79adb6526a5ce67bfc839ac0dcd514e4de84d60c87e81b4c3c72`  
		Last Modified: Tue, 13 Jan 2026 07:37:24 GMT  
		Size: 16.5 KB (16533 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f5e375cf7a6a98c02e5b90822c47e2aa63f2849040dd538042c942e462b20393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186629131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a668bd2f703cd99826f2e147580a98ec5d01a512c4793da7976f792f15be39`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 02:57:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 14 Jan 2026 02:57:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 14 Jan 2026 02:57:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 02:57:56 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 14 Jan 2026 02:57:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 14 Jan 2026 02:57:58 GMT
WORKDIR /tmp
# Wed, 14 Jan 2026 02:58:45 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 14 Jan 2026 02:58:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 14 Jan 2026 02:58:45 GMT
ENV LEIN_ROOT=1
# Wed, 14 Jan 2026 02:58:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 14 Jan 2026 02:58:49 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:24 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ae8aec7fabdb66b1b658466f357cc9eed9d6e897dab0fa1101510489c06012`  
		Last Modified: Wed, 14 Jan 2026 02:59:42 GMT  
		Size: 132.1 MB (132081949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6fe62c98520ad4f7c0e5bbc4afa28d128d64a9f335b8f38e7650de89e83a8c`  
		Last Modified: Wed, 14 Jan 2026 02:59:34 GMT  
		Size: 18.0 MB (17960688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f14009a7a89667f68665b6fbf73d7a021eb60b7c8db48e928d54e5b16345f7`  
		Last Modified: Wed, 14 Jan 2026 02:59:34 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1311da89164ae569f8efce20ef8256935ea24da73130dfdba37306eaf0dcbb14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2766611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e7b2c755d0210f9680d4a2e7b903b3a00fed150b856b7dca702daacc503e32`

```dockerfile
```

-	Layers:
	-	`sha256:dc952ca0575435f0f0d8fb0b572df7394c8339dc69fa7e52913c99d703ee26e7`  
		Last Modified: Wed, 14 Jan 2026 04:35:01 GMT  
		Size: 2.8 MB (2750155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0333bd5fb8e6b722a1975de7467a9fbac98a7ad25e2b935094a499722bfe147`  
		Last Modified: Wed, 14 Jan 2026 04:35:02 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:8493fd1a0231abff95c2ae5f9dfcad89fef6f87e0977300e31d8652c3cdf0cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174517339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9234f5fdd26768bb19d1f39c015bb1076454b9eec4676ad16ea0f287ed17dd6f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:00:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:00:02 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:00:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:00:02 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:00:11 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:00:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:00:11 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:00:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:00:13 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2104eb39bbc69183dd23dffad5f8c58a1c4c5d3829b73838f28190eb500055c`  
		Last Modified: Tue, 13 Jan 2026 03:00:55 GMT  
		Size: 125.7 MB (125694399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79708bf64ebe3b7c5ef45ca3647bc2373339674e2e56638bab835e2104764e35`  
		Last Modified: Tue, 13 Jan 2026 03:00:47 GMT  
		Size: 17.4 MB (17420763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ec62c69ce849e9191533934bd165818d5a2393164d326431d4f74a282be29e`  
		Last Modified: Tue, 13 Jan 2026 03:00:45 GMT  
		Size: 4.5 MB (4517730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e5e73d2b5a965300e8a69e386ba24f49fae037b3fbc8947183ba95313d6b2fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2757167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9937168d58150c3a3793a1ed873e12d2a18514ba8450d5677c3fa83dde29d7c`

```dockerfile
```

-	Layers:
	-	`sha256:07a6dc5cb750d66ec925a906d1a3c0729a49013c527c6bb80b778e1f66800d7d`  
		Last Modified: Tue, 13 Jan 2026 04:36:11 GMT  
		Size: 2.7 MB (2740755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d07a263fe574b8fe3ddf85d5d8c5a5326fc0e030fc61979fddf227cb18a8d362`  
		Last Modified: Tue, 13 Jan 2026 04:36:17 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json
