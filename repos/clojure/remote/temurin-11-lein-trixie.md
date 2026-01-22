## `clojure:temurin-11-lein-trixie`

```console
$ docker pull clojure@sha256:8b47cada217fb52355261946955aeb20b0aec5879889d8b3f31b323a15aafd3f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:133dcb6070fa80bfe6843dbdb5eebbdb7343a4c4ddbe08d3ffd42696b95d8652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217349780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c0555130f274499104a5f37c46be68591d412d0de603cd562d903b73aa37e5`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 01:47:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:47:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:47:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:47:46 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:47:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:47:46 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:48:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:48:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:48:03 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:48:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:48:05 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228463410826e2bede81246fb401b9b9cd78dcb7c47df56f5eb47714d278e82e`  
		Last Modified: Fri, 16 Jan 2026 01:48:25 GMT  
		Size: 145.0 MB (144966647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964268bfda997365af9b430efa8c6f4731499f13159ab0390ae7a77ce67851e9`  
		Last Modified: Fri, 16 Jan 2026 01:48:22 GMT  
		Size: 18.6 MB (18579741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c788d9ac7ccf1b56fb0cb7c7c3f20286e2cc2f39a70c8f788c8acecb6653b8a`  
		Last Modified: Fri, 16 Jan 2026 01:48:21 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1ae83880d698fe5d5b1bcdc7e7fdf20ee77521bfc859ea8f86c3a8845738d51b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0147b18d6e54a7825aee2358837b93a42cd8791f4fd2ad5398407b98ffb927d1`

```dockerfile
```

-	Layers:
	-	`sha256:d36298d21ffe197fbcea8b63bd97082481b4fb31241642ee79772d886f7b74f8`  
		Last Modified: Fri, 16 Jan 2026 01:48:21 GMT  
		Size: 3.8 MB (3834378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37bf568e18bd41a4faec63e039f937e0ae48f4216d10e0065913c0ae017f3760`  
		Last Modified: Fri, 16 Jan 2026 01:48:21 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f3bc902cc07e03f926d0ab57a64e3255e9841668a957f030673c1d3ea0d58cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214436505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f145f20b27ccac0a52927e1ce43f2efcad8ea5257d990617e6fcf2d376cf776`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 01:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:51:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:51:38 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:51:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:51:38 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:51:54 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:51:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:51:54 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:51:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:51:56 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee176b161fa2fb69d62466e5b597523041faf78620e4a334b47b60bbd28e8b29`  
		Last Modified: Fri, 16 Jan 2026 01:52:16 GMT  
		Size: 141.7 MB (141729881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ed7227331c3b1b066781c8f9396f21a913441905e866fe8bb43c06998239b2`  
		Last Modified: Fri, 16 Jan 2026 01:52:13 GMT  
		Size: 18.5 MB (18540751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ef90ba1359e4ca90491275feacefc96dcc14de1dd113eed723d44946c88ac6`  
		Last Modified: Fri, 16 Jan 2026 01:52:13 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3c9f6397f84a6002790e6a6f353cd2f6877886a1370a6068c423fd1507c5739c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31aae2ee216ce0aad09f566769e89e3317aa2bb2c7ab9cf64f3309f94caf05e0`

```dockerfile
```

-	Layers:
	-	`sha256:a07bfac19ec92c9f1a7e27ffb0dd0a21bc9a7ff9a350e28039c1974af869f272`  
		Last Modified: Fri, 16 Jan 2026 01:52:13 GMT  
		Size: 3.8 MB (3835873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9cdc1da2cf50842b42522fce5b2b02a0eec8800d1270dc0f10905e33bd691b3`  
		Last Modified: Fri, 16 Jan 2026 01:52:12 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:f1d19853c9b005492168da9d17f1b854943a24b874e9bebadff766cc99a1ba87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208341769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37bfab8260edba01c19c636a815b7340fe376a67ddae1f882e50fee24e4dcc6c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:01:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:01:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:01:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:01:56 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 03:01:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 03:01:58 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:02:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 03:02:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 03:02:52 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 03:02:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:02:55 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535e69c188d843a40931640c882aeab8cb565638d03ecacffc478c1a783da983`  
		Last Modified: Fri, 16 Jan 2026 03:03:52 GMT  
		Size: 132.1 MB (132079785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c447425ff0a1d69069ff6cff29101b3443ed740e1c7fae4a5c2f93e7bc9238`  
		Last Modified: Fri, 16 Jan 2026 03:03:48 GMT  
		Size: 18.6 MB (18637244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ac5540439fe76318562e3107066691ed7b5d98365904e808500d7c5cde0770`  
		Last Modified: Fri, 16 Jan 2026 03:03:47 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6409831dcdbd7f0b691d71163ad5bd3b5a3af2ac51eea67d5c451f3ca02b97aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3851171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16724bdeee44b6e141c4c76e90ae82d1af7e8918691fa487179701611cb79a62`

```dockerfile
```

-	Layers:
	-	`sha256:a03885eb0240dd67b21c9845701754f1dbf29f9a76a2e54afe1bca9ace144c89`  
		Last Modified: Fri, 16 Jan 2026 03:03:47 GMT  
		Size: 3.8 MB (3834763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95ac0298bae67c1a7d35dbf73484c2e3c836e67b107826b9a6766af26fdad9bb`  
		Last Modified: Fri, 16 Jan 2026 03:03:46 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:42e5c99d326e3e945be2b6c4db1d55e80f8d026a84a214b3afb292169711392a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198182012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aca03f81a1b1ff36cd49710d39cf54e8d4123fba2e975e2c2ee33562dcaea99`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:10:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:10:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:10:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:10:51 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:10:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:10:51 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:11:10 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 15 Jan 2026 23:11:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Jan 2026 23:11:10 GMT
ENV LEIN_ROOT=1
# Thu, 15 Jan 2026 23:11:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 15 Jan 2026 23:11:12 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:46 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96aae73d6ca9c475bb213977dcd29121719a295968930d64b57e8491e3a1f0e1`  
		Last Modified: Thu, 15 Jan 2026 23:11:36 GMT  
		Size: 125.7 MB (125694843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9bae4406cf2439c57383f0423b7a7b5b3a60b43e463d6c99b7c434d6b024f1`  
		Last Modified: Thu, 15 Jan 2026 23:11:34 GMT  
		Size: 18.6 MB (18620683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca46c915fa4e3898b3d680c3931e3db4362d6f619eb657fef1057d678c2be94`  
		Last Modified: Thu, 15 Jan 2026 23:11:34 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ebabaf913605460119b175cde36703ffbfed515f97ed6550d2fdfafef52410d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3847172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a6d7a936dcbcb523ed7da6acd9b9ef6487540a9bd7b3085ebcc0aab94502ba`

```dockerfile
```

-	Layers:
	-	`sha256:caf7f93c7ebef48ef91d22e1b134e543a8a32f591edc5c42109e1dab5b67b118`  
		Last Modified: Thu, 15 Jan 2026 23:11:34 GMT  
		Size: 3.8 MB (3830809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcc3f8b576fe6ed079dbe14b1e91ffc8b7579b4f42188500609e10eaddd508c4`  
		Last Modified: Thu, 15 Jan 2026 23:11:34 GMT  
		Size: 16.4 KB (16363 bytes)  
		MIME: application/vnd.in-toto+json
