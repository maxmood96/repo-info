## `clojure:temurin-21-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:7b5cf9913715dda8092a94008650bbf325a15f8699671f8cfbe0db8b5cd090d3
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

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3bde7c773e70eb92749f084712a5098136833ba4f197ecdd04bad82e637fca62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208569728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974b7a88967da3c2f8ee34928218d1aea32f0828ccc325e0cc3099dc106a1818`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:54:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:54:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:54:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:54:19 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:54:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:54:19 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:54:35 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:54:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:54:35 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:54:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:54:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:54:36 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:54:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c6fd01e89a6adbac73a89cd8d8bc23eadda7d9dcbd51dd87217e264044f56b`  
		Last Modified: Sat, 15 Nov 2025 03:32:37 GMT  
		Size: 157.8 MB (157825981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f8f2f12018de6d78a1bea9ac19bd4a5a267db4ab27f72c83496fbff3b5f45c`  
		Last Modified: Fri, 14 Nov 2025 00:55:05 GMT  
		Size: 16.4 MB (16447481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9ecb4902974a5765a39e87ebffc686cc749ee4b154b3030bde7545b062c86f`  
		Last Modified: Fri, 14 Nov 2025 00:55:04 GMT  
		Size: 4.5 MB (4517731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9f46cd70f5eae59945b916447946447bc540b76acbd6a33a9d42099884fccb`  
		Last Modified: Fri, 14 Nov 2025 00:55:04 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0ae2c5bd03217a0d585d41445d6f2b141a4279e1d21e5394f1466fbe63fb21b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ebef1580a298aaf5802f6e64d4bcad9120cdc914f9274a0f50191b7f9bb94f`

```dockerfile
```

-	Layers:
	-	`sha256:4d0dc0da60a828ba32a24ab3262b9396fb777a603e61724319a693cf3aec870b`  
		Last Modified: Fri, 14 Nov 2025 04:40:22 GMT  
		Size: 2.4 MB (2366546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:306fbd07053b7b7aab78b032ccc0211015823c7c0ae98d881b2cf7eab4475307`  
		Last Modified: Fri, 14 Nov 2025 04:40:23 GMT  
		Size: 18.4 KB (18385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:74faf1e33dec2a8930eca0efa38bcff98c9da0865ef0115a8dec65cbd02f3286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207181727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a9f1e2f5b0444972714c09a4e5b509c8f534150a28e53aed198375de77f8bc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:56:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:56:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:56:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:56:17 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:56:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:56:17 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:56:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:56:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:56:33 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:56:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:56:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:56:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:56:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1d054dab43f3d356da8ad60eb96cbcb1b333af2139189aafd40e280ad6dd91`  
		Last Modified: Sat, 15 Nov 2025 04:02:30 GMT  
		Size: 156.1 MB (156107673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194a213f773c09164101ec37a12cae6f752582eb7fa61d477192b9d684f3a3a0`  
		Last Modified: Fri, 14 Nov 2025 00:57:02 GMT  
		Size: 16.4 MB (16413590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0978fc3f3d277dc7171d4fba6816ecf0e4aa80a3360f5acb6795a164e38c617`  
		Last Modified: Fri, 14 Nov 2025 00:57:02 GMT  
		Size: 4.5 MB (4517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce425f2a1bfc7194e67d879d0968619b7dc01edcfac089258fe102b3275fe616`  
		Last Modified: Fri, 14 Nov 2025 00:57:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7762a745add371fbc43d0bec302c37375a73fbaf6bbf3f9e99ba4f27279b0611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8996977e94e0f94d54c5e1b996afcf4a4e42e47e8314075d72f1ddd9f5057a`

```dockerfile
```

-	Layers:
	-	`sha256:d5c2b73d41384a667acb5ecc822f5621962a91746e4de7b06626c3789a44ed14`  
		Last Modified: Fri, 14 Nov 2025 01:44:52 GMT  
		Size: 2.4 MB (2366164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05d3545f86595a046d7b12e6c3638c09cd8d9c45806467aff7205382692bdb43`  
		Last Modified: Fri, 14 Nov 2025 01:44:53 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:de57de2d459c24c3575b3fc90b6e51e7a3802844a8b3f0b4c3da8311502e05b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212546137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a74fca010409aa4cbd304c0e973d31a6e9036518d0339cb1cacad4eb9dbbd44`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 07:24:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 07:24:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 07:24:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 07:24:19 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 07:24:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 07:24:19 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 07:24:47 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 07:24:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 07:24:47 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 07:24:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 07:24:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 07:24:51 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 07:24:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d06d2d74488e794ade9cf41666e84e2b03e4c9b061aa03ab78c9135204b2c53`  
		Last Modified: Fri, 14 Nov 2025 07:25:37 GMT  
		Size: 157.9 MB (157942937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859a9a7efd5294e60b30bfda11e58fc1696d11ed54996f68f92af47ee99ada80`  
		Last Modified: Fri, 14 Nov 2025 07:25:45 GMT  
		Size: 16.5 MB (16486386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3d466d8e40ff9a54e457b6bf63b11a4677115ae808c3aa8cd003b2f107905a`  
		Last Modified: Fri, 14 Nov 2025 07:25:43 GMT  
		Size: 4.5 MB (4517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a61604b34b6bec38f140cff43dd3b68d00f3d5128f1f5e398f3cb78719b81a0`  
		Last Modified: Fri, 14 Nov 2025 07:25:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fcd105b58fee2c88518b072a8f063b0c5d07b248928878521c13115a60e13d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d819b210a2a71bae8ef3be3b33717b9771f53c20f8b0718bb98a11ea532f47`

```dockerfile
```

-	Layers:
	-	`sha256:215e22d0bf5b83f5872b0c28158f99a1b0c06c280dd4a9ea6f681652afe2b309`  
		Last Modified: Fri, 14 Nov 2025 10:38:08 GMT  
		Size: 2.4 MB (2367526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c753ee55e69114970d4fb889acd802348de5e10ac2b73c2619673eccd7330066`  
		Last Modified: Fri, 14 Nov 2025 10:38:08 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:ce0877b351dfe38da5d14dc8f72f3b5415128b975a2c774207b8a3ab2cef7d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.0 MB (209004656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a61df8f5845e6103b06bca7a1325eebf29bf6a776f6a447a416396ec8d87088`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Sat, 15 Nov 2025 21:45:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 15 Nov 2025 21:45:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 15 Nov 2025 21:45:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 21:45:53 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 15 Nov 2025 21:45:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 15 Nov 2025 21:45:54 GMT
WORKDIR /tmp
# Sat, 15 Nov 2025 21:47:25 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 15 Nov 2025 21:47:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 15 Nov 2025 21:47:25 GMT
ENV LEIN_ROOT=1
# Sat, 15 Nov 2025 21:47:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 15 Nov 2025 21:47:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 15 Nov 2025 21:47:42 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 15 Nov 2025 21:47:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5131465c25b63b9013929a6ddbb0fdc268fccc3764e5911f5216cdadb1f24e79`  
		Last Modified: Sat, 15 Nov 2025 21:54:18 GMT  
		Size: 157.2 MB (157194312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3560f147ab2154261b37841778070faa15aa3c8c037d739f623e596c3506f0b9`  
		Last Modified: Sat, 15 Nov 2025 21:52:15 GMT  
		Size: 19.0 MB (19016334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754e3257eaebae3c8918ff925fe3b85f3f253d57124470e22fe8878ec3245223`  
		Last Modified: Sat, 15 Nov 2025 21:52:14 GMT  
		Size: 4.5 MB (4517793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe24f640a64435abb64a2f721301bd471358b5a72b71600f5b02ce74e7fb340`  
		Last Modified: Sat, 15 Nov 2025 21:52:13 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9be7842e9dcb6cc8970cb44719ad6f56fa9940b9476022318c1c065fed6fe76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded2963072eee1e29410aeecddb195d402e6168e9555d36334125e9240d69503`

```dockerfile
```

-	Layers:
	-	`sha256:5b588ab6ab1ab1970396bc6fbfe1f3532c9c160212808bae610a46e1c2a466e7`  
		Last Modified: Sat, 15 Nov 2025 22:36:56 GMT  
		Size: 2.4 MB (2358588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae219a55902c4cdfa853feeb65247b7ee4826fc11dc9f65897bd24b3509f0311`  
		Last Modified: Sat, 15 Nov 2025 22:36:56 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:0ef400afe25fd966d06a1159f0e08339e0a0231c7f21b37d481c2c117a428887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197909083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae961a316471ebae1e49f3e09e9b2a09f35a2f653e696976d6aff5ed04cb56f5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 01:00:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:00:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 01:00:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:00:31 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 01:00:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 01:00:31 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 01:00:47 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 01:00:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 01:00:47 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 01:00:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 01:00:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 01:00:49 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 01:00:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be32e0cd1b5024cab0eecf981b3706b2b67d3726475f3a177973892118fff5b`  
		Last Modified: Sun, 16 Nov 2025 01:43:22 GMT  
		Size: 147.1 MB (147069832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644faad4e0727cd2c1aa82b812b93c75d05d0559f2f2f08d11c1abe1341df44a`  
		Last Modified: Fri, 14 Nov 2025 01:01:22 GMT  
		Size: 16.5 MB (16483696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e9a3ab2f4799026cba3195eb9781a143140a6109d465249d5b432be3e7de13`  
		Last Modified: Fri, 14 Nov 2025 01:01:22 GMT  
		Size: 4.5 MB (4517733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2005268a97ca6931ea428bbc6e0fe299223146b615c0d9a049c6971697f62eac`  
		Last Modified: Fri, 14 Nov 2025 01:01:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1f6b7c14be675b760bcf483d80d6cb8c1bce86cf6b10218c38719c09e8559e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e992e66cfeeaca7044a7aaf148d05721dc1153e863f4871bf14dd75f727add`

```dockerfile
```

-	Layers:
	-	`sha256:d925c1b7e3be85b51f07e7a59e10cc9407f89ad2237a961d6c3f912f4f3ebed9`  
		Last Modified: Fri, 14 Nov 2025 01:45:04 GMT  
		Size: 2.4 MB (2362973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41692c3c5cf83605599864143839cf9337f1abaee50da4560b19577c99bdf33d`  
		Last Modified: Fri, 14 Nov 2025 01:45:05 GMT  
		Size: 18.4 KB (18386 bytes)  
		MIME: application/vnd.in-toto+json
