## `clojure:temurin-8-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:6213a009a85a8d1e3abbf68ffb62b5303b2a986f3f370e30cc11d4bca509d01f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9494291765ee46ecc3b9899ead95975059337027722b5e62082e3e8682b2a135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105710265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4cddfb5c687d2dad63806a9f020cfc3ac4e9c1255729040602ab9d34f61b8f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:55:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:55:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:55:29 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:55:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:55:29 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:55:43 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 19 May 2026 23:55:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 May 2026 23:55:43 GMT
ENV LEIN_ROOT=1
# Tue, 19 May 2026 23:55:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 19 May 2026 23:55:44 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae93db75a8bf470500d8da02150e2232ae3749f2ba0d70ded8828c9d13ac3f79`  
		Last Modified: Tue, 19 May 2026 23:55:59 GMT  
		Size: 55.2 MB (55198723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6880dd7c3ba1b4c0e0ea645af79dd8763cb5b15bf1634ae7c0b4b78a6ea27fd`  
		Last Modified: Tue, 19 May 2026 23:55:58 GMT  
		Size: 17.8 MB (17760254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fc98a0709e53e49faf324ce1143b5dc1c84cf14983b010f308c7c1ad2a53fb`  
		Last Modified: Tue, 19 May 2026 23:55:57 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c3c4fc4fe0f9e1008318245250d042fb9ca2c64ef9a518f522f4dbd13a765523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742de7a927b09c59f6c02263c68592e2078264422f0a507b88205506ba46ce64`

```dockerfile
```

-	Layers:
	-	`sha256:89ff1bff1b547add79c306ae428468fa3f94d24a344b524561ac4132545b7528`  
		Last Modified: Tue, 19 May 2026 23:55:57 GMT  
		Size: 2.9 MB (2851057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea14ec0c478320777fb0af4cac7f4a918f913ece9b588efb1bb00d97325d0fc9`  
		Last Modified: Tue, 19 May 2026 23:55:57 GMT  
		Size: 16.6 KB (16554 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ec4fcb18e1a0567611e927048d644f148452dd8543b52a6866f388071595a083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104499529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7d8e6e4e241d87d917fc3e8820c62064caea00285218acc2ac7c615c808f6b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:02:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:02:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:02:52 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:02:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:02:52 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:03:05 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:03:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:03:05 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:03:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:03:07 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1118c945a8f5ed4be0133088b6adffeeb4a0923ad2f423fe89c754f333f4056c`  
		Last Modified: Wed, 20 May 2026 00:03:20 GMT  
		Size: 54.3 MB (54272922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca805e8e68b39cf3d36b8d0b3c86d8c745397df64e860a3070e0fdcb8dcea295`  
		Last Modified: Wed, 20 May 2026 00:03:20 GMT  
		Size: 17.6 MB (17593801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fa4b930fc2bd7a199df91ad98ba2839ecd83eefbfb927bab273719646bfaaa`  
		Last Modified: Wed, 20 May 2026 00:03:19 GMT  
		Size: 4.5 MB (4517731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4ea352967239b845c2e5dacfc1c38109fcc4ee2df4d3cbc910421ec58c60704f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2868047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d5bc68a51c6d8d2f53fb67559792df086996a52a296b959ed3ea752c479639`

```dockerfile
```

-	Layers:
	-	`sha256:3e40cabea24e11ef5b2f289f13392545d725c217511ef0dfcff58b3074bece7c`  
		Last Modified: Wed, 20 May 2026 00:03:18 GMT  
		Size: 2.9 MB (2851372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45d271e0668f20ace654577d85ae218ce4c26129956bbc09ba3a713f9d983553`  
		Last Modified: Wed, 20 May 2026 00:03:18 GMT  
		Size: 16.7 KB (16675 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6f79bdd3d6f83afc471a6c7eac6b61338af76c6297cb308ba86120be678a4fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107226033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34edaf672998bc6f6a7a439257c76e2b5e4f28ce2eb3c7e7a8d16c091494a72`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 05:43:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:43:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:43:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:43:16 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 05:43:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 05:43:17 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:43:43 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 05:43:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 05:43:43 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 05:43:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 05:43:47 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e7d2adee20295d3b262cdd2cfe943ade2d2c668cc3b4db782efb9526da7915`  
		Last Modified: Wed, 20 May 2026 05:44:13 GMT  
		Size: 52.7 MB (52669153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a97e9d7518ef179d34e6236251c54c00236be93277dbefc0ecf678c28f765a`  
		Last Modified: Wed, 20 May 2026 05:44:12 GMT  
		Size: 18.0 MB (17963354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a8e3b6cc229f96fdbb3f3edf5a3e5f5f21bfcc79f1dcc0c94994f55a07ed1f`  
		Last Modified: Wed, 20 May 2026 05:44:12 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8c69da7a7eb0a5b3fe943e08add452e1755da51dd5bff913e062c8036670336d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2d9aa2dcc1d81b1fc25ef08efd271d1fc36b7cb6c65956dc2a77fdfae4eb39`

```dockerfile
```

-	Layers:
	-	`sha256:ec6eb434d3d29fef03ddb6056f5a6b1e00da99b56a0567ee0c67dd1348dd82a2`  
		Last Modified: Wed, 20 May 2026 05:44:11 GMT  
		Size: 2.9 MB (2853485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2428c5ee1dcf0c9231ad968816e0e1772a5d8a2ef89f8e817287894e0d417752`  
		Last Modified: Wed, 20 May 2026 05:44:11 GMT  
		Size: 16.6 KB (16598 bytes)  
		MIME: application/vnd.in-toto+json
