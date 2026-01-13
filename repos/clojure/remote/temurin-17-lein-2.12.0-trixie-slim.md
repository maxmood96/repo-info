## `clojure:temurin-17-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:612a33cd86e87564a11d12ac32080e23287cad7725141a8b0a4031fc73308e67
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

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f4544bd26b659c470ea7ee7960535db8547b182c5a89b7c0bf2b9f590c905b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195587096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01035277d8edce808c316195891319f66b7d02915c42fa4b13c4124739adb9e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:31:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:31:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:31:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:31:24 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:31:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:31:24 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:31:39 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:31:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:31:39 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:31:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:31:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:31:41 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:31:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1d59f6464533e209c9cdd150de02c47223e137fe641f9cf4cf9cd30c580291`  
		Last Modified: Tue, 13 Jan 2026 10:03:33 GMT  
		Size: 144.8 MB (144847951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45f7552f75358db84827d094ec8c7800fd30ad8054a17f8ca58be9a228b1631`  
		Last Modified: Tue, 13 Jan 2026 03:32:08 GMT  
		Size: 16.4 MB (16447287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1393363d3786f1991ade6fa7389129cc72691fb9f91da503afac8c3ed4793c64`  
		Last Modified: Tue, 13 Jan 2026 03:32:07 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927da4dc35c1894c32cd0e257d4f362e70a2f75f721850fbab604054ef521147`  
		Last Modified: Tue, 13 Jan 2026 03:32:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1eab17d34e40565a627e91d8e7aa61e97266cd7c4082d885bd5d3ca873c4b885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58343923672df887bd583ab446e1639a5c3681f29bb7094441811fd488dcae18`

```dockerfile
```

-	Layers:
	-	`sha256:3b23fdc37a7f98051cb86b836b58140899ccd6f3d3efbf70eb895577588628dc`  
		Last Modified: Tue, 13 Jan 2026 07:40:45 GMT  
		Size: 2.4 MB (2363500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46e2aaa8f47dddafce5c906349865390c12aa1dcca10b3ed925b24c07df4a451`  
		Last Modified: Tue, 13 Jan 2026 07:40:46 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:73602fa487593ab88d0de7f3ecff70ebbe22c153801041eed17670535496ff30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194746093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe8daa68593895d91920f98ee8afbdab4ab9a1bea38656021f5ba0aba4c2ff3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:34:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:34:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:34:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:34:38 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:34:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:34:38 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:34:53 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:34:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:34:53 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:34:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:34:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:34:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:34:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a246cec0e69e29858e4eb10b2f983c068b2ceff99b78a556efbe79ee01ba9ad`  
		Last Modified: Tue, 13 Jan 2026 03:35:15 GMT  
		Size: 143.7 MB (143679920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ad355eddda06906bf9d6faf7a9795a4069f30cec7785fee66f0d5c9654059a`  
		Last Modified: Tue, 13 Jan 2026 03:35:23 GMT  
		Size: 16.4 MB (16413942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3ddfd0e05e76354f7529714a16f13737771a5f7774655bff62a2cd0911ba01`  
		Last Modified: Tue, 13 Jan 2026 03:35:22 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62157f13d26c9de03cd1c6dc85c859061cd5130256e0d3fda5f11b1b5a496ef5`  
		Last Modified: Tue, 13 Jan 2026 03:35:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:611513ea1ea0fd4d5bcb4464a2b6aa725c2d9a89c929fb271e8381dc5f553f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753bee9f2d59abbdf855cfeae02213af8ece2d161a115e6e9e595450fd20e2d4`

```dockerfile
```

-	Layers:
	-	`sha256:e0f6326454d1804ff5ea9f026b8ba017d8be98d5af4de8c08ac109d009f25845`  
		Last Modified: Tue, 13 Jan 2026 07:40:50 GMT  
		Size: 2.4 MB (2363118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac6c3ac25df8606db3021cccc6435dd33be60a45ed4e178cb0035aa47badcc48`  
		Last Modified: Tue, 13 Jan 2026 07:40:51 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:bff5df8c6fd3f29d0eedd272eed0aeb3d363a9fa745846aba77cc5e7317f0812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199124489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f66e562c07c9fb61dc8177cb2b7a161a4ef9bd7b93822a3ead4f069dd6db25c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 05:42:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 05:42:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 05:42:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:42:48 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 05:42:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 05:42:49 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 05:43:37 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 05:43:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 05:43:37 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 05:43:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 05:43:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 05:43:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 05:43:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27844d738e02788c6b697812732ba5feb3fc1d5093e037428695dcbe90d378f0`  
		Last Modified: Tue, 13 Jan 2026 05:50:04 GMT  
		Size: 144.5 MB (144525242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1188bdf23ac705b15204573cedaa54ddab0ed8dc872236511707bee5d84a3620`  
		Last Modified: Tue, 13 Jan 2026 05:44:39 GMT  
		Size: 16.5 MB (16485460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fc568db772a925925979ece8495bc1ca0a07b237bc1dcd50d41713fefa647e`  
		Last Modified: Tue, 13 Jan 2026 05:44:37 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4a82485d95d3511ddc3170e2dab82000098edac84d8c9ef0c4c66cb251b9c1`  
		Last Modified: Tue, 13 Jan 2026 05:44:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fd21a230cb5d35b89b1763181c128ea531c22afe5b1cf7451f7399d89a380303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5857cbdd41d88b8d0547b7b7b6cdfc0889561c1761753560390c0d2b1209b5f`

```dockerfile
```

-	Layers:
	-	`sha256:6c0e80b47b2bffec2d7b17aa7e6dcd8fec178cf47ef1817178b6b2577039bbf8`  
		Last Modified: Tue, 13 Jan 2026 07:40:58 GMT  
		Size: 2.4 MB (2364480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dd07a89644635ce36e461673f6c77425ec483a338b90e7954d306a1066ed6b7`  
		Last Modified: Tue, 13 Jan 2026 07:40:59 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:732b9223d2291e0de32f48226ad671d6946075752deeeca7966a0cd8b0103b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191078794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcdc8bb0df493078b042e21029b6fb9f37f4a49555b4bd39b8cbe96f550ad86e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 06:35:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 06:35:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 06:35:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 06:35:03 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 01 Jan 2026 06:35:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Jan 2026 06:35:03 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 06:36:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 01 Jan 2026 06:36:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Jan 2026 06:36:32 GMT
ENV LEIN_ROOT=1
# Thu, 01 Jan 2026 06:36:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 01 Jan 2026 06:36:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 06:36:48 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 06:36:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c47e4b223479384cb91259f631c9c203246ef873e850a7fe5e6ff70d31329ee`  
		Last Modified: Thu, 01 Jan 2026 06:41:38 GMT  
		Size: 141.9 MB (141889571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0591ee09b2863914415e637a3ba7b7d5114b6a4955e460a07d0fc4a3b9f3b360`  
		Last Modified: Thu, 01 Jan 2026 06:40:56 GMT  
		Size: 16.4 MB (16397866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e85171745efb01db392846d6e6fe56b52bbd6d7b8211054c36949ed33e16378`  
		Last Modified: Thu, 01 Jan 2026 06:40:55 GMT  
		Size: 4.5 MB (4517798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8eb6db56aae90e171960e18f1ec188bddeb42891a4711e3a1673403d8a7c4c`  
		Last Modified: Thu, 01 Jan 2026 06:40:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:43147db8897a1a1a8c249abc857ebc749a9d8486097f91bac06d2d211816a1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2371998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad40619b0a0b68b799348bda9a8ab86df25a589c1ff2954411ee323bcdc9419d`

```dockerfile
```

-	Layers:
	-	`sha256:fe3b9be83ee0fdfd0a259ea3ac25871303bc85b5e9c10a7855061dd5472b7026`  
		Last Modified: Thu, 01 Jan 2026 07:35:29 GMT  
		Size: 2.4 MB (2353567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf800a7f03af0c78d4b017177f43ff2fd942884f7c790896d079f6e09582884a`  
		Last Modified: Thu, 01 Jan 2026 07:35:30 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c35f7f0a2d79a7547c523e427bedfa35a824826e86538f8f0564c4ff7ce4c6a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.7 MB (185693681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae61ff364e4e34ff6aa770675dfd3f58cb85e92e21c869cfc687f03ef97d90b5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 15:37:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 15:37:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 15:37:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 15:37:06 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 15:37:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 15:37:06 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 15:37:19 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 15:37:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 15:37:19 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 15:37:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 15:37:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 15:37:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 15:37:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e64d5ec2147af2d5c4761a51ff0030df1c3af8dbd9a803085548341f615872`  
		Last Modified: Tue, 13 Jan 2026 15:38:11 GMT  
		Size: 134.9 MB (134859069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae3a2822674ba1d711ed3c4c4a4ed70a294f34a6709031e7e39123de4065d94`  
		Last Modified: Tue, 13 Jan 2026 15:37:55 GMT  
		Size: 16.5 MB (16483062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334565a544a3604a766f983f7c10da5ede3cde70f131cae13b450745064463f7`  
		Last Modified: Tue, 13 Jan 2026 15:37:54 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5523b9ace15156abc9ceb5d21db3d73dc690c43c4c5442f4e5d698e5cf47364`  
		Last Modified: Tue, 13 Jan 2026 15:37:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:23afdc85d60ac5000abc563b8b39e492959507886f8e573d9cbc7521d7f2db75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3c6cf2826f4aae9874e0fd89ee7b5ed58369eb7318ecc02a9c4ae51c1ee05f`

```dockerfile
```

-	Layers:
	-	`sha256:b89570872b102b0a898a5e7831f062b21aead74358b826d09d4149292b77c366`  
		Last Modified: Tue, 13 Jan 2026 16:36:01 GMT  
		Size: 2.4 MB (2359927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98726b06d999c930d84a1717c373e4f6de22ab9a0d412ca8c85c854c7447f532`  
		Last Modified: Tue, 13 Jan 2026 16:36:02 GMT  
		Size: 18.4 KB (18386 bytes)  
		MIME: application/vnd.in-toto+json
