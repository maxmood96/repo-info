## `clojure:temurin-8-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:7c1a369869b38ac1ff3e98daeb5c91f55536877a3cffe98fe89f0f80039d174a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4d01d3148f8e5d80f02ea9b9e08422157ace2f4168316b4a3b64b0c4214e5e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105714200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fdea1745f6cde2873ca2a057a1d2f7b3407a1fbda78dfdfbd879bd9388dfbd9`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:15:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:15:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:15:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:15:22 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:15:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:15:22 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:15:36 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:15:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:15:36 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:15:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:15:37 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294de08a41493927c24ae0b34735087730ae6da6066a60c13d374219cb9c2c84`  
		Last Modified: Thu, 11 Jun 2026 01:15:52 GMT  
		Size: 55.2 MB (55198716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b677121a06355caa9cc6b28cfb1fe9137c85f8c750a917745a94126249e93d8`  
		Last Modified: Thu, 11 Jun 2026 01:15:51 GMT  
		Size: 17.8 MB (17760112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725b10e69ad0a713c29436bf658f308fb7c092522dd723ebbe5ab6ec6a2490a4`  
		Last Modified: Thu, 11 Jun 2026 01:15:50 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2b60e84abc184159347c82e0646b0d75bfb21abaf721aad139d1ccac7ad1456c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddea6e973beec18a350833e6b8d9e8815bdfbedcc80be8480c6a77d4ed92f878`

```dockerfile
```

-	Layers:
	-	`sha256:57e06d6c898551e39ba203d7b2facf92cd675002fc37e5c24c1065eaa4cb21c1`  
		Last Modified: Thu, 11 Jun 2026 01:15:50 GMT  
		Size: 2.9 MB (2851075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a80d12ad62fc29d1ed585ade441e8fa1c00a07d966e8c3be151ed60178c92490`  
		Last Modified: Thu, 11 Jun 2026 01:15:50 GMT  
		Size: 16.6 KB (16554 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2f89dc4c0c1bf08db3a11f896bb54d313f9265821f4ddc12f60a7cb4e25646fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104507018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5c4d0a1ab20fe614b2144657fecf112b93b461e2c75ba5cef7a5f59aec72f3`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:19:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:19:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:19:15 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:19:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:19:15 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:19:30 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:19:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:19:30 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:19:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:19:32 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2a703ef983b251932b1d7db00cea7bef8aa196aaf8955a419066cd471b1a65`  
		Last Modified: Thu, 11 Jun 2026 01:19:44 GMT  
		Size: 54.3 MB (54272904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8c40a1c11aafa6930557a3fdf1f7f9527662c763d0dfb62f190149deed58ce`  
		Last Modified: Thu, 11 Jun 2026 01:19:43 GMT  
		Size: 17.6 MB (17594061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0f883e59478ee8e0cfc221af4fe3443a123139304009d85cc232b048346b1a`  
		Last Modified: Thu, 11 Jun 2026 01:19:43 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3795a27a2de34dd676cbae6344eb43e5adfbeb79568dba87cf8a20c8ef825031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2868065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10620531a1924160493c041fe77d9d437bd1c4621b1e8bc07e02099814ae59ff`

```dockerfile
```

-	Layers:
	-	`sha256:bcd7fd15ec916e76ac0ef78d2afbec26037717568d5b6a44761ea5ec5ccdac47`  
		Last Modified: Thu, 11 Jun 2026 01:19:43 GMT  
		Size: 2.9 MB (2851390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37f50308e82afbe83b3e171a396e075dbb6312a7c80e5c97dad5f3c8b7df3c91`  
		Last Modified: Thu, 11 Jun 2026 01:19:42 GMT  
		Size: 16.7 KB (16675 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6f79bdd3d6f83afc471a6c7eac6b61338af76c6297cb308ba86120be678a4fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107226033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34edaf672998bc6f6a7a439257c76e2b5e4f28ce2eb3c7e7a8d16c091494a72`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 05:43:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:43:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:43:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:43:16 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 05:43:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 05:43:17 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:43:43 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 05:43:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 05:43:43 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 05:43:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 05:43:47 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e7d2adee20295d3b262cdd2cfe943ade2d2c668cc3b4db782efb9526da7915`  
		Last Modified: Wed, 20 May 2026 05:44:13 GMT  
		Size: 52.7 MB (52669153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a97e9d7518ef179d34e6236251c54c00236be93277dbefc0ecf678c28f765a`  
		Last Modified: Wed, 20 May 2026 05:44:12 GMT  
		Size: 18.0 MB (17963354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a8e3b6cc229f96fdbb3f3edf5a3e5f5f21bfcc79f1dcc0c94994f55a07ed1f`  
		Last Modified: Wed, 20 May 2026 05:44:12 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8c69da7a7eb0a5b3fe943e08add452e1755da51dd5bff913e062c8036670336d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2d9aa2dcc1d81b1fc25ef08efd271d1fc36b7cb6c65956dc2a77fdfae4eb39`

```dockerfile
```

-	Layers:
	-	`sha256:ec6eb434d3d29fef03ddb6056f5a6b1e00da99b56a0567ee0c67dd1348dd82a2`  
		Last Modified: Wed, 20 May 2026 05:44:11 GMT  
		Size: 2.9 MB (2853485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2428c5ee1dcf0c9231ad968816e0e1772a5d8a2ef89f8e817287894e0d417752`  
		Last Modified: Wed, 20 May 2026 05:44:11 GMT  
		Size: 16.6 KB (16598 bytes)  
		MIME: application/vnd.in-toto+json
