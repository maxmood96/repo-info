## `clojure:temurin-21-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:59717627040342d9696ade4d4da09e3c31e60d3d8f78d307148fc09f30b9c0b4
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

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:86ed58c7ef31f510376f6546296965801c1b1722d79ed59f984e2a00cb710274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.6 MB (211552833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cdfdcf222eeaa849fe7c73f2594e2eed473b90a5b23c3a0ec8b75d987fdc6b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 21:40:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:40:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 21:40:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:40:38 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 21:40:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:05:13 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:05:30 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:05:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:05:30 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:05:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:05:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:05:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:05:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b191a82337ac2ae5ca7dbc7bbc422df576bb6c534c23e21764123330cb817307`  
		Last Modified: Wed, 15 Apr 2026 21:41:25 GMT  
		Size: 157.9 MB (157857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d374ca1426585caa36a7a0fc8f93ac25c1541eb8623af08e1066c4af9fdafc`  
		Last Modified: Wed, 15 Apr 2026 22:05:41 GMT  
		Size: 19.4 MB (19401972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d56c5d4763e8bf3c7ed03ba0718eae9d7c30628cfc527af37a7f18505cda35e`  
		Last Modified: Wed, 15 Apr 2026 22:05:41 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38724b05d0a97f156a80de9c1f515f085473086a1268bdf5d3e1174f76f6d498`  
		Last Modified: Wed, 15 Apr 2026 22:05:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:525ab5d60627307be32eee6eec7bd1b0fa6fabd86f09ec3f67fee9a810736818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba4752d78b2be12109c48fc46301e0e149fb894bdde6e7e443021b8b08383ae`

```dockerfile
```

-	Layers:
	-	`sha256:d4da2ffad4739795a72be958c96fdfac462ced3bdffdd1efc53622ca7aef4eca`  
		Last Modified: Wed, 15 Apr 2026 22:05:41 GMT  
		Size: 2.4 MB (2366640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5e7521c86aad1636d4563630642d40050dea2b81cf216b4acd74d1d3ac74520`  
		Last Modified: Wed, 15 Apr 2026 22:05:40 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d2ddb1f7cda8447dc130dcf1671200137da7a21a0089796b244901231ed5443d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210524680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7959c9c2a8e17f1c99794e27498454fec8db77671b1ef97fc801967a52f9a810`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:16:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:16:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:16:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:16:41 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:16:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:16:41 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:16:57 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:16:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:16:57 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:16:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:16:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:16:59 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:16:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40002a76df96ea56270f2b32f834fb63893831735752fe8d5b2bb4fa52514133`  
		Last Modified: Wed, 15 Apr 2026 22:17:23 GMT  
		Size: 156.1 MB (156133065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c91f2ff6855cee22ea0ccbdad2fb8c58fadc27b1e41cc4972e626323abdcff9`  
		Last Modified: Wed, 15 Apr 2026 22:17:18 GMT  
		Size: 19.7 MB (19734907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a67a63dcbd69a2db3b8e1557b5cff807165acd0f88bb95de9cecb41331f8ba`  
		Last Modified: Wed, 15 Apr 2026 22:17:18 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff19ab42b9854b47146e5358934959db5f8b535b149236d83dfdc3f2ed063a52`  
		Last Modified: Wed, 15 Apr 2026 22:17:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c715d93500f0eef75b1ea2f839a2444c7ab272d543d6f3e427b7f34c1380a42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007cbe933bfcac3ca1cbfe2ccb7b50f9282e7bbce0fa7e1e901dbc3b4433db03`

```dockerfile
```

-	Layers:
	-	`sha256:c65887a7da6c2c6fe078e3dfe29de808309024fffe0760cb8caa309495e441ff`  
		Last Modified: Wed, 15 Apr 2026 22:17:17 GMT  
		Size: 2.4 MB (2366258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:043bda9e8616269f4a5ad65697c23038c1c93fd0791c8df88da6ef4db51695dc`  
		Last Modified: Wed, 15 Apr 2026 22:17:17 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b54831de1636a81308803686fd45d926c076d5c10e3e452dfc1f32ac97f40895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212574033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305cc567b81a33af02c745c1b88ca87969aaf9eb4aef7ea10bedcf313c653329`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:48:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:48:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:48:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:48:08 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:48:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:48:09 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:48:45 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:48:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:48:45 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:48:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:48:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:48:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:48:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba66074989fc6e37b18a04cc78cb4c1a09ae249fb0aea194ade5c8d6049e645`  
		Last Modified: Tue, 07 Apr 2026 14:49:29 GMT  
		Size: 158.0 MB (157977472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b914d76085c4006245f3c5dca4adf48ce9369ebc5272dfb822718c84520efe5`  
		Last Modified: Tue, 07 Apr 2026 14:49:25 GMT  
		Size: 16.5 MB (16485380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242ee3441b55904443bca9506bf9108a7f8fd85673253cc3806f9bd3117307b2`  
		Last Modified: Tue, 07 Apr 2026 14:49:25 GMT  
		Size: 4.5 MB (4517735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de275d6feab38a27902138c00dcddb25c8a30dab4c6a3a1d4d104c39ab21cf7b`  
		Last Modified: Tue, 07 Apr 2026 14:49:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1a9366bd4ae72dd091cc93234f01d753dd02560dbb9a27f1c7cada2cee1f1824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593fe79883f20d3b2649384c84750f0af30198f7538c81b3dbc3d3f511f070da`

```dockerfile
```

-	Layers:
	-	`sha256:8b7fc0a37395c163c23b1f5419b7a46dd538a64b958050368ec6346f8834ff8f`  
		Last Modified: Tue, 07 Apr 2026 14:49:24 GMT  
		Size: 2.4 MB (2367620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ba12c055e4c75578485e5326850f27dc4b7abb0b61389cfd7e4946f5b72800c`  
		Last Modified: Tue, 07 Apr 2026 14:49:24 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:94415b92cd015d3220b2f6c11057740806d8455ece15fba634c646f74cd7e9c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.0 MB (209029007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f144f37dff4c691e05fa84c81537b0e6fd1dc9e473b54b15f9d45db71fc255b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 22:00:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 22:00:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 22:00:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 22:00:57 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 11 Apr 2026 22:00:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 11 Apr 2026 22:00:57 GMT
WORKDIR /tmp
# Sat, 11 Apr 2026 22:02:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 11 Apr 2026 22:02:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 11 Apr 2026 22:02:32 GMT
ENV LEIN_ROOT=1
# Sat, 11 Apr 2026 22:02:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 11 Apr 2026 22:02:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 11 Apr 2026 22:02:47 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 11 Apr 2026 22:02:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5427f8f7357cd1c2f90f35451416b331ea3c682f95a93bd8689b142ddc99805`  
		Last Modified: Sat, 11 Apr 2026 22:07:07 GMT  
		Size: 157.2 MB (157216895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f59eb2176b5c554edc1e95885f260b8164158eac9ea19a152e12316e8da6f5a`  
		Last Modified: Sat, 11 Apr 2026 22:06:47 GMT  
		Size: 19.0 MB (19018122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23af71c01bde7375e68c11947a0fa8bdc5dbbdad2891274c6e57a92667faacd`  
		Last Modified: Sat, 11 Apr 2026 22:06:42 GMT  
		Size: 4.5 MB (4517782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991d08aa1603edfda4611d58fe8d397631e39bb6dede09638dd26b3051051ce8`  
		Last Modified: Sat, 11 Apr 2026 22:06:40 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dd0899f9ff2aa354927a73ecabb63cb41320b8cb22495069d9700097a0da32ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8fe8b641c9daee65e7bd71e7ad48fab013217c8350f5cb1d284aed4c80e453`

```dockerfile
```

-	Layers:
	-	`sha256:dc3f10ac2cb76c50c2ab195e431aecdfc85a3928864419bef105e9d0bb3fa395`  
		Last Modified: Sat, 11 Apr 2026 22:06:41 GMT  
		Size: 2.4 MB (2358688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45411b34706c73cdd2efe0872681ee9110f04565685c78f0aaacca655ce52766`  
		Last Modified: Sat, 11 Apr 2026 22:06:40 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:30d60a7da59e29dbdeaa9b6ee42045c470fecf12747b13a9ef9a5870117b6089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.5 MB (200548982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa670d58d108a3973d7a31b7d0ac0ab151dfad85e7b7cde96d0ff86d30cf082`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:41:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:41:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:41:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:41:51 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 00:41:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 00:41:51 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:42:04 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:42:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:42:04 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:42:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:42:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:42:06 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:42:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcda4ee8bd621aac2ef8027b80495558658cc850eca58d63e93743bca8b01b4`  
		Last Modified: Thu, 16 Apr 2026 00:42:33 GMT  
		Size: 147.1 MB (147105251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659f1f18ca7322e214430cf3fd9f252602b503bfde82628d5f33ed9e481c1f29`  
		Last Modified: Thu, 16 Apr 2026 00:42:31 GMT  
		Size: 19.1 MB (19090141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b338857b0bc8d840cae1656d7ff58df1cfc434e057aa4d43ed4536edf9609f68`  
		Last Modified: Thu, 16 Apr 2026 00:42:31 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f73b255601137d87a42aa3f991543a804b5b525616223b1a718673ede7f7d6`  
		Last Modified: Thu, 16 Apr 2026 00:42:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a98ca9fbf0f75bf48fbe8628c8f045edb85b44935c631ee451db0b7a63da58fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d977ddf6454ebae91728ba5e3e510d127ace98854a6cf9fd0b1898216c3c1a0e`

```dockerfile
```

-	Layers:
	-	`sha256:9ee0698aab20249df7866f6e2cfae17f036b8d38d331e2818c091d416836c07c`  
		Last Modified: Thu, 16 Apr 2026 00:42:31 GMT  
		Size: 2.4 MB (2363067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd91bb415454503ffd12a486ad7e995a5ffd5c464fc208ed5282ebabd6c26d2`  
		Last Modified: Thu, 16 Apr 2026 00:42:30 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
