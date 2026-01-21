## `clojure:temurin-21-lein-trixie-slim`

```console
$ docker pull clojure@sha256:df99c6f02aad4b76f0ebf4b251ba047eede24d50c18dc3725664f174cc8dba2a
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
$ docker pull clojure@sha256:d3d00977018eed0b63afa49fdae7fc81a71bca9e4ca4d5954c0cba2b1ed33e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208565165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d11ae48b55a641ddc4cea549382c36f7a345d31959066e904b2744cbfa033a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 01:59:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:59:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:59:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:59:27 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:59:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:59:27 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:59:43 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:59:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:59:43 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:59:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:59:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:59:45 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:59:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c6aa70fda217ede84008b918e11566e117cf5e1ff8f6d8d1b7393d604fef2b`  
		Last Modified: Fri, 16 Jan 2026 02:00:08 GMT  
		Size: 157.8 MB (157826005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d6c215fec9d778b2e26cc8753489f5a740d8b8aaaac5c5d8abca5fb110c9bb`  
		Last Modified: Fri, 16 Jan 2026 02:00:06 GMT  
		Size: 16.4 MB (16447296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86e3bc33e4734dbbc046702d570463341641b41f2c806a0c7d34d94943490ad`  
		Last Modified: Fri, 16 Jan 2026 02:00:18 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33701b706a82d8db211ae078f00becf7e9b38a9b5b2ea460703a676253066cf`  
		Last Modified: Fri, 16 Jan 2026 02:00:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1e6e680ab1e88b54d7fff7c333d80662499fd831ecb17c9dc76a36c77deac5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00cd3d0cbad76b91714ee556d2bbaaec76dfc3a43c5da1ccdec907ce075ed873`

```dockerfile
```

-	Layers:
	-	`sha256:999310fb5806bc98bb809c19b8fffd9ff2d9cf0187d4175ec8194846c326ae88`  
		Last Modified: Fri, 16 Jan 2026 02:00:01 GMT  
		Size: 2.4 MB (2366602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae26c2d76f422ab0aac047f8099d1824470c22de6662ccfa8a38312671c4692b`  
		Last Modified: Fri, 16 Jan 2026 02:00:01 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:87428936d08de110ebd81ba513335f88279230eb7c58a76b692e14676b3eeff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207173810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b2e934b71cd88dc931f468819507a6f44108b47fa6d06ed192ce921e97541f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:04:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:04:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:04:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:04:06 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 02:04:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 02:04:06 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:04:22 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 02:04:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 02:04:22 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 02:04:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 02:04:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:04:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:04:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cafb5a971b1ee814d44feca292438852d6e528b42a099971dc54232f02073dac`  
		Last Modified: Fri, 16 Jan 2026 02:05:15 GMT  
		Size: 156.1 MB (156107670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01b79369e4e024bcd3e7a16f5ec06f1d39e647a8a466ba84ddca357cfa067fa`  
		Last Modified: Fri, 16 Jan 2026 02:04:43 GMT  
		Size: 16.4 MB (16413929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947abfd4f260ccf9f860fb427a9dc6010031e15ced602fd800030d4e3bdf0b72`  
		Last Modified: Fri, 16 Jan 2026 02:04:43 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dcd6c35a9b35dc3e4ba7325b8e447841b98307eb5f747fbdef97cc73c47752`  
		Last Modified: Fri, 16 Jan 2026 02:04:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:365e0c9288c078ed4eb6adf3225ab96281ad02c0699ef75380fbc1c307ac3c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d6b104146f3af1e155afb4f6b89c730db6e3145b92a35f0aea175789b34afc`

```dockerfile
```

-	Layers:
	-	`sha256:f287b3d1e682a4d9634a5c6a4c755db3cbed399459e5f004811b42ee33934fc3`  
		Last Modified: Fri, 16 Jan 2026 04:47:24 GMT  
		Size: 2.4 MB (2366220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1018b0ccd3106bb4d5c2f2d30904cf1c89e7525d467316f5c2ef680ad6742ce3`  
		Last Modified: Fri, 16 Jan 2026 02:04:42 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1d199da81529806d9719926a1940cdaf4da083d69cfd3091484f1d25ae348624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212542190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2957b090d4b303bd5bcf2ba775e11e6aa40fc3aa021bb10d3660053c7300e088`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:32:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:32:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:32:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:32:35 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 03:32:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 03:32:37 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:33:30 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 03:33:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 03:33:30 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 03:33:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:33:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:33:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:33:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb8419d04d870182d92f9dd23172b44a59edb435e25623743b58a1807e6008`  
		Last Modified: Fri, 16 Jan 2026 03:34:25 GMT  
		Size: 157.9 MB (157942967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533c4fbbaa8e975bc0429ca07be97ff3f9cf83c1e7ff46128925443cab78ea9f`  
		Last Modified: Fri, 16 Jan 2026 03:34:22 GMT  
		Size: 16.5 MB (16485461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcf0edc473116a0e243e43fb61ff4be53eca39e46f27a5f5e5c8b80b2756e01`  
		Last Modified: Fri, 16 Jan 2026 03:34:21 GMT  
		Size: 4.5 MB (4517733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf07eb97b5e14107a458576a4082f1c80a732fe3f558f05ade81079541744de`  
		Last Modified: Fri, 16 Jan 2026 03:34:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1773201d5eecadf1f9c7f2f3e20c8f936de973e4bdf1b7bcedfe0536e1d0d2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab65bcb61f749e3da3f2c7319d265d655ceee0e3d2d68375b7e6f45f1470c4d`

```dockerfile
```

-	Layers:
	-	`sha256:40ad01095aefe1a3792c77b22572ed2bf43aa03540caea79cd60393cf681d209`  
		Last Modified: Fri, 16 Jan 2026 04:47:28 GMT  
		Size: 2.4 MB (2367582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:988fc7fe1721aa3b1e0de76d295b6472bb34f25318c6c0e35f8882e3fd5ac8fb`  
		Last Modified: Fri, 16 Jan 2026 03:34:20 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:2803d46f2bfa472966b2222fca5f8599ce3a66a31d949afef5e1b38b04d3d371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206383512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdca38adfa0107b29164d2fef99e1dae3c5faf99c70b1dbded43829216ba08b8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 07:02:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 07:02:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 07:02:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 07:02:49 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 01 Jan 2026 07:02:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Jan 2026 07:02:50 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 07:04:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 01 Jan 2026 07:04:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Jan 2026 07:04:18 GMT
ENV LEIN_ROOT=1
# Thu, 01 Jan 2026 07:04:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 01 Jan 2026 07:04:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 07:04:35 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 07:04:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:14 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091162d898a2d4e7b50f7bb9588aeb36e7979c2a93097ad0bdcd2473aa01fb84`  
		Last Modified: Thu, 01 Jan 2026 07:09:19 GMT  
		Size: 157.2 MB (157194291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8287ad8a14910988816ff3b67e28645e2d2b3201648b8cccccf52952ed27b9a3`  
		Last Modified: Thu, 01 Jan 2026 07:08:37 GMT  
		Size: 16.4 MB (16397852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4680422d3a15eed5753c613e8f36f58302302a629757877840cfc3f14d8e63`  
		Last Modified: Thu, 01 Jan 2026 07:08:34 GMT  
		Size: 4.5 MB (4517811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b76f537afe0360d541b762c58c1909c154fa78a592ddae382498a59fbf912b`  
		Last Modified: Thu, 01 Jan 2026 07:08:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:38209183e8f547417d164a415860204f5227dbedf3aff30991f0fed0bae1cc0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec04403c029e300b2394b030e5a176cd3209e400e8552327380c4e3be81d7187`

```dockerfile
```

-	Layers:
	-	`sha256:dd3f659dd3a821814abbc6cbc57a56b364bef2e8ce3d4c73fe41dae4b75d8bd3`  
		Last Modified: Thu, 01 Jan 2026 07:08:32 GMT  
		Size: 2.4 MB (2358588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:706fd3a476b4e1a72ab3151d52bda6113c29b85602039a09b959cb7948f9f9bd`  
		Last Modified: Thu, 01 Jan 2026 10:36:42 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:780e72bcd0c49bd3c4b2967d67eac9aa82af64afa72b9127942fe2ca71ceb10c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197904393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44236c8cbcc1e60f70cb9322f8cfeaa94725063a926d5d803edc9defce2925f5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:19:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:19:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:19:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:19:34 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:19:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:19:34 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:19:45 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 15 Jan 2026 23:19:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Jan 2026 23:19:45 GMT
ENV LEIN_ROOT=1
# Thu, 15 Jan 2026 23:19:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 15 Jan 2026 23:19:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:19:47 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:19:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e307e5df525a8baf85f7de5a221c6604e3d80753489f585e9dde342af99154`  
		Last Modified: Thu, 15 Jan 2026 23:20:32 GMT  
		Size: 147.1 MB (147069858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1b9a3a9ca2ca930e1481c72fb487b843751e684e50bda5a0e4a23537c5b4da`  
		Last Modified: Thu, 15 Jan 2026 23:20:11 GMT  
		Size: 16.5 MB (16482988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7b5390d24c1eb7970bdf83e8d25ee55d4f0eadba790583c15c84e181df7d96`  
		Last Modified: Thu, 15 Jan 2026 23:20:20 GMT  
		Size: 4.5 MB (4517708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a63f6659c70d9d19aeda1a650f308cdb70d53d393a7460998d5f9921119555`  
		Last Modified: Thu, 15 Jan 2026 23:20:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:47ba1d6e0f160609d207393f18fae066766a56a3de737a8aa00b338b6ee6c86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2b90260efc642473b72eea2f101735e0d995cee01fde0e7b2d073d4f4cc45e`

```dockerfile
```

-	Layers:
	-	`sha256:b67b57ee9008d6bfa48554b6a0531e39d53f10c2fe1312e7ee0bd1b98164e727`  
		Last Modified: Thu, 15 Jan 2026 23:20:11 GMT  
		Size: 2.4 MB (2363029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dbfd53ea32c52826bab375f03a17150616126ed5cc6bfd359e8b7614ca4d0a6`  
		Last Modified: Fri, 16 Jan 2026 01:42:21 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
