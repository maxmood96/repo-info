## `clojure:temurin-21-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:42ba8f6e993cb326fa34a34cf3c932e8580c6365f60bec560a36fdfdbbcacfbe
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
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c6aa70fda217ede84008b918e11566e117cf5e1ff8f6d8d1b7393d604fef2b`  
		Last Modified: Fri, 16 Jan 2026 02:00:36 GMT  
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

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

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
		Last Modified: Fri, 16 Jan 2026 04:47:20 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

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

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; ppc64le

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
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
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
		Last Modified: Fri, 16 Jan 2026 03:34:33 GMT  
		Size: 16.5 MB (16485461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcf0edc473116a0e243e43fb61ff4be53eca39e46f27a5f5e5c8b80b2756e01`  
		Last Modified: Fri, 16 Jan 2026 03:34:31 GMT  
		Size: 4.5 MB (4517733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf07eb97b5e14107a458576a4082f1c80a732fe3f558f05ade81079541744de`  
		Last Modified: Fri, 16 Jan 2026 03:34:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

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
		Last Modified: Fri, 16 Jan 2026 03:34:21 GMT  
		Size: 2.4 MB (2367582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:988fc7fe1721aa3b1e0de76d295b6472bb34f25318c6c0e35f8882e3fd5ac8fb`  
		Last Modified: Fri, 16 Jan 2026 03:34:20 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:a06413c72c07d61e0e3329fb3ead91ca3d94d447c645d1f7f1bc6a7e7727618d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206382137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c0d9bd3fe865d6143e0a62ee7f70b6584ae2e00d878de0fb016ab0fb3d2fa9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 03:58:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jan 2026 03:58:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Jan 2026 03:58:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 03:58:05 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 22 Jan 2026 03:58:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 22 Jan 2026 03:58:06 GMT
WORKDIR /tmp
# Thu, 22 Jan 2026 03:59:35 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 22 Jan 2026 03:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 22 Jan 2026 03:59:35 GMT
ENV LEIN_ROOT=1
# Thu, 22 Jan 2026 03:59:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 22 Jan 2026 03:59:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 22 Jan 2026 03:59:52 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 22 Jan 2026 03:59:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:08:06 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ce3d8fe97e3f0f300cf6a379bdf8a6818893898d0842fdaef865eeba68c7ff`  
		Last Modified: Thu, 22 Jan 2026 04:04:03 GMT  
		Size: 157.2 MB (157194340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41a28d163708ea7d7dfccc19f791eed8c97abc8960d03006ce79712bd01f523`  
		Last Modified: Thu, 22 Jan 2026 04:03:42 GMT  
		Size: 16.4 MB (16397911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70147e8942b8894dcf3bc8586175a5a92433859a1236bd7eb4b30e1e91d9b0ef`  
		Last Modified: Thu, 22 Jan 2026 04:04:10 GMT  
		Size: 4.5 MB (4517770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1978bce5081256c41dd60049a163bc0e4e8183f7e084aabfd6f6a3c23fee0ba2`  
		Last Modified: Thu, 22 Jan 2026 04:04:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9130829ee88d8930691db7688e4a3ca560e2b15f8035bcf18dfff4d4e4ef8e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e9abd36848b4c8321c026151ba568bd14b2494b46c7c5a8d13b7cca1cf4d4b`

```dockerfile
```

-	Layers:
	-	`sha256:49415e4b8aa90d745344413d1c7af7dff752cd3ef5ca74a4f4b224e3faef115f`  
		Last Modified: Thu, 22 Jan 2026 04:03:38 GMT  
		Size: 2.4 MB (2358650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fa2948a16a1b175e1a80ff9f5f72670c58836762b3da1796363c31be83e9f91`  
		Last Modified: Thu, 22 Jan 2026 04:03:38 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; s390x

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

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

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
