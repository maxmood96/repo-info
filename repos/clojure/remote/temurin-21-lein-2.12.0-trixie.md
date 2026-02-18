## `clojure:temurin-21-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:a91ab97c5e9a4cce17cc83fe9d82d249c9dd510dc855d49618546befaab1c798
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

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:ef3fa7922863723a6bcfe49678cad80c376c20690299bca341a6060d5b42c160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230248243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989cca34e248f83419cfb0fa32b152eb7b0e11a9b8aa7b9bc933d9523ed67ecb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:44:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:44:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:44:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:44:11 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:44:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:44:11 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:44:32 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:44:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:44:32 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:44:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:44:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:44:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:44:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5643e48ada99838f7f59b01bb1a5f218613e8ded360067227178a666b6c49653`  
		Last Modified: Tue, 17 Feb 2026 21:44:55 GMT  
		Size: 157.9 MB (157857066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf889bcbfd77686d79c5013406248f2b7fdfc3e382ab355b124f7733ed1e0bf4`  
		Last Modified: Tue, 17 Feb 2026 21:44:52 GMT  
		Size: 18.6 MB (18580083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547f22531e2453d1c9a155d2e18898455ae242f30832a29970d67376b5bb3c08`  
		Last Modified: Tue, 17 Feb 2026 21:44:51 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2732bfb9d0f2bf5c68520983cf04454c8b063fdb4994c846d308dbddb01b232a`  
		Last Modified: Tue, 17 Feb 2026 21:44:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:da902f549079cd9457601fb2fff6163c88021ab5178be75d009919527c50cd71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13db5d6587ff4c4a03c6f0880ee05eab6938c634bf870059d214ab852755cfe`

```dockerfile
```

-	Layers:
	-	`sha256:27985aaa7ef4a3915e63626b38cab5283b8cc248993f3209f04e628e9a486108`  
		Last Modified: Tue, 17 Feb 2026 21:44:51 GMT  
		Size: 3.8 MB (3817343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe83b2e09f95edb3466e479c639ee58b95bdc25e33decc798b57c2795f257e37`  
		Last Modified: Tue, 17 Feb 2026 21:44:51 GMT  
		Size: 18.4 KB (18351 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d5986c46497afa43567fe6975f8f313f645e8918ea06e4a3d0b0a64279a81222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228844709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1650be48ad3ebe4dcce006057ff878ec99d806450fd3fc16acf5c82cba753d7e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:44:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:44:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:44:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:44:06 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:44:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:44:06 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:44:26 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:44:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:44:26 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:44:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:44:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:44:27 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:44:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d31f950630ef93cbfac78528a1eea0e4711eda7f95c5fdad8a3a69aa614f36`  
		Last Modified: Tue, 17 Feb 2026 21:44:49 GMT  
		Size: 156.1 MB (156133063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22501555d0d4d1da66ab085798b655feb9f6da17f82e31d12ffd12ff97fb9ce1`  
		Last Modified: Tue, 17 Feb 2026 21:44:46 GMT  
		Size: 18.5 MB (18541488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1d07f6270c8fb1ec8e704a91bc2a125affea2d9c96da62e2c2cee20718fa18`  
		Last Modified: Tue, 17 Feb 2026 21:44:46 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e25c7a26140234c4b5ebbafac26fadd32577907a04652168def7bcbf28cc7cd`  
		Last Modified: Tue, 17 Feb 2026 21:44:45 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e58e21439399a308a50b706ef65b8f1534d4b8ed08e034dca55bc5f8808b4eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42a50f1d0c6cf27906073e39db141e78c5d60ad39e5dee12c6ab0f521ecc1af`

```dockerfile
```

-	Layers:
	-	`sha256:298be56c7d4fd3d70947fa3a1df2eb85747796598c346c3f3aabd3701e7d7e92`  
		Last Modified: Tue, 17 Feb 2026 21:44:46 GMT  
		Size: 3.8 MB (3818220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e3fb9fe0cf1a930371e3f1c1b26a8962218e12cb617ae60a5accd70a20f8233`  
		Last Modified: Tue, 17 Feb 2026 21:44:45 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:83d955d77b8755382ea2f0f23fea1673e290d30931637e823ab564c3518c332c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234245381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc05c51b92adf05ccaca1c2c40a616c5678d6ce1ad6218e6a833ed34260452b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:37:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:37:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:37:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:37:54 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 06 Feb 2026 00:37:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 06 Feb 2026 00:37:56 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:38:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 06 Feb 2026 00:38:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 06 Feb 2026 00:38:53 GMT
ENV LEIN_ROOT=1
# Fri, 06 Feb 2026 00:38:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Feb 2026 00:38:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:38:57 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:38:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d803d46010c6f6fae7ea82f881a836bc9d2bf4afad631cfb7ffd52616e4eec`  
		Last Modified: Fri, 06 Feb 2026 00:39:44 GMT  
		Size: 158.0 MB (157977492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0102041d69bcc6f979348014d7f317870f7043d507982ca14e7db62bc89f9d`  
		Last Modified: Fri, 06 Feb 2026 00:39:44 GMT  
		Size: 18.6 MB (18637604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7dec1ea7883b3f1e03363b33f175a032a2efb6be7dae92577c18604a1c8369`  
		Last Modified: Fri, 06 Feb 2026 00:39:43 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ac1dbd83479c04d0086ec4af0e6f854675b9502fcb13a4d557f2b451719510`  
		Last Modified: Fri, 06 Feb 2026 00:39:43 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d907972e11d93d334059d5a5c844c659f850cce51b4d4cd646e6e1645154b0f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a7800aa92bac7bebb2fdfef9a4a29e25fd0f635f2af8955ddc170209494bc1`

```dockerfile
```

-	Layers:
	-	`sha256:c2c7d50b07424dc5c9669635e6270f0f0452f26523dfa8b2318e93ba2698f432`  
		Last Modified: Tue, 17 Feb 2026 23:59:04 GMT  
		Size: 3.8 MB (3818343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ccdc70fb7b91628ec3ce414656324ff196840a073a946549b509d24c399c07f`  
		Last Modified: Tue, 17 Feb 2026 23:59:04 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:e03655dff73c966da3904cd423849f6a4c16b07b72bdbb3eadf585ca07a55e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228043674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddf6eb22210a6e5c15c3fbe2b30ca8b740b1244a60b4987f53ea96dee97e6e6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 12:14:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Feb 2026 12:14:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Feb 2026 12:14:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 12:14:12 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 09 Feb 2026 12:14:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 09 Feb 2026 12:14:12 GMT
WORKDIR /tmp
# Mon, 09 Feb 2026 12:15:51 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 09 Feb 2026 12:15:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 09 Feb 2026 12:15:51 GMT
ENV LEIN_ROOT=1
# Mon, 09 Feb 2026 12:16:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 09 Feb 2026 12:16:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Feb 2026 12:16:08 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Feb 2026 12:16:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4679cba1526d236633941ffa3c6d13fad991fde42b4ce1329897774df20befca`  
		Last Modified: Mon, 09 Feb 2026 12:20:51 GMT  
		Size: 157.2 MB (157216869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f17140d95821772939e4f3fbbcc69e2b5a3f6e978529f6b3c48aea1cd399ac6`  
		Last Modified: Mon, 09 Feb 2026 12:20:30 GMT  
		Size: 18.5 MB (18531825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb209d6383e76fb09bb033c6c1b3321d1157c7a39b5861712eedb0d2f60dd06`  
		Last Modified: Mon, 09 Feb 2026 12:20:27 GMT  
		Size: 4.5 MB (4517787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a08fa0934f91f9a853f515bcd2c34cb2ecf118166b98927407200cd44294dc6`  
		Last Modified: Mon, 09 Feb 2026 12:20:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e78396c15d4bec9f9d1defd91cff080141b9cebf9a33e6e2585b268965e1cd69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3826216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f62210b080aa4e439f11e781515732a97411126cefd36d441d9f8c027bc507`

```dockerfile
```

-	Layers:
	-	`sha256:980b8ce7b4085ce6a86a471fabfe96adbdab0d41b46b9bb685529ea3c28e758c`  
		Last Modified: Mon, 09 Feb 2026 12:20:25 GMT  
		Size: 3.8 MB (3807820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b9dda127422928df82ead6629a34a8616715790b93f18956a02c9c1af7d24b`  
		Last Modified: Mon, 09 Feb 2026 12:20:24 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:c5c1496253900a5b3fab472d324035d862fc305b0aa181f75dd2e0ca2bdd24a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219599160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c5b393a532479b7740bb4128bdea0a6d0ac4e4bae115b01432f089dc7a8db8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 22:12:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:12:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:12:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:12:44 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 22:12:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 22:12:44 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:13:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 22:13:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 22:13:23 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 22:13:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 22:13:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:13:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:13:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbcb2a4eb68d199106dfb710f086ecdf2ee7d722b55f808aa430670d4adeb`  
		Last Modified: Tue, 17 Feb 2026 22:14:07 GMT  
		Size: 147.1 MB (147105303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0c10d5c0e49ff3505e97129379c2ec4fb92ba4f15f43f1d9309337380e3e00`  
		Last Modified: Tue, 17 Feb 2026 22:14:08 GMT  
		Size: 18.6 MB (18621294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a798b208c74f9ac42e46572b8c83bb3d44b1e5d46229082157a4e4738650e8`  
		Last Modified: Tue, 17 Feb 2026 22:14:06 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786117b6675e04ec523b486d7752189c11bd4fda443d1993d7850677b11b7dfa`  
		Last Modified: Tue, 17 Feb 2026 22:14:05 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6b4a847a2dc1519df78ef9837e223ba067ff1c197541a4a037ada2e474a8f778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5671677c781bc407178ed12993f9c2999db0e814deed5793633b18647d306a40`

```dockerfile
```

-	Layers:
	-	`sha256:3051ce4875d1c6b9cbef2cac52866cdf027a2a4ab543dcd64f5eaa484218cadd`  
		Last Modified: Tue, 17 Feb 2026 22:14:06 GMT  
		Size: 3.8 MB (3813770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a99238b0d10cbe7b57034b58df45275b1c6dc1bd97adc11b289ce4868c04bbc1`  
		Last Modified: Tue, 17 Feb 2026 22:14:04 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
