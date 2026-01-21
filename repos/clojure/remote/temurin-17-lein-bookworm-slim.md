## `clojure:temurin-17-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:53a44c9dd48952aceb6b52b3cf60bbd59070cb799612ea53f4de30deefae33d7
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
$ docker pull clojure@sha256:b9e3ce5b056fcd8b98fd84c4a689a9648bae12d050258dacd1db63920fa0f6e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.4 MB (195353116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af795a266a686874d83f3d16299d1f1b2320cc95c54b66291b9b91aeb510bedc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:51:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:51:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:51:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:51:42 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:51:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:51:42 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:51:56 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:51:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:51:56 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:51:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:51:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:51:58 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:51:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d704414a27be74217bac186ebe3b00b549fa1c0fd511d6a8207dc73bf855570a`  
		Last Modified: Fri, 16 Jan 2026 01:52:34 GMT  
		Size: 144.8 MB (144847942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb708028a97da807d953de00881bda8ef55f74fd03c9ebcd9287341f99380e41`  
		Last Modified: Fri, 16 Jan 2026 01:52:24 GMT  
		Size: 17.8 MB (17758418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c918b534cd3053f67abff573cb76618d0300d2544a9eceaea3a3d91f282757b`  
		Last Modified: Fri, 16 Jan 2026 01:52:14 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c0acfed43244ac80b10173af1008508df70cb522b5c13e6dcbbb7d073673dc`  
		Last Modified: Fri, 16 Jan 2026 01:52:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a61b669c9f47950416af4a3cd43e33322fd30c6463c2b050a454c4506fab55d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2747201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f65a947943701302e88f5560e82889917555021d9de5f089b1f0e446da73d9`

```dockerfile
```

-	Layers:
	-	`sha256:3282dbc62a2a5f65cfbe268410df70f907823dd9c7a8ab0aaaf8a379ee2e2877`  
		Last Modified: Fri, 16 Jan 2026 04:42:05 GMT  
		Size: 2.7 MB (2728798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ddd72564da2ec43a57a8078ec7a3a65a3d121b1f409d7563b4b51bd9d6aa4f3`  
		Last Modified: Fri, 16 Jan 2026 04:42:06 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8870c33cbccd8209fcca84b2dfc61b807d25772769751e207b4a003e73f97863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193898071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccd8b3209c82ad901fa7181df053c568c52c3a30cefcea83e3267d8afb49049`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:56:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:56:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:56:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:56:02 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:56:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:56:02 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:56:15 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:56:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:56:15 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:56:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:56:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:56:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:56:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d704c45db3a91ceeaf91d0587d498f6ebdbfe602acc981aa4628ff23c01121`  
		Last Modified: Fri, 16 Jan 2026 01:58:25 GMT  
		Size: 143.7 MB (143679931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648c616212fadc6cfc1b1a4ec60c3185b0abb23683d2fe578be8a0b83f60a381`  
		Last Modified: Fri, 16 Jan 2026 01:56:35 GMT  
		Size: 17.6 MB (17592089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b57eec08434a0a3c264ad5b6702ff2635c4f36ff1b0c08d2626c2b61f5d96d`  
		Last Modified: Fri, 16 Jan 2026 01:56:44 GMT  
		Size: 4.5 MB (4517734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3c1749174708050cbcb2e039781a93b6c09dd82b293e9a97b0a10a87a06ebf`  
		Last Modified: Fri, 16 Jan 2026 01:56:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:04cd7df2a800d66bc7898ab14edcb3e9421c9ee24eff3da6cd7bf4eb3f5d6062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2746936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c57d14d669276200932d5148481b326a720a0233fe270fdccbe9486fd94889d`

```dockerfile
```

-	Layers:
	-	`sha256:c039e925f277d82a04f9937c87a276927a0435c298e3a0bad820cd95fd2002ce`  
		Last Modified: Fri, 16 Jan 2026 01:56:35 GMT  
		Size: 2.7 MB (2728413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f74d5fd11fd3a52e0a23bb2188423fdd9c034470f86a83f27de1eefdb9e78eeb`  
		Last Modified: Fri, 16 Jan 2026 04:42:10 GMT  
		Size: 18.5 KB (18523 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e08f36566e4fcb9c27ed3c7d1b41d624c2281ed574be5ab0442439f0eaf71cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199072341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12388b5bf8c2a136e16fafc653a61a1d6d81635e5467701d995212c1aa6a8d0f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 03:12:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:12:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:12:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:12:14 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 03:12:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 03:12:15 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:13:10 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 03:13:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 03:13:10 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 03:13:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:13:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:13:15 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:13:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:24 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59571788fceb185f89ae2134067b41fea4b2a91989cd4404e661c3dd827195b9`  
		Last Modified: Fri, 16 Jan 2026 03:14:22 GMT  
		Size: 144.5 MB (144524717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501ffe627dc0cc6f573fbb5639c9f4ea55bfdf083b9a4cc6ff68de830a145ff1`  
		Last Modified: Fri, 16 Jan 2026 03:14:04 GMT  
		Size: 18.0 MB (17960727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b728223550b412f79e47d0bf22e9a753131481abba54c0a12632bb94eb30a5b1`  
		Last Modified: Fri, 16 Jan 2026 03:14:28 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfeaa23e240008a8185fb6ea861e30adad4db5bd76a13866f7100b49181e054`  
		Last Modified: Fri, 16 Jan 2026 03:14:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e09dab19aa6adbbc99a5b497372a7bace1bbc6cc205a9b83566f3a7d806be9c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2749076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa80dcb7e7fae9d63b86a4499c2c4ba2a8f366b2f512a84bac2ddce958cf666`

```dockerfile
```

-	Layers:
	-	`sha256:dffb74417f9b8f9a4b01ffc334c3d680e3f8befcb7e7587735f73fe8f733bd15`  
		Last Modified: Fri, 16 Jan 2026 03:13:59 GMT  
		Size: 2.7 MB (2730631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6888fe63666ab26d00f8f0ee615d6d6c5ccb1a688d4200b82305252baa3f598`  
		Last Modified: Fri, 16 Jan 2026 03:13:58 GMT  
		Size: 18.4 KB (18445 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:aaa8e29375109b007d8cd6272ef0642f54a1cc1611d166ccf443806e60496e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183683119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2965f5eaf62dd01599cd4206598cae43cc8f48bd7456fffa2f4361ee9d7b359e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:14:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:14:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:14:15 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:14:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:14:15 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:14:25 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 15 Jan 2026 23:14:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Jan 2026 23:14:25 GMT
ENV LEIN_ROOT=1
# Thu, 15 Jan 2026 23:14:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 15 Jan 2026 23:14:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:14:26 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:14:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499182964acbb7a6f7acaa4f23aaad30ee7cbc97ce9848f38909ebdaca216d40`  
		Last Modified: Thu, 15 Jan 2026 23:14:51 GMT  
		Size: 134.9 MB (134859713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a331b268feb0cb6eb9c20821ed9bd26f4a665cbee0e9f5620b9f048296af2ba1`  
		Last Modified: Thu, 15 Jan 2026 23:14:58 GMT  
		Size: 17.4 MB (17420845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ed11886ddbd9fa993f626f354de1382aa5ff377ae9ed08254a70486bef6100`  
		Last Modified: Thu, 15 Jan 2026 23:14:57 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c8d1af6a390695a6aa18eeb2a33fc8e7af4211204da13464a626fb13479089`  
		Last Modified: Thu, 15 Jan 2026 23:14:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2517780c5482b2088e8525632f6e432fbc03c68662996b8cd1ca8fe40356778c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2739014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd530a057eaad52e261c70d8954ef0f78cea21e109d8e46fc8a846672a1038e1`

```dockerfile
```

-	Layers:
	-	`sha256:5d44f267401bcb01a6812d3be57cb937c18a159002f2c82c1d9b06f4b74ebc13`  
		Last Modified: Fri, 16 Jan 2026 01:39:27 GMT  
		Size: 2.7 MB (2720612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ae3eabdd440be8495fced7d352337e69404e00a49e60700591c546beee11013`  
		Last Modified: Fri, 16 Jan 2026 01:39:28 GMT  
		Size: 18.4 KB (18402 bytes)  
		MIME: application/vnd.in-toto+json
