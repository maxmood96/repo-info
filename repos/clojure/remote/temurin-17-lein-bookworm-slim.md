## `clojure:temurin-17-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:2b2643047ec41618145fb274daf5775796e7844b5187f15a05ceaf2141409784
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

### `clojure:temurin-17-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7d4c359efc024bddea79924d523f2bd9115c02083bb4bfc2da09d3c0c513145e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196142812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26af2f1eced962a00b46eff796d4666e37b1aeac98b830b8b9d8ae35038dd0fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:03:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:03:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:03:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:03:35 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:03:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:03:35 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:03:48 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:03:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:03:48 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:03:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:03:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:03:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:03:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49a066dff832f8d96ebdf5e025ce162dedc7737f2851674b0859d2859244ede`  
		Last Modified: Wed, 15 Apr 2026 22:04:08 GMT  
		Size: 145.6 MB (145628750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d162c2cfce57cb58008e34044aafdd6f6d0ecbe83dc3a1c1daf38619a690fe4c`  
		Last Modified: Wed, 15 Apr 2026 22:04:05 GMT  
		Size: 17.8 MB (17759589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c388b26fce42192c17f5d685b0cbf68959752fc0e0beba4d2c06102f9590f9f`  
		Last Modified: Wed, 15 Apr 2026 22:04:05 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d28f1ced9d90f7a1b88c72545b8d9a21917c28ec2a32b2a761804caad235f2d`  
		Last Modified: Wed, 15 Apr 2026 22:04:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1cb555471b9dcdd967b61bdef816eb3075cfaac0e6bba2b13337005eebdc20f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2748453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca440f54020aea8e9affdf6b2428a9fd8f997c60afa4fa0ef9ed0df59f7a5b37`

```dockerfile
```

-	Layers:
	-	`sha256:23fcd543aa054d28cd1d08c8da6b4bb40df0567440f7bb5f771f81df9dab95e1`  
		Last Modified: Wed, 15 Apr 2026 22:04:05 GMT  
		Size: 2.7 MB (2730050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfc0ad5ed949296e77860ef2349a97a71a388666895824c2223ea2e72e0bb98c`  
		Last Modified: Wed, 15 Apr 2026 22:04:05 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e98957db7cd2601f00f84251644cc7819b9ae36fafd166f4e64089d56305a937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194663572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f240345247728c249ce14c66ff3c69d2f9d1f368eba62b24f56cb4c48081237e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:14:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:14:47 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:14:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:14:47 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:15:00 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:15:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:15:00 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:15:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:15:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:15:02 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:15:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1765bcedeb9f138daf8c279bda34e3d3b7502843c19121db15c229881e421e`  
		Last Modified: Wed, 15 Apr 2026 22:15:24 GMT  
		Size: 144.4 MB (144436187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca48102e12bfc8bb0013404051d157da9018c99394a884c1bc59c161c121610`  
		Last Modified: Wed, 15 Apr 2026 22:15:20 GMT  
		Size: 17.6 MB (17593034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46054153a03c7307e3c1f7cd379685ca75a88999bb9ab6a4a58ddba708f33c7`  
		Last Modified: Wed, 15 Apr 2026 22:15:20 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ff7d60d195a91b4e5854a8b6cd7b87dd160ab831165c77273ae0937b143bc1`  
		Last Modified: Wed, 15 Apr 2026 22:15:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f4b54daaf316704ec3c6973fc597dcdfb9636c24823ccc2aa175b6ec0f34c984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2748189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9a6ce1a7f7be7cc8493935d13ebb8ae0cd2b334052dfdab573b16c9ebe3df8`

```dockerfile
```

-	Layers:
	-	`sha256:5436660bb4c6efc7fe9068406b414af37e292bebda6423ac246447d85a78a473`  
		Last Modified: Wed, 15 Apr 2026 22:15:20 GMT  
		Size: 2.7 MB (2729665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65d75ea285aefe7f742a07392f17fb299166155ecf42e5093baa40d5f0d6204b`  
		Last Modified: Wed, 15 Apr 2026 22:15:19 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f8c99c8445cb28828b43b424f81d4ad54fb86ae0577b67321b08cf3244b73bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.0 MB (199995899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928e292cda62af6821d2896c19bd1dadff2c5217c00e4e49015b43c26dbd9f25`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 14:37:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:37:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:37:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:37:47 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:37:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:37:47 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:38:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:38:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:38:20 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:38:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:38:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:38:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:38:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e8da204b05d826de29378d25fee6dd2692a8f7fbf5cb6fc40cf39d76c6561f`  
		Last Modified: Tue, 07 Apr 2026 14:39:05 GMT  
		Size: 145.4 MB (145438191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65802fe0f2fbfb336e7fa74525e2babc3f621b5c4e768fa744482edad644f408`  
		Last Modified: Tue, 07 Apr 2026 14:39:01 GMT  
		Size: 18.0 MB (17961056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37a55a1c15a50098bda4b7071ecb0df62f30f0b6d974c912ccd9d858b896d6d`  
		Last Modified: Tue, 07 Apr 2026 14:39:00 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033a6e889f79ad36d31e00b7fcde83ee0a237df354a6082787ee5ab7bb138e22`  
		Last Modified: Tue, 07 Apr 2026 14:39:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dc949eae88cae76a3e24fc34c9a8907284244eadc6d56ee69f6f7790e85cf7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2679f9b4ad72ed63dd82801e122d28a68fea5517cb74fa6eafe0c5c5281f8c`

```dockerfile
```

-	Layers:
	-	`sha256:75e14f4c0eb6a2591d4b099715d8fe41680c529ba7b9da92971a557b62f069ff`  
		Last Modified: Tue, 07 Apr 2026 14:39:00 GMT  
		Size: 2.7 MB (2731883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42a56d3c11b5041ed5228a8ab34ad2fa76ee6ebc95d76e0b32834197993f2467`  
		Last Modified: Tue, 07 Apr 2026 14:39:00 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a30e44672310c9e95ba4132651ee59fed339f5efba591c1a044e1548eb61e1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.5 MB (184458821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:649024d5303c9721269fb319026ef0a60b3529004d61d1ada5b76099c2f674b6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:38:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:38:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:38:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:38:05 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 00:38:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 00:38:05 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:38:15 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:38:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:38:15 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:38:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:38:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:38:17 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:38:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c713317975041bf27c66cb35f6d637abc30dc9f0e4406c9dc6ab930521f9b233`  
		Last Modified: Thu, 16 Apr 2026 00:38:45 GMT  
		Size: 135.6 MB (135627010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15794faee5162ead825970e19ef0948dc9b3e7f06b7160e96496e47ead006898`  
		Last Modified: Thu, 16 Apr 2026 00:38:43 GMT  
		Size: 17.4 MB (17422005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7898b2471a146349a4b4a9d2c6ac69b1584e5e31ab1d2749e35f31688e4d00f`  
		Last Modified: Thu, 16 Apr 2026 00:38:42 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbdec7da14d5b67c4e5fc3c0d42dafb60235f3fc4ac2b7db517666c8bdd55ee`  
		Last Modified: Thu, 16 Apr 2026 00:38:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b5beaac8ce292d120df4c71cedd499fc2d65150f462851c81f85b89ff4d77f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2740266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ca2d4556089fa1d55d2ff96d7475262646a11d25cadcea2784eecf2e22c519`

```dockerfile
```

-	Layers:
	-	`sha256:f3a8a48bd95cb2f8a4696524b5b38619c3410ebf0f76156de6c6327931deec3a`  
		Last Modified: Thu, 16 Apr 2026 00:38:42 GMT  
		Size: 2.7 MB (2721864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb43b14b6f1b6db0be379532ed88e6151a8025803f9e67938debfc4fe2c10053`  
		Last Modified: Thu, 16 Apr 2026 00:38:42 GMT  
		Size: 18.4 KB (18402 bytes)  
		MIME: application/vnd.in-toto+json
