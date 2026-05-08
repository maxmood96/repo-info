## `clojure:temurin-21-lein-trixie`

```console
$ docker pull clojure@sha256:53e08cf2249539818a52f02c5896a8b4468e386f94dff5e867b047eb623c768d
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

### `clojure:temurin-21-lein-trixie` - unknown; unknown

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

### `clojure:temurin-21-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:58d5950aa65d3de727ca482029b72c1b271fc276f70a86450f291c854f0da32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229193983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf5d4df744e67cdedafa6b2d0a2610d335d8900e7e5a6556e38192a067b1ee0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:26:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:26:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:26:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:26:07 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:26:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:26:07 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:26:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:26:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:26:24 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:26:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:26:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:26:25 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:26:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6551e3d385cff774658bd30a09601c92e30e51e98f6fdc8ded1bd44eba90374`  
		Last Modified: Fri, 08 May 2026 00:26:48 GMT  
		Size: 156.5 MB (156461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4d4f872e3ed9195bffc57ea01cda2216d160b1a866ca0d3d6ab5a23dba2047`  
		Last Modified: Fri, 08 May 2026 00:26:44 GMT  
		Size: 18.5 MB (18545414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db91bf2c38d67673e2d27ef9fbd5e286ce37c874c4711371c0a4ef319ad35c4`  
		Last Modified: Fri, 08 May 2026 00:26:45 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567b8e5ffac7ec58c6429acf1303341c6003ae8554ce430d6a6dad088b0d0ce3`  
		Last Modified: Fri, 08 May 2026 00:26:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:23cb9f2c27ca37ffa308c0923ba5b05092544ee30c9be88c947fffcb373673fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3837510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68a95ae6886fb5ac131fc5c5f6680ac54e0c10d9dc6468955f9b07177a69b7a`

```dockerfile
```

-	Layers:
	-	`sha256:1e2ecbd7b073f212b21cf828e47634374a84aed81fcb9731afec2ec904d8d796`  
		Last Modified: Fri, 08 May 2026 00:26:44 GMT  
		Size: 3.8 MB (3818883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83acba80c4e9640f4b52ad1124055776349a06d1bb4e0a5a57511e485d64d608`  
		Last Modified: Fri, 08 May 2026 00:26:43 GMT  
		Size: 18.6 KB (18627 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:8590f56c6541271c87a24d7099113a0b701694e8d01d50e5f89385bfd2eab556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234625394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd49b8044c353b2fd9ca0c5b4f368b8754f33a0803cf39e362b8c8156dd25ed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 01:38:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:38:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:38:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:38:05 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 01:38:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 01:38:06 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:38:39 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 01:38:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 01:38:39 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 01:38:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 01:38:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:38:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:38:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef2aeb89dd432248a27be9658c9ad2fe8736e1bb0a40602c7b1b444a977ed1e`  
		Last Modified: Fri, 08 May 2026 01:39:21 GMT  
		Size: 158.3 MB (158343239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748cf280f6b471c4065778f2a810fbbb535e9293d68eb100b11d1d99a495581e`  
		Last Modified: Fri, 08 May 2026 01:39:18 GMT  
		Size: 18.6 MB (18641002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2929e2060c35294dec2e5300200e09d0d87897fb11382524a6f91c877dbb5d34`  
		Last Modified: Fri, 08 May 2026 01:39:17 GMT  
		Size: 4.5 MB (4517740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94318bc6637e9adc3364a12237a6d9526e686133933b8245043a549a423a619f`  
		Last Modified: Fri, 08 May 2026 01:39:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:780bdb11e1c0b25cb43481ea49c70c8d1c97af0504cff70b38a0716206ed77c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3837556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb63659f9f76a18c5dae576375ad799f9fd2aaf14aed41fc83884d615a6ee9a`

```dockerfile
```

-	Layers:
	-	`sha256:30f3a7fb178151bf2545f6d848c60abaf769e5a33cfd0f6ff9f9675dd9d7ee4b`  
		Last Modified: Fri, 08 May 2026 01:39:17 GMT  
		Size: 3.8 MB (3819006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:211ef3a1a874b33e37722bbac3e1cbbed3d78a75e0a8e645a383c37c6ddd635c`  
		Last Modified: Fri, 08 May 2026 01:39:17 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:e1e6ec957a18083d174010f72408db64d5b8bd96fe86abe5956b319085aa7ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 MB (228071525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bfa85d7ac8163066e446b62e13353e5d664441d8974da58eeb956c81d35eb4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 18:09:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Apr 2026 18:09:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 24 Apr 2026 18:09:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 18:09:44 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 24 Apr 2026 18:09:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 24 Apr 2026 18:09:44 GMT
WORKDIR /tmp
# Fri, 24 Apr 2026 18:11:21 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 24 Apr 2026 18:11:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 24 Apr 2026 18:11:21 GMT
ENV LEIN_ROOT=1
# Fri, 24 Apr 2026 18:11:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 24 Apr 2026 18:11:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 24 Apr 2026 18:11:38 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 24 Apr 2026 18:11:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d4384d0aaf4c67d90bf2e07cb4852bca10fcf970d4b6c61ba3f1acafc7915a`  
		Last Modified: Fri, 24 Apr 2026 18:16:13 GMT  
		Size: 157.2 MB (157216912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1abf9bd70e9a882571c42e9955460e7695282f7fd72cd7e61890ea7e182ff1`  
		Last Modified: Fri, 24 Apr 2026 18:15:53 GMT  
		Size: 18.5 MB (18538170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4d67f3c844d17dbaa6186223ea2349dd4c649c30eec5fde5aedf2ccf303b1d`  
		Last Modified: Fri, 24 Apr 2026 18:15:48 GMT  
		Size: 4.5 MB (4517796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142daaaac6e1affb28294d0bd80b652fd54e6dbcb1a43ff723b889d8ebeed938`  
		Last Modified: Fri, 24 Apr 2026 18:15:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1de1aec204e13ac6433d356457ae0968d7385e328a21a209e818efc5ea6cf20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3826251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77cd986089425f0474855e1835e95842fd042ad865be71a6ec99b891239b0c9`

```dockerfile
```

-	Layers:
	-	`sha256:4041bc6b43b8b25590af4627b8c0d455c357c78cd3a55deb8450ceb1b1d85910`  
		Last Modified: Fri, 24 Apr 2026 18:15:48 GMT  
		Size: 3.8 MB (3807856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fbdbc254298d730e1a9078c67f24c577048f9245838c8e8d6b4aeeedb9d2035`  
		Last Modified: Fri, 24 Apr 2026 18:15:46 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; s390x

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

### `clojure:temurin-21-lein-trixie` - unknown; unknown

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
