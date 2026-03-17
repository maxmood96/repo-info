## `clojure:temurin-11-lein-trixie-slim`

```console
$ docker pull clojure@sha256:ac8906d309295b5de08ba0405cd840288f952ebce6ad84067571053cb855abf3
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

### `clojure:temurin-11-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a6a2c0bac2655a786dedaaacef752df36636ebb8316f8a82b9fb69a16e1ced42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196548279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7242d804493fb9c47e3e91af66cba0ed2932f62a4bd688a1cfa5d0faa2f12e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 02:56:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:56:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:56:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:56:55 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 02:56:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 02:56:55 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:57:10 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 02:57:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 02:57:10 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 02:57:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 02:57:12 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed691587beedb0eedd19048697067550dea0952b0183bf9fc045203f58344a9`  
		Last Modified: Tue, 17 Mar 2026 02:57:31 GMT  
		Size: 145.8 MB (145806979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aac3ef17ab3678c18c10bccd3fae8985d636b2d81a6c9f03f3f7ba6d19e9d17`  
		Last Modified: Tue, 17 Mar 2026 02:57:28 GMT  
		Size: 16.4 MB (16448027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5d9e3d53daec3b476165b05edebee5621e7dcf6c86155d72928eb2b58de810`  
		Last Modified: Tue, 17 Mar 2026 02:57:28 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c87b2fea8e88cb63dddc58d6a315833c9f2013432e46c1390cbb11d8525883c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3293e5fa95b0ef3ee63e278f273adc2005a42ae38842c93162e6ff303317775`

```dockerfile
```

-	Layers:
	-	`sha256:ba07c8aa4b207e1649d449575d2ed051fd63ba18a2cf1921deac88ea161a688d`  
		Last Modified: Tue, 17 Mar 2026 02:57:28 GMT  
		Size: 2.4 MB (2384929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edd83425ed1493f220cba4d31d74296999537ac569b6d2f30941b0aff2c4e7fe`  
		Last Modified: Tue, 17 Mar 2026 02:57:28 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:16bf6dfa88bfc6d09316c2d4f3627955c6274ed4ce866928d0a6990595c04ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193570257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509dcbd4942b84bf4462887a5e897c61fb3f6723904026e70ed040d60e4cdafe`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:01:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:01:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:01:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:01:26 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:01:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:01:26 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:01:44 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:01:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:01:44 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:01:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:01:46 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7173674b53b4a9e2f0793f43b81befc0b922caadedc8741c480ab2de8a4f370`  
		Last Modified: Tue, 17 Mar 2026 03:02:08 GMT  
		Size: 142.5 MB (142500001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f08f9beccfcf79fc35154d422be99d400e6825e6e68116ea9a66a60bbeae386`  
		Last Modified: Tue, 17 Mar 2026 03:02:05 GMT  
		Size: 16.4 MB (16414065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d9d8248fd6708138f16bfd844510daf8ecaebd7fc8d53fff571ca9ee8845bd`  
		Last Modified: Tue, 17 Mar 2026 03:02:04 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b6e7ced2a2160a4afd8502e9fff2ede0bcfeeea646ffb3cec1f452c2f57ef5a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7838f94755c74cb9f50f1704c3741f807628a903967ba7ceb0ead2c286475a`

```dockerfile
```

-	Layers:
	-	`sha256:799f63b5029513bb985931576e1e48dac8e6d11aa2225198a6dc0ffaa23ab48a`  
		Last Modified: Tue, 17 Mar 2026 03:02:04 GMT  
		Size: 2.4 MB (2385165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7829e1dbe2c553992296029080d1d3d785853bc883f6d3732a2c21756b886ffc`  
		Last Modified: Tue, 17 Mar 2026 03:02:04 GMT  
		Size: 16.5 KB (16515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b9d08be7ce75e897d0330d7b49209b9c4f7222a28574bdd740a1cf97a117cc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187600721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27bb8eb47e05f9919520d7e13b3fcb94599dd0ea6f0c7b0e06b8d45d789a734e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 01:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:51:09 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 01:51:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 01:51:10 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:52:12 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 01:52:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 01:52:12 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 01:52:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 01:52:16 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21426e09421bed3f9e9b43d31a1a5b3e053a0afe29ad9d5a421aeefd9dec6ac2`  
		Last Modified: Wed, 25 Feb 2026 01:52:55 GMT  
		Size: 133.0 MB (132997815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67eba9ef769962b6e662a08c1bee2cdde1db2162ed2b01e447da6e634d0abd8`  
		Last Modified: Wed, 25 Feb 2026 01:52:52 GMT  
		Size: 16.5 MB (16484888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e0fbaeb76022bd7891791d73298f83cf442e8674879572b0efbd9a5c438d68`  
		Last Modified: Wed, 25 Feb 2026 01:52:52 GMT  
		Size: 4.5 MB (4517770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b4b6c453392f717cf57e3b728de62deb5c77eae220d238bc77e31fc9276b8938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0721f0548d680a1bbbc54b62e8f4e623323697b163adb721686b1736db1071`

```dockerfile
```

-	Layers:
	-	`sha256:9fd90e6211db69c674d6e8fee6a956156792a9d4e11c3b2e0951aae1c7da9d32`  
		Last Modified: Wed, 25 Feb 2026 01:52:52 GMT  
		Size: 2.4 MB (2385258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c28f3b8a078420b874499d83e0b88dd7a52f7549bc4ad8ba487d97a029b1c64`  
		Last Modified: Wed, 25 Feb 2026 01:52:51 GMT  
		Size: 16.4 KB (16437 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:100d827a4da0aab28101b1104a02e73d67c1b2b3bd2e85616837704f5fcb4fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177401403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50458726018ee78e1b6c5337adf5fd209c5d7598bff68d34b613fcf164b37ed`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:13:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:13:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:13:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:13:08 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:13:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:13:08 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:13:46 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:13:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:13:46 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:13:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:13:48 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773136b18489da474dab6c335e3fb6d61644f01d540ea474ac9f79a4dfb431fe`  
		Last Modified: Tue, 24 Feb 2026 23:14:24 GMT  
		Size: 126.6 MB (126561996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981b90611ca498fc2c87915fd190d7eb75fc1e22b09719855a0a731c20610696`  
		Last Modified: Tue, 24 Feb 2026 23:14:21 GMT  
		Size: 16.5 MB (16483448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25788fd0764163ac3ca68267094c94e43ea5524490b29e2efdd7c3bd115198c7`  
		Last Modified: Tue, 24 Feb 2026 23:14:21 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1236e0bad527783026c262a5625957884bb5ec4c254a978633e1138a99937081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468a60a5ca892ff26a45748bf9c5267b62deb6ded32a421ab7e41c90764d2bb7`

```dockerfile
```

-	Layers:
	-	`sha256:8fe6d0fa050f862c9d5c9fd58591e7c986899eb4826f9cbbed5dd2f7c1db703c`  
		Last Modified: Tue, 24 Feb 2026 23:14:21 GMT  
		Size: 2.4 MB (2381324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b4ab527280ad295e537e8f54681cd097b08acfdadbed70f66c71565b62de4ca`  
		Last Modified: Tue, 24 Feb 2026 23:14:21 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json
