## `clojure:temurin-17-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:b9c890afcf14dea92f46b1da2906bc93290b8fb8d1c6421b03ae669c1ec8a8dd
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

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3b4847680fdbce4eb1f9ffe3796eb30ef7bbadc2414647096c1cdbc5153bf1eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.4 MB (195352637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d050f14d969b0f895e02af9bc42984fca32ed1a548e20b0e4bd1c1a950cc10`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:57:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:57:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:57:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:57:51 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 00:57:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:57:51 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:58:06 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 00:58:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 00:58:06 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 00:58:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 00:58:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 00:58:07 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 00:58:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8809c8f46a973630c8def1b8b1698ce283758dbf7b4c523c0203ec15c5ef9890`  
		Last Modified: Tue, 30 Dec 2025 00:59:05 GMT  
		Size: 144.8 MB (144847979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ec95c614e8cf4e1ce0450e69a23f7d9b2489189e8fc4e9a7c9ee57d595ed58`  
		Last Modified: Tue, 30 Dec 2025 00:58:33 GMT  
		Size: 17.8 MB (17758046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2196aeeae94bdf387bbe70cf8caf932f449bff6595dac86dd1f703fc7b9086`  
		Last Modified: Tue, 30 Dec 2025 00:58:32 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbf755888e2ffef5fa5fff59c6e767802bfe86b84e9c02e8b89b50ad2a9bfd4`  
		Last Modified: Tue, 30 Dec 2025 00:58:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8684720d9553a2246654994dd73809d28a90e9b8ade9e1830943f36e6dd04ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2747191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ced210926e9b06d1ccfa06f117f0b4852828c8ff1945c0b8b03e9c2a474a393`

```dockerfile
```

-	Layers:
	-	`sha256:f61f264ba31fe703b7304822541455318c0bfa385c521f31217fa409aa7319c0`  
		Last Modified: Tue, 30 Dec 2025 04:40:22 GMT  
		Size: 2.7 MB (2728788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e1cfb35070adfa045e0d84c04ff72b1cebfff6252097d1bb57adac54cfbb887`  
		Last Modified: Tue, 30 Dec 2025 04:40:23 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4b8a0d14b7e7f050b391451d427044f5bf7016bc686936aac0056db98264480e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193891438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f617c7d9ca0ffa38f8a0f6768f64f60f047d42e68556f45d140badafd38d95`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:58:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:58:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:58:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:58:49 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 00:58:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:58:49 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:59:02 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 00:59:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 00:59:02 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 00:59:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 00:59:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 00:59:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 00:59:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8b54a0e271e46d833589d912696a463a0635ca7e7820b81c94420ae3fe7fe4`  
		Last Modified: Tue, 30 Dec 2025 00:59:55 GMT  
		Size: 143.7 MB (143679919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f55d3d6f20f514369ffe6757b53a8c70118ab226a78e934e87c39928fb883b5`  
		Last Modified: Tue, 30 Dec 2025 00:59:31 GMT  
		Size: 17.6 MB (17591141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fb150755de528371874c239683931d3863c6d27bebf2fc76c7c3709e1da828`  
		Last Modified: Tue, 30 Dec 2025 00:59:30 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9917236498b0c950c7e8da7e5e728b06ffc0ff05f67137b3585c02be8b61031c`  
		Last Modified: Tue, 30 Dec 2025 00:59:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ed38cc9598979c7930476766e57aa1f3b1960f4954eac29b96389122f3f4d273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2746927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2543accdd1c3e7bc988dc71c9c47d915de55af1a77aab95dfb06f7fcef4bc3e5`

```dockerfile
```

-	Layers:
	-	`sha256:cf8e125a447e93438f5aa00dde68b5168756a5036797b806427f8f6a03ab4834`  
		Last Modified: Tue, 30 Dec 2025 04:40:26 GMT  
		Size: 2.7 MB (2728403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:430e3979832a04994d6f0327567f25e351b0cbb7cd7ecddfb46b51d721b8b8d2`  
		Last Modified: Tue, 30 Dec 2025 04:40:27 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4ceac9d662ac8e22fc5a378233e422cf05e4caa7254824dc2d56e0f13398f8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199071992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef15568201b4c95e89504533405cbff6e42264b0aabf0b89f4d7f92c4e7ad2a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 05:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:17:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:17:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:17:49 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 05:17:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 05:17:50 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:18:28 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 05:18:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 05:18:28 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 05:18:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 05:18:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 05:18:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 05:18:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c662a1580b47c492cf3baff3cc57fac4e48d81084d9a9ed82cf007a60ca93b2`  
		Last Modified: Tue, 30 Dec 2025 05:19:12 GMT  
		Size: 144.5 MB (144525257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0284cfea86dcff276d654e1ff0ea33c7d1904207c7764603c5553f155434ee70`  
		Last Modified: Tue, 30 Dec 2025 05:19:19 GMT  
		Size: 18.0 MB (17959721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8943e6c429d2c9b636e443f5a6c39014beb6946a730a4e1e9bca5020bca88c24`  
		Last Modified: Tue, 30 Dec 2025 05:19:18 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0175f33e65cc4af7b4adce103997232bd4c68f242436969f1bc62cba85ae28bd`  
		Last Modified: Tue, 30 Dec 2025 05:19:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:92997fb6e8f377e6228f0b67a4978e6ffb35ee975cb4591b74e633521c5b7dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2749068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1868e667c42ac3d504d1642bb33eb981d41a76b3cf6c1589d91be8bfe09dd5a1`

```dockerfile
```

-	Layers:
	-	`sha256:deff0c4a7afe9550da08f7ad8205ff18d95a0ef2ea842698a99f4b853d31b7f7`  
		Last Modified: Tue, 30 Dec 2025 07:36:23 GMT  
		Size: 2.7 MB (2730621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75915388817db29211cd72b03e6aca239f8110ec2fdcf112699ccc96c3d23898`  
		Last Modified: Tue, 30 Dec 2025 07:36:23 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:16fbd91c39fe4ce094443e2a812214e92b71a423ce73ef258128d9e6e53a7b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183681420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db12e14580f3cae4779ed272f6aff857e1aa732c85325f6e3fe649915505da87`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 02:02:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 02:02:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 02:02:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:02:26 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 02:02:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 02:02:26 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 02:02:42 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 02:02:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 02:02:42 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 02:02:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 02:02:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 02:02:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 02:02:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c5ac6ff88101ab235cdce6d5bf5fbe508e81392d7c56a55438aa9880ee68ec`  
		Last Modified: Tue, 30 Dec 2025 02:03:25 GMT  
		Size: 134.9 MB (134859036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6e8143b8779ab6bf71de51ceaacf3ee7c21d2fcfe10d835619779030234c0a`  
		Last Modified: Tue, 30 Dec 2025 02:03:18 GMT  
		Size: 17.4 MB (17419803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2c96cf1bcb904f962bf0aac18a914d7d1eb64e8f594b01c24119815ad59185`  
		Last Modified: Tue, 30 Dec 2025 02:03:17 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5385947763249e00ae7f18a4e44b1c28150fd43ef337fd660fdac742beecb959`  
		Last Modified: Tue, 30 Dec 2025 02:03:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:40e9ea8a306347d9fe09555b2fb2cafae46313ab6aab224af2b3831f212dff76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2739005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca450137f4cd6c9f066df8498b6ae412cf44f9a6db0dc511ac57a32da2143df`

```dockerfile
```

-	Layers:
	-	`sha256:f8c565c175799d0e7d37dd51d7d129e96e814f099631a775c8eedbb799ca8e7d`  
		Last Modified: Tue, 30 Dec 2025 04:40:34 GMT  
		Size: 2.7 MB (2720602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdbcba8bcb46c65b92be53a3fd8354433884d76806375f83fc639ef16e345f5d`  
		Last Modified: Tue, 30 Dec 2025 04:40:35 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json
