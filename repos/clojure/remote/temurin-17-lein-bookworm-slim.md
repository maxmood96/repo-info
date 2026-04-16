## `clojure:temurin-17-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:d7b0745211ebf94f79ce88504eabe9a4e2bb9dc781c14865937f19872e6c2577
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
$ docker pull clojure@sha256:65bb1c06417351e5b02c3eec33a2949e23b9b5d2d787a0dd0ac696504b2a8f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194662242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974d2c1f32d10c5b00c91b17afda8a4ef465acb30d38c9924c9b2dfe53b724a0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:25:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:25:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:25:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:25:06 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:25:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:25:06 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:25:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:25:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:25:20 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:25:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:25:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:25:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:25:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355ca048bebab1889bfb4c93ba32d1eca2f181a3350b08e8d77663450ab61cb3`  
		Last Modified: Tue, 07 Apr 2026 03:25:51 GMT  
		Size: 144.4 MB (144436222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014a9b1f9d55ec53097ad7dfb5763ccc57e540d43034852109ec428556d6adf4`  
		Last Modified: Tue, 07 Apr 2026 03:25:42 GMT  
		Size: 17.6 MB (17591721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4dc3046509d662124e6edf91e69709ce0ccb285d1d6f5c1527905ce9d38bef`  
		Last Modified: Tue, 07 Apr 2026 03:25:40 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9310ae3a7b8cdfd793b5ddab3e8a0d5dbccdffe0a27b2c85710a6171d5869ee0`  
		Last Modified: Tue, 07 Apr 2026 03:25:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fd4910a5247480a42396d5973bb791d717b6d59453d4ec7987d6c91e340aeab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2748189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81686f32a792904d88f0c9ce4e57bea08abdce70998c30c5d08f8b52b0b97261`

```dockerfile
```

-	Layers:
	-	`sha256:44e92b4107e44455d519188141782f8332cfac8566c89383c1eb5bfe4cc8b383`  
		Last Modified: Tue, 07 Apr 2026 03:25:39 GMT  
		Size: 2.7 MB (2729665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dc077b8c94cbcd98efd872797636c4be62196d5a72babd103d75a1cae730296`  
		Last Modified: Tue, 07 Apr 2026 03:25:38 GMT  
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
$ docker pull clojure@sha256:c98fb44f2bcd2863eee27a30bffdf5af5e69755dbb685a71b9144b7741cf0908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.5 MB (184457730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8025916ba325a19c1c1d7644183773889488b6f39b5ea8a21c8bbd565a1daef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:41:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:41:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:41:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:41:51 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:41:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:41:51 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:42:01 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:42:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:42:01 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:42:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:42:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:42:03 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:42:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5bb5c429c7fc69853b04b7b379880a199d321686ac73dcbc03c18f0876fec8`  
		Last Modified: Tue, 07 Apr 2026 05:42:27 GMT  
		Size: 135.6 MB (135626852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325808f73e8f388e4951eb7b96e4e92075e92da606e6cf93652a52e765810dd1`  
		Last Modified: Tue, 07 Apr 2026 05:42:25 GMT  
		Size: 17.4 MB (17421087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41067c022b1888529dc9e4360508cc4f4e7c2e3ae04893e485e230ac3eb5bf68`  
		Last Modified: Tue, 07 Apr 2026 05:42:25 GMT  
		Size: 4.5 MB (4517728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29bb477ed9d3d1e77bd0e1689d25e71421a1cbf64aec7310b5468d8fee97736`  
		Last Modified: Tue, 07 Apr 2026 05:42:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fc82e1eaf7fe1fb7fb85c24253efba0f576e7f078d87282c6b2be940f6ee1528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2740267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ebb9d0aca78c7418d138ca13a5c602968a65661ef719816a130e49ebb015139`

```dockerfile
```

-	Layers:
	-	`sha256:4e56f7b2b0aa5850d6bd9eab7f03dfef23df9078d9eb5e0d676a13fa3afcc0d9`  
		Last Modified: Tue, 07 Apr 2026 05:42:25 GMT  
		Size: 2.7 MB (2721864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8a9907ef179f113ec65a5f4597fb6bcfb624c31855fb9cc8c5b7809fae5f6c3`  
		Last Modified: Tue, 07 Apr 2026 05:42:24 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json
