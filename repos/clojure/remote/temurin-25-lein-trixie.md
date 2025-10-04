## `clojure:temurin-25-lein-trixie`

```console
$ docker pull clojure@sha256:181144f9dcb8bb095f69663db1945dd179beda6a9f13dbb600cacc0caaca1969
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

### `clojure:temurin-25-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:9f8312dc622d3fda1dbcda7427367fb5de8495e39c5f88cee2165f2048683645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167383082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764c0c96012cb33c6b52c65daa3020245b991ffc051436405d42163dcf39258c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113e990b36da608061711e7597ab27a1eaaa3a8ea326bb027f5928cd4e87f99f`  
		Last Modified: Thu, 02 Oct 2025 09:01:16 GMT  
		Size: 92.0 MB (92036038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78025a52bf2c7328c0cc3ca6d23936d8f99a1ebf867aa5b3d73c173a74f302a`  
		Last Modified: Thu, 02 Oct 2025 09:01:17 GMT  
		Size: 21.5 MB (21544239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f836773a29bcc93a3eda88cef088d6e26bfebdbe0b40ee0531d6c7a1294fc12`  
		Last Modified: Thu, 02 Oct 2025 09:01:12 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1c7a2f0145561603bf8ee9065714c8bfd20db7cfb1510982ab5d04ba5d253b`  
		Last Modified: Thu, 02 Oct 2025 10:49:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b372923e8b203f2fcd58e14f9419e73a3a9f2caeab7aab8404994de5229fcec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46f719d9875ff9aeb5d5bc5977eafac658fc098db1a9d3470e5e889a00cf280`

```dockerfile
```

-	Layers:
	-	`sha256:d82baf028307f42b7c8b2ca49b2f359c1174f5511f0f9b4bc2d704fd8ddedce9`  
		Last Modified: Thu, 02 Oct 2025 12:35:04 GMT  
		Size: 3.8 MB (3764668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c29e1abda2419e03207175129490c674d728a0bfe9ed4c5a3977117eb706a99`  
		Last Modified: Thu, 02 Oct 2025 12:35:05 GMT  
		Size: 19.0 KB (19022 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4f90936709510de90cb88f9789b13b74a856fad823284750bf103bd5d0c2b79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167088375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94c502bc16c0627c7cd61b4be09a9133de68ea95bff09932fd7e5e57895077f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cea2cd7d6abd3430f4569e5c97650c3955c6bda01a06c24b0eb7dd1ffec69f`  
		Last Modified: Thu, 02 Oct 2025 02:47:13 GMT  
		Size: 91.0 MB (91045273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff520791c307c281db0ce2cf4ddffb05754ee15eab55bf6ffc327f1ebbca302`  
		Last Modified: Thu, 02 Oct 2025 02:47:05 GMT  
		Size: 21.9 MB (21876233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f781b92d94ae53cffe0149c799c62bb4b7313216ca97b7948bda0b7d06b728`  
		Last Modified: Thu, 02 Oct 2025 02:47:04 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4c5d06f5a353ed7412167ddc4f6b25c7fcd44e8af1251320ed206e7ef2b22d`  
		Last Modified: Thu, 02 Oct 2025 02:47:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e854660f0b6077bc5bfc0814d48bc61e15737ca1e66adb7bc5b2bef970171113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4255fe43310b189c75d6adb6eb7ace1faf62cd58941a741f4ea9459ae2bfe02`

```dockerfile
```

-	Layers:
	-	`sha256:19a6ce9cc8075f512cb6c491c27612c183a607b33b04fc7bcebad3d3fb406667`  
		Last Modified: Thu, 02 Oct 2025 06:35:11 GMT  
		Size: 3.8 MB (3765566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ce4a3c030f6ecf703e0879c0d5e8996be6b25016604de3018f5e74beb3ccf0`  
		Last Modified: Thu, 02 Oct 2025 06:35:11 GMT  
		Size: 19.2 KB (19167 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:cd929c6f5e3fd9fc6fee7ba3238c09dbf994378adbf98baa79bca76604f0b4a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171075629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a058fb5993dacaf679fe85200084d7ad319b7f82e4e840e268e4862fd0ff71a0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26068084d5c0d18ceb5891b6fd4231786726d8ad744810400957e5a91ddb77fc`  
		Last Modified: Thu, 02 Oct 2025 20:36:58 GMT  
		Size: 91.6 MB (91601758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f427b0a099717c359d0ec0a4788cd9edc0294649d6b3a3da5f0a13ccdea536`  
		Last Modified: Thu, 02 Oct 2025 09:35:24 GMT  
		Size: 21.8 MB (21846515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39798fa7c74cfff406131f6e98f65b181a1f7bdeb03eb47481d19d6c98ab60f8`  
		Last Modified: Fri, 03 Oct 2025 15:18:37 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4ddef5057dd0c8eaaf8fee636096a952a039a109293e28b871472af8e79aef`  
		Last Modified: Thu, 02 Oct 2025 10:31:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:43be90076d00bb24a393f81d21332f052c15f1ac7eacfe21a750fbe69cd570b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39129b6c0cb776418071dc059cb143803a9c57c1ecaa23ea8efde2e91357543d`

```dockerfile
```

-	Layers:
	-	`sha256:ace4a82541aa16e832df38f2b14dd5d93f860f1a419ac7bf74e44d69fac76c69`  
		Last Modified: Thu, 02 Oct 2025 12:35:12 GMT  
		Size: 3.8 MB (3766976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc0fdd207e00a5ae1749b057b5d001d579c7863c7890b82fb4aea63fea04277c`  
		Last Modified: Thu, 02 Oct 2025 12:35:13 GMT  
		Size: 19.1 KB (19078 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:75ca81029d5c9dfdb338215c8c4e5ec318415883439d477b281cbbb4588f69fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164190651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ea82df4885d83032b8be2adca071cba56ad64226da856b2f0f9106a33ed249`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:913254a25f5e448a50a1e74fa50f037e22f85cfe4d6a3c626f4b7405299b7c1b`  
		Last Modified: Tue, 30 Sep 2025 01:03:38 GMT  
		Size: 47.8 MB (47770009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964f0570909b5b1168e8db033d13313402e740c877ecfa3fc939ead46e3f0584`  
		Last Modified: Sat, 04 Oct 2025 15:08:07 GMT  
		Size: 90.8 MB (90752390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385bc980073baa5cbdbbf4e0c6567f1091e3115986e976a25c423ce49ebd7d26`  
		Last Modified: Sat, 04 Oct 2025 15:08:00 GMT  
		Size: 21.2 MB (21150051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313fb0b0984d84de0d8fbbe25a3561f9fa7aa15565789fb7e7d4bf50e1f97030`  
		Last Modified: Sat, 04 Oct 2025 15:08:01 GMT  
		Size: 4.5 MB (4517772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190a10c1f3c254097280382a454d9037c924fd6e23c25d8adb2ec1fc2b343652`  
		Last Modified: Sat, 04 Oct 2025 15:07:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b134aa4914175629fff8e3d610a3f35f9d65d4a7b9a7f0173ff606bfe71d5996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4e93c89aeb9d207d06f4df6ed9e0de65bb76f3f2b22568a7e862f3056b2167`

```dockerfile
```

-	Layers:
	-	`sha256:7b42c3774f911970ae98b00604a1cc9d3ed39fbfeefe029dec0c2bac320ed42d`  
		Last Modified: Sat, 04 Oct 2025 15:34:35 GMT  
		Size: 3.8 MB (3755152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc6f9f07c68382143713a9a6adee032e85f9aaea780757aa018ac75351f117dd`  
		Last Modified: Sat, 04 Oct 2025 15:34:36 GMT  
		Size: 19.1 KB (19077 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:4a89af0c95b2483752b301f8f44b5ac160e9bb64c57588b9e7f4ff095de16f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163307521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3928632374ef80d5fec8e33911a252525fb19d79607588eff0563b68cd6bb8bc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:024d6c344f0b9dbb2baf07e95dfd2abbfadc5c8262ca381f39f6489670cbaff5`  
		Last Modified: Mon, 29 Sep 2025 23:41:06 GMT  
		Size: 49.4 MB (49351442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daa2639a0298f6857127b224fd64cd213fa2e6d60da8408ea6f993388788a1b`  
		Last Modified: Thu, 02 Oct 2025 04:57:03 GMT  
		Size: 88.2 MB (88206443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6831bb4ca4f62d1b4a37a9b5a3a7fa37c4b2d100b907b051d7c1667b99522a`  
		Last Modified: Thu, 02 Oct 2025 04:57:00 GMT  
		Size: 21.2 MB (21231448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56809fecb39751c24f94cb25eaa519a8e741d07e10706514dbaf6905909f56d5`  
		Last Modified: Thu, 02 Oct 2025 04:56:55 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdace7b8d568cf2c47d6be4675ddf121ccc2c0dd64ae4082ec5ae9ab13d4a8`  
		Last Modified: Thu, 02 Oct 2025 04:56:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b9176d3736c6612c9199f7cdb69649ded1f9ddc89885088458490455026c91e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3782664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff507eccc9b9e04b464a996bfc79f1e6598a8ee7d553b71aac4f72e878f50cf`

```dockerfile
```

-	Layers:
	-	`sha256:d0a1a230c2bc36572341d9a9659572bf5c444434008e55d54e43b8ff3cef4549`  
		Last Modified: Thu, 02 Oct 2025 06:35:21 GMT  
		Size: 3.8 MB (3763643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc65d8a886ccf97788845cc92b588cc9a0ca0661bfaf0d585e8dec396bb4a785`  
		Last Modified: Thu, 02 Oct 2025 06:35:22 GMT  
		Size: 19.0 KB (19021 bytes)  
		MIME: application/vnd.in-toto+json
