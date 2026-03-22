## `clojure:temurin-21-lein-trixie-slim`

```console
$ docker pull clojure@sha256:794c9283d968ea6b23da789bf96cdee2f122d6fb02f3e0c79d6d0218385d9873
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

### `clojure:temurin-21-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7d14a837ce567d79ecddb3de40a2f66ab9221ad2cd61deeadff70aee317fca5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208598755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51048d1fbb63c2226a774ada249015b4508e0aaac8334df0077f2c5f56367907`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 02:59:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:24 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 02:59:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 02:59:24 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:59:40 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 02:59:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 02:59:40 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 02:59:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 02:59:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:59:41 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:59:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b01c302ead9d1c750ea4265a829c4c4a9a741709775864be42a0cba41205c90`  
		Last Modified: Tue, 17 Mar 2026 03:00:04 GMT  
		Size: 157.9 MB (157857092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8a1f4a5593241814976fabc912b7fe80855e9334d2edaadf2e5b551630630c`  
		Last Modified: Tue, 17 Mar 2026 02:59:59 GMT  
		Size: 16.4 MB (16448025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194406b26a2ffe36bf48110ae3dbec32939bf708041e741034ec1edecd09679f`  
		Last Modified: Tue, 17 Mar 2026 02:59:58 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4e258c6fad29aff285ad217ee2aa2e07fd815f20991906558c0a817fdab96`  
		Last Modified: Tue, 17 Mar 2026 02:59:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1057c268991fdf31e4b34a8d92617800e6033c7fa5823caabb9855aac734576f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdc8e90a03fad20722992b80a44c1777d91097be96f9c4427881083c3280429`

```dockerfile
```

-	Layers:
	-	`sha256:9bf4cd5782f8ad1b531b6ef88bd666f247f0e3ec4b5910c7e7ba65fc6c09e6bb`  
		Last Modified: Tue, 17 Mar 2026 02:59:58 GMT  
		Size: 2.4 MB (2366640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e46fda8fe14330d384cfc4d7636166391dc5f8ff5bf829da556795e7d4639cb`  
		Last Modified: Tue, 17 Mar 2026 02:59:58 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:40270c202ec0fae51f2a08c7cb3d4fd160074d3238ab39586ff7e77b210d8635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207203599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b004851966d0962231a0ae256f90b4e9fddd9d8dedde47d8564b248a6ec7940c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:04:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:04:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:04:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:04:29 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:04:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:04:29 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:04:45 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:04:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:04:45 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:04:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:04:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:04:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:04:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047a4aa49db7657c8894d706bf99568b4a9b1cd8e7c68cb7b7d39468e9c12d77`  
		Last Modified: Tue, 17 Mar 2026 03:05:08 GMT  
		Size: 156.1 MB (156133057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df4a4570603a7dfa68c26542e12f8a2d97438de1e4e596ecbc280f57af7f366`  
		Last Modified: Tue, 17 Mar 2026 03:05:05 GMT  
		Size: 16.4 MB (16413970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3394085506a88360c741bf4602e2c50d3bcee4ca1464e03105702453df2b27b9`  
		Last Modified: Tue, 17 Mar 2026 03:05:04 GMT  
		Size: 4.5 MB (4517727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb34194a940e9a4916310d7f4636aa8699c20453dfb406050562316099b8860`  
		Last Modified: Tue, 17 Mar 2026 03:05:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e4f17cab2dc47c95b9d7dd2dec75d8e80d9eaadc6c3d03e8a70197fc48210b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795a5a83edd5c4bb6de4ea8eba6d558733b58806d7d3d4771f0a013e9e02e83f`

```dockerfile
```

-	Layers:
	-	`sha256:815d83426e7802babfdfc41ff291c3720c87044f9b0de88bfce954130aa3f906`  
		Last Modified: Tue, 17 Mar 2026 03:05:04 GMT  
		Size: 2.4 MB (2366258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db4439b9b16e22160209653569d4632318b629e33b017c279b4fdcfe99289ce8`  
		Last Modified: Tue, 17 Mar 2026 03:05:04 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:696c2669cbb5ede58fa82a80be29aa193cc0301b98fb60a8a86a4367bc8dad26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212573900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3e84b795577ffeed3ef92dbc5af40be2bfe3dcac0cb736d89a46a4b2f6a03f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:37:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:37:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:37:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:37:33 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 18:37:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 18:37:33 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:38:13 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:38:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:38:13 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:38:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:38:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:38:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:38:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a3ec6fdaa48a78814b25d06b8958fec2609466001981f561b8114f6360e796`  
		Last Modified: Tue, 17 Mar 2026 18:39:04 GMT  
		Size: 158.0 MB (157977471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7951cff6f42d8a93b0e4660143a0764434e033c34d8517efc3a77596cfb0ef62`  
		Last Modified: Tue, 17 Mar 2026 18:39:01 GMT  
		Size: 16.5 MB (16485460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16ca3a0cb94a4e61f8fd14a89c0bffb21a25f739631ffe2430092de34f98e5c`  
		Last Modified: Tue, 17 Mar 2026 18:39:00 GMT  
		Size: 4.5 MB (4517706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12452ba8700f17f6120f574af6cc3bc9a5f657ae7bfc7e638b1f1273543b608b`  
		Last Modified: Tue, 17 Mar 2026 18:39:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3d8978e99045035a84b292225c8250b63000441d71ddaf21059b7aa6c1c40a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8dc0fe82560e7e1a3586e5a702e8b40782bf4f709180b98e3605cac2eb52af8`

```dockerfile
```

-	Layers:
	-	`sha256:5ceabaa56d9e795cdd10d28fabe900daa7fc740711e82b0d724807bd8d30e373`  
		Last Modified: Tue, 17 Mar 2026 18:39:00 GMT  
		Size: 2.4 MB (2367620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:406236764f38f639def5db0fd45e9196d3f4c39f3613da14d333f1facc30285b`  
		Last Modified: Tue, 17 Mar 2026 18:39:00 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:6b57a02ebb9d67d41647b98ba12912da9af5e2e55f486d20627a08de7e501601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206408824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dffb53b21e7317a55364d4b016ccd62889eec7bc0ad13eaf99353d323244d8e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Sun, 22 Mar 2026 18:55:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Mar 2026 18:55:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 22 Mar 2026 18:55:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Mar 2026 18:55:45 GMT
ENV LEIN_VERSION=2.12.0
# Sun, 22 Mar 2026 18:55:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sun, 22 Mar 2026 18:55:45 GMT
WORKDIR /tmp
# Sun, 22 Mar 2026 18:57:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sun, 22 Mar 2026 18:57:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sun, 22 Mar 2026 18:57:18 GMT
ENV LEIN_ROOT=1
# Sun, 22 Mar 2026 18:57:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sun, 22 Mar 2026 18:57:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 22 Mar 2026 18:57:34 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 22 Mar 2026 18:57:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0b5164900a4737bd8c71921f9d6095f2a9499d5081755c56a4aa46d8f37e9865`  
		Last Modified: Mon, 16 Mar 2026 22:10:41 GMT  
		Size: 28.3 MB (28275636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ee54184b00a8250bd83765fa0f3fb43da949588b64be8499761fc35178cc57`  
		Last Modified: Sun, 22 Mar 2026 19:01:53 GMT  
		Size: 157.2 MB (157216875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61a38861a9c94c2dd7d4df0e9eaa4cc0d2c6d67bed0177d70f98d4f4a19549c`  
		Last Modified: Sun, 22 Mar 2026 19:01:33 GMT  
		Size: 16.4 MB (16398108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d083f0cc0b9f1d22dcc01bbe332e984a4f36c2c847f577b10dfc6b326750936e`  
		Last Modified: Sun, 22 Mar 2026 19:01:29 GMT  
		Size: 4.5 MB (4517775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505b8fdbb5f2893ea10e5b44c3645d7a1e5a4c6357a4f19e80ed8d6b5630808c`  
		Last Modified: Sun, 22 Mar 2026 19:01:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9771e7be93948d0d2a8a679e371fb836faa8fc0c79267673731b507dcf348776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78de3e4b0cb8af97679bc938a693702b4ded3788f826f6edbeae63bfbbba4c31`

```dockerfile
```

-	Layers:
	-	`sha256:769a087541dd49cb75a42ca748e2ca449658d38a79fabbba9e732dc044601e11`  
		Last Modified: Sun, 22 Mar 2026 19:01:28 GMT  
		Size: 2.4 MB (2358688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d33722463c31260b62f6ebfd35b07b71183828aa7facc0cf1010091ac889fb17`  
		Last Modified: Sun, 22 Mar 2026 19:01:27 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:1725890133eefc75350848889e4f25bf7ebc8849f9381ceb59599a4ecaddc5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197942486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f52e212860e2c2322e630a9715019abec4c290810eacbe4f932b545313ca81e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 11:40:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:40:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:40:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:40:08 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 11:40:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 11:40:08 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:40:29 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 11:40:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 11:40:29 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 11:40:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 11:40:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:40:31 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:40:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd026936285793508add596e10e931d1e32392a546e973362cc8527ce291c92b`  
		Last Modified: Tue, 17 Mar 2026 11:41:09 GMT  
		Size: 147.1 MB (147105212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4fb47bcfb2ff1d51b6b640f2ce1cba0546a929bcf364bb18cbbd450ae85bb9`  
		Last Modified: Tue, 17 Mar 2026 11:41:06 GMT  
		Size: 16.5 MB (16483826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7752ce91d5d753801acad22029035ec7e9d96104ba8dd767bf6f4ce7957c15dd`  
		Last Modified: Tue, 17 Mar 2026 11:41:06 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1a6d498d62c1fba52ec2f1bb73d38fb0e382d58405f10cb9430c7a755c6962`  
		Last Modified: Tue, 17 Mar 2026 11:41:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e9c0756a4df66d85c66b80b24981db0240156bdfb42d343c2b96c8860f65d7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7b6c83900abf87cb697b9dc00bb74ecf4e20a76c8c90169847a45c5ab0cd32`

```dockerfile
```

-	Layers:
	-	`sha256:07701a7f85de8296d964f308beb2c0dc257e77b7bb1f5caec7bc06e4ff77c1dd`  
		Last Modified: Tue, 17 Mar 2026 11:41:05 GMT  
		Size: 2.4 MB (2363067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc02513991c88ef3fe9df239f2e5360cf8448710127508967b29a69dfdae2243`  
		Last Modified: Tue, 17 Mar 2026 11:41:05 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
