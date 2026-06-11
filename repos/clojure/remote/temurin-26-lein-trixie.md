## `clojure:temurin-26-lein-trixie`

```console
$ docker pull clojure@sha256:8ae6c77ba5982c0736d0068f58b25322bafc40372e577eecc388818bad545fc3
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

### `clojure:temurin-26-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:c6506cf9e97daa6351ef1d3297e1e8d0bf64fbbbc9d195909a041f5a4d332980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166949579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d50ea5958c02212e216e5d86c50ce6d8affbc64f7b5f276f9fdc9ffab9c30d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:21:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:21:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:21:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:21:45 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:21:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:21:45 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:22:10 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:22:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:22:10 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:22:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:22:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:22:11 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:22:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b22d69f9dde278978cad073fa4bf669da804dd36e84baf0bc4ef5f4735ceeb4`  
		Last Modified: Thu, 11 Jun 2026 01:22:30 GMT  
		Size: 94.5 MB (94524374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e630f694843014a2856c05c95c1bff4ae2b2e99890f4f42e19c88bd7e47713`  
		Last Modified: Thu, 11 Jun 2026 01:22:29 GMT  
		Size: 18.6 MB (18589943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a2cb72bdeb456ea98d309ba99408de6355792a854b5e6eaa7993b7105506f9`  
		Last Modified: Thu, 11 Jun 2026 01:22:28 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94ac51f102033366abe7ddfaa507d3c3996125fff070c460d3da56f007ec846`  
		Last Modified: Thu, 11 Jun 2026 01:22:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:335b8a37c61d174d2428d40451e42bca323266b0e1aa60b87c381bca7b31b653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab03235ac53c0cbdcac80b123284845311dd8bc4797f79b43157888cccc3a35`

```dockerfile
```

-	Layers:
	-	`sha256:25ea0a316093e1f1a6d9723e751e33d3dbc4574b9e80a7b67c5f3521cb2c752d`  
		Last Modified: Thu, 11 Jun 2026 01:22:28 GMT  
		Size: 3.8 MB (3781087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92a3807ac9db6361459d92f6d5f1db64a269758f2d951013ec28fb8de332f8f6`  
		Last Modified: Thu, 11 Jun 2026 01:22:28 GMT  
		Size: 18.5 KB (18499 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7bebbfdab248f5a1b88539c723e55803a91f6319c6ab899ce37910daa1e3e4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166248956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8847118e03d0a29903de7fab4c28fd8fe47723e6f01a72960e727704a29d012`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:25:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:25:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:25:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:25:55 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:25:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:25:55 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:26:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:26:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:26:14 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:26:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:26:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:26:16 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:26:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569c89dc39fae601ad8a41a697ab112d2c8474ef1c87cdb55c3d606de1139088`  
		Last Modified: Thu, 11 Jun 2026 01:26:36 GMT  
		Size: 93.5 MB (93504334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd57047adae20e0961732f2a143467b64d6925e42e6a3fef3ec7e5459be0543`  
		Last Modified: Thu, 11 Jun 2026 01:26:34 GMT  
		Size: 18.5 MB (18548271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dd2f005bfeb28c50822eafb4d49b80075ecf4040a5c74a73bd49c43a97ed4c`  
		Last Modified: Thu, 11 Jun 2026 01:26:33 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bd6615bf1c8aef3d334a47261734da6cd61697a8aed1f51977b6e05fb76312`  
		Last Modified: Thu, 11 Jun 2026 01:26:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7c32537782d406f050732509cabcda297e292304e7b00fa647c21f98c70e78b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c345fa5930ba8ee60526f86002c204400effd0d70cbeeee1738e35c177ad8c4`

```dockerfile
```

-	Layers:
	-	`sha256:e837c679e67d89c7a9870e0ec32e4823070c23d1b5d7d6f1a601ce896bcc7917`  
		Last Modified: Thu, 11 Jun 2026 01:26:33 GMT  
		Size: 3.8 MB (3781324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10cebdc224d10983d61c5cfbd13fb5c5275a2c915c2225072bb5b488f40e24b3`  
		Last Modified: Thu, 11 Jun 2026 01:26:33 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:523c952e09d19516a0dd3b0b8c25b7f53942cda9d8dbb7c05b1af3d7f7c0941b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170203431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523e11b36390a7cc726205e816b1ca85631026bf564bc3f9604f78e9ae6a8c3b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 09:50:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:50:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:50:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:50:44 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 09:50:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 09:50:44 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:51:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 09:51:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 09:51:20 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 09:51:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 09:51:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 09:51:23 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 09:51:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fac88a415233061e8cb9413720c4c9b2448dc4d46ee0ec98a8e747d248efd3`  
		Last Modified: Thu, 11 Jun 2026 09:51:58 GMT  
		Size: 93.9 MB (93902050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fef437d058f715c21a9cc73db71c1ab5c8c7275af3fbeccf2e8a5ed9a5359a1`  
		Last Modified: Thu, 11 Jun 2026 09:51:56 GMT  
		Size: 18.6 MB (18645277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8f60ac347826c995598b9b11620b7e2694d3265634369a18900e1d4cb3b8e7`  
		Last Modified: Thu, 11 Jun 2026 09:51:55 GMT  
		Size: 4.5 MB (4517736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5105bd3b28b825ea89c3fb0ada82bfbd7d5f75dc4c053fccd796f37e8d498f1e`  
		Last Modified: Thu, 11 Jun 2026 09:51:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:604ac444e23da383f13e4a3040a2db9081bf737afbe91c871a74f536c93ab12b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:505c635db4a81c683b1334948ee155309c3d7345adae95bf1717ff6d75bea66a`

```dockerfile
```

-	Layers:
	-	`sha256:fb8a9704036a9af7fe80e03f4c7b34341b4dacb945a1cd60c330500dceeb9743`  
		Last Modified: Thu, 11 Jun 2026 09:51:55 GMT  
		Size: 3.8 MB (3766023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5dc3804e146d2e8efdc7808ebcb3aada3e1687dc81db4f1b3b079b2a490da77`  
		Last Modified: Thu, 11 Jun 2026 09:51:55 GMT  
		Size: 18.5 KB (18543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:d75388f17c162a88e520d51da6c62ebb252a20319232c64fee2c2e0dfc10c896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163072144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b139548bb456ee86d45bb666596510284153cde14e7bf9f06816d4e5927ef1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:15:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:15:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:15:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:15:37 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 03:15:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 03:15:37 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:15:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 03:15:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 03:15:52 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 03:15:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 03:15:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:15:54 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:15:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cff8bbb29e668e8dc090e00a7af5aee6abd7ccfc1db8f297307fd489ce5911`  
		Last Modified: Thu, 11 Jun 2026 03:16:21 GMT  
		Size: 90.5 MB (90536968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae7d8588537c7999056cece79f7e4d08e2cb7a454f3cd4f2ad23e5ac6924d8`  
		Last Modified: Thu, 11 Jun 2026 03:16:20 GMT  
		Size: 18.6 MB (18631103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263f059cb8baf85a7d3f9061a359d0a27a0be9b7269f9b26e23fabe43155b2a1`  
		Last Modified: Thu, 11 Jun 2026 03:16:19 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c8434dc547874a8d5a249ec5c1f474d8ef756541e6359a22923fd0402d9770`  
		Last Modified: Thu, 11 Jun 2026 03:16:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6b96f4317efa2572816f6761516023185046832fbc2b77415f8f8d2615af2630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04f21bac67a9ba5dba2da0e995bbbd4a7c283f7543107c8eb798d6b06b4a140`

```dockerfile
```

-	Layers:
	-	`sha256:cb291d74e4c7eb31f2c9156637adbbd47f72e667e74b248d12b9498e544de864`  
		Last Modified: Thu, 11 Jun 2026 03:16:19 GMT  
		Size: 3.8 MB (3762700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c656d1dc5f387072327cfd1670393526028cff0ea4992680e53573c46d5a4b4`  
		Last Modified: Thu, 11 Jun 2026 03:16:19 GMT  
		Size: 18.5 KB (18499 bytes)  
		MIME: application/vnd.in-toto+json
