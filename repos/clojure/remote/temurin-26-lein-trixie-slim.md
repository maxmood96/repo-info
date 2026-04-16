## `clojure:temurin-26-lein-trixie-slim`

```console
$ docker pull clojure@sha256:431b5f0144a0fb5b36eb6cf10919885419e52a1dcc3150fce92192d20fbbb444
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

### `clojure:temurin-26-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b87ccdad03c43db172780c1efb99d032da72972118ed4d30b04dd54337fdea82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.2 MB (148151420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8144795895a86b09cb2f4ae8c02c1a8c063c1933d693c17eb8cfc79147acca8b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:07:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:07:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:07:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:07:45 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:07:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:07:46 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:08:02 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:08:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:08:02 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:08:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:08:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:08:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:08:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b349650c3b3f541f795e4422d60fe54eda85d91b57b26b111f524abc6995be3`  
		Last Modified: Wed, 15 Apr 2026 22:08:23 GMT  
		Size: 94.5 MB (94455691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c4292826caa5ec2feafb8df3c98067a9e04231a3af5c622cf4f3979989b566`  
		Last Modified: Wed, 15 Apr 2026 22:08:20 GMT  
		Size: 19.4 MB (19401929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4877b426a6593a761d53c95571ffe1481ce419b1b37a78c5d0032b1f9bf2e611`  
		Last Modified: Wed, 15 Apr 2026 22:08:20 GMT  
		Size: 4.5 MB (4517731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41538c5b82680b16ab00a7dea95bc89ca738a61284d050ad7639579622edc72d`  
		Last Modified: Wed, 15 Apr 2026 22:08:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:316ac3e3d89c03cf8c7458b42c1f90d67a8279b06f92556b6d2c278745bc6466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2348672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81441da7c8a862aedb34bbc64ebbfd421cadb6bdc2bafb831f993c02ecc9e260`

```dockerfile
```

-	Layers:
	-	`sha256:fba5615e2c71a8d239ee21dbff17d3a7bccc56efe153ff72aa84210c663db68d`  
		Last Modified: Wed, 15 Apr 2026 22:08:19 GMT  
		Size: 2.3 MB (2330292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83e7c7cfbb67c87ceb2fda9a2e12614f443d86fe52d2822124a3d099e0e564b2`  
		Last Modified: Wed, 15 Apr 2026 22:08:19 GMT  
		Size: 18.4 KB (18380 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:72f5a45b3dcd27746ce5b664c0667dd54cad7a3d4063c5f58d8c3effe3a68ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147786786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ba7aa48a589b970bccf20b8453c002e0f2d434629cb22a489912aa01a171e4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:19:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:19:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:19:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:19:21 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:19:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:19:21 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:19:38 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:19:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:19:38 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:19:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:19:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:19:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:19:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acea215fd53ec722a89344fedc20eb4c313b7c3a593f1cbb39f5f132d76b8553`  
		Last Modified: Wed, 15 Apr 2026 22:19:58 GMT  
		Size: 93.4 MB (93395204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757686fda6670abbed32b978168ad69496ad1a32b08b96b49f890cfb86ce73a3`  
		Last Modified: Wed, 15 Apr 2026 22:19:56 GMT  
		Size: 19.7 MB (19734889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3f0cb8578f0248a19a0881da1ce98f47e77bbb5321ebb8017b4f48c5ab7cbf`  
		Last Modified: Wed, 15 Apr 2026 22:19:56 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcb071721df1935a59fa2ac3effe02d355f16f8949f8f9d9d11cb1414e3837b`  
		Last Modified: Wed, 15 Apr 2026 22:19:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2d64af076a33804403b0a3b4ffb3b97b1664f482de90b44fd67fe68a5ed81355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2348408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594029ab778cf8a41efdb55c55c6ddfed53f0d204c6afa244c5970e8930db8ec`

```dockerfile
```

-	Layers:
	-	`sha256:aaff02690eedc33ad1eff5417a03a1c232ae6bb29609297756dac368be67908c`  
		Last Modified: Wed, 15 Apr 2026 22:19:55 GMT  
		Size: 2.3 MB (2329907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:419b7afa506df44e1e85638d4b77a7b6214206ebe6af94c2d2a84beb2e9a4115`  
		Last Modified: Wed, 15 Apr 2026 22:19:55 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:575690a4d8357dbc28fc9c7d6d2c26494b1aade998b49066eb85a039d7053ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151579042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a463f8da126605c62f5b368f0933438737c7aafd7095863d30e1a20b6f4dca3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 00:53:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Apr 2026 00:53:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 10 Apr 2026 00:53:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 00:53:44 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 10 Apr 2026 00:53:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 10 Apr 2026 00:53:45 GMT
WORKDIR /tmp
# Fri, 10 Apr 2026 00:54:19 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 10 Apr 2026 00:54:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 10 Apr 2026 00:54:19 GMT
ENV LEIN_ROOT=1
# Fri, 10 Apr 2026 00:54:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 10 Apr 2026 00:54:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 10 Apr 2026 00:54:23 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 10 Apr 2026 00:54:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ad9d78de109af0508c6cea77373f8cb08369c373cf24c72f7da9935301139a`  
		Last Modified: Fri, 10 Apr 2026 00:55:00 GMT  
		Size: 93.8 MB (93781481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a3210fca8d79f1cc1db27f62cc3cf989202e9c6ea247f650aba49efb4798e1`  
		Last Modified: Fri, 10 Apr 2026 00:54:58 GMT  
		Size: 19.7 MB (19686375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4b0d54f122881561f793d16774b08bcf63cf9a64e2bd9dca615eb5ce11342f`  
		Last Modified: Fri, 10 Apr 2026 00:54:58 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743cad04e5b3d7c7fb3acf83c6b27da564b8be22fdd69a026044d98a9c3a8d9d`  
		Last Modified: Fri, 10 Apr 2026 00:54:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:35d0c8e25eebe9165824b66276318d37721b4a3fec693f979e8a95cb99ff44ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9c659e1d604e37db9ba728186b36b74703b83464a4299a5880924106e9043c`

```dockerfile
```

-	Layers:
	-	`sha256:7b3a01059a48b29a4cc991b50f04ba24a6207d561ffae2d50db340ea21d2493f`  
		Last Modified: Thu, 16 Apr 2026 03:16:44 GMT  
		Size: 2.3 MB (2315208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0660a8d4b40037f149e783054e63a2f54d678ba67c1aea8c329b2ea4a80b1717`  
		Last Modified: Thu, 16 Apr 2026 03:16:44 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:8a09dd40f25e423b70789c7f673943db60fe55e4f6cc9a78467a39bdd32a5551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144820253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1fc61e0550c68d508c9a10b043d8fc91d9b5b93f454e67bbe2d1e80c2580db4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sun, 12 Apr 2026 18:55:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 12 Apr 2026 18:55:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 12 Apr 2026 18:55:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 12 Apr 2026 18:55:33 GMT
ENV LEIN_VERSION=2.12.0
# Sun, 12 Apr 2026 18:55:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sun, 12 Apr 2026 18:55:33 GMT
WORKDIR /tmp
# Sun, 12 Apr 2026 18:57:19 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sun, 12 Apr 2026 18:57:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sun, 12 Apr 2026 18:57:19 GMT
ENV LEIN_ROOT=1
# Sun, 12 Apr 2026 18:57:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sun, 12 Apr 2026 18:57:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 12 Apr 2026 18:57:36 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 12 Apr 2026 18:57:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7fc246f5e32984af9b4236c90104244f3679fa7192854d7e61221c59edbfc2c`  
		Last Modified: Sun, 12 Apr 2026 19:01:08 GMT  
		Size: 93.0 MB (93008131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40190e01f7e46397fa21648abc6218b0fb5b437dd838943c6ea4dbbfa0b2730d`  
		Last Modified: Sun, 12 Apr 2026 19:00:56 GMT  
		Size: 19.0 MB (19018118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be8ce5a9de528e7e7ec36831edd301f67bddc72eb140bd3202f2dfdf95b4d0a`  
		Last Modified: Sun, 12 Apr 2026 19:00:52 GMT  
		Size: 4.5 MB (4517798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541f9793ed1f917285da3bcd32e885725295a5cb906fe9044c8cbb608d4043ee`  
		Last Modified: Sun, 12 Apr 2026 19:00:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:376d73a194ca7fc637049a6da7de5e2d41c569069bf692fa8775eb9c3066b3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2323399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337820679fd671ee70277fe6e8aa2e1da154d1f0b378ea477520fc46c2961cca`

```dockerfile
```

-	Layers:
	-	`sha256:e23d049a19c5590ca09ed72d49783a351d8b00e5b9e17674d514e1d1f4706087`  
		Last Modified: Sun, 12 Apr 2026 19:00:52 GMT  
		Size: 2.3 MB (2304975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6947168ddfa2c439d22f7bf6e7563af33018528e8e54e71f5e3759ca004e34d8`  
		Last Modified: Sun, 12 Apr 2026 19:00:52 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d10a4cdfc8b093a9560e9df627e872207bfdc6ee8aa69adfb38be6707f05d713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143991443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6ace61fd085feb634246017ad67b515875723cdd5df843b7b2375eccffb709`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:46:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:46:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:46:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:46:45 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 00:46:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 00:46:46 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:46:58 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:46:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:46:58 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:47:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:47:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:47:00 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:47:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d73a2a76ddf7460ab2878123e70b72f683be95027429b7589ec35877df13dc`  
		Last Modified: Thu, 16 Apr 2026 00:47:24 GMT  
		Size: 90.5 MB (90547699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb5aee781f83961958b6227ca6effbf88aa1ffbf24f6710b7a69cf0edf6a4a2`  
		Last Modified: Thu, 16 Apr 2026 00:47:23 GMT  
		Size: 19.1 MB (19090153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8122f968ec4371d2ca299fa84c848b6be08e699a7ebea9bcac2b50625ee55af`  
		Last Modified: Thu, 16 Apr 2026 00:47:22 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f034908d35ddd7f6018d501add2175752bcb69139ea7d512bb571bbd24e372dd`  
		Last Modified: Thu, 16 Apr 2026 00:47:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b090ad487d87f86f53bdeba78abb534cc3152ea837297f74978fbb6744f290ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d76ac34ed68f1c718d18ae1c947012187259561253ce61274902aaf50bd10bc`

```dockerfile
```

-	Layers:
	-	`sha256:2a878e762e1558ab4dbc5bc8f724001360d089ad342c9b7f0845cb968654005b`  
		Last Modified: Thu, 16 Apr 2026 00:47:22 GMT  
		Size: 2.3 MB (2311905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c6d0dce7d833a99793cbab75fbc96e5d9fcf979066cf5a19d9ffc07a9f07a72`  
		Last Modified: Thu, 16 Apr 2026 00:47:22 GMT  
		Size: 18.4 KB (18380 bytes)  
		MIME: application/vnd.in-toto+json
