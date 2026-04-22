## `clojure:temurin-21-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:8476bd9cd63aefc342e3fccf31ef00c624bee2e1914ddd293f2059d7ee059b01
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
$ docker pull clojure@sha256:0bd0df52e2a9f100be4e8a3e788facc79a35c7b0401d40fa50dcb07324d8fdc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230262820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f01d80e5730d228ca305ceb678d95db95461c066fd82b956040e38f317f1e61`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:19:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:38 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:19:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:19:38 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:54 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:19:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:19:54 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:19:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:19:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:19:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:19:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018a1463b6f6f8f826cb066261c7adb7f592473f694f23f4bf16b18460dfcc6c`  
		Last Modified: Wed, 22 Apr 2026 02:20:19 GMT  
		Size: 157.9 MB (157857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6c8e566a3ce4314f417afcbb99d7a9d748044d2da6e5e554c336ff91945e7b`  
		Last Modified: Wed, 22 Apr 2026 02:20:13 GMT  
		Size: 18.6 MB (18585509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9107120f6c4f4fff0e94243ee9aeda635b108d5235f7fe3dbbd5741daedb8de6`  
		Last Modified: Wed, 22 Apr 2026 02:20:12 GMT  
		Size: 4.5 MB (4517699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2f7bb144b9ee11c304535235f5ea8794038455133cc8a8454d2d72a5dc2d5a`  
		Last Modified: Wed, 22 Apr 2026 02:20:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:361c46895354d8013aa8a6c3f08441a95a889b3f1e49e1127caac9e67b87fec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f74ce347c62dd9c73a733fadd118f4f8b69063a04265d9cd14fdf899219b6f`

```dockerfile
```

-	Layers:
	-	`sha256:5ff157cca822fa3c6bbaa7239d09da4d0e770d2fc5c7976c5791ff9410720a8b`  
		Last Modified: Wed, 22 Apr 2026 02:20:13 GMT  
		Size: 3.8 MB (3817379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87cbb8f0bc9244e135c81b010e51ad04643778878951e93aa50f6df0bd9b08db`  
		Last Modified: Wed, 22 Apr 2026 02:20:12 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:18aafca67a0ee523fd3a14622892598c759a69b623704447221ead1620de06da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228865887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753bcc3ce9ea2f3bd69e0516a4e33893dd3106a7ac61bac68993ed31e444ac22`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:22:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:34 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:22:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:22:34 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:50 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:22:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:22:50 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:22:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:22:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:52 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52eda08e4497389d8d73c2832713c0f34794fe77e8c51321cab4dc749d9d9e46`  
		Last Modified: Wed, 22 Apr 2026 02:23:13 GMT  
		Size: 156.1 MB (156133044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a668c0b39bd8f44d4bb488133450abb4b82d00cfa25ee5af80e0e86eafd8207`  
		Last Modified: Wed, 22 Apr 2026 02:23:09 GMT  
		Size: 18.5 MB (18545431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518a73b9ff63e8d5b8e26c54210263f4f8b18bbc6f9fc6e2b72aacd2c9368127`  
		Last Modified: Wed, 22 Apr 2026 02:23:09 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d7c8e9e24fc4474f2d2a51f6bf56603104e91ccad5947462fa484051d49d8c`  
		Last Modified: Wed, 22 Apr 2026 02:23:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f99c95940f96b1b5d8468b5ee250b0df4926588f570fa445ac40f604ab35fd1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ad983162265f925da42d5c90be08f5783b8dd6b8b8818231a7319585fda5b2`

```dockerfile
```

-	Layers:
	-	`sha256:02931cd7932b2f0dfb42435fb5b0817b53527dc117ad000f597192d1898af334`  
		Last Modified: Wed, 22 Apr 2026 02:23:09 GMT  
		Size: 3.8 MB (3818256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d184b9778b85fe4db7eb7aeabc0c88efc533ebf22ce073662b73ca13978775a`  
		Last Modified: Wed, 22 Apr 2026 02:23:08 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:7d20cb2442ee8218fb3a27d5f3421a2bf55428683edb27e2ec7cf3e681bdfcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.0 MB (238006012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb82513fbbc4928ea6ca290f3980c61050402a7735dfd880ccc0965de0821cd2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 03:01:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 03:01:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 03:01:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 03:01:40 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 03:01:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 03:01:40 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 03:02:32 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 03:02:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 03:02:32 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 03:02:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 03:02:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 03:02:35 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 03:02:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5605a6e452c48331997194aeebeaa58faccfc0cd45ba29af35316c69a1fefd`  
		Last Modified: Thu, 16 Apr 2026 03:03:21 GMT  
		Size: 158.0 MB (157977558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8a0a769f80792888c7cf0fea4f5d5feeac9762469fbe35efc8f1453e02324a`  
		Last Modified: Thu, 16 Apr 2026 03:03:17 GMT  
		Size: 22.4 MB (22391608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab92443e6c9b71e0ffdc721b946f80d321923145a51a931eab9c704a79ebffd`  
		Last Modified: Thu, 16 Apr 2026 03:03:16 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f87ccb9203b5ce47e9663851b441004d1e54f18594358a0327047fed4c919f6`  
		Last Modified: Thu, 16 Apr 2026 03:03:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:18c518a2d1962df151c5f54b3dfe1c38d61cd497103875720da59e9ad2223a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572a50e091691010b8316dc0a3b20234d746a1a68b905ce61b851d53ba969590`

```dockerfile
```

-	Layers:
	-	`sha256:81201cd4ccbf05e40a26b2efc78251bddc698f476b3bc080936e90751c199172`  
		Last Modified: Thu, 16 Apr 2026 03:03:16 GMT  
		Size: 3.8 MB (3818379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:151d8b3448e01dbbe85924fc97a6f3b56560d7ec8625a67095b33f471fd0c2ec`  
		Last Modified: Thu, 16 Apr 2026 03:03:16 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:102f8ee7bd13b7702b6c4ec42f95e2819dff71d6a23b1563ea20bf6f2d7265da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.2 MB (231223861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bb04e091f55e26e0b09814668fbb7e991af4624cbd8567af28c2525009edcd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 21:53:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 21:53:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 21:53:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 21:53:48 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 11 Apr 2026 21:53:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 18 Apr 2026 04:44:33 GMT
WORKDIR /tmp
# Sat, 18 Apr 2026 04:46:09 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 18 Apr 2026 04:46:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 18 Apr 2026 04:46:09 GMT
ENV LEIN_ROOT=1
# Sat, 18 Apr 2026 04:46:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 18 Apr 2026 04:46:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 18 Apr 2026 04:46:25 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 18 Apr 2026 04:46:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2e07983918932b6a7d3f5b469a0f96350899d0eb2de01a34ca1ec47825c8ec`  
		Last Modified: Sat, 11 Apr 2026 22:00:22 GMT  
		Size: 157.2 MB (157216895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905a5f9466a426d876b698c85807c80c357796a74b8b9b3065dcd59cf013e188`  
		Last Modified: Sat, 18 Apr 2026 04:48:52 GMT  
		Size: 21.7 MB (21696121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56bc7986563d8208eff3dc264f451c0c373aef9912cefa4c8cbd3835d0dde7a`  
		Last Modified: Sat, 18 Apr 2026 04:48:50 GMT  
		Size: 4.5 MB (4517788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519af63317d768dc7afb4213745c2c9d518329bd902a7a74656623f0818ed300`  
		Last Modified: Sat, 18 Apr 2026 04:48:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1b936d47c866c97c9d663420b0f1bb5ee792cbc349e29b7c761c2cfeca33ffd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3826252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c17a506dce8dcf8ac2870adb36b50ddd7d358a33fe2a4712d98eb33a40242f5`

```dockerfile
```

-	Layers:
	-	`sha256:40f3b973545151ddec19f9643e064e2c1f883071bac537b69161b4604ba3c419`  
		Last Modified: Sat, 18 Apr 2026 04:48:50 GMT  
		Size: 3.8 MB (3807856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5c1a1a66a991acaa32f49b47a3ca74ef675ba2610cb39f7d9119b1bf4900764`  
		Last Modified: Sat, 18 Apr 2026 04:48:48 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:d0340b6d0a88b87dad9f567bcfad7e8c8c175c61bdd1fbdd9c0b7bbb3763703e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219622102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6f0dc8f9e85a43bfc48f05c2396071ceb6e8a933c2264193956f2c7dee1e8d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 04:03:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:03:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:03:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:03:12 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 04:03:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 04:03:12 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:03:25 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 04:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 04:03:25 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 04:03:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 04:03:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:03:26 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:03:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cdd84aff24f59863daaed198419b0074a2a76183e68980d9cedc370030291a`  
		Last Modified: Wed, 22 Apr 2026 04:03:54 GMT  
		Size: 147.1 MB (147105212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1260f52fd49ac87fdbf4ff1845bc1c950b4c9c0c47e97b666cba964fd2ee8b7`  
		Last Modified: Wed, 22 Apr 2026 04:03:51 GMT  
		Size: 18.6 MB (18626652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683bcb46db46ae364ccaacbfe876d9afb83b2d71c79f3a089b6cf6f172d5b47e`  
		Last Modified: Wed, 22 Apr 2026 04:03:51 GMT  
		Size: 4.5 MB (4517703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f74a3b2195d493ab90e93dcaecf3e9c468ab8fd1be3b8b5af8fba4d783cfee2`  
		Last Modified: Wed, 22 Apr 2026 04:03:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4ca259f9e013a9a4f1a4409305da96b67176f1a04f7bc60c53369f5956b15367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d4851fd4f93c81bebceffe8e8211f24d7dd8133c5a8142434a6a489a96ec53`

```dockerfile
```

-	Layers:
	-	`sha256:263ece61d397c94b9e461c4c3e00fd75413f83dd660e279cbb06d86d797e7c1f`  
		Last Modified: Wed, 22 Apr 2026 04:03:51 GMT  
		Size: 3.8 MB (3813806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7feca5401451967ce6cd5b88d487608457ff30d1ad0ae1a2943dd4d8e3b07ba`  
		Last Modified: Wed, 22 Apr 2026 04:03:51 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
