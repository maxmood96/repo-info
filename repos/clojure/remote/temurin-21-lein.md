## `clojure:temurin-21-lein`

```console
$ docker pull clojure@sha256:88b21a5cffbf0aa11c34fe88bd374c82143384c046f9550421fcedd233256632
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

### `clojure:temurin-21-lein` - linux; amd64

```console
$ docker pull clojure@sha256:df4c1a66d9dcdfdc92f66a1a7e2d97e0a6a633719ceda5ddd4ba26f0bba65dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230603436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2cf15847265dc47c1327f501607e5eed5ea431d7f8e674f7d5a9d6d5c55889`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e13b90a4183690662b9a1e90e5e43dbc5c45caa27c7d8233f38be4ee410f23`  
		Last Modified: Sat, 13 Sep 2025 01:01:48 GMT  
		Size: 157.8 MB (157804809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea96b5f5f027759418e9f0f9d28ee0b232b736adaea81320d615bbf5ab4d82e7`  
		Last Modified: Sat, 13 Sep 2025 00:03:53 GMT  
		Size: 19.8 MB (19799883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c6f7852e452f7b07fb39630ef13c10f6e00adf5960a01c67ce6c9226d55980`  
		Last Modified: Sat, 13 Sep 2025 00:03:53 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7194b9654db202a20a3a7ea9593b2d467e7a85807725000f0b6569351da2e620`  
		Last Modified: Sat, 13 Sep 2025 00:03:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:c9f5afc07a2d4eba5e404ddd7ac23dc961e5e1842e046716518f821590ae7fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca7c7cb6d24c42adb03f75577921b067bec20d92498403799494574eb5dba9b`

```dockerfile
```

-	Layers:
	-	`sha256:171276f5448370b640186ab7a1ac9e164c8942d45fc2e302dd4d7842475dcb17`  
		Last Modified: Sat, 13 Sep 2025 00:34:37 GMT  
		Size: 4.3 MB (4284834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b6a5866cbad79342aafb839bd11ebc6dd4f5c9650791262ceb821f9418f47c7`  
		Last Modified: Sat, 13 Sep 2025 00:34:38 GMT  
		Size: 20.3 KB (20309 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b339f18375f58ba1bd6e10e0ee9a42c23d8d37b3b16fadeb263f9820c11f1c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228586924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb261b6306f573ba14bbf0572231666246e8c7f4c4d8d0494fbb1a8bbe76262`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6f204523fbc7726f928608b78ac85a020e5505d04416f292aa0eb0f32e56b6`  
		Last Modified: Sat, 13 Sep 2025 04:03:06 GMT  
		Size: 156.1 MB (156081190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a41c99d5ec5d247e0a5bb64a67a9b07afac100596bd5b7858b6be13d39f28d`  
		Last Modified: Sat, 13 Sep 2025 00:16:29 GMT  
		Size: 19.6 MB (19628583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ae4572c3d4d382c5fea4501ef630a47686b29f7176bce3128a39dde6319d4f`  
		Last Modified: Sat, 13 Sep 2025 00:16:27 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f8dc26fb7ab04e19b6f272c24f8fbdfefe7f2202692315a581b1d5242b9a8d`  
		Last Modified: Sat, 13 Sep 2025 00:16:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:7e9b2de4597334f9a00935f5b3685f14f0dc23c14b33a1beff20e97b308d576b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cff5533aca0f2077d464c125313b6e77916ec2e85a124984ea974899565b11`

```dockerfile
```

-	Layers:
	-	`sha256:986487a913452dab54d50a5c19be07db52185c6f9fae00d35bc2e1a1708f1859`  
		Last Modified: Sat, 13 Sep 2025 03:34:29 GMT  
		Size: 4.3 MB (4284521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1ccc50c532e2fbf84f4fd947d72a139ed4cf82c1a3e2d4d1ff73eba99104094`  
		Last Modified: Sat, 13 Sep 2025 03:34:30 GMT  
		Size: 20.5 KB (20502 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein` - linux; ppc64le

```console
$ docker pull clojure@sha256:53e017a545166f3a76f743b9e8acc831c41a1b361ef10ff400bc56cb8d7967f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234827464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3104acc19c1a37feb1e64cde189546b09cf60aae9ea0b083052b3aa20a80df81`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b2ca9ff1a3fccb012f6c51a9f097c6995575e5e55d69deb7d54ac91943ca62`  
		Last Modified: Tue, 09 Sep 2025 09:35:24 GMT  
		Size: 158.0 MB (157963479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d44049f2345d5fc93f110ec14e393e02b339e7a221e9a738b65aa22b6a45da1`  
		Last Modified: Sat, 13 Sep 2025 03:20:03 GMT  
		Size: 20.0 MB (20018975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81df610ae69f6502d6e4f4c380c98b4454a30094ed96dae7d931c73782283d51`  
		Last Modified: Sat, 13 Sep 2025 03:19:30 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac14d0c15422d0fe65f3980b9ef3f6ed873af77f5c3d1ecc4ff351765ab8968`  
		Last Modified: Sat, 13 Sep 2025 03:41:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:b0fc85440f5b4896fcf14ccfe5cb73f64ac777d46e4edb7a386e66bc0474861d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4307118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885a4206e21a3a2252722e013991b3d2119d1b85e1702ff13e869bd2b942de18`

```dockerfile
```

-	Layers:
	-	`sha256:4a9cc344a4884026be9e3d12d3cb6e9e72b647662dfffaa1da4de7f5996047b5`  
		Last Modified: Sat, 13 Sep 2025 06:34:32 GMT  
		Size: 4.3 MB (4286729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c980357010d18fad7fe8bf7fc851c9d80fc9976be8df65c4f3273da07d0e9ac3`  
		Last Modified: Sat, 13 Sep 2025 06:34:33 GMT  
		Size: 20.4 KB (20389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein` - linux; s390x

```console
$ docker pull clojure@sha256:a2d74dd10bb780e7118c85b47bcfa8d8dd460b7e5eedaf35bb172f7da056f2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218141559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a41ca016dc6e49ff746a3db63ae5c93ba4b78a081a11e0b3e6faa3c15742075`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84772536e34edd89b294c09dbe86293a053e24f7d3644f8bc0e4612df16f4795`  
		Last Modified: Tue, 09 Sep 2025 07:01:48 GMT  
		Size: 147.0 MB (147027040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ab2b8177ec9b51a4840afef0d7c5f2194f79b9121a2956bc3d8f590416e0c2`  
		Last Modified: Sat, 13 Sep 2025 03:00:28 GMT  
		Size: 19.5 MB (19458801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f3f1ee53736cb6161ffc9beef70dabc78f8b2f54fb095d2eb1949845fe22c0`  
		Last Modified: Sat, 13 Sep 2025 03:00:27 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf067097f3b4b77b80c9761ee3f24bb74b4c51e3144c30d3ebe6d8acf88423d2`  
		Last Modified: Sat, 13 Sep 2025 03:12:35 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:499ba66ae65e95aed000c429cade248c458e1fdf431a1ad9d6fe026c023105f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4296957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546c2eeaf6ca1839196ef08224c3d537ca7deceb7fa35aa347826a9ff5101bec`

```dockerfile
```

-	Layers:
	-	`sha256:a688f80177641fa0595ae1f922c9acb7823c20343dbce144521126b27b6cb556`  
		Last Modified: Sat, 13 Sep 2025 06:34:36 GMT  
		Size: 4.3 MB (4276648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3a0064f7f50ed703b762a3f320efe9d52bf82c57ed1160cdb28347a3e85a380`  
		Last Modified: Sat, 13 Sep 2025 06:34:37 GMT  
		Size: 20.3 KB (20309 bytes)  
		MIME: application/vnd.in-toto+json
