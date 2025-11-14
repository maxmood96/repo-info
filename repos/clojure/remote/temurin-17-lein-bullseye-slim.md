## `clojure:temurin-17-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:22a2180fc2c0b9cecf8a20a8746426b5d259ce32cac5c71c33e3beb1d764f647
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b53d420e9795470dac9fb1c72226457b186c91e08e331c205a5c104c15fb9d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194943480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2754827853fd0bfc7f3603f25a7bc2d44cc59a414414abc59dbbce0e7d5b7b0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:52:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:52:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:52:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:52:15 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:52:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:52:15 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:52:29 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:52:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:52:29 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:52:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:52:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:52:31 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:52:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd27d62c2fc064d987964aedbb52dd18e1f67701acf38dd1f4195e2362dc5b7d`  
		Last Modified: Fri, 14 Nov 2025 00:52:51 GMT  
		Size: 144.8 MB (144847974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08db742eacd461838bebe4b34af5dcf275a547b2e4092403d631b6268d54814a`  
		Last Modified: Fri, 14 Nov 2025 00:52:59 GMT  
		Size: 15.3 MB (15318762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7390df5a48a06b4a1476d810a5f3c1bcbd193481f367d148fc2ed537e514a0`  
		Last Modified: Fri, 14 Nov 2025 00:52:58 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f744f9784f02ab2cdfaef7dc4bcb0457269b5f53182eeb9beffef3c1deb1e20`  
		Last Modified: Fri, 14 Nov 2025 00:52:58 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d3174a626a02bff92c6c772227d9484420c1944f42d73c0ba7b7596cbaf4f23d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b43078d856c3ecf31fdd935cbe7c37c5521541b56a6ae3da6d55d0397479c4`

```dockerfile
```

-	Layers:
	-	`sha256:13b1c624e9bfe417920356fd9d126dd390d9d437ca7ec7b8abda19f6068af61a`  
		Last Modified: Fri, 14 Nov 2025 01:40:09 GMT  
		Size: 3.0 MB (3017910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c361f868eecae838db1de8c583bfa00955a91a1142f3d2728b817497f29cf88a`  
		Last Modified: Fri, 14 Nov 2025 01:40:10 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1d0d72b98d2b8ab1256600a30d4052738f0ff2c18baa6f0eecd28fa4b166859f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192252513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13b1160c57bf7b1b3ae817424195efdb8a680fed25212db9f68dea268ffde5a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:30:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:30:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:30:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:30:28 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:30:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:54:28 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:54:41 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:54:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:54:41 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:54:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:54:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:54:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:54:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9366146ac0faadb7b8911c40201a147e5f2f4ec5d7cc8603b0501e4e651c501`  
		Last Modified: Fri, 14 Nov 2025 03:48:16 GMT  
		Size: 143.7 MB (143679960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86884c1e170f95733ffccaa15412fc7d42c676d2c356a8afd33c7516c037049`  
		Last Modified: Fri, 14 Nov 2025 00:55:02 GMT  
		Size: 15.3 MB (15305839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae46ade8504467e6d53dc004ab5e92cfe32e6cc83edb8e4401663cb50a202bee`  
		Last Modified: Fri, 14 Nov 2025 00:55:02 GMT  
		Size: 4.5 MB (4517731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4ff1f5dabc5a51ab547972a97d476936953adecbed4a2d1a062c4680de3038`  
		Last Modified: Fri, 14 Nov 2025 00:55:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1a86944be8c1664b3dce0207ba7c37d057f54a7b2d1bc06d057245f7d5f9d234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1b388e9a9ed81f0ce2ebb736cb7678d0dbed039d84fd0ed15c201a0ad8ad6a`

```dockerfile
```

-	Layers:
	-	`sha256:5f7393894645a32f3c5df51095e7e789424aa79b6a3e422e960810a18656d4be`  
		Last Modified: Fri, 14 Nov 2025 01:40:15 GMT  
		Size: 3.0 MB (3017519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09db14887b598231c4c4a6ca7c6d3a261a0552fa97a34ebcf0da445a99586297`  
		Last Modified: Fri, 14 Nov 2025 01:40:16 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json
