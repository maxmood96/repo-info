## `clojure:temurin-21-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:335c0e06c3ebe89d9f8d0c9caa186e457eb72ad89e84dd738775794c44259cf7
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

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:15f6822c06e2a0adc5d36fc68161154b428f777b8b79cc7981e72498373ac107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230670404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7189c7f478f642636fbb6c064f3f345bc2d8bf4a282b636badcb8a3ae0de97bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:19:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:04 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:19:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:19:05 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:19 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:19:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:19:19 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:19:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:19:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:19:20 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:19:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70639dbe883abd9164d9209cfa5dae977a3d26ba1adbf7c007dc1175f1c41ce8`  
		Last Modified: Wed, 22 Apr 2026 02:19:41 GMT  
		Size: 157.9 MB (157857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d287f06fcd3be1badf8ef5703cf1e15c79de73fad1c1c0193c694f804d1845`  
		Last Modified: Wed, 22 Apr 2026 02:19:38 GMT  
		Size: 19.8 MB (19806559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93d47c0491d08cd5ec82236ba418e5d8af646f142da8953dba1449a910a3b88`  
		Last Modified: Wed, 22 Apr 2026 02:19:38 GMT  
		Size: 4.5 MB (4517709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f654fac9c12e9800a18039372896eb618a33af446fdd5b341e98e45a3eb894c9`  
		Last Modified: Wed, 22 Apr 2026 02:19:37 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2bca790bc48ba8a22967496a9572b039bb76343e8ed60d398457454c9aec37a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d854521f9d94e2a0b9ed9b87f5039885e9e9ca6417b1e47c1f8877b982671f0e`

```dockerfile
```

-	Layers:
	-	`sha256:355e862d1230521f5168809b8688b9b6c70b4b0945db8b8d7d9527f71097eada`  
		Last Modified: Wed, 22 Apr 2026 02:19:38 GMT  
		Size: 4.3 MB (4284233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efcd5a445d1d22156b59d973f29b3d5ac0a942a6ea150dddc987d0d0404940bd`  
		Last Modified: Wed, 22 Apr 2026 02:19:37 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:35c3653eabd385fc8d4322505f6a7ca137293ad39cdf11e5f03ec04f23310948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228989470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65074240839b141cf452951c765c92cab079b1dac5d86e792d44f85ec8425810`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:25:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:25:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:25:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:25:46 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:25:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:25:46 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:26:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:26:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:26:00 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:26:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:26:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:26:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:26:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f247c09c346552e5b6a19f3e3bacce6e3b75f9d4c879692747fe6f216b20a85`  
		Last Modified: Fri, 08 May 2026 00:26:34 GMT  
		Size: 156.5 MB (156461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effe63ef3dbb966f54a18b385fa3c83651bb354cb7473fc373ed6b4397e2ad6f`  
		Last Modified: Fri, 08 May 2026 00:26:24 GMT  
		Size: 19.6 MB (19637064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cd60449a753bfe9236207423a8806bc8d08d0ae447e19cfe1f77886280f5d7`  
		Last Modified: Fri, 08 May 2026 00:26:23 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4454bd10f761ba3d1885f14e6fe26bc4f7f7f78760a7206bb26ab7b0d1e976c4`  
		Last Modified: Fri, 08 May 2026 00:26:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8a1a03dae952b8ba6d5d05d145ef61405f1bb08e8555f2035057f17c4f6e9ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9ad5e8fb0550a3eb48e9250df6e0cff5428b50c2414a70a2ad6bf11a12fd01`

```dockerfile
```

-	Layers:
	-	`sha256:26d592247920f3120e5ca11dea4811e256aacf2600a53882fe5530222ea0901e`  
		Last Modified: Fri, 08 May 2026 00:26:23 GMT  
		Size: 4.3 MB (4284499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65d2480867bdfdc234bdfe874181b3cc6f31497f03461ab7e313d86671167353`  
		Last Modified: Fri, 08 May 2026 00:26:23 GMT  
		Size: 19.3 KB (19317 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:cda5e3cea133b5a1a1fd49edb9d1b9a946d4f640f68107151515c6fdd03c38bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235228643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44186dca7312c123e901a2cf2b9aaa40803561a77ee00ab7dcbb0adda6a7060f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 01:35:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:35:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:35:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:35:27 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 01:35:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 01:35:27 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:36:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 01:36:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 01:36:13 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 01:36:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 01:36:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:36:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:36:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0398f5f2459bce57485cbf20c7c00c0cc4acd23743ed54d0ac36f4b1a739a3a`  
		Last Modified: Fri, 08 May 2026 01:36:55 GMT  
		Size: 158.3 MB (158343239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541c5703a7b7340507844b07f8d626073251d495efb65ccf0abba853af9fa90b`  
		Last Modified: Fri, 08 May 2026 01:36:52 GMT  
		Size: 20.0 MB (20030483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088ba6f28e124233c168e6fa2940e67395ef6ecc70f915af44d9579c97386ce1`  
		Last Modified: Fri, 08 May 2026 01:36:51 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0362590cb2d90b00932e39ba3a4c486c5f75995d0bad62a98ee37994c2b65`  
		Last Modified: Fri, 08 May 2026 01:36:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:52d79e74749c3b78aeb88160ae0cd5a4384799d21df9d15780c144dce3a4a8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930aa8d66a5d1b702bba596dafbd52acd1d5c75512877818c5bed150c971959d`

```dockerfile
```

-	Layers:
	-	`sha256:bb184743dcf9d4630f1d1976eab5baa103172ee362c6649632a3b47196dc4358`  
		Last Modified: Fri, 08 May 2026 01:36:51 GMT  
		Size: 4.3 MB (4286733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd93ebee90bd62fd0559638452e406f272606081c49e5fce467e095d15ac7a7e`  
		Last Modified: Fri, 08 May 2026 01:36:51 GMT  
		Size: 19.2 KB (19228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:01682b605d8c6344528535c68d0810dd93d9f5a9e30a9c51bb0f9a7ccbe1a256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218238162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95dc2be0e1161f099e4efbf44a95b0359859ce9b5b5a741f650eb52ed7e7d02`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 04:02:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:02:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:02:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:02:51 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 04:02:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 04:02:51 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:03:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 04:03:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 04:03:03 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 04:03:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 04:03:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:03:05 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:03:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823a94a034a486e2e5ad070f6a03cf5992927682e92a4d8ac4bb69d1ed8dc2bb`  
		Last Modified: Wed, 22 Apr 2026 04:03:34 GMT  
		Size: 147.1 MB (147105251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fc716cc5c406fab87a4a83e76effed44345382cfd45668eafb82a50d40a387`  
		Last Modified: Wed, 22 Apr 2026 04:03:31 GMT  
		Size: 19.5 MB (19466776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625e0c3b42156b7a9bb7d872cdb6e38a221487c81bfd86a4568f05302d14ed0d`  
		Last Modified: Wed, 22 Apr 2026 04:03:31 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255d14a2f90b312bb672a0228cb78c26add9aa6b5189c2fd24225329d823a78e`  
		Last Modified: Wed, 22 Apr 2026 04:03:31 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dc093c7a24de859e11bf1f318f4c29edc6016bb9001ec756c3f25fd73191c21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4295065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26cd8f2868f8445ea52f8805e532a8a9892453c4a1a9206ec77dccf394d930bf`

```dockerfile
```

-	Layers:
	-	`sha256:670590443c28bd6764c80bfe606adf2408d4f58a65707d866f08f63a840c9f69`  
		Last Modified: Wed, 22 Apr 2026 04:03:31 GMT  
		Size: 4.3 MB (4276047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:814dae891cd2d3e9001782abafab911244b0c235880f1ec3f1eafbd8c76bc572`  
		Last Modified: Wed, 22 Apr 2026 04:03:31 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json
