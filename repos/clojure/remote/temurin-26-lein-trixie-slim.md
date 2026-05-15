## `clojure:temurin-26-lein-trixie-slim`

```console
$ docker pull clojure@sha256:5b66777c65e6d3df82f3199812d1821496fd401ec83c14570b36e3b7476460fa
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

### `clojure:temurin-26-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a22f92ed92e03daa70c09f5f8cf042cad83aaff36e54c0005bdc3986f74283de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145202163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c312bc066bda3d632ac3889b287c128200d16ec9a3324134c59f89315a5d1058`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:20:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:10 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:20:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:20:10 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:20:25 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:20:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:20:25 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:20:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:20:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:20:27 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:20:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be32fea9dd551ce0e23bdf7f872985d5f481db359d473ff8cb56a70d6d376bb`  
		Last Modified: Fri, 08 May 2026 20:20:46 GMT  
		Size: 94.5 MB (94455680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b6739cdd48ed0389142846a762b95b2a0e4fc5adb19928804aaba3129f40be`  
		Last Modified: Fri, 08 May 2026 20:20:44 GMT  
		Size: 16.4 MB (16448060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9c47e2c54c17ed0d193fe5fbc25d16d707cfd0350ca9d625483ca1d98f6e8c`  
		Last Modified: Fri, 08 May 2026 20:20:43 GMT  
		Size: 4.5 MB (4517767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd380b89b40144fab75ac1a6d8acb518ed25f713d1d3e1026ecb229538fac6ba`  
		Last Modified: Fri, 08 May 2026 20:20:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:40ad6913ae4b3e3f770abb5929fb8e09d6399c1fe949834287378bbc5a7526fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2348672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f455af1cd44eb79c3181845510dab0b1ede5112e3e84e2250e7e755c81ad0c`

```dockerfile
```

-	Layers:
	-	`sha256:9e3ac9f1e51fd5b46537b350030ed2203efb96cc113fe75aff8366d097ac79d9`  
		Last Modified: Fri, 08 May 2026 20:20:43 GMT  
		Size: 2.3 MB (2330292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba2daaaed9d31b61918b9e0f94ee50b2ad55c070f77a013585b7d60f839aaee3`  
		Last Modified: Fri, 08 May 2026 20:20:43 GMT  
		Size: 18.4 KB (18380 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:81beceb11489f3b2aed8b805b2d20cef3bfb547b0433da4afe9e1dc80d69e7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144470984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30131ea115711713266747cbb233da2e897d0224d91352d2547fe73a88c9db6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:24:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:24:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:24:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:24:49 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:24:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:24:49 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:25:05 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:25:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:25:05 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:25:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:25:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:25:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:25:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4f435b402653f303138c5d99b81ead694bda07b100d4c9e60cc31eaccac694`  
		Last Modified: Fri, 08 May 2026 20:25:26 GMT  
		Size: 93.4 MB (93395169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280d85a6e285db9dc872fd8016c2e7b0aba0df76e8c03f5a8b7ad4f81b02389b`  
		Last Modified: Fri, 08 May 2026 20:25:24 GMT  
		Size: 16.4 MB (16414003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067cec9da239ae8b59e250daa8ff7736d44540d06131f22743e9076d6d0338e0`  
		Last Modified: Fri, 08 May 2026 20:25:23 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc855ec72a43931d50e075d4e59ba2bcc5820914666f178b4baf6e5da33a2e07`  
		Last Modified: Fri, 08 May 2026 20:25:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:443ebc8decf974865a9642be96c5f7e8c3ece968c6c9c3fe3f6169a15345d1c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2348408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3a0e24d4478380ebf0e41416330d7912efc516e9afa31f08d1f1816ec6f191a`

```dockerfile
```

-	Layers:
	-	`sha256:17c7301367032e1c23f8fa458b6ae612c6aa8ebc3a4f8836e61ffc087d8a8458`  
		Last Modified: Fri, 08 May 2026 20:25:24 GMT  
		Size: 2.3 MB (2329907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f52c4b59f94861a47e45255b421089f4d39662887873afd226a4821b084a1f34`  
		Last Modified: Fri, 08 May 2026 20:25:23 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:5e6f66533c321b6282ca2cc486b4dc67bc3f07adccc51e8e00996270073d9e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148383054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42639cea3cab7de07ec1902fbbad654bf3b518181c1a1d5d68bec88125d15b87`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:48:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:48:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:48:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:48:40 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 09 May 2026 02:48:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 09 May 2026 02:48:40 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:49:10 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 09 May 2026 02:49:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 May 2026 02:49:10 GMT
ENV LEIN_ROOT=1
# Sat, 09 May 2026 02:49:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 09 May 2026 02:49:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:49:15 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:49:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c851b38219aaa7b8bb1dc9df4fae07f486ef426ba65b2ac9fddc58f5530e930e`  
		Last Modified: Sat, 09 May 2026 02:49:48 GMT  
		Size: 93.8 MB (93781452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7d7d4407596d99ce90d341c22f0c265a9a0c736716ce8ef7d0683e0bc08dfe`  
		Last Modified: Sat, 09 May 2026 02:49:46 GMT  
		Size: 16.5 MB (16485342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11f5a1e4e67cd0d35ac99a96a20a4c8557fd3b72d3d8fbf389dffe401fdc51b`  
		Last Modified: Sat, 09 May 2026 02:49:45 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f170ac5cdff9ee39e788b1a0b5dc5550c0dd235820b278118a61505c5b0ffbec`  
		Last Modified: Sat, 09 May 2026 02:49:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:529b5e39224854877dd638128db5cf8c3a047fe4762017c6c057350d3c305ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60793cb77106e2f648a685af92cf7ebbd9298cc8fe1acb854b85ddf1c4dc3cc7`

```dockerfile
```

-	Layers:
	-	`sha256:05c4d2ab304def534b6a61bda977a04b5475d2bd82a1ec0a99dfb35f488051b7`  
		Last Modified: Sat, 09 May 2026 02:49:45 GMT  
		Size: 2.3 MB (2315208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b997b5062619729796f77a45ac34b523e629b230cc78eaf20f6d9d1f9b6899da`  
		Last Modified: Sat, 09 May 2026 02:49:45 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:5030f9bc612a4ffffab3022468c9719466bef84ce752a474173914e597a2cdaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141390008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a60a50a64c18a6d0c83b16ab6aafb8f972aa9c2d7895ed2f44e4e13561bfb9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:21:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:21:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:21:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:21:40 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:21:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:21:40 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:21:52 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:21:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:21:52 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:21:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:21:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:21:54 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:21:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3817b208f05ee63b0a9ce8a4a4cea90fec7bb6bb641467a82d11ac5bde2fac`  
		Last Modified: Fri, 08 May 2026 22:22:19 GMT  
		Size: 90.5 MB (90547679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce5b87fe145fbcfa7707f21d7ae73844ac2ae8a1996c5b6bcd4bdf36f4ae510`  
		Last Modified: Fri, 08 May 2026 22:22:17 GMT  
		Size: 16.5 MB (16483801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ca6a8a4a1e74d9ad5395fb5213d2014d55929b94cbdc96865fbc5ed556874`  
		Last Modified: Fri, 08 May 2026 22:22:17 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d973f7c5c16e1f652ec3b3db6bec591edf98a1cbf8eed3cf1c2f45bd9ce5e4b3`  
		Last Modified: Fri, 08 May 2026 22:22:17 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9db3107e419d204d9a13b7fa3c79270e52148f6c4fe79e81d7c524d8e9c3f111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f82c85917a5f452fa69d4283eda49346948d6542034f2a81c8784df3b1cb5c`

```dockerfile
```

-	Layers:
	-	`sha256:e032626aebffa94d344a8027dd33c6bede41a620dc4f7580e67106084748c61d`  
		Last Modified: Fri, 08 May 2026 22:22:17 GMT  
		Size: 2.3 MB (2311905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a9860778b035489ead4804fddd1b09151f56476e7e04c9d56a1b22a9c81f8d`  
		Last Modified: Fri, 08 May 2026 22:22:17 GMT  
		Size: 18.4 KB (18380 bytes)  
		MIME: application/vnd.in-toto+json
