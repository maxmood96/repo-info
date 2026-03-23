## `clojure:temurin-17-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:d1a57f16c30cc2e030d2635e3a23ba3a3b414fe8c426bac9b8f03a46e97f4150
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

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9623333e82bd891341cc3942d3aeeecf57b8d3256fe1e67abaccf5ed38b09068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196370212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519db326a77b6e35628b425af9c33bc2c7fa22461a5e8e49898edf6ac59d1575`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 02:58:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:58:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:58:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:58:12 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 02:58:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 02:58:12 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:58:29 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 02:58:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 02:58:29 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 02:58:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 02:58:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:58:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:58:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93936a066753616fb653f771ff4fb99af22eca13854e6c96cb53ebfdf9e554f3`  
		Last Modified: Tue, 17 Mar 2026 02:58:49 GMT  
		Size: 145.6 MB (145628510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a164b1a7310cb5efc92daf51aed0d26e1ee9a0f3dfc392f709992cf44597ec6`  
		Last Modified: Tue, 17 Mar 2026 02:58:46 GMT  
		Size: 16.4 MB (16448025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4d78dd95f7d3ea3e87487fa129c28a59edf1caaaaa718358da8d34299433ee`  
		Last Modified: Tue, 17 Mar 2026 02:58:45 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6932a8ebef9de3c5a3d0cf01ee76f4916fa660ff0dbc08b2fd58f4f39230cac`  
		Last Modified: Tue, 17 Mar 2026 02:58:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a4cc5e34cd5ae5a2ec22ce2ec00cb324d34a915ae6ae473e77ea6a291dcc1160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1022688e5c83d84e58f512e198601694f53e251aa67f99c0403084db7a15f46`

```dockerfile
```

-	Layers:
	-	`sha256:ed9f38dd83ec43d38cd0ed1b8c919c20ae5bab5ac7467434aa87df490887a59f`  
		Last Modified: Tue, 17 Mar 2026 02:58:45 GMT  
		Size: 2.4 MB (2364788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46bb4d33a2d94747b642e05bdc22a5877d84456333fb4c3f7ee7b9432726ecd2`  
		Last Modified: Tue, 17 Mar 2026 02:58:45 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b67ab32388d44f0d283675b393d2b3949c36d8161c7557c49dc9e6660990fee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195506773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3b8f13d2b5073800ea2cc755f42ee14b529a9d48fe5c16b2bd91ba2eac8491`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:03:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:03:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:03:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:03:05 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:03:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:03:05 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:03:23 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:03:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:03:23 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:03:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:03:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:03:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:03:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e623a1cf1d27d6230b52c544efb51346b826f7b02d5e0296b7b649f5158c39`  
		Last Modified: Tue, 17 Mar 2026 03:03:46 GMT  
		Size: 144.4 MB (144436241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70873f79c45527f9e9bf9518c74363b4a300a1ba3281deb4529c233351649a2`  
		Last Modified: Tue, 17 Mar 2026 03:03:44 GMT  
		Size: 16.4 MB (16413983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fff8124a93dc20063f947229f1b6885c6666482c861749b9bbc416316c4ccc8`  
		Last Modified: Tue, 17 Mar 2026 03:03:43 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0eda00e4e783d02f8fc34becae4d2fd2f675d5840cb94b9ee3ad4eb7cfd7071`  
		Last Modified: Tue, 17 Mar 2026 03:03:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6bc80fbb42e31f580481b1b04ddc668148da4ed98b5a2ea5426bc82d5b5a4386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2446ee8d331b4b2e29161f7ef3f9e767d75c1c6c0e919a36d7581e2a8938e70`

```dockerfile
```

-	Layers:
	-	`sha256:9ab0d014f05de3b35d3fc7fb2ea7a2cbeb4cc78f54fc8363c3568709b0f678a5`  
		Last Modified: Tue, 17 Mar 2026 03:03:43 GMT  
		Size: 2.4 MB (2364406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad143cb07c7002df6ab4503e3aa199828dcba990ff5d35297748a5101e0f1688`  
		Last Modified: Tue, 17 Mar 2026 03:03:43 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a4010814ded7742c695c82d981dabc4c26b0ab031951c7dd95629741168ca834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.0 MB (200034682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e1666a1cf0118b591893d7c236a00a1f6535eaaf784f8fc233f733750189b8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:27:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:27:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:27:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:27:35 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 18:27:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 18:27:35 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:28:15 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:28:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:28:15 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:28:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:28:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:28:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:28:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822c66d457280a71230ad4487fd70323ef90d3d8e95b8850297f2bd84ecbef19`  
		Last Modified: Tue, 17 Mar 2026 18:29:06 GMT  
		Size: 145.4 MB (145438236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33a7afd6028e3a8314ca7b2ff714db0478cf3430b619aade53b78a126b1221e`  
		Last Modified: Tue, 17 Mar 2026 18:29:02 GMT  
		Size: 16.5 MB (16485457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7f37f26783d7fc6129e54053e2bfe2969de777377ef7210c61ed75ba669638`  
		Last Modified: Tue, 17 Mar 2026 18:29:02 GMT  
		Size: 4.5 MB (4517726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f4254bad334e79eb192038353cb1e8ae0848f28f08f871bf4f039ffea274fb`  
		Last Modified: Tue, 17 Mar 2026 18:29:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6fa6b2d23bc2de3f9fcc9186a546174751e65262cb4987992a2a603e2b4f37bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77aadec8f6bb32c374f8b7da1e7af757a12e04805be921e9b0d1dd5c5aa9723`

```dockerfile
```

-	Layers:
	-	`sha256:798848ce22934d0ac646173c83aa30c970953c734a74412c0ba8209165a9acd8`  
		Last Modified: Tue, 17 Mar 2026 18:29:01 GMT  
		Size: 2.4 MB (2365768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5961ad06c11087076468885328eb1f7ecf41faeaaa917fad42a9556faf73e103`  
		Last Modified: Tue, 17 Mar 2026 18:29:01 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:2416d8c5cf40a7aad0a03caadbaa32cfc4111679c968f31eda7d2d9780ccab9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191854845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b487e9e9f351d9da8d95c781a6311500bc06b71599ade5665435ece10e9f8381`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Sun, 22 Mar 2026 18:36:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Mar 2026 18:36:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 22 Mar 2026 18:36:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Mar 2026 18:36:25 GMT
ENV LEIN_VERSION=2.12.0
# Sun, 22 Mar 2026 18:36:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sun, 22 Mar 2026 18:36:25 GMT
WORKDIR /tmp
# Mon, 23 Mar 2026 03:25:39 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 23 Mar 2026 03:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 23 Mar 2026 03:25:39 GMT
ENV LEIN_ROOT=1
# Mon, 23 Mar 2026 03:25:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 23 Mar 2026 03:25:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 23 Mar 2026 03:25:55 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 23 Mar 2026 03:25:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0b5164900a4737bd8c71921f9d6095f2a9499d5081755c56a4aa46d8f37e9865`  
		Last Modified: Mon, 16 Mar 2026 22:10:41 GMT  
		Size: 28.3 MB (28275636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc59ab8223d6223d60aa7ae5a907145f2fb35e6994bbb8454d7fb04c39041b0`  
		Last Modified: Sun, 22 Mar 2026 18:44:02 GMT  
		Size: 142.7 MB (142662945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cab77b5bfc8474ebfdcfe971054d428434b9f82b1af64749790d6ec46d2bd38`  
		Last Modified: Mon, 23 Mar 2026 03:27:55 GMT  
		Size: 16.4 MB (16398046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb333e2cb825a389a21cf118d7a1ff80545967b8b24cdc0e85f96f86f4f695f`  
		Last Modified: Mon, 23 Mar 2026 03:27:53 GMT  
		Size: 4.5 MB (4517789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0706f7a2ec4f5c05e15364d815208e32c0982adee0b110fc783147f19692b9a`  
		Last Modified: Mon, 23 Mar 2026 03:27:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:03669ad8a60565819be5f3583af5c8ea29127155f6918742ec60e27a8d9d6ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6929be7c2286782783d2d9e853d37daccae3be9dee29be955661baff95b26cd9`

```dockerfile
```

-	Layers:
	-	`sha256:17d9c6be846bd7a8dac474b2778c1a3889f8ad5ca5f82e9247e90802214ffbf2`  
		Last Modified: Mon, 23 Mar 2026 03:27:52 GMT  
		Size: 2.4 MB (2354917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeda7168290eccd0170f92e254d3851e6463208999137246df723d7b72902e5e`  
		Last Modified: Mon, 23 Mar 2026 03:27:52 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:5a29ec1df5054de6d7b590fcb10c4cb77067f0b94cd2864e3b8624b374a30a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186464250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e672011543a45606795ba8d1b136bb8da3e159113ece3a22162a131390118a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 11:35:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:35:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:35:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:35:31 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 11:35:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 11:35:31 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:36:06 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 11:36:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 11:36:06 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 11:36:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 11:36:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:36:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:36:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e279b6c9da89319bfeb452be1320b3e797c3fb77fd2b092fee70646718ebcdd7`  
		Last Modified: Tue, 17 Mar 2026 11:36:47 GMT  
		Size: 135.6 MB (135626828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42142f968f347f39595fa6c0f89b2df4620061193a52b87426afd79a70b62aaf`  
		Last Modified: Tue, 17 Mar 2026 11:36:44 GMT  
		Size: 16.5 MB (16483970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46874a75f23f330374ce94d3ee9553b69964a70cd26bea0824f4779f3632e129`  
		Last Modified: Tue, 17 Mar 2026 11:36:44 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27247db9dc97cf9d96ddaa646fa75fdec9035703ed8a6237ac6df21740200c6`  
		Last Modified: Tue, 17 Mar 2026 11:36:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9e3ee742cfb1683458c6673826926d3aad8314ec0dc5f58e0326d574349bf481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d568466e6e21510934e5f7b2d95d65a01ae6cb3b00e7a049469e0cdb7270b09d`

```dockerfile
```

-	Layers:
	-	`sha256:0524934ab59def5ef2fe3cd5a066231be93638171e5719efcb3306cedb1084d2`  
		Last Modified: Tue, 17 Mar 2026 11:36:43 GMT  
		Size: 2.4 MB (2361215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f641dd2a85887bf7eb7ae447f9685886d157622d24aabde42e1fa599d0e7d2c`  
		Last Modified: Tue, 17 Mar 2026 11:36:42 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
