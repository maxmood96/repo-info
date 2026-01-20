## `clojure:temurin-11-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:ae8b9a40a3aedbe6ab1fd27b9de6b34587b1763099db199dbe9047d94dd512b2
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

### `clojure:temurin-11-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3330a9d3267183fe3bd47eadf639d4cf2776173004d0063d7ec3e4aad209df06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195471439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16de60ffd0b35a668caa3c4b99af3ffab5fa89e9825a53c919a5e4cba293392f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:45:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:45:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:45:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:45:33 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:45:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:45:33 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:48:09 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:48:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:48:09 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:48:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:48:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99105d78eafe759a9628decd746116810182050b8063c8b9fd4d944c5fbcabe`  
		Last Modified: Fri, 16 Jan 2026 01:49:06 GMT  
		Size: 145.0 MB (144966614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02feef747f412a5430f06eb9f2d739fcb7cfcf863f0040138e3ebe102f81d97e`  
		Last Modified: Fri, 16 Jan 2026 01:48:36 GMT  
		Size: 17.8 MB (17758510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c350bc05b1ffd277afd4b3f6e88f4d9aa1aabac0942a1a99a0a9e63014cd3548`  
		Last Modified: Fri, 16 Jan 2026 01:48:36 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d7755c6e163b4a2c11b37c32d8f5222c479fa7b0a211d1ed95df96877b955b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2765349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d4abc66e221ce15ec638d321db2fdb177081d543e3262a04f80830dad959c7`

```dockerfile
```

-	Layers:
	-	`sha256:5cd0f70a8ff9cbdf3b73204f775edc21c3cb233c7b5da09b9e65a63b426be939`  
		Last Modified: Fri, 16 Jan 2026 04:37:49 GMT  
		Size: 2.7 MB (2748937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c86222eb1d78f442c5f83deefc2df7cef818386ab22eccbfd643d20d227210a`  
		Last Modified: Fri, 16 Jan 2026 04:37:50 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:662e3802c5b80fbb1575324866f1d0b05624f16734353f6181e9fca3786de578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191947663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c1b6c1f91e68247eb9f80a2ddac55eaaa88f62a97a6d8124becc677e571abd`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:49:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:49:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:49:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:49:56 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:49:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:49:56 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:50:09 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:50:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:50:09 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:50:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:50:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4310d5c299f93b8b4bfe0617d4d41bcb16d50a54761a167feee4b4968de5027b`  
		Last Modified: Fri, 16 Jan 2026 01:50:30 GMT  
		Size: 141.7 MB (141729867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b23efcaf8e08af24626d833d4e5d87137d515fe002f57d439a1e357b283c20c`  
		Last Modified: Fri, 16 Jan 2026 01:50:28 GMT  
		Size: 17.6 MB (17592118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b540d1277c387a55d48de1fed7fa33570dc947078d6e74d56f5c03742f24f35`  
		Last Modified: Fri, 16 Jan 2026 01:50:27 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2b6e97dd4f5baff71738bafedf48c942b827949249c8e8c186b33fa6231faf34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2765703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55d7cf3d55b99fefc8fda0362978025395f317f1fcdb309e60c32d56eb1ef4a`

```dockerfile
```

-	Layers:
	-	`sha256:1567de445fa0333f5e501a7076430bccaaf113b242f3978bf14911aa35992867`  
		Last Modified: Fri, 16 Jan 2026 01:50:27 GMT  
		Size: 2.7 MB (2749170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa60297c2c4c22b6f5c9aea40ff6909009c04c5eb465f686ed8b0cc37c6216a4`  
		Last Modified: Fri, 16 Jan 2026 01:50:27 GMT  
		Size: 16.5 KB (16533 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e8ba721bb3b655236daa162581fdf29f4cc49cdac482615c505f1fc55fd7060a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186626908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045be4a88100cb9568133000013be5de207ae5158da06771a5efcfb8e562abb8`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 02:57:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:57:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:57:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:57:41 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 02:57:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 02:57:42 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:58:26 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 02:58:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 02:58:26 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 02:58:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 02:58:29 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:03 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68470ec8404f299576dbb308d66a6189dbad0deedfff83c1babcebaadce578a`  
		Last Modified: Fri, 16 Jan 2026 02:59:18 GMT  
		Size: 132.1 MB (132079791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c846ed850fbd234ede970557d32f20690749dad45aedf4e6d0505fb782e4d8f6`  
		Last Modified: Fri, 16 Jan 2026 02:59:25 GMT  
		Size: 18.0 MB (17960629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f879cd4b35903f1289234e4722465634438e88471387ae9da92fd51526ddcb`  
		Last Modified: Fri, 16 Jan 2026 02:59:14 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ad1761e897af33c1616dc76aada4ab1735602d212c408b0ccb96a05c7b38b165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2766611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8f3ccd30f6acf31dcb4e62f82745421b24acb1cd1eba512b5e58a3bf1bd222`

```dockerfile
```

-	Layers:
	-	`sha256:7247ae398405a2606f0b3912df27a6f5df4fae01ad64f121d6bd081c3f5b38e6`  
		Last Modified: Fri, 16 Jan 2026 02:59:14 GMT  
		Size: 2.8 MB (2750155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:728ace3ea9310812164a1d9291ccb6c374c700083ad31dd38592874a871a0702`  
		Last Modified: Fri, 16 Jan 2026 04:38:41 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b9e741ee2456d57cd7c758f0d559ae9684bcc1d9a92430bc9db1f42732ff1599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174517789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603bffdd5e733fb67a521c42fa171531071cfa2115ce929e2e4d8d9eeeba4805`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:10:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:10:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:10:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:10:27 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:10:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:10:27 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:10:42 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 15 Jan 2026 23:10:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Jan 2026 23:10:42 GMT
ENV LEIN_ROOT=1
# Thu, 15 Jan 2026 23:10:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 15 Jan 2026 23:10:43 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:08 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6afc4974fb908d05b5af46341b93ddf48b979f8e96d01fa55d603a755a876a2`  
		Last Modified: Thu, 15 Jan 2026 23:11:24 GMT  
		Size: 125.7 MB (125694860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684e7d771427bce2c5478bd04db770e053336e0d25dff77159bf35929d18e02c`  
		Last Modified: Thu, 15 Jan 2026 23:11:14 GMT  
		Size: 17.4 MB (17420777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06456ddc898837cfce677f3e446ecaddd257b96d6a4530f5a19550822746c9f7`  
		Last Modified: Thu, 15 Jan 2026 23:11:14 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f2454f4037d32f01a06a5287ced17de05dd54db5dfbfdcbd995bc443c41f9f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2757167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fddabeb8597c850e5957055aaaf28417f182393b2867b865454a33d90ccb8e7a`

```dockerfile
```

-	Layers:
	-	`sha256:e6c5e5c68bd0ac04f70e8c322c146f62cfa7928d8f648ada144f319a3072543a`  
		Last Modified: Fri, 16 Jan 2026 01:37:14 GMT  
		Size: 2.7 MB (2740755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:919fb894a42387866cdc0141ef56aaaa9e373f4ebd99da513d7af4dc3ab5bc25`  
		Last Modified: Fri, 16 Jan 2026 01:37:15 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json
