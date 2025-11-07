## `clojure:temurin-21-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:fab781f457692825b65b7e2e9d3cbbae9b48b96466aef686f0b86bf0986b4342
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7c25326148c4432f5e6406caaff36353b934d92d0c2df133eed0321e19365e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232687175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd17162903da9c14d6b01884328c7c638c49195a38ea82c67813aa95765df908`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:55:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:55:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:55:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:55:27 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:55:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:55:27 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:55:41 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:55:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:55:41 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:55:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:55:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:55:43 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:55:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3462acca2b1e3c0b363f501a96c9489d08f6c73f88759ab4c8e4474cc861c73d`  
		Last Modified: Thu, 06 Nov 2025 04:13:00 GMT  
		Size: 157.8 MB (157804746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b177207be63a4219513d67ac81822ff263d014a27d4500386fa086bd2abeb0bb`  
		Last Modified: Tue, 04 Nov 2025 00:56:11 GMT  
		Size: 16.6 MB (16607587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cafcdfcbddf6d1ecb1d5452b7b13b3f8c00128fa815f326ab5707d9d3f29e7`  
		Last Modified: Tue, 04 Nov 2025 00:56:10 GMT  
		Size: 4.5 MB (4517720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4004a68146d014b286aa1ecb34c2486349baf3fa5598d9ca5a8335bbcb4101`  
		Last Modified: Tue, 04 Nov 2025 00:56:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0d8adc265d3a6337d252e1968fb4fc16f44311a29640e3f74f6ede3cde90bc88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc0c8316c61805d9c6efdcd8dd7f3e4fea800e59723854fa1ea8e989268a539`

```dockerfile
```

-	Layers:
	-	`sha256:f2874ed4c8f547c26e3dee0aaf9490a80b9a37fe28f07ba7bcaa57ab161415cc`  
		Last Modified: Tue, 04 Nov 2025 10:43:19 GMT  
		Size: 4.5 MB (4479290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04728184ffe677c85324999c6fdd61249ed1c7ca1d5e904fd2cfc1266eb6b758`  
		Last Modified: Tue, 04 Nov 2025 10:43:20 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:62dab1878f12dd0c9cf9c7d874ae55713bbf06844c387d1c9a829bfd0e51fbaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229452408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa76c1cd57e6ad202548170e9d2db3a95615a5e11b7408459147138f47800ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:56:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:56:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:56:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:56:29 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:56:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:56:29 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:56:43 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:56:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:56:43 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:56:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:56:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:56:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:56:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344b5bd99559cb6cd48ae1fdd980e6f7b8440a6148e0a06b048391e371e5941f`  
		Last Modified: Fri, 07 Nov 2025 15:06:58 GMT  
		Size: 156.1 MB (156081238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde0cdf3362912eb573021f0ceb18489b3f8e15e4016107b80afb9a71980a302`  
		Last Modified: Tue, 04 Nov 2025 00:57:16 GMT  
		Size: 16.6 MB (16595021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c69ff56eeba7d41da4fdf3dc8ed04cbc25e062eacbdce259834ec52886bdd7`  
		Last Modified: Tue, 04 Nov 2025 00:57:15 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df3765ca578e7bdc94cb6589b368d6f98934060696870cd51457cbf05629e32`  
		Last Modified: Tue, 04 Nov 2025 00:57:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6b334b30dd614fc3e62ec1a08c6175d9a26748f72017a6147efc4a3b6cc52e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4496753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f8ad75e3a795a836f98ba67086a9bdd05998acd973442b9d420499846c1257`

```dockerfile
```

-	Layers:
	-	`sha256:0febff0c52834078e4144d15cd00f3a2aa8eeb5a7c17100e3381d62a556af37d`  
		Last Modified: Tue, 04 Nov 2025 00:57:03 GMT  
		Size: 4.5 MB (4478264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41148f1120da348aeeb59f995b01b0060888a563de4976b00067c42635a70bf0`  
		Last Modified: Tue, 04 Nov 2025 00:57:03 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json
