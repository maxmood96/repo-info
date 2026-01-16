## `clojure:temurin-21-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:d4af30dc15ba81fc17b95dda4275daa3ecfcd2bc6ad5b36f964fc375c35c55df
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

### `clojure:temurin-21-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8e5b872aed2b9ca03ac07785802898efe9ee826f95fe7712f4cf59c02d4d7c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208331244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7b329f884d8e21810d218e41aa1376a21baf166aa3acc68dc9793974ddb8ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:33:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:33:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:33:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:33:57 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:33:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:33:57 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:34:11 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:34:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:34:11 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:34:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:34:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:34:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:34:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3e3d747350a74f2c42286e13ecde8c504dc00d1332a052399dad2228cb5d58`  
		Last Modified: Tue, 13 Jan 2026 13:01:09 GMT  
		Size: 157.8 MB (157826042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9913bc9a17a838bde89eedbe80ecf027fb3f3a5b2f93b37f39907d4d59c207`  
		Last Modified: Tue, 13 Jan 2026 03:34:48 GMT  
		Size: 17.8 MB (17758473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5607d168cb09c190b2f5923f17acbd9659c6899ca689c2923eb8b039ef4f5bd0`  
		Last Modified: Tue, 13 Jan 2026 03:34:46 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709a350ad4c906918627717d6ee3579e0bf4e26256c6037a1d6959c9bbe7f499`  
		Last Modified: Tue, 13 Jan 2026 03:34:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4c0d13dc85bba954d59403736a5cb738dba9199af0b89ef823c34d7942953dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf06874761c29bb3dedcf482232cbcbef53f4129b0a1106e58b0f3233583034`

```dockerfile
```

-	Layers:
	-	`sha256:8ffd8cfb3f3c41a62bb9ee9fbb9a8fac368e0ce63f960764d81a3f2cc67854f9`  
		Last Modified: Tue, 13 Jan 2026 07:43:07 GMT  
		Size: 2.7 MB (2731900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:430d03e31e77c9da1da224fb05ed58bf3d6e6c01ecda27f167239281f20d2377`  
		Last Modified: Tue, 13 Jan 2026 07:43:08 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c72d188164b5d85fdc342c4374da35e48ad41ec1155fcdaa3fdea37efb97f901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206325727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b480f0fed3492a9367fc6063681c61ad70c53db9bb6bc215ce3933b6ccf36386`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:37:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:37:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:37:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:37:36 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:37:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:37:36 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:37:48 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:37:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:37:48 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:37:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:37:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:37:50 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:37:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1677a10d0046e060240e31b3983eff2c5917320fd12a7c37d0ab8ffbb796c91a`  
		Last Modified: Tue, 13 Jan 2026 11:21:49 GMT  
		Size: 156.1 MB (156107651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699ec8d524d54560f193ce234680920f05913969ce5cc4880b99094f530bd140`  
		Last Modified: Tue, 13 Jan 2026 03:38:19 GMT  
		Size: 17.6 MB (17592041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f960e0fc8c1f51d406709e1df9cc41c50279a33a1da370622f64851eef23b8`  
		Last Modified: Tue, 13 Jan 2026 03:38:19 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d931c3eab63d074af4b01879afbebe838d2ca8a73d596f2d90fd056cd64f0d`  
		Last Modified: Tue, 13 Jan 2026 03:38:18 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1daa07c2c69ba51b9f7f5981103d5edd1b9a1e70237ed2c95ca3fbf989710cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efebcd0644669db030fb92aa76d90d7714adc0a14036d816826f55461f44ea42`

```dockerfile
```

-	Layers:
	-	`sha256:528ddf8cb47120bec212845d101597be0a2ec4d7a63332ac8d3caf6936067841`  
		Last Modified: Tue, 13 Jan 2026 07:43:17 GMT  
		Size: 2.7 MB (2731515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a3375a59c1b5913ca48d2f413ae6c0fa72399b022a49a3f2ab32c2c4b76cfe3`  
		Last Modified: Tue, 13 Jan 2026 07:43:18 GMT  
		Size: 18.5 KB (18523 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:95cdbe522b37c0e27b8aaeead8ba6a6ddf4b9ca7e8ca2208300b393455ed5de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212490494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39af63d206904be8dc7938f13baec7fc650250a9463982c09433899ba2e7f237`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 03:02:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 14 Jan 2026 03:02:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 14 Jan 2026 03:02:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 03:02:22 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 14 Jan 2026 03:02:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 14 Jan 2026 03:02:23 GMT
WORKDIR /tmp
# Wed, 14 Jan 2026 03:03:13 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 14 Jan 2026 03:03:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 14 Jan 2026 03:03:13 GMT
ENV LEIN_ROOT=1
# Wed, 14 Jan 2026 03:03:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 14 Jan 2026 03:03:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 14 Jan 2026 03:03:17 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 14 Jan 2026 03:03:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:24 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f988a99efa32b6764c786b7a182133c65d55660c4cf1e6f5287fce43c2a14051`  
		Last Modified: Wed, 14 Jan 2026 03:04:43 GMT  
		Size: 157.9 MB (157942950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb330fa740900964cfd208e2d16f71356cfe63c00db4cda046ea1bc518b00b4e`  
		Last Modified: Wed, 14 Jan 2026 03:04:20 GMT  
		Size: 18.0 MB (17960677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac69ef8ac7a2dc0cd4fc058fc2ffed202fac9e592b6b74d0efd059681caffa40`  
		Last Modified: Wed, 14 Jan 2026 03:04:19 GMT  
		Size: 4.5 MB (4517730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4388810628b6206a90177cec429eb9deba5986d75c06689fc0b67c955f5b9f`  
		Last Modified: Wed, 14 Jan 2026 03:04:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e02195d64f3e087ece486dd465bb28bc035a8d1d43a6fabf7baa2041a5ac2e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a738a922784bcd60bb143883cfc809e3a7b47c25ec5ce85300d60f662faadc23`

```dockerfile
```

-	Layers:
	-	`sha256:b01d3fd50713c0940d2162a8dbd70c2dba7a334c526c54a2442c344a67d25655`  
		Last Modified: Wed, 14 Jan 2026 04:36:40 GMT  
		Size: 2.7 MB (2733733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1ed228217029548f231ae7e598f621073aa170481013b2f340c8ec4286a540`  
		Last Modified: Wed, 14 Jan 2026 04:36:41 GMT  
		Size: 18.4 KB (18446 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d6b07582599ece2f0a7a5efadd7b7654d7d75ccbfa7050ce68af5c51d2fe00dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195893285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce21100c61dfcf82405fb43199c89260a1f921be37e0037ea8ce8bbf29442575`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:18:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:18:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:18:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:18:27 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:18:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:18:27 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:18:38 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 15 Jan 2026 23:18:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Jan 2026 23:18:38 GMT
ENV LEIN_ROOT=1
# Thu, 15 Jan 2026 23:18:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 15 Jan 2026 23:18:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:18:40 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:18:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee49ba92133d874b741829618924bc0c05855d3180b0f68c63b8b6afccf9583`  
		Last Modified: Thu, 15 Jan 2026 23:19:25 GMT  
		Size: 147.1 MB (147069856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69434feae3f38e80d56b3c0706e601a75ee8928330a7a56576dbe24ae07692ca`  
		Last Modified: Thu, 15 Jan 2026 23:19:12 GMT  
		Size: 17.4 MB (17420861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a406d372c3a8e1a6cda31b6c97a6a20824de8d7a9fb7e1a6c3ef1a0abe825c6`  
		Last Modified: Thu, 15 Jan 2026 23:19:11 GMT  
		Size: 4.5 MB (4517725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0747c68b63481f16e76c7b6615d89e1d255179468cc2e0e3aca44f731a8e3e59`  
		Last Modified: Thu, 15 Jan 2026 23:19:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d8e7caff80c018e46521a273e278b5bb1d4f9f63e4e00c370ab30bbb9b0b6cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44994519f0a636e537448b764aaaebe808477f75cb47c291b0db9cc88ff3e90`

```dockerfile
```

-	Layers:
	-	`sha256:d35b2f0d9b1d35c78b0df80c74717f6407f59fd8128773ddbca3d26a76811376`  
		Last Modified: Fri, 16 Jan 2026 01:41:47 GMT  
		Size: 2.7 MB (2723714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e772a620c0e11eb572cd656d178f5083ba6ca2573e9f86b29c48dafb1ab19c3`  
		Last Modified: Fri, 16 Jan 2026 01:41:48 GMT  
		Size: 18.4 KB (18402 bytes)  
		MIME: application/vnd.in-toto+json
