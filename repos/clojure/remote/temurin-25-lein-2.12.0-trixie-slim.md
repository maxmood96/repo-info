## `clojure:temurin-25-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:e6361a5e020c437847b9f417aa256fb4b46c9817570e5da7690fcb18059caa43
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

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cb48be1472e951602e2491c56616fa00824e8220ab48edbb29afb58a95a8acae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143321005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2a404f5571324209de3f4f72966068db007abc1dae83094d5e5fdc6f70da45`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 19:42:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 19:42:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:42:32 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 19:42:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:19:07 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:22 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:19:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:19:22 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:19:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:19:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:19:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:19:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c932e6872b37fb626b9c05f0eddc412f9c275d7aa4f870bb5f174f0aaae9873`  
		Last Modified: Fri, 08 May 2026 19:43:20 GMT  
		Size: 92.6 MB (92574597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715532e14c8a1b8ba34493c168d230fcd5afd9cc5a3ae29c5a3dc26ac3e02832`  
		Last Modified: Fri, 08 May 2026 20:19:32 GMT  
		Size: 16.4 MB (16448007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fed66f6182912730e3af3632e9989425299814a98bbcf37998045b63a57dc2b`  
		Last Modified: Fri, 08 May 2026 20:19:32 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b1b990a02d122e6213d07f790e0879b170ce55302eb1b7bfe8e15b4f6df6fd`  
		Last Modified: Fri, 08 May 2026 20:19:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:521ad0e1885e32edc07355aa66e85018e3c9a4426e8020b67a195e60ff605866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2351697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7e2cf2d5bf74dfc742c3bf6998f50cbfb83d90ccaa68ca5dd01bb72b00337d`

```dockerfile
```

-	Layers:
	-	`sha256:37dbd672ecaeed80de43bf1c92ab7a3284299f78fb872fb2f4c53ad9b5f899a2`  
		Last Modified: Fri, 08 May 2026 20:19:32 GMT  
		Size: 2.3 MB (2333463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71aaa3772cf1496394f09414872fe52875341f806336e87805347cb3bec2354b`  
		Last Modified: Fri, 08 May 2026 20:19:31 GMT  
		Size: 18.2 KB (18234 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f4997e4ae3ad8f67844110c42e28717f4a55be0308108f213bdc6131fb6cf074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142618116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6804b1e7229a6549c2f2efcbbe744bdfa44c688aae52bd5c327019b4086a0f3c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:23:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:23:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:23:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:23:46 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:23:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:23:46 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:24:01 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:24:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:24:01 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:24:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:24:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:24:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:24:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9684d3a522e2364c2bddd6798cb5042b996cecd1b693cf07fd27253efc64efe7`  
		Last Modified: Fri, 08 May 2026 20:24:22 GMT  
		Size: 91.5 MB (91542269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcb33e81c36482430f018849c1208d25d13e8c7bdd253d427ee8c8a392a41de`  
		Last Modified: Fri, 08 May 2026 20:24:20 GMT  
		Size: 16.4 MB (16414016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707f04270285f468dcdd0172b41d01ce741263fbc029eb58726f8546d7bf0adc`  
		Last Modified: Fri, 08 May 2026 20:24:20 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f9160406d9b18b3a0792d3df19abc24ddb891094b66f8b9651372248f833b0`  
		Last Modified: Fri, 08 May 2026 20:24:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ad8690bb778f0ecea3351d184ab148f4d0ca2585091ecb0c88398fbd700dd6b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2352435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0a3a0a6d55465cb5f6c2aa3010b5f93b57047963ee060e37b1ec7bf7c94624`

```dockerfile
```

-	Layers:
	-	`sha256:8680d6f86c834d04de46304f1e96198a0e74c2c0922e9f919ae9ac2ac6539337`  
		Last Modified: Fri, 08 May 2026 20:24:19 GMT  
		Size: 2.3 MB (2333102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6727be29d8f164c88a2ad80f43dd21ec69d64e590bcd56f62a020167f76dc88d`  
		Last Modified: Fri, 08 May 2026 20:24:19 GMT  
		Size: 19.3 KB (19333 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:75ef67e8f30db4aebcf621a00abf13688f5527b7e3a6b89f8ca3b3c3c07877f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146515629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2f609075f74011f7604a18834b5664faad4252673522cee51ce428ef0545a0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:43:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:43:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:43:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:43:32 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 09 May 2026 02:43:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 09 May 2026 02:43:32 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:44:02 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 09 May 2026 02:44:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 May 2026 02:44:02 GMT
ENV LEIN_ROOT=1
# Sat, 09 May 2026 02:44:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 09 May 2026 02:44:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:44:07 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:44:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac28bbda9cf605f0d239dc381ad9eec484e7e0bec93b2a70b5e743abff1b6d9`  
		Last Modified: Sat, 09 May 2026 02:44:39 GMT  
		Size: 91.9 MB (91914009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e8f99858a9728b1155f5b2342cda98385d24fb3ef5b10d6a133ea77ee1dd67`  
		Last Modified: Sat, 09 May 2026 02:44:38 GMT  
		Size: 16.5 MB (16485349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b507c0fe871f35f77c0fce4b00a2481ba7d8480be12a5d22007d8505d816ff72`  
		Last Modified: Sat, 09 May 2026 02:44:37 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15eac5b8d584c6cbca32e24121288f88eaa0e398919a4fc3c15a4b6761207a7`  
		Last Modified: Sat, 09 May 2026 02:44:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5191cf0d4dca48a1c21f0107c8a284c98363bf1b2e48c93e4a1261a69eee6b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2337008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760932c7d136959736fe93bb7fd50478501939e26aca7a462c82a754570231dd`

```dockerfile
```

-	Layers:
	-	`sha256:07db77177c0e465289d11cf19464b4f27c1ec788c9eb1ed6d6ad5692183347a6`  
		Last Modified: Sat, 09 May 2026 02:44:37 GMT  
		Size: 2.3 MB (2317767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c80695464f9228f65c9e969b08c9ee8a82961c6db36ea85b17e6e0c5eebbc1f5`  
		Last Modified: Sat, 09 May 2026 02:44:36 GMT  
		Size: 19.2 KB (19241 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:900cbedf8dca9b67300d5d8bad3769a90379ef10440bfe1cee2fbc89c581559f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140211419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a03af4b185cb035b42ee926157033521029908df8389e3bcce8bc1e45746908`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 01 May 2026 01:17:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 May 2026 01:17:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 01 May 2026 01:17:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 01:17:25 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 01 May 2026 01:17:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 01 May 2026 01:17:25 GMT
WORKDIR /tmp
# Fri, 01 May 2026 01:18:58 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 01 May 2026 01:18:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 01 May 2026 01:18:58 GMT
ENV LEIN_ROOT=1
# Fri, 01 May 2026 01:19:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 01 May 2026 01:19:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 01 May 2026 01:19:14 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 01 May 2026 01:19:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a463537893b115e8f6bf5847dfb28b93d1015ffeaba8f0acf52e10133dfcf3`  
		Last Modified: Fri, 01 May 2026 01:22:48 GMT  
		Size: 91.0 MB (91014937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afe464ad1976fb5b9efa95b108a07377f29e8f3228ca04fa66e55042dbc3650`  
		Last Modified: Fri, 01 May 2026 01:22:37 GMT  
		Size: 16.4 MB (16398071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a825bba06ff3acbd94734a7a0a9e7117dbaa3d9e38b04292a6d5d9b64f0569fb`  
		Last Modified: Fri, 01 May 2026 01:22:33 GMT  
		Size: 4.5 MB (4517787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f019656c71b82322c680c851338fc1e20b860bd07fcf5d51d78722328d87f4aa`  
		Last Modified: Fri, 01 May 2026 01:22:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fa02d2492bd0e379f1278e8347aacc1bb0bf932fad84cb785852a7f466ba9198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2326624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc67c2ee42ff833d0f803f6de0bb83f44dcda2d35ba1758c747e37460e1a3a4`

```dockerfile
```

-	Layers:
	-	`sha256:c2d2a776c55825968393e2e40687efc7c9b8507292060f5393002cc3b4d2b48b`  
		Last Modified: Fri, 01 May 2026 01:22:32 GMT  
		Size: 2.3 MB (2307534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd73606e40f77c5dd00dbd8631ce9b549001ec06fca7d3eac4daa808015b8c49`  
		Last Modified: Fri, 01 May 2026 01:22:31 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:09508c5d551150c8220669ee33f1c7f85ac2a480e86f977cdae1f50cdb6f66c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139262622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641317fd8e02acd15aab8de7ea2485023eb8f66585f0bd52158ab56970eb2b3a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:19:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:19:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:19:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:19:47 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:19:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:19:47 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:20:00 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:20:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:20:00 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:20:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:20:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:20:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:20:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e938f267ce0fd10a0af51ad69cff5393dd662d7cd6252b86c266d7de2c2375c`  
		Last Modified: Fri, 08 May 2026 22:20:26 GMT  
		Size: 88.4 MB (88420315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b443bac9a437fb441007056e8c09a3e56b4813af193cddc67c5180466590e3a6`  
		Last Modified: Fri, 08 May 2026 22:20:25 GMT  
		Size: 16.5 MB (16483779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce563827ba748cd7d4262e34540f9b46c66c4dfefe4d301c62dc804df7f7f4f8`  
		Last Modified: Fri, 08 May 2026 22:20:24 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4956847e63922fed2826cbd5e4d429b0c27b015b91f39e3468d1b133ba071dd9`  
		Last Modified: Fri, 08 May 2026 22:20:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:de776eefd95fe4941733883240b26fa76a017f8ea5276288237856bd4003096a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd0b1beb8cf4c76c408904df78b801be71e10354cfa25dbc59bd48e51e850ed`

```dockerfile
```

-	Layers:
	-	`sha256:cc42b1bd4cd16f56349eb2c311376c441477b0c636bad5cd9a8c61893b90cf5b`  
		Last Modified: Fri, 08 May 2026 22:20:24 GMT  
		Size: 2.3 MB (2314452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a797a2a64bc7f0ba2f06d7879efe9cac17fa58d0b317adb5364d300d32b2b69e`  
		Last Modified: Fri, 08 May 2026 22:20:24 GMT  
		Size: 19.2 KB (19187 bytes)  
		MIME: application/vnd.in-toto+json
