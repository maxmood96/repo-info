## `clojure:temurin-21-lein-trixie-slim`

```console
$ docker pull clojure@sha256:f600ffae656f5a751b4328bf16f6bb189c381f118d0bbc18d1d8327fee77c3b7
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

### `clojure:temurin-21-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9beb835c64eb502cdc14144901a5f3016a8a6f9face53cd9fc8b30df7c40c8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208567808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad23ee463e3329c0cb16be8bce7bd8662b420dc542cf2bcccc1bff204e4e98e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:13:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:13:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:13:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:13:01 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:13:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:13:01 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:13:16 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:13:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:13:16 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:13:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:13:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:13:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:13:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ca9ec522c0105b79e85b0720f9c6da94909674059a9a6fca215edccf61edc1`  
		Last Modified: Tue, 18 Nov 2025 06:13:40 GMT  
		Size: 157.8 MB (157826031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5e0793cbbb2f6c0d5408092f37a738a6b33546c9e6657ec1fb8252134bd983`  
		Last Modified: Tue, 18 Nov 2025 06:13:46 GMT  
		Size: 16.4 MB (16447142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bd41e2e299f703ca4d16474f1d3dc02d0dd468da9d051578c43c0d06240574`  
		Last Modified: Tue, 18 Nov 2025 06:13:45 GMT  
		Size: 4.5 MB (4517722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a331bb0059f8d4fd1b3ea13b2a711176183d20fa0619c95b07ace9a16b9ef62`  
		Last Modified: Tue, 18 Nov 2025 06:13:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2c4481fe416bed06ff7b4394db789def200b33463692d4ba1101b36c1de2bdbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac93aa16371cf6f9a839971fc90a743e739bd7ba77a29b18eb9fe0ca0f0d38a`

```dockerfile
```

-	Layers:
	-	`sha256:123318cea77d8eaa020295380a4454c0fcff0e1554381ca397eaa0a8a89a3081`  
		Last Modified: Tue, 18 Nov 2025 07:45:27 GMT  
		Size: 2.4 MB (2366540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5dcc97d748592284ed0fd9c56e374ace4ef28b56d56187484fb2b27efb689b0`  
		Last Modified: Tue, 18 Nov 2025 07:45:27 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7aed48ee13853b5af6ea56a43f7c5c973d69bc1fca4af670e5ca997d2973536c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207178287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647beb15cbba1de51e8e1d750df323d047c6328c7821219c354f49274cedb50f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:08:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:08:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:08:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:08:17 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:08:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:08:17 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:08:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:08:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:08:33 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:08:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:08:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:08:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:08:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e974ce1e70ad2f909acef3786f5059655c8c35da8b6b8f2a46b1cfe818203410`  
		Last Modified: Tue, 18 Nov 2025 05:08:56 GMT  
		Size: 156.1 MB (156107672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29c6d83fd726055ac72ed33ad0c7dc3f59c96b0896af71518164176ab383f46`  
		Last Modified: Tue, 18 Nov 2025 05:09:03 GMT  
		Size: 16.4 MB (16413819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e873136794096c2c4303f96ca045276a4b6f6df60c4ee22e6cd8cb2fd3c1b3c`  
		Last Modified: Tue, 18 Nov 2025 05:09:02 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e58bb2e4f0b4952dad20bf5840ce0f80d6726f08da5966ee3e79673e014d230`  
		Last Modified: Tue, 18 Nov 2025 05:09:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:486e234de97310e8a7c339f5989cd67b16f51cc9d476fdc0881def81f91baf80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a40c06242a77d2a5f0bb6c0251e916c382f5df770112b0e1fc1b0b36ff7ffa`

```dockerfile
```

-	Layers:
	-	`sha256:d6a95c8bdae3a1bd117257244d798e440d891bd1f0ee1ca990a2953e4ace8515`  
		Last Modified: Tue, 18 Nov 2025 07:45:31 GMT  
		Size: 2.4 MB (2366158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cefe7cbffa893614410b84083115f086e5509247682c9fdd055aee2f311b907d`  
		Last Modified: Tue, 18 Nov 2025 07:45:32 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; ppc64le

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

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-lein-trixie-slim` - linux; riscv64

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

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:99bb966bf7f48cba48c7a3d069a39cc6e3c6d87bed6248f982628286a9261a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197905385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7e0e9a7d70f61d48a370cebce5fb3f033a41f2cce4b10c5da09fe60b464695`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:29:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:29:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:29:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:29:24 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:29:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:29:25 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:29:40 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:29:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:29:40 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:29:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:29:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:29:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:29:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15456efc8c56111be75fbb32203283de9917eff33d36ac2a49eec5455d7ae626`  
		Last Modified: Tue, 18 Nov 2025 05:30:10 GMT  
		Size: 147.1 MB (147069840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d08265487bf5c25e52f405bb7d75e830baea4489a37f1071880837237b4240`  
		Last Modified: Tue, 18 Nov 2025 05:30:17 GMT  
		Size: 16.5 MB (16483007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f33c5fd1ef44d7a510c708110eeefa101ae239efd20d89504fcb553f611d03`  
		Last Modified: Tue, 18 Nov 2025 05:30:16 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d9dfc3e1370c26b0b4f9447122ab39f16226884714849594914527bedf2b96`  
		Last Modified: Tue, 18 Nov 2025 05:30:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:092417cf96bb517c0e4d7dcd43b6c7277a918ec6bf0b205fa18a98a06cb359f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae533f7dd7e61d28adb1056c013af28fa204ead063b7a66f443c3ab003ba5b22`

```dockerfile
```

-	Layers:
	-	`sha256:d0189d856ca3ad34371a385d23c8729de9ac01fe6942af437edd3f549780c704`  
		Last Modified: Tue, 18 Nov 2025 07:45:41 GMT  
		Size: 2.4 MB (2362967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a8988daace6cdc152c8e4dce7a8b827f7baf9df23436d1ad94ac573a3ed36bb`  
		Last Modified: Tue, 18 Nov 2025 07:45:42 GMT  
		Size: 18.4 KB (18386 bytes)  
		MIME: application/vnd.in-toto+json
