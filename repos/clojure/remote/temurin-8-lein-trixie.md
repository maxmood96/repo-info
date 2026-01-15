## `clojure:temurin-8-lein-trixie`

```console
$ docker pull clojure@sha256:c935f4f80ac891915d380de3781113ff1423ad156fe0900c9d5c28215100d518
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:cab1acef3630c7b094012193d7ec25247c6880e10e3e439bc03ea96c1aa5e2a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127116409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dc82b76985eaaa673a0622e256b0a47b7df0d4e7c65170868a80d755ad88c0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:19:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:19:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:19:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:19:52 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:19:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:19:52 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:20:10 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:20:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:20:10 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:20:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:20:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1721f2d0732ab6fc7ba8df5470a7e37eac137d92735b8bd682c2d1a0e94081f9`  
		Last Modified: Tue, 13 Jan 2026 03:20:37 GMT  
		Size: 54.7 MB (54733370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24c1a73d41d402383787d089ef5d17e342aebe1b7ddfa4e2d90dc8edaee9a48`  
		Last Modified: Tue, 13 Jan 2026 03:20:34 GMT  
		Size: 18.6 MB (18579682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426495eab649c8873a8a7cf9c167b08ae5b85d5680856bdec9385d8a564a215a`  
		Last Modified: Tue, 13 Jan 2026 03:20:32 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1ec62c9d8a6aa166c0670bebf90877a0488e6ae7fd949cde1f6ff971f8c90c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfc80d2faa962dd37d352fdb877f13283c3d84a287cf658403d92a80dc3899f`

```dockerfile
```

-	Layers:
	-	`sha256:0e7342fa2d18f4baadf5bbfc5b5e4fad50141700afeb4d8343083057af4c7bdd`  
		Last Modified: Tue, 13 Jan 2026 07:48:42 GMT  
		Size: 3.9 MB (3935849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:620f275035a3dec4c750330358cb425c99c2988ecd688cfd52d103e379436729`  
		Last Modified: Tue, 13 Jan 2026 07:48:42 GMT  
		Size: 16.4 KB (16352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bd150bb719cdc6a65d2c3093060b08896739b694c77c4f971f9d017b86e0d217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126521517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0764abfa5d2a20e544ed320861607e588cd8447637ee07e302fde637603e77a3`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:28:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:28:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:28:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:28:14 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:28:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:28:14 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:28:30 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:28:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:28:30 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:28:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:28:32 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5480ba41e3bcfb93e424f39a4c17f892847d2e9ebd790a09ce51b8ec2ece28`  
		Last Modified: Tue, 13 Jan 2026 03:28:57 GMT  
		Size: 53.8 MB (53814999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1935b6f9e502e3b3c61602fb5541e3f8315ceb2af12ca3a1cca206fcbf965d6c`  
		Last Modified: Tue, 13 Jan 2026 03:28:54 GMT  
		Size: 18.5 MB (18540676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0115e8e9bfbbb60a8b58e797641bcd1d5b8215be7145a38dff4714936442d48d`  
		Last Modified: Tue, 13 Jan 2026 03:28:53 GMT  
		Size: 4.5 MB (4517727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a498427c7607d6f4603b081ff51abd743f136db99d315a07a954ef9a837b183d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd54f32e31b40a64631c7b9184da16cdd70489ca9cee97c7808a622661e793c1`

```dockerfile
```

-	Layers:
	-	`sha256:58a41082301ba2b9357ed1310770622a64e9a08a3e3ac76e89dc6fb1bf326f0f`  
		Last Modified: Tue, 13 Jan 2026 07:48:47 GMT  
		Size: 3.9 MB (3937424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e63ae223eec22583714f81ab92adeff8f64fd1d08c0438c80194e6b97eb6d65`  
		Last Modified: Tue, 13 Jan 2026 07:48:47 GMT  
		Size: 16.5 KB (16473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:07c357ba1e63674d91eb7d1c60be99209a12339b7a525bf17065442c4dc04801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128437110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294292a2bafb5ea73ab74a14b56195bfbfe40c3f12c2a7f5ca1f8f9982b5bc7c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 12:14:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 12:14:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 12:14:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 12:14:11 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 12:14:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 12:14:13 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 12:15:09 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 12:15:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 12:15:09 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 12:15:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 12:15:15 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:58 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a202991c9fc912af0fae06ba1526b88510b4fa61eb11725151ed1a5d4ec93ffa`  
		Last Modified: Tue, 13 Jan 2026 12:16:09 GMT  
		Size: 52.2 MB (52175138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c8123ced91eb80cbb86c5b06233afd33a56ed5b0d998f8d242b5ba132aa267`  
		Last Modified: Tue, 13 Jan 2026 12:16:06 GMT  
		Size: 18.6 MB (18637225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77030a01a1eae86694d5eb15d845930128ab63709219a8d54bed52c9db25906`  
		Last Modified: Tue, 13 Jan 2026 12:16:04 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:06c00dcce63c70a3cc23a1bb0f9d046691f74dec051d4cfc0e9d74fa2eb4144d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed7d5b441e627deeb9db04b2d1444024c8896a387237f7ac1f890aa4a3e69e6`

```dockerfile
```

-	Layers:
	-	`sha256:e904396f55b5d48abf584aa379a8027af5e0913f5afeb6c474373148f8f592b4`  
		Last Modified: Tue, 13 Jan 2026 12:15:53 GMT  
		Size: 3.9 MB (3937442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d3abd6b8a9801499294d31e5bc6024a98b00a55059853b5569475bc138b1b60`  
		Last Modified: Tue, 13 Jan 2026 13:38:06 GMT  
		Size: 16.4 KB (16396 bytes)  
		MIME: application/vnd.in-toto+json
