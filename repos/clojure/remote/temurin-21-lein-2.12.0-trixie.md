## `clojure:temurin-21-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:7dae6ad271276fa9df4885e9cbff28a74aff4b46f7d88236518cd59f7398dee5
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

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:039bf00483113fd4ac72d602900994ef38533b503f21002f4113abf6a8d7937b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230213386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66597f9a7923fa7cb0eaa39aa366dcfcad33e833212ab2e68c4f355b65348524`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:12:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:12:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:12:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:12:40 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:12:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:12:40 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:12:57 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:12:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:12:57 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:12:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:12:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:12:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:12:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d371c6d0a2dc44823411141a6f09b982463a7e1ce00e9fcc4a401022ade4db1d`  
		Last Modified: Tue, 18 Nov 2025 09:03:32 GMT  
		Size: 157.8 MB (157826031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8eba051bebb7f7c772d96c7cc0ca9a80fd4e36a69663041c903279e23d685a`  
		Last Modified: Tue, 18 Nov 2025 06:13:29 GMT  
		Size: 18.6 MB (18579675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b4588985f99bf9d371f0e7c9ddb1bb437b299aa0131295bf837d153f5282e9`  
		Last Modified: Tue, 18 Nov 2025 06:13:25 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e3cdc09146077f1c8ee3d3766e5a00787759547696e5cd18c2d59f7350f3c0`  
		Last Modified: Tue, 18 Nov 2025 06:13:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c2b3b8d55ff9ea6684042ddebf3acd53991c01466797ab22cb7566fa023476f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0baaddcdc78abe2d08fb568d36ced662babb41c1fad24052c43bfe4d09c23900`

```dockerfile
```

-	Layers:
	-	`sha256:88b4788d953ff4d8dab7e85ef0c73a283bb7f9674be5e115ae0d674dc4cb9912`  
		Last Modified: Tue, 18 Nov 2025 07:45:15 GMT  
		Size: 3.8 MB (3816482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc4c6cea50bb3f37c32f8cbdc71dc2dd08c8d9e05c3147b3f118d439ecaaafe`  
		Last Modified: Tue, 18 Nov 2025 07:45:16 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1e69ca5a27b4feb6e8e7daeb05d61a0e6516dba794cb1120a68e4d88f4d7284d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228816720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07977655483c488b7699936612b959cf2ca2fb8a6727c451c92bf391978f29b9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:07:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:07:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:07:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:07:52 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:07:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:07:52 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:08:08 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:08:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:08:08 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:08:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:08:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:08:10 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:08:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e388ee6e90b1f6181c638403b326a3e32aae3fa0a69e81dc9f52d854b8fccb6`  
		Last Modified: Tue, 18 Nov 2025 05:08:31 GMT  
		Size: 156.1 MB (156107650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c543e6aa1be3300fe8c544defe1aa808eb96f1711fab541e999b1519f939cc`  
		Last Modified: Tue, 18 Nov 2025 05:08:37 GMT  
		Size: 18.5 MB (18540653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a7612890f6e2588ac5aaf384bd5524b9b58624b6dbe6d2082c56e521270e43`  
		Last Modified: Tue, 18 Nov 2025 05:08:36 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bad078c294fa202528e699430ec62f14d81d485aa302cfc39a0caf12e65abd`  
		Last Modified: Tue, 18 Nov 2025 05:08:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a944de306a6eea38848e3fe4c09cc24ee6e9fa6afc6cfa4b2058fe984e1f1ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdb8ed6e29aa956f4d61d437492c6c6274542151669341b55a3af358d6f4daf`

```dockerfile
```

-	Layers:
	-	`sha256:6d972fdb054a472676da0c271972e69d7e616190efba933fc739fc9b7b057b70`  
		Last Modified: Tue, 18 Nov 2025 07:45:20 GMT  
		Size: 3.8 MB (3817359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80020b52997c15d02eb78673896df06b819f4bb672ef4e9738e0cdf003fe7b6b`  
		Last Modified: Tue, 18 Nov 2025 07:45:21 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:17fbcb0853cd42b05da50fff506af9099703237378d8079e13d1ee4759200fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234206702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec5d7a505f79ce025d64ca62440ca24328f20c59a73c4532bc280106955df54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:34:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:34:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:34:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:34:28 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:34:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:34:29 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:35:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:35:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:35:20 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:35:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:35:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:35:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:35:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ae38687874ad4b2ca525fe856d3d2a658b265c8f3cd684d6e8c1efb9f28a6bb3`  
		Last Modified: Tue, 18 Nov 2025 01:57:18 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c7f6d790536283fa4178bfde3ea5f1b1cc9108e82e0ddd4085ecfe61c31b5b`  
		Last Modified: Tue, 18 Nov 2025 06:36:19 GMT  
		Size: 157.9 MB (157942949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd026024fc3afb577183808a78c0115b02ad1d95653376b456149e8a1d93249`  
		Last Modified: Tue, 18 Nov 2025 06:36:25 GMT  
		Size: 18.6 MB (18637108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b7048dc70a77bcc637bbcb0968b9380e9d3a45115aacee5c643388c3cbc120`  
		Last Modified: Tue, 18 Nov 2025 06:36:25 GMT  
		Size: 4.5 MB (4517732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac70a8c593acc6865698725248bd45e98fac8250d99c95f2bf5ac75f71425a6`  
		Last Modified: Tue, 18 Nov 2025 06:36:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:43f4c08cdeb021022c14eb174601c6aef359688405698d6d6776655af0aa0595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a796bbb9a50530d9d3aec4c357b1e42ea36305c140f04bf4940e4a899b7218f`

```dockerfile
```

-	Layers:
	-	`sha256:6bb5a51e796daca9c91b6aa298e9159978f80b20df216aedba8480a00952c636`  
		Last Modified: Tue, 18 Nov 2025 07:45:25 GMT  
		Size: 3.8 MB (3817480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca7c6a9eef42e794b71d391353e1aef757b13ad67c2f4f318bd3c923c820b5e6`  
		Last Modified: Tue, 18 Nov 2025 07:45:26 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:f4cb4a02b60304b8b228bebe8e8064c6a3a3bc5aae4c4d88f827877b5dc9d628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.2 MB (231165697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6c39b065c970b1688e84fedb97bdb7985f9f76ec1bdb5f81c696d55cbcd423`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Sat, 15 Nov 2025 21:38:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 15 Nov 2025 21:38:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 15 Nov 2025 21:38:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 21:38:54 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 15 Nov 2025 21:38:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 15 Nov 2025 21:38:54 GMT
WORKDIR /tmp
# Sat, 15 Nov 2025 21:40:27 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 15 Nov 2025 21:40:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 15 Nov 2025 21:40:27 GMT
ENV LEIN_ROOT=1
# Sat, 15 Nov 2025 21:40:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 15 Nov 2025 21:40:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 15 Nov 2025 21:40:43 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 15 Nov 2025 21:40:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe42759cef2146504be423e60ac7679f70f706af7aa21b4bb2ceea0eff9279b`  
		Last Modified: Sat, 15 Nov 2025 21:48:51 GMT  
		Size: 157.2 MB (157194310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9478dc3c39124c4e9906153315fa60cde5bb45acc444141a34bfe17c4014677b`  
		Last Modified: Sat, 15 Nov 2025 21:45:29 GMT  
		Size: 21.7 MB (21682242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac264842943366e11a7cc1775de2a84f3812c05655b0e477ec33702498297ba`  
		Last Modified: Sat, 15 Nov 2025 21:45:28 GMT  
		Size: 4.5 MB (4517790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c158d489173083212d6725d0d6bed7bab0167a740dc2e185af3152b6b3640375`  
		Last Modified: Sat, 15 Nov 2025 21:45:27 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:da7a0ec15ef4bd46062455f83978a3fb7e76114934210b53c827f38bc368d994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3825353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be9be1de86ba321d6291d3fdde8445172ca6a5cace514bb0c445660b69efb98`

```dockerfile
```

-	Layers:
	-	`sha256:ad60f2f539bf8dbd8dcfc4ff0f7f2b4c101a9a0f9fd17978a63fbef92927f9fe`  
		Last Modified: Sat, 15 Nov 2025 22:36:55 GMT  
		Size: 3.8 MB (3806957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac7333b2d00f3925c93df5136e3d650398da8beb355251eede25299668b58e62`  
		Last Modified: Sat, 15 Nov 2025 22:36:55 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:88ee42a74c812e96ba307fa4e06b9621572f4f56916fa329aeba23649013208a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219554649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de04c76dc9739240decb173c8dec67e376e8d305066c4f05b321580e05a9c5e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:29:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:29:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:29:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:29:15 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:29:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:29:15 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:29:29 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:29:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:29:29 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:29:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:29:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:29:31 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:29:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:af4c50a2cf2848edb9e1797defa12d9a203416cf14b67469a37a418b1d0bb175`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 49.3 MB (49346014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8a57fefe2d70f30d604267be848d56002a7ea2490463d77ec5cf62b33d73df`  
		Last Modified: Tue, 18 Nov 2025 05:30:00 GMT  
		Size: 147.1 MB (147069831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80557973dd8ee0f9638cadb998f51c4cc921c645125afae5c129e7a266f5ec6`  
		Last Modified: Tue, 18 Nov 2025 05:30:09 GMT  
		Size: 18.6 MB (18620623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f594903ee3b09f51c7c24f3d9c342a49a90ddd51ff62bb0104e738f3a5dcf282`  
		Last Modified: Tue, 18 Nov 2025 05:30:05 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c81e6f26edeb682a1098d34910343f813c53b3a0571146229fc7acd05b5a14`  
		Last Modified: Tue, 18 Nov 2025 05:30:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:12d0cf7f67c742f8437360c05e7f8f74f799f172467648ab74a196dfc24f5ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5742e3a750afdaf2ca16a59be553028f2d9595fc88f1ec0da262f7f2417ac6b`

```dockerfile
```

-	Layers:
	-	`sha256:5b6d451ae5435185d78cd6834e7ddd5abe070abe3c8d38abf97fb29ed6b8b29a`  
		Last Modified: Tue, 18 Nov 2025 07:45:33 GMT  
		Size: 3.8 MB (3812909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da582b270cb7c821e48386fd9380e86172630406dfc0bc849f263e6042bc3a1`  
		Last Modified: Tue, 18 Nov 2025 07:45:34 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
