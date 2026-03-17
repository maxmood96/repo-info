## `clojure:temurin-25-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:117d04b7d430aa29066f9f4e720e40b11ad332e9e5938294fab4811ea8076552
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9792faf4ba5e2c10de5383dddfc4a78190fffe7873899b1c42282f36b80971b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167166528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d89cae471fcc5a96ad0707b5ff571c7a50ca4908781440a209a12041f99db75`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:00:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:00:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:00:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:00:37 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:00:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:00:37 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:00:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:00:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:00:53 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:00:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:00:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:00:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:00:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e759575b5b0029fea51256b7ad3afa90c8ff1a6a9457787359c2b05b4a964edd`  
		Last Modified: Mon, 16 Mar 2026 21:52:53 GMT  
		Size: 53.8 MB (53762481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5284fe4fa97bb3474a90b93e59a0655a06e11d244767364fb7a7fd0f23093489`  
		Last Modified: Tue, 17 Mar 2026 03:01:21 GMT  
		Size: 92.3 MB (92256314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db8c6fc45e96d5af9e26a86a90ad5c098425d38b616b7181c3719f7b38c897c`  
		Last Modified: Tue, 17 Mar 2026 03:01:19 GMT  
		Size: 16.6 MB (16629554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbbfa599e8ad99ece3174e9e8645156aa9707ab6dc624796e8dc6fa1cd902ed`  
		Last Modified: Tue, 17 Mar 2026 03:01:19 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17861f2137bcc84cd573a9572c64d7f56063fa189c07a0ddc29cdccd874d31d0`  
		Last Modified: Tue, 17 Mar 2026 03:01:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3e552052eec883201fc487e3129d1f89d79ec3743907049b745d90ae94f7c5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4472905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18288cca2515c1e2454e6afb4fd87b408941e67d51b0d8d59594e4c3b4a3544`

```dockerfile
```

-	Layers:
	-	`sha256:cdbb3d25863ed33b258c0ebf3223fea32ad48862e01a8e63bfc8b5712f48cb03`  
		Last Modified: Tue, 17 Mar 2026 03:01:19 GMT  
		Size: 4.5 MB (4453902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71b8de56be3d8913123d8f3f14198d82bb9be5610eafd69066475c4f88661869`  
		Last Modified: Tue, 17 Mar 2026 03:01:18 GMT  
		Size: 19.0 KB (19003 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bd3ea561deeaac0b344a2d93798ef14ffd26b00ae99a97574e4d9d5f80f64fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164670181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7182164aedd48906ce75f8d2850fcda6675e71c60dfadb360e52d78f545378c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:05:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:05:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:05:18 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:05:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:05:18 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:05:34 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:05:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:05:34 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:05:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:05:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:05:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:05:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:da8e260297fdb91b3f012b26dd982feb43d0bf977ff8adeb7a850ef9c5829770`  
		Last Modified: Mon, 16 Mar 2026 21:52:51 GMT  
		Size: 52.2 MB (52247254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25aa2efafed304bea1776c3a7671e08441223b1ec5fcde3c9b46e89eb6fd5ade`  
		Last Modified: Tue, 17 Mar 2026 03:05:56 GMT  
		Size: 91.3 MB (91288272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2ea0fb7f3f074ef2a9c0ace6ea8b10967018dddcaa6f59434531e79923a016`  
		Last Modified: Tue, 17 Mar 2026 03:05:55 GMT  
		Size: 16.6 MB (16616512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a6f5cda5a8100fad857857bc4575eaed81ec570085632286752acc64e02e7a`  
		Last Modified: Tue, 17 Mar 2026 03:05:54 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aff47484330ab968aadd5a200561f236cb7b3d46c74abd275833b0e26441521`  
		Last Modified: Tue, 17 Mar 2026 03:05:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5ebac91f308316b7c9588b36f0ef626b961c65a8db757c56692887df256e4f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4472045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7781b5d42507286f29438cf4e10567b66c0da6135a26d70116f6cfc7bdd8312`

```dockerfile
```

-	Layers:
	-	`sha256:9cf9810640dcf3165276d8dca41e918ac94855f7af746e2355ffad95a0657af6`  
		Last Modified: Tue, 17 Mar 2026 03:05:54 GMT  
		Size: 4.5 MB (4452897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee66d31173d9807a3b4a8df6751b8fa13ee24d00c216b8db571b9be867b47766`  
		Last Modified: Tue, 17 Mar 2026 03:05:54 GMT  
		Size: 19.1 KB (19148 bytes)  
		MIME: application/vnd.in-toto+json
