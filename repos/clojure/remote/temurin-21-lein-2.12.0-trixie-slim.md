## `clojure:temurin-21-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:b29aae1a374150e882b152e409855c0bc738da0f248bd97000966c1f9ded5639
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
$ docker pull clojure@sha256:504cef575fb57e9b3392f11efbf977da48a478b62d93bd4a0e9bfbc2b12700a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208565070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23be8c6d7a836c6b95d31d41b50955cfbb39c865e8ca044727cc4cea2d0f522c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:35:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:35:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:35:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:35:11 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:35:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:35:11 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:35:28 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:35:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:35:28 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:35:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:35:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:35:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:35:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d583676ee2894dad7a9afde419d6a4b09a062ae13ed46a3fc862bce43ae3f029`  
		Last Modified: Tue, 13 Jan 2026 08:29:02 GMT  
		Size: 157.8 MB (157825959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a4cfe803e7b8ef3ab5f05924e57e4e5fad6325f5b939b364c4a7078276dda3`  
		Last Modified: Tue, 13 Jan 2026 03:35:58 GMT  
		Size: 16.4 MB (16447245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72e2704945397b34d5fa3ea4a65bdd20c6001a1fa4e3b5d5b8f78034c8d6b23`  
		Last Modified: Tue, 13 Jan 2026 03:35:57 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729f8f97945d260b125004e852d5dd4fded6e85e3932f5f2890b3e3a46e318be`  
		Last Modified: Tue, 13 Jan 2026 03:35:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e0512881b82ec86351f8350f3b4e01558cbd3923460d6506438d7ebe09745bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82bafdb05492391c718a004fbe8107449bcd92153006d8f53bcae96d1a702e5`

```dockerfile
```

-	Layers:
	-	`sha256:8f638686150a61a44843fb23e28e79539ba199c4e79bf8ad123ce96d1c1dbe18`  
		Last Modified: Tue, 13 Jan 2026 07:43:49 GMT  
		Size: 2.4 MB (2366602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96344a012d72c99074bdac3fd79c257110758321b40a4740d0fe32f9b74d04b0`  
		Last Modified: Tue, 13 Jan 2026 07:43:50 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:21193d67792bd0d7b81240727cc6a60f865f546f38a2eef97af26ea97cd5ee2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207173770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a3371130c4e2903b0f18ac1630d0e9f6d66a37532fccd78ad6880649461ed8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:38:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:38:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:38:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:38:50 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:38:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:38:50 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:39:06 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:39:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:39:06 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:39:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:39:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:39:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:39:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710930c01fef01b123f86c8e8294381895c415902f25f0b4afbcb9bfc005761f`  
		Last Modified: Tue, 13 Jan 2026 21:09:39 GMT  
		Size: 156.1 MB (156107637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeeda62ae6c6280ad4854a14232774ae17369de944ecc6d61184b8707edc791`  
		Last Modified: Tue, 13 Jan 2026 03:39:40 GMT  
		Size: 16.4 MB (16413920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0193381129499b987212bb71f4d2821c31486bdc14dc0e3612bc8e40b07bee51`  
		Last Modified: Tue, 13 Jan 2026 03:39:37 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5360a09f390c5fef13d78ffbc8e1b8982d497eac0f1956b85621177aa6d63f9c`  
		Last Modified: Tue, 13 Jan 2026 03:39:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:69e4e9452fb53cbe493baeda6fcb7e8b0bfb0b6bcfda35d10ecf6f11ecb912a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9efc4ff73c7c39afee72a4168ea79faf4add2c8640bfe11de2b1a4b3a557162`

```dockerfile
```

-	Layers:
	-	`sha256:4e68c6f347e61843630b5646e3d353d3aad6eb30fd88a9c4a3ebc46bd16b9da6`  
		Last Modified: Tue, 13 Jan 2026 07:43:54 GMT  
		Size: 2.4 MB (2366220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6bdccc5215356e5d4cd8b28c40c044cd8589fe356a8689342c72432d5e67848`  
		Last Modified: Tue, 13 Jan 2026 07:43:55 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a290b37d2ed179392b1584573ae109fc76fcaf254fd73b27e8a91162afff14ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212542192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74098d967410cb39e1f0bf0d14d0252aec59b2410b668855298ca77cddb27b99`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 05:47:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 05:47:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 05:47:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:47:27 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 05:47:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 05:47:28 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 05:48:15 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 05:48:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 05:48:15 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 05:48:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 05:48:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 05:48:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 05:48:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58a834387b09bddb874696b527c7ae70b8166b6d2486c2a53584c23551b3001`  
		Last Modified: Tue, 13 Jan 2026 05:49:08 GMT  
		Size: 157.9 MB (157942939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f79a082dc72a335068c431a38c2219c4671749c9741523b58c43372a8ad57b`  
		Last Modified: Tue, 13 Jan 2026 05:49:15 GMT  
		Size: 16.5 MB (16485460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b027517cbf609096a6f7f47c5657bb3efebc47e42e555da85a36a7bee7ab4a3`  
		Last Modified: Tue, 13 Jan 2026 05:49:15 GMT  
		Size: 4.5 MB (4517764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b83c44b30d43d688d7d0738dad07b70985c2c8b3342c8d009a2cc6395933d5`  
		Last Modified: Tue, 13 Jan 2026 05:49:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:16e5b7d21d84512f2eabe3f8209f6e9b39a0325c086cc2e6d110bca3f6e479a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8f0f1606fca17844a0f15321de167cc3883067c37b0bd9c65fb0ef6d13db33`

```dockerfile
```

-	Layers:
	-	`sha256:3537ebd990c02c28056a1c4db8300bf45c876ae1b9f9aae5d1dd952f5d67d27c`  
		Last Modified: Tue, 13 Jan 2026 07:43:59 GMT  
		Size: 2.4 MB (2367582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fa0d8496c0bce0b45c6502880c892e60e4a001a2f1e4079635bff0815fce2b2`  
		Last Modified: Tue, 13 Jan 2026 07:44:00 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:2803d46f2bfa472966b2222fca5f8599ce3a66a31d949afef5e1b38b04d3d371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206383512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdca38adfa0107b29164d2fef99e1dae3c5faf99c70b1dbded43829216ba08b8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 07:02:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 07:02:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 07:02:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 07:02:49 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 01 Jan 2026 07:02:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Jan 2026 07:02:50 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 07:04:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 01 Jan 2026 07:04:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Jan 2026 07:04:18 GMT
ENV LEIN_ROOT=1
# Thu, 01 Jan 2026 07:04:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 01 Jan 2026 07:04:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 07:04:35 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 07:04:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091162d898a2d4e7b50f7bb9588aeb36e7979c2a93097ad0bdcd2473aa01fb84`  
		Last Modified: Thu, 01 Jan 2026 07:08:57 GMT  
		Size: 157.2 MB (157194291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8287ad8a14910988816ff3b67e28645e2d2b3201648b8cccccf52952ed27b9a3`  
		Last Modified: Thu, 01 Jan 2026 07:09:08 GMT  
		Size: 16.4 MB (16397852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4680422d3a15eed5753c613e8f36f58302302a629757877840cfc3f14d8e63`  
		Last Modified: Thu, 01 Jan 2026 07:09:05 GMT  
		Size: 4.5 MB (4517811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b76f537afe0360d541b762c58c1909c154fa78a592ddae382498a59fbf912b`  
		Last Modified: Thu, 01 Jan 2026 07:09:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:38209183e8f547417d164a415860204f5227dbedf3aff30991f0fed0bae1cc0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec04403c029e300b2394b030e5a176cd3209e400e8552327380c4e3be81d7187`

```dockerfile
```

-	Layers:
	-	`sha256:dd3f659dd3a821814abbc6cbc57a56b364bef2e8ce3d4c73fe41dae4b75d8bd3`  
		Last Modified: Thu, 01 Jan 2026 10:36:42 GMT  
		Size: 2.4 MB (2358588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:706fd3a476b4e1a72ab3151d52bda6113c29b85602039a09b959cb7948f9f9bd`  
		Last Modified: Thu, 01 Jan 2026 10:36:42 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b1643c6bc99d011709cc667b54b11055aa00ce37fc5f8a50b373dc8221db1f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197904530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c8b43039a61baa16bbbc18d9a814fa0fe8e8525d06bf8277326ef0bbd6fc05`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 15:37:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 15:37:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 15:37:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 15:37:40 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 15:37:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 15:37:40 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 15:37:52 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 15:37:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 15:37:52 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 15:37:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 15:37:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 15:37:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 15:37:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7592af43bff998b173c1ca21b4043a1892061f2ffd627ae263a939a00f54de1`  
		Last Modified: Tue, 13 Jan 2026 15:38:57 GMT  
		Size: 147.1 MB (147069840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf0115c7ca1ce020b654d057b7c16eb3a916ae54ccf35eb648b65e7cf66e829`  
		Last Modified: Tue, 13 Jan 2026 15:38:28 GMT  
		Size: 16.5 MB (16483098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92aace0cdce4cce7f2a0c632435a846293babaab4f25fa76fc68570172543c5d`  
		Last Modified: Tue, 13 Jan 2026 15:38:27 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbf1a07663f025e6f47945f4599115f208c13395650864be8996fba4c93e863`  
		Last Modified: Tue, 13 Jan 2026 15:38:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:637957681f24da9cf739c52fcb140c27aa27ebedf3e4bb9425ca17eef1170466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19f29c9bcc410e83ae3fbb35e382c9ec9bfecc3df55ab61507c7d25bc7c781e`

```dockerfile
```

-	Layers:
	-	`sha256:2e91b0df9facf1aac2cce9ef02a8ace7e6ed4ff658e62739e2c1718afabb0d22`  
		Last Modified: Tue, 13 Jan 2026 16:36:52 GMT  
		Size: 2.4 MB (2363029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd7631811887855329aa7e52ec65963800e2aad6011434bcd5c1585797a765c6`  
		Last Modified: Tue, 13 Jan 2026 16:36:53 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
