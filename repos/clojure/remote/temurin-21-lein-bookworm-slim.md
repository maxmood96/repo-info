## `clojure:temurin-21-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:6e190f26c2ba6a3cea8d5337012367bef76546e5d56f0f1e7c8400b72088d40b
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
		Last Modified: Tue, 13 Jan 2026 03:34:36 GMT  
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
$ docker pull clojure@sha256:eb1355915325bb4abeb57d8bc1b882e24a90a6caf9d86daabe357e6ccf757d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212489668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6592d2152066d8533b1b21a9c7434ec25858faf92053f0ebb9a9677b7fff3390`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 05:21:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:21:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:21:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:21:25 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 05:21:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 05:21:25 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:22:06 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 05:22:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 05:22:06 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 05:22:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 05:22:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 05:22:10 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 05:22:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5205a1e1f7238574a7d52bb96b174549098b3440c35820756b8c8be70a79f64d`  
		Last Modified: Tue, 30 Dec 2025 09:15:38 GMT  
		Size: 157.9 MB (157942950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70dd4ae8fa1777a3c9acac4931612deec51b925832b22d342bb7453ee5e49e8f`  
		Last Modified: Tue, 30 Dec 2025 09:00:38 GMT  
		Size: 18.0 MB (17959704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca98bbde25fa1e20d9e33d327d577a20a8480df66768526930e86b5eab82d08f`  
		Last Modified: Tue, 30 Dec 2025 09:00:37 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7bf1384474575be3992eda371a5231d3756d0d09b85d6ada796cc61c0327`  
		Last Modified: Tue, 30 Dec 2025 09:00:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9a8452111f0b696a323e5b4191cb1c893da08b8799d560426e9d5e0b769d4dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f11c38fbc4e33f11e0a0400a537e61f1d662721871e428ad44a347741d90872`

```dockerfile
```

-	Layers:
	-	`sha256:00e3ac79b3f2ac316eef09a9acf606108fa0d3138647b00fed774d4c471e2ef3`  
		Last Modified: Tue, 30 Dec 2025 10:35:56 GMT  
		Size: 2.7 MB (2733723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddc5a1b7af2c6c219a3095e98abe4faa1fd54a8280fff19031a317fd153cc486`  
		Last Modified: Tue, 30 Dec 2025 10:35:57 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b330da1f1292e0ecfe2d07a9c66edee2b27a14ac322e1bbab09ec32667f9edfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195893162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4982d3d3399c57312d7f3254e6b7c7282cd90d3c562d060f52792af3bac5345`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:05:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:05:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:05:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:05:26 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:05:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:05:26 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:05:36 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:05:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:05:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:05:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:05:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:05:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:05:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b30689a6c8fb0d3773ac5b39e3291262242aa068cabd739b185d23b4c70da67`  
		Last Modified: Tue, 13 Jan 2026 03:06:22 GMT  
		Size: 147.1 MB (147069857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debe0cf03b0d8d86ce3365f87a88009f0accf20cecf209e13f211d658813af49`  
		Last Modified: Tue, 13 Jan 2026 03:06:11 GMT  
		Size: 17.4 MB (17420710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40d4f76eb9bcc31899cacfe5c606d95f82a648840c372be2b39708d54db6290`  
		Last Modified: Tue, 13 Jan 2026 03:06:09 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6da08754dd6f14914dd48f11c929cc21b5da748aaf89ab4258902db6bf013d`  
		Last Modified: Tue, 13 Jan 2026 03:06:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ee07ee4cc50082e9208c7ebb31adc35871d7ec2ac9b91d3c1fe04b20f8d3aeb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366fd196e7a06070db5f9f2abf63b9edaad00e60f5bf82bbca31feab7c83970e`

```dockerfile
```

-	Layers:
	-	`sha256:510371a003bafb1f3e79a1abae8fe374f4f033d03e5f25ad96363f9ee858f078`  
		Last Modified: Tue, 13 Jan 2026 04:39:01 GMT  
		Size: 2.7 MB (2723714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e6be765864ef49bf8cdb88027712e328861e4d5360b7ca5c50491e8b866616`  
		Last Modified: Tue, 13 Jan 2026 04:39:01 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json
