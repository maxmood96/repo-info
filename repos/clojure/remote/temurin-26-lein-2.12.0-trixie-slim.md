## `clojure:temurin-26-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:1f0a6bccca3b248614c4a1fc26c2d8e21ded12a6a45a549ae35bfb35a99e252f
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

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a28a0a45ecb2748ede3da87346168c695fbf5816c37764affeac1d61aa48e994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145276132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5318caae6946768236aa4b50e82c94c5bce58c52177e7d61e90cd3206583d5b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:21:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:21:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:21:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:21:58 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:21:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:21:58 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:22:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:22:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:22:18 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:22:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:22:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:22:20 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:22:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3857c81c5e2c7141a5f5ea51a554def1981bbcb4f40849768029dad476d333`  
		Last Modified: Thu, 11 Jun 2026 01:22:42 GMT  
		Size: 94.5 MB (94524388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1ed98e7261b5bf3ec7d8e08b829d8f09a407c3cd31821190a1e7d5a655172f`  
		Last Modified: Thu, 11 Jun 2026 01:22:37 GMT  
		Size: 16.4 MB (16448173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c6581b68613752cfcc17402d4a8980b358acb0bd9197cf4ca83fa2ce35f3e8`  
		Last Modified: Thu, 11 Jun 2026 01:22:37 GMT  
		Size: 4.5 MB (4517727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04a70b4e501875236608ae90884532d9acdd66080a6d159ca65fc30e5fca4c6`  
		Last Modified: Thu, 11 Jun 2026 01:22:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a497fec6ee440f10194e3ff8161af6d73e20dab9a3870db9da14ecee0ec812ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2348881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49fdb4298cfab13e54e4605eb98075d656eb99c505d21d41326160d6c9d50e2`

```dockerfile
```

-	Layers:
	-	`sha256:d37bd870432aee77c6068a795bbb068ad524e3b5d509b0d11ebb5bb71cb731f6`  
		Last Modified: Thu, 11 Jun 2026 01:22:36 GMT  
		Size: 2.3 MB (2330348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77944fdd54afb922443e3e8da6f4862da5209c711c19b6958c5fd2eabbe4caa7`  
		Last Modified: Thu, 11 Jun 2026 01:22:37 GMT  
		Size: 18.5 KB (18533 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b1398540e1e66ab01a880671ccfec1b9116a1b45267abf600bc62a5a44db1029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144585234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8a29881ef372aeecfded409953f80c36fa6ea614ce08efed1aacaf1a0ea4a0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:26:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:26:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:26:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:26:04 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:26:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:26:04 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:26:21 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:26:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:26:21 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:26:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:26:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:26:23 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:26:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac8bae1418c85d7fa7a64b3df585e9c516c35dfbdc309a868f619ff9bb698cb`  
		Last Modified: Thu, 11 Jun 2026 01:26:41 GMT  
		Size: 93.5 MB (93504334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607521ea77a4ed857685b966ef37fc6ff22c97476513d8ab5aa44c6f9898fcd8`  
		Last Modified: Thu, 11 Jun 2026 01:26:40 GMT  
		Size: 16.4 MB (16414199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509e90febb34ea561d28ec34d800a52cb985d9eda175c37654d6b40e7bcccb56`  
		Last Modified: Thu, 11 Jun 2026 01:26:39 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a1ee33201b5ab7c71160c6f20f4125fabd2636fbbf183b750717902102dbbf`  
		Last Modified: Thu, 11 Jun 2026 01:26:39 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8716b4a6ba0c0c1c19f46f981ba18f628a342dff56d516f4d062116f97cba3a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2348609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2222c1899f34834f12718abe72c594c344db14f25f925452e9979a80d5fb8168`

```dockerfile
```

-	Layers:
	-	`sha256:e48309dfdaaf9b4b2b48c5ce34e11b817fe91cd091327c25c8b90d0aa42dc02e`  
		Last Modified: Thu, 11 Jun 2026 01:26:39 GMT  
		Size: 2.3 MB (2329955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b968a41d8b5dcc173612cd1bd305d750576379ddef955d41c7160ea66660d9e`  
		Last Modified: Thu, 11 Jun 2026 01:26:39 GMT  
		Size: 18.7 KB (18654 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e19151b2209900a95c4a1ace2e98af37bcdd961725aeb5bd57b263d07b9edd0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148512600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ac6d6476828f3bcb429ce1d43a0618ce6c78d1156c65ead68860137c5e8b84`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 09:51:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:51:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:51:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:51:25 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 09:51:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 09:51:25 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:52:00 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 09:52:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 09:52:00 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 09:52:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 09:52:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 09:52:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 09:52:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8f241d1a8e8f2d8598ca90989e9feace81f191fea6f8c838a337195fe31db4`  
		Last Modified: Thu, 11 Jun 2026 09:52:35 GMT  
		Size: 93.9 MB (93902068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76daa9658db9061c996749729a500ddc957e7c805de4599ed23cbc093e526954`  
		Last Modified: Thu, 11 Jun 2026 09:52:33 GMT  
		Size: 16.5 MB (16486016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a9161abda0698bf47a6d175b04c908d11a67d076f13d2b660a64ad61389d38`  
		Last Modified: Thu, 11 Jun 2026 09:52:33 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bc71a9e96cbd69037de57cf3f55d3c4d96cb99ef127ee52579fcbc0aa8021c`  
		Last Modified: Thu, 11 Jun 2026 09:52:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9e3c8273133f78fd1cced2ac4c26099746b9d2b5aa5b81b1533478cefca1ace2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066cdd71caa0fa5b81f85178c05e7a38888d83e199b7ca0260a6698b5914b6c4`

```dockerfile
```

-	Layers:
	-	`sha256:68d97dde0a1bb4ebabe0fe9a83c07c90ec7f9df0119d1790e7e31b25512ac0b2`  
		Last Modified: Thu, 11 Jun 2026 09:52:32 GMT  
		Size: 2.3 MB (2315264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7700c92ae4b997daace9b981d8e9e3c794bd556100cf82baf74e0c1f771944fe`  
		Last Modified: Thu, 11 Jun 2026 09:52:32 GMT  
		Size: 18.6 KB (18578 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:59450b429c7b841a9752feb9e06701a6d7402182be928b77de04fe7bf021a265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141390713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e251c5083a6e69d39607d63c3500dd2e2d96c9d38ebbd1acacce05f760d0843`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:16:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:16:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:16:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:16:26 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 03:16:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 03:16:26 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:16:39 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 03:16:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 03:16:39 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 03:16:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 03:16:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:16:41 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:16:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998e6856ed4cc7f466e9564c409f52bd5a1f2f29ca0fca792dcb3f6beb75816d`  
		Last Modified: Thu, 11 Jun 2026 03:17:08 GMT  
		Size: 90.5 MB (90536968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07a867546ee53984081f3e37e3a1643361106a05be9f132f61d4ce55867051e`  
		Last Modified: Thu, 11 Jun 2026 03:17:06 GMT  
		Size: 16.5 MB (16484229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33cd1c6fd7cbf9f713f8e0f81133c78f0d7b008d0382dadc86c634742ab8200`  
		Last Modified: Thu, 11 Jun 2026 03:17:05 GMT  
		Size: 4.5 MB (4517736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2583b167554497a14444e98c8735db71be868d222ac382590d20a01a3d37a3c5`  
		Last Modified: Thu, 11 Jun 2026 03:17:05 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ecfa45f5a39053e64833bd3c3d0e0a78b6e939bc8f38d2d3685bd4ac2c025146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa35b60230f23d373b50103124b1fc4953f980eabf3594ccc1304ee0f0eddbb`

```dockerfile
```

-	Layers:
	-	`sha256:085768b6a0d91aec00a8c1e98ae0384efd3cc5c66fd392a351c262ab105e3245`  
		Last Modified: Thu, 11 Jun 2026 03:17:05 GMT  
		Size: 2.3 MB (2311961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acdd8ba326055b6477a86661a10dac9b63f38d5780058f90a50d630d18eb994e`  
		Last Modified: Thu, 11 Jun 2026 03:17:04 GMT  
		Size: 18.5 KB (18534 bytes)  
		MIME: application/vnd.in-toto+json
