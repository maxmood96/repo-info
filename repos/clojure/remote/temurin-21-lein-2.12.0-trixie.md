## `clojure:temurin-21-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:56aa0d1fa2d4148f9d484b6e6b6a4e95e4d85347ef71126de980309002486766
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
$ docker pull clojure@sha256:6732ad1bd669cea149ea1d186129e83d0d3c24e47850ed24997435addc621630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233762328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3554b027fbbb0be77a41f04890f0c60e3f935797402428c983f86ce0a459c678`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:05:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:05:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:05:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:05:10 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:05:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:05:10 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:05:27 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:05:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:05:27 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:05:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:05:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:05:29 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:05:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01572fbfa5e8f5ccaf11e6b2237b48c86a941936bdfbbc3b571073be097c760`  
		Last Modified: Wed, 15 Apr 2026 22:05:50 GMT  
		Size: 157.9 MB (157857105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a942fb55dcea9a472922c60736c1b2f75217b60f3b94d15e1c8c7d47747900e`  
		Last Modified: Wed, 15 Apr 2026 22:05:47 GMT  
		Size: 22.1 MB (22089215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c673ee0a80ee360c5207d2f8a4c7aa87801db74e63b1a69260173aa0ec5509a3`  
		Last Modified: Wed, 15 Apr 2026 22:05:46 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3645c2214b7ea2b6e77d94e9b314d3359b6dcbcb0c703d88abdf9cacd69914e`  
		Last Modified: Wed, 15 Apr 2026 22:05:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:eee69f36d913e4e709be7bfe94ccda9064aa040b33dd1631286191b2d2c0fc35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6273e343271fc9a7ebf67731a404599ce0f0f84e34fc1957d610c171a19eccf4`

```dockerfile
```

-	Layers:
	-	`sha256:e78609f7204b822c574eea7dd33cd7726b4640fc6c17d06cd0ba7b5daedbe0eb`  
		Last Modified: Wed, 15 Apr 2026 22:05:46 GMT  
		Size: 3.8 MB (3817379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23177a63b7cdc83a9f917d98101dd49e274565076a7e453600fd0d6b4a4db5d8`  
		Last Modified: Wed, 15 Apr 2026 22:05:46 GMT  
		Size: 18.4 KB (18351 bytes)  
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
$ docker pull clojure@sha256:b163f4755ae8cb87d642a358405e07db0cdca411e5357fcd4411e755a271d6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.8 MB (222770754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c84387eb7aa3960533bda36cd6f18d9c0a1859e01c716d6238f3a0a76631fc6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:41:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:41:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:41:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:41:46 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 00:41:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 00:41:46 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:41:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:41:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:41:59 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:42:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:42:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:42:01 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:42:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e022bafa62bda64d6a51a016ec92ced7e9445747c5f54cb72881b028f644c812`  
		Last Modified: Thu, 16 Apr 2026 00:42:30 GMT  
		Size: 147.1 MB (147105267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe385b46156283dc57aeada317ca963415ac76b796c0243a94674091ade3161a`  
		Last Modified: Thu, 16 Apr 2026 00:42:27 GMT  
		Size: 21.8 MB (21782220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19992ce4203051d9e8525be2b210b7d84cc4d38b981794c293929fd7a8e8370`  
		Last Modified: Thu, 16 Apr 2026 00:42:27 GMT  
		Size: 4.5 MB (4517735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43673596be7c48994bb4a5d6cf72457c7713fc3e0563e702a3b685e5df58e87`  
		Last Modified: Thu, 16 Apr 2026 00:42:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:896c31423709f3ade29684d5d9b03d1d5014a033bb898247bb3623ac01936d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a719a1e98204cf4d11bce02c461938d9aea339ab50cc168ee2a9982a86463`

```dockerfile
```

-	Layers:
	-	`sha256:4403323a6dd1d3689552aa24f677dd903f08faa597059014bc6dcd4dd835a00f`  
		Last Modified: Thu, 16 Apr 2026 00:42:27 GMT  
		Size: 3.8 MB (3813806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e917ed333bf378a509f70eec65fee8f12636dc219a3efb77e9a8753560564c72`  
		Last Modified: Thu, 16 Apr 2026 00:42:26 GMT  
		Size: 18.4 KB (18351 bytes)  
		MIME: application/vnd.in-toto+json
