## `clojure:temurin-25-lein-bookworm`

```console
$ docker pull clojure@sha256:6894ccbbacaae0b54d1bfa90351f589e6e8dfe0f8f16215fdc80e1f409a088d1
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

### `clojure:temurin-25-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d24e74046ed363ecdd92f00ad767fd7ddbd31caa158d44f0517d98184325fbc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164847452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7e33470c8425b8935ac72b44f2d252cc26db0811c8ef1bc052ea2a41430016`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:40:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:40:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:40:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:40:26 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:40:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:40:26 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:40:39 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:40:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:40:39 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:40:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:45:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a36ea574d1796a3f2007b7ea49e3f47e0d9c29d1afdbacf3f64dfbf8ceba51`  
		Last Modified: Sat, 08 Nov 2025 18:41:52 GMT  
		Size: 92.0 MB (92045291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91866dfa0b5da5fed947b46d471b6ff81d05ea53869481d31025ea0d870a88f`  
		Last Modified: Sat, 08 Nov 2025 18:41:47 GMT  
		Size: 19.8 MB (19802919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d190065e800107c1e15cf2debfb990888757f5e3566f62092b59ac0c6032ff`  
		Last Modified: Sat, 08 Nov 2025 18:41:47 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6150b4a9ec8acc9cd7d7b4ff1b79254b7f7612da7bced76dd4dac96962c53fb`  
		Last Modified: Sat, 08 Nov 2025 18:45:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:78b03dcbb947e16eff719b4073a22a188b99b863bf7417e2b93e9d1238a233fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286f10faf6323922317d95ce618ff74a08cf3de52dc260a20c1f7f0c2dff81cd`

```dockerfile
```

-	Layers:
	-	`sha256:bb8d64441d718fa4fa83d9ae7d50221679160277657a25d535fa89f1f0fd38ae`  
		Last Modified: Sat, 08 Nov 2025 22:34:43 GMT  
		Size: 4.2 MB (4232396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15ddb57e5f5b03fa73425f5db588cbec82868cc0c01dac5e8b6d0a3912d1de92`  
		Last Modified: Sat, 08 Nov 2025 22:34:44 GMT  
		Size: 20.3 KB (20258 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:198e898ef2268e6d3c6adbee44ef50cbb35af8ae3ed730c48785d36430f17404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163562305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96014a2135a42773ab71fedad93771e511c4ba783a72667c187a69fa325299f8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:44:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:44:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:44:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:44:53 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:44:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:44:53 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:45:06 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:45:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:45:06 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:45:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:45:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:45:08 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:45:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580ffe682cc578ba845dc4c1cc67de62dd647c6dd6d5e636876121a4f6d2288f`  
		Last Modified: Sat, 08 Nov 2025 18:45:46 GMT  
		Size: 91.1 MB (91052531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1caa063da222e5940a1824c1cf6d9fc43295ed4736775e72819260ae8e483ad5`  
		Last Modified: Sat, 08 Nov 2025 18:45:36 GMT  
		Size: 19.6 MB (19632147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820a3c57f38557857b9e6a809be0461b4264d27bba47d725f04620a1233298a9`  
		Last Modified: Sat, 08 Nov 2025 18:45:35 GMT  
		Size: 4.5 MB (4517720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfacb47f741bd99f16a715f494aadd896981ef8ba4b886afe8ee48f431dec033`  
		Last Modified: Sat, 08 Nov 2025 18:45:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5dc40170b70a689d7c7d349f063854a7a1860dbd909d58a89a3e63f55c859340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec30c66c03075f7d2946b9e1bf2516a0dbc08741586db46f9f389a4be1c7659`

```dockerfile
```

-	Layers:
	-	`sha256:1a98d758fec3b194a5dc15cb593f1875c872aff3262996c296da9429b4173e78`  
		Last Modified: Sat, 08 Nov 2025 22:34:49 GMT  
		Size: 4.2 MB (4232080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91e5c5ea99a459a82c7d3059b6410acaeff7eab5e5b44919462c7f6c138e308c`  
		Last Modified: Sat, 08 Nov 2025 22:34:49 GMT  
		Size: 20.5 KB (20452 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:f6fe737fba177d19453d5b4adce219a93dd7702a9714acab7078c45169b6323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168477943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a0bb3175d47406d0ac451a4bea2b8b1ce72cde1f2976556844dcbe2b0bf78f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 21:11:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:11:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:11:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:11:15 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 21:11:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 21:11:15 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:11:54 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 21:11:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 21:11:54 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 21:11:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 21:46:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:46:21 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:46:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7b1be4bd5c392224945402db7277dc7a8f213a2d808e9ddd6b01efa46c2c1a`  
		Last Modified: Sat, 08 Nov 2025 21:13:29 GMT  
		Size: 91.6 MB (91610767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316b575cf1afaa8963f13df103df3d17de3fefd35c53a5ec73d8d70ec3dac4be`  
		Last Modified: Sat, 08 Nov 2025 21:13:25 GMT  
		Size: 20.0 MB (20021711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d1aced351c2585e8d7e3cefd3b7458567544d63a2f21de92867d6bf4d84dbc`  
		Last Modified: Sat, 08 Nov 2025 21:13:22 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d956ea3b5f6b141a4de91a029408a9a5eadde128286bc6d83897e2b89a27fb81`  
		Last Modified: Sat, 08 Nov 2025 21:46:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:af3d5fd4b8c3dd679938da99fa441df9898216485217baca7c1f1c93d68500d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4255928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b08cbbcfce08453d5455d680fc63a78fad27cad26bd51f2ff50430227ec320`

```dockerfile
```

-	Layers:
	-	`sha256:debd2521326c244b5c5dfcc6aa2b46015375649a673fe801996430d081a314a6`  
		Last Modified: Sat, 08 Nov 2025 22:34:53 GMT  
		Size: 4.2 MB (4235589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d6a490f3d6e007e956af102942a31b9506ac0d955439af9ae9acc13965056b`  
		Last Modified: Sat, 08 Nov 2025 22:34:54 GMT  
		Size: 20.3 KB (20339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:8e6df15c8878b3aaa2ea4d2c79c4046514f0d80a7ed153a4176ec98fa083b191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159327656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fb00783ceed20e7617fcaf3097c4c84b39a8e035024eee833bccba8bb49d70`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 20:26:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 20:26:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 20:26:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 20:26:21 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 20:26:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 20:26:22 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 20:26:33 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 20:26:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 20:26:33 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 20:26:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 20:37:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 20:37:08 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 20:37:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ae75030561f486cc06d185594ec7a542d92180c2f5992e92b8dd3ccfe9149e`  
		Last Modified: Sat, 08 Nov 2025 20:27:32 GMT  
		Size: 88.2 MB (88210702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7466bbd5b7cce27a78c0b92cbb735dd19a58ab57c1448cb86fa684e0e8765064`  
		Last Modified: Sat, 08 Nov 2025 20:27:25 GMT  
		Size: 19.5 MB (19460675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef5a2c9fef553d84a125064c91229f84c9ce59d02994b548ebc32595d4317a6`  
		Last Modified: Sat, 08 Nov 2025 20:27:24 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdfb9f444a6801073c48456477fb694b0a4d256e737180ad040e12f71d4cbbf`  
		Last Modified: Sat, 08 Nov 2025 20:37:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dc862aed4065e095d6b632a60a6fe02e11c67ec3fd53ab3f33c5f04b075e0164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72429850054740461df308aa74c1b2c335f27df3b5eeb14b479ad38497cf6125`

```dockerfile
```

-	Layers:
	-	`sha256:da740beae51abacdba5c4fa0b4f2993e6b2a8bfe8a3c89c780dd07a3b82592c0`  
		Last Modified: Sat, 08 Nov 2025 22:34:58 GMT  
		Size: 4.2 MB (4226758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3241811698d210f3c8b05018b128aa989c0ad23048a6213e00c246781ae4f471`  
		Last Modified: Sat, 08 Nov 2025 22:34:59 GMT  
		Size: 20.3 KB (20258 bytes)  
		MIME: application/vnd.in-toto+json
