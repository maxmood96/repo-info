## `clojure:temurin-11-lein-trixie`

```console
$ docker pull clojure@sha256:7fe5a2fc22bf24867715a66203b4d6a428f88137bc973176f01576a19c70195e
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
$ docker pull clojure@sha256:be80db91fb998ac1226494d134e19dbb18dad57270e0db00eaea24b11dd2e7b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218197636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e36291c92c7634066ee020bf72b3ba307fbdef74fe323469cea5912d69cd955`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:53:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:53:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:53:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:53:41 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:53:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:53:41 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:53:58 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:53:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:53:58 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:53:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:53:59 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aaa94620f19c680d9b585e4e1c25f5d8685057bce47d4b9176ccb4a92d6ebf4`  
		Last Modified: Tue, 24 Feb 2026 19:54:22 GMT  
		Size: 145.8 MB (145806748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b7300492294e6b4e526512c062e0374e6356912cb29cedf1a0bb06be08ee0b`  
		Last Modified: Tue, 24 Feb 2026 19:54:18 GMT  
		Size: 18.6 MB (18580027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f45a2f270b52e1bc6c678862e3b33a57683174375a2e64865d1283ffa25137f`  
		Last Modified: Tue, 24 Feb 2026 19:54:18 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:250dc37f15ab3ddfdc8042986fc5f3df8d754ed743fda71813946b06d3c7695b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3851996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c798474a753979c0f6acfaf198b5776582d9768698db18f1f49927797933d8`

```dockerfile
```

-	Layers:
	-	`sha256:41b7f8b568678dd9040a173851e762603f9377fe3ee1939843688a8b8ffd2fd5`  
		Last Modified: Tue, 24 Feb 2026 19:54:18 GMT  
		Size: 3.8 MB (3835632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d691869c119f3c22bea4c7a62cb9675f5f7d28877fb8571bf95081a92ee1a044`  
		Last Modified: Tue, 24 Feb 2026 19:54:17 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f841b6fef4a8e4097ebf1fb46ab24487cf01316a1795d83165ce01f01f40aa8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.2 MB (215212744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6ccf6dd3c2b0564b05620ca612294b36b934a9211bf8d16e869a6f0e81ae7d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:04:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:04:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:04:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:04:26 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:04:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:04:26 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:04:42 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:04:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:04:42 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:04:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:04:44 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8906215ffa0f509e4a3a93a064f24454da830af7c160fe8bba2904b053a4184d`  
		Last Modified: Tue, 24 Feb 2026 20:05:04 GMT  
		Size: 142.5 MB (142501415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b2ce36c08f5a8014c17c9938b9cec100f92d74ffa836b35b4f94ca6845b9af`  
		Last Modified: Tue, 24 Feb 2026 20:05:02 GMT  
		Size: 18.5 MB (18541410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecac825aadc2fcda73b2a1e0fe856f682c5941fd55d9487aecd88592173680b`  
		Last Modified: Tue, 24 Feb 2026 20:05:01 GMT  
		Size: 4.5 MB (4517719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:92b9857b3d0abd5bfdbb7661609114414250a9592bd69e28dce08a53f3d10b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7cd183750dfd3b5a23aa2a6d7a948f0436d8400dada385cc185dce2c3c0447`

```dockerfile
```

-	Layers:
	-	`sha256:72fa429197d65d70297fb390be72d460987064ccf3502cdd093ded143717e8d4`  
		Last Modified: Tue, 24 Feb 2026 20:05:01 GMT  
		Size: 3.8 MB (3837127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4882beb4b75d1918aa76b734ff3781d13c4b699bb0f73220fcd27c6c62f19e6e`  
		Last Modified: Tue, 24 Feb 2026 20:05:01 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:5559a63d07c6c4fc5a9833fa77c3dce98526142b183dab8d0b8d99638d93f23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.3 MB (209265442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf0fb920ccb7c0bbf2db274e4beef114de56a75604c3ec6de5c29f05f9dc1f0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 01:50:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:50:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:50:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:50:51 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 01:50:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 01:50:52 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:51:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 01:51:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 01:51:52 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 01:51:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 01:51:56 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd587e6f98d18981b1fa39b879e07792b8b34045978a1c4c5b8a1982d2ae24e7`  
		Last Modified: Wed, 25 Feb 2026 01:52:39 GMT  
		Size: 133.0 MB (132997811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eeae89419bda9d4065ade61895cffc8935cf4d7c520c2f6252996f0150d533b`  
		Last Modified: Wed, 25 Feb 2026 01:52:36 GMT  
		Size: 18.6 MB (18637576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f336c8753f8a591d0e3ccf1d8fb211aea4db0ae9797dfa0648f9393c46bb7e`  
		Last Modified: Wed, 25 Feb 2026 01:52:36 GMT  
		Size: 4.5 MB (4517762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:40f73dc67b2d787357fc2faf5de86ca75dc35316898fdb14b1b737d9169000f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d28a15770147302baa200a9119cf508328ada6177b332e609e74fdf3960e3d`

```dockerfile
```

-	Layers:
	-	`sha256:2461f497f73eb554757ee9d5dc974a84f8aadd85bbd4a1d01ebbb8bff56c75d4`  
		Last Modified: Wed, 25 Feb 2026 01:52:36 GMT  
		Size: 3.8 MB (3836017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cad10bb33535c8cf949a7edaf59176b2ff1b40fa32aa5282738b38f66248522`  
		Last Modified: Wed, 25 Feb 2026 01:52:35 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:ec248f352fdb1b3b17eab7d75b5057c613bc08331ff919c6719d03a857802c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199055436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f229b50a7baedf12fe9aad6ef4654e9cf9c4a42eab483c953d4f0a17fff1f9e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:12:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:12:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:12:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:12:58 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:12:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:12:58 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:14:02 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:14:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:14:02 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:14:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:14:05 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf3ca8078f9a8ff06106e2ddc819bac030792db65741aa1c31b6c84c638804f`  
		Last Modified: Tue, 24 Feb 2026 23:14:35 GMT  
		Size: 126.6 MB (126562017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94986e899e765aca4ad65f2e12811988ad9171752b28ea1b04a36e132994f5d`  
		Last Modified: Tue, 24 Feb 2026 23:14:33 GMT  
		Size: 18.6 MB (18621126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2283c15c5a05ed7f2b26f7c8843b9964955dc7bd291e708411dd827ba3a30a2a`  
		Last Modified: Tue, 24 Feb 2026 23:14:32 GMT  
		Size: 4.5 MB (4517727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3f3e1fbbaaf327e9e9dbe91f8a042c041d3f2f0e2f0e7f84dac9c26a9ccb8a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3848426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b1b45dae9ea78a7d5d02f661c4bcedaaeb628054ee764f5006f5307ed24408`

```dockerfile
```

-	Layers:
	-	`sha256:a0e21ca6afd968290e029f3ce9b9cda30e2106add0b8e5b4ac7ca94d402a1093`  
		Last Modified: Tue, 24 Feb 2026 23:14:32 GMT  
		Size: 3.8 MB (3832063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffe410b9fc0b04ee2ef8d67f406ac2a4b790cd88583f5ae9d0c8ebb3ddc6f78a`  
		Last Modified: Tue, 24 Feb 2026 23:14:32 GMT  
		Size: 16.4 KB (16363 bytes)  
		MIME: application/vnd.in-toto+json
