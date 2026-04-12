## `clojure:temurin-21-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:0a142c0f9cc71aee649c5226bd3b84e42f189bc070768c5e9bd38d40f2473bf6
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
$ docker pull clojure@sha256:c7e39b0df0ae044ac2bb6eb2251465002faaece12eaafcbc3d01d771ef4dce74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208598927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a679d67d5ca9ead47e784c4c9ce853cc3c87c2e361363d6615fa271f4705c1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:57:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 02:57:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 02:57:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:57:59 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 02:57:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:15:52 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:16:09 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:16:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:16:09 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:16:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:16:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:16:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:16:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4905befd0b435d073e97888696f8eed85871988758a17f818cd43af9647c0963`  
		Last Modified: Tue, 07 Apr 2026 02:58:48 GMT  
		Size: 157.9 MB (157857048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a5cf5790470163f40e2201ed542275413f9ddbea026c82766459509819e1c6`  
		Last Modified: Tue, 07 Apr 2026 03:16:22 GMT  
		Size: 16.4 MB (16448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfb66fc0f9defaafc1de3dbaa4afb6b962e036ca72a1d12412d7a0447944754`  
		Last Modified: Tue, 07 Apr 2026 03:16:21 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db6bdaf4ca21e440cd9e5e483c97020bc1b2b74719f6033cf8287ba478e14cc`  
		Last Modified: Tue, 07 Apr 2026 03:16:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a1e290b26a39638f99667ff444c4198061f9522baf0d54bea3ac3333fe7e0442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6414d3b2b07e0a4f2706212e839c786b4d39865966f72b0ce9038bdbddef26d`

```dockerfile
```

-	Layers:
	-	`sha256:cd53fc387a4a8b6265d7c9c0cd998ec04847f80c4036a4e563454cce4ab53617`  
		Last Modified: Tue, 07 Apr 2026 03:16:21 GMT  
		Size: 2.4 MB (2366640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acf764edb88e729ac7f9a7e233ef41b6659d202927de3ebf1f8288d2a7827963`  
		Last Modified: Tue, 07 Apr 2026 03:16:21 GMT  
		Size: 17.6 KB (17586 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3f9832d3eb520608823dfc8f76e7022f1c2ca0716c24c1b6391f0d05dff1d69b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207203800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16376fad2ebd9d513a047bfea0b63ed5a1d48fd3c630050bf7478d6a86acaf7d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:26:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:26:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:26:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:26:33 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:26:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:26:33 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:26:51 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:26:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:26:51 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:26:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:26:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:26:53 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:26:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c1c3a34ef57280cf5c0e533c81d90c0e60f26075860ec24985d325b0935a93`  
		Last Modified: Tue, 07 Apr 2026 03:27:14 GMT  
		Size: 156.1 MB (156133064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffab16460e3f0c6a31e7405f015da37dac45a7cb45b08236ae0ced1e5ac7e5ce`  
		Last Modified: Tue, 07 Apr 2026 03:27:11 GMT  
		Size: 16.4 MB (16414022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a9497d66abbc363cd6ca46c78df4aae40c5e3e05291bd0b419e38b6433117f`  
		Last Modified: Tue, 07 Apr 2026 03:27:10 GMT  
		Size: 4.5 MB (4517735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cf9b5b5212dc5ba9164ebff04afeb0fbd9861f90e343e4999bea136fc4e6b5`  
		Last Modified: Tue, 07 Apr 2026 03:27:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:26b3542a678de761d678a8ed1d170f7c014efbbf19a550bda863fb1d0d430b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b8fcf1298203acf5316d8f97fb984c536d6ab672a950c5307c4977e06d83bf`

```dockerfile
```

-	Layers:
	-	`sha256:6301ead9cc9282132205dfdc4c3d2ac37f941cb148a638f6cea5aee8997ea412`  
		Last Modified: Tue, 07 Apr 2026 03:27:10 GMT  
		Size: 2.4 MB (2366258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:471d69e13f3b5e8a11e9ee66cc20217f83bed933c80ab3e99c36ae8e181bf045`  
		Last Modified: Tue, 07 Apr 2026 03:27:10 GMT  
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
$ docker pull clojure@sha256:66e434bc29abd1be484026834c25005ba9e01a1a42da4b8f75a08c7993e7addb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197942719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cdb9e2ff8dd7b86ef0f37aef79cfbb814345e692c213f2797dc16fbdd20e8f5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:44:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:44:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:44:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:44:54 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:44:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:44:54 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:45:08 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:45:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:45:08 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:45:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:45:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:45:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:45:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64db56f7965b765f0e39653c084418dd2902ad80e13793882547069cfd06d5d`  
		Last Modified: Tue, 07 Apr 2026 05:45:37 GMT  
		Size: 147.1 MB (147105311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b81e2e836a59b1aa0dc5a762eb042c2ff463064b75f79bc5ff448f3cfa7db5`  
		Last Modified: Tue, 07 Apr 2026 05:45:36 GMT  
		Size: 16.5 MB (16483850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74c26d70e5dbea0b5f132eb60aed1b11ff34d5aa0d0507b6cd7f2c97faf4234`  
		Last Modified: Tue, 07 Apr 2026 05:45:36 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a022423da6fcc3e1e2eb6d044405b0dfe799b83ad0bf00f3f229f4e3e31884`  
		Last Modified: Tue, 07 Apr 2026 05:45:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:923d7a5ec4dd8037252e576167b1ec11483904a2e9eb26eca9d2448c25abc621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf551944ffa8e312dd9763cc3df34df14e7fd274431d8a3db300b323d63c5efc`

```dockerfile
```

-	Layers:
	-	`sha256:00fe141e70b3e5d82b8316e32045e001451ae6d6b40eb969e13af9c3284e6761`  
		Last Modified: Tue, 07 Apr 2026 05:45:36 GMT  
		Size: 2.4 MB (2363067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88a4a061202ecf4c8b9b21492e6685983d23ff333baebf6d5f73e4223d51cf9f`  
		Last Modified: Tue, 07 Apr 2026 05:45:36 GMT  
		Size: 18.4 KB (18386 bytes)  
		MIME: application/vnd.in-toto+json
