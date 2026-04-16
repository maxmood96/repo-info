## `clojure:temurin-21-lein-trixie`

```console
$ docker pull clojure@sha256:b1502e6a2c5567f9e7075dd29cadd53774eed249b740550d6b3649798802da1c
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

### `clojure:temurin-21-lein-trixie` - linux; amd64

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

### `clojure:temurin-21-lein-trixie` - unknown; unknown

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

### `clojure:temurin-21-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2f0e064d35fa7e34ba03b889b94bdbb692da31b134e313c4e6f70483609bf74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232740706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ecafd0ce0c4ff0c86de59e5b6bd3dde3318f6a96f4d88c0afd8edc88587672`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:16:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:16:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:16:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:16:29 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:16:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:16:29 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:16:46 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:16:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:16:46 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:16:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:16:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:16:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:16:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35925ac2d3a9c5c9603f6e88800e0aaa34268ec65eb891afc66055af64dbe686`  
		Last Modified: Wed, 15 Apr 2026 22:17:10 GMT  
		Size: 156.1 MB (156133027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef270869f7b9f57dc62a35444c1400251b508fea19b4c6bb7906d80ece8e0fc8`  
		Last Modified: Wed, 15 Apr 2026 22:17:07 GMT  
		Size: 22.4 MB (22424282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e1b8f3caecfa48b2769309752277f4aedaaa22a0b2ba70be2fd37dd2612957`  
		Last Modified: Wed, 15 Apr 2026 22:17:07 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b234cd6484c3f665e0ebda019a4ca22437111cc7fd8e8d731fe1fc48271627af`  
		Last Modified: Wed, 15 Apr 2026 22:17:06 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9f3e5891a807c9575c03ab32731b8455cd368f40b906b911994018888c188ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584816acfed27cc2ec001511fbd0e4f671c68308474fd1b3d8e7f6553193a121`

```dockerfile
```

-	Layers:
	-	`sha256:3dbedf6aa4bf51e70cc8425d1ada20f948b8319e39a1e4a53afa172a1bf0ac57`  
		Last Modified: Wed, 15 Apr 2026 22:17:07 GMT  
		Size: 3.8 MB (3818256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16121ac02b210c8585d9d6333083a69e464ea0f4f658797bdbdc489b352c9b89`  
		Last Modified: Wed, 15 Apr 2026 22:17:06 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:2454acbf5939706a20f352e34d8f3b44efff9981c356bea79d84bb1b558863b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234255251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba39f3c7d918bf52c7588a47a56968703b43a8f1cb3a5e690edf3478d4ce93d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:47:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:47:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:47:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:47:39 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:47:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:47:41 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:48:32 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:48:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:48:32 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:48:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:48:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:48:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:48:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dae9dc83e459c0aac03f4da141b2222e67e4c531d619bb7dabf0549311b9fd0`  
		Last Modified: Tue, 07 Apr 2026 14:49:20 GMT  
		Size: 158.0 MB (157977541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776aa01d52077d6c0143b43bd6d28a8953fd333afb636ca91e350d9f92c6e725`  
		Last Modified: Tue, 07 Apr 2026 14:49:16 GMT  
		Size: 18.6 MB (18640845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a0fb9d7c2ddecc99307cc822d4a0bc6eb0c7386b1dd3b0b883df447080ae9`  
		Last Modified: Tue, 07 Apr 2026 14:49:16 GMT  
		Size: 4.5 MB (4517766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec8b5243d42ec54a6e45cfbdbf61e7c6f7a355cac787f4a3e0688d5f51ca581`  
		Last Modified: Tue, 07 Apr 2026 14:49:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f3ebb3f6eecdda6905352cd3adf67b7bd33d4a291f86d22638e80a4bb75a45d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9de31357d81c042d0979464017e3b039d433c5c7cdf343ef7e81b7bf468bab`

```dockerfile
```

-	Layers:
	-	`sha256:b826b7451d15dfc49ccd0f7ed041a28d690449ff8436439bafae83bfb6441fdc`  
		Last Modified: Tue, 07 Apr 2026 14:49:16 GMT  
		Size: 3.8 MB (3818379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaaeabf77fc6adba192d7143b49db9d31e8a5cb95e8338922b2e11196d4c7084`  
		Last Modified: Tue, 07 Apr 2026 14:49:15 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:342c836a2424754be1fdebb843a977294078eb0e5ef6273cc1dfc77907376838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.2 MB (231223921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd5f22a1787eaada79e13f6206a261026f87c452104abda6d0e3ef936bd447a`
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
# Sat, 11 Apr 2026 21:53:48 GMT
WORKDIR /tmp
# Sat, 11 Apr 2026 21:55:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 11 Apr 2026 21:55:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 11 Apr 2026 21:55:24 GMT
ENV LEIN_ROOT=1
# Sat, 11 Apr 2026 21:55:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 11 Apr 2026 21:55:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 11 Apr 2026 21:55:41 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 11 Apr 2026 21:55:41 GMT
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
	-	`sha256:25e5a28b485204477d524eea38e022437aaeff4d9b3784e1cc57e569a9647aab`  
		Last Modified: Sat, 11 Apr 2026 22:00:02 GMT  
		Size: 21.7 MB (21696175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b29c807c1ea424013655c38985382b6edd4cda882bfc561933aa8c13cdc6d2`  
		Last Modified: Sat, 11 Apr 2026 21:59:57 GMT  
		Size: 4.5 MB (4517795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3258811f6b3373510ac2c8fb02d7ec3056f6c7ec3df3764e4ccbbc44bdd22b18`  
		Last Modified: Sat, 11 Apr 2026 21:59:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5e87e66027e72adeec6f0356c8e8a1f47dca1e76ad7fa87b34f3bf7c13d74ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3826252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d1bb772adcde47b077efee756cbd15db07663157f6fbddda2e7337e36b81ae`

```dockerfile
```

-	Layers:
	-	`sha256:bdab5e961fda88046fb66c9f287b652f5e470d755decc75299509f0a7f163d3a`  
		Last Modified: Sat, 11 Apr 2026 21:59:56 GMT  
		Size: 3.8 MB (3807856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c12aee0c6c2a9a6765dad4fc04e9eb80cfbbec9a90a96b2816fbb33ae1113d27`  
		Last Modified: Sat, 11 Apr 2026 21:59:54 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; s390x

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

### `clojure:temurin-21-lein-trixie` - unknown; unknown

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
