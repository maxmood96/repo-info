## `clojure:temurin-17-lein-trixie-slim`

```console
$ docker pull clojure@sha256:95ca235a71bc21c4386c3bb3c91cfc87c4ca0b32ab12e9edb4f52479b1e61587
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

### `clojure:temurin-17-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c75be7ff12ca1fee1d375dd232753112e13d664bf8c2178c16a1a4af7535b5a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195589792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2daf7d4398bff6f62190f1b25195a6502f075934c4953a5f60e95fc63a3717d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:58:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:58:54 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 00:58:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:58:54 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:59:09 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 00:59:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 00:59:09 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 00:59:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 00:59:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 00:59:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 00:59:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c1901db754e37b643a39343cb8305dcff5e821ece8bb233169a441355fe228`  
		Last Modified: Tue, 30 Dec 2025 00:59:44 GMT  
		Size: 144.8 MB (144847922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538a78911604f7f44d170ab5095c2b15d69de16d377ff4d62fbf96037235fa0a`  
		Last Modified: Tue, 30 Dec 2025 00:59:38 GMT  
		Size: 16.4 MB (16447149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22430c022410a34ef0161efa61f7a579ce0e0cf9146931390dee8c5e58b75f1`  
		Last Modified: Tue, 30 Dec 2025 00:59:37 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4ec031994d94bc5c3069915b22be85e44ad46ed79ac865aa5855578ddd4a56`  
		Last Modified: Tue, 30 Dec 2025 00:59:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ff30d66abf1f95857af88ebce075396f32f67c73983e89f6e8710e4e57c76be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4868cce201d73e30c663c059e084d917f81e4e700036592e1abc3882e3b2b79`

```dockerfile
```

-	Layers:
	-	`sha256:34004b8c30fa218d54a22f16702e8b45d28cfd18b4e8a88efc4e9863564b1f88`  
		Last Modified: Tue, 30 Dec 2025 04:41:08 GMT  
		Size: 2.4 MB (2363438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0341084a88e79da032b37be5281950da7038fef246c9a08daa87bfc3e408d388`  
		Last Modified: Tue, 30 Dec 2025 04:41:09 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:34b8981fe3241e61b4c892100d7574740256f611596c5e0f9c36e09243a30401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194750536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffe5d9e1dcba15dae90ee57c7ffe06e26073ce0cc6a7f6048029c9ca4064f86`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:59:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:59:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:59:55 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 00:59:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:59:55 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:00:12 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:00:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:00:12 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:00:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:00:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:00:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:00:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6333fb1275e3fcff1ec232f69ef464a04bf3ed28f6d6cc1b884d8e694326cd32`  
		Last Modified: Tue, 30 Dec 2025 01:00:50 GMT  
		Size: 143.7 MB (143679913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a48fe27cc6e1249cf6200c692938223502cb7dc88c1ccfb3df19b6bfff424d`  
		Last Modified: Tue, 30 Dec 2025 01:00:44 GMT  
		Size: 16.4 MB (16413844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1d408e15c8ad48723f63de19e6b7b82fa06dd5b6904e0b45971a5307673e8a`  
		Last Modified: Tue, 30 Dec 2025 01:00:42 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a35a0eef0509f8eaf90b95cb353e52b948322887b53cda6c67ab0d4c4f6be5`  
		Last Modified: Tue, 30 Dec 2025 01:00:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e148d000bc7cb19a72b98ec135ac0eb5f25ab8c8594d9cc86752d59216593dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e87d167444e9823687dfe405c065fcbcacec0f4d6a6a83c23e95f31fa585dde`

```dockerfile
```

-	Layers:
	-	`sha256:31c0fe271969de779dc76df2670286349cdc78e2506a97c2edc731a32fcfebb9`  
		Last Modified: Tue, 30 Dec 2025 04:41:12 GMT  
		Size: 2.4 MB (2363056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb31dffd972f0def56b5da4c17f58937c20aa0fac134434257ae2dd2c0b06cf`  
		Last Modified: Tue, 30 Dec 2025 04:41:13 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:40fcc815a180278b7e5463ec8c42c2d41e8c1a743409680db085e79fc13b8173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199125568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed12744279190ceefc970b8bcb5f0ac3b7e04000f55603b96d73b49880d9e7c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:51:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 03:51:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 03:51:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 03:51:36 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 03:51:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 03:51:37 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 03:52:13 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 03:52:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 03:52:13 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 03:52:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 03:52:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 03:52:16 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 03:52:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bf16378c0060db84f932d737d6c281316c915f7a3a4ce2efa43f2817d95192`  
		Last Modified: Tue, 09 Dec 2025 03:56:09 GMT  
		Size: 144.5 MB (144525257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c606804ebff95afaf5f23fc9add9f9b8bb5042fb2805bb645795e8d3284abecc`  
		Last Modified: Tue, 09 Dec 2025 03:53:06 GMT  
		Size: 16.5 MB (16485235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4d902365cb1fc47c28e0dd2b7472e308db7768ec4f4ed4bee6e5f2f67f5c79`  
		Last Modified: Tue, 09 Dec 2025 03:53:06 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c9b113ba71b113f389a5e1f8532934307f21053044689b21fad3b083d61e52`  
		Last Modified: Tue, 09 Dec 2025 03:53:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1611366e2385a870fe0a7ba6740935720334d8b5c082851ab19218c4db2534e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb3ab70f32d8496325b5faabebbd96dda6302ff00d8c005563caea2b9e53f34`

```dockerfile
```

-	Layers:
	-	`sha256:db08628792b59cb56dcb695bbe7f6ab525f41dcdc1ad43cc9bd7da96325dfd98`  
		Last Modified: Tue, 09 Dec 2025 04:40:52 GMT  
		Size: 2.4 MB (2364418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42bd5427389cab6d0e0f8fdcc6fedd49717903669c05c460748e68e330108b11`  
		Last Modified: Tue, 09 Dec 2025 04:41:03 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:966cf34941502ea5e0f35bbac79bbbde93c2aa5bcd07a1daed87e36d2d168f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191078813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64a7e7cf9b3b860dac55edaa21ea2ebe3678fb31e217c44d2e6d270db06192e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Sat, 13 Dec 2025 18:46:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 13 Dec 2025 18:46:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 13 Dec 2025 18:46:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 18:46:20 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 13 Dec 2025 18:46:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 13 Dec 2025 18:46:20 GMT
WORKDIR /tmp
# Sat, 13 Dec 2025 18:48:11 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 13 Dec 2025 18:48:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 13 Dec 2025 18:48:11 GMT
ENV LEIN_ROOT=1
# Sat, 13 Dec 2025 18:48:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 13 Dec 2025 18:48:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 13 Dec 2025 18:48:26 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 13 Dec 2025 18:48:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48c227efd13f09a34b153f418d7d540a21d31aecdd5fd15ad6529d2a559ad99`  
		Last Modified: Sat, 13 Dec 2025 18:52:43 GMT  
		Size: 141.9 MB (141889553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e6bb75cb8683761bd4618a655e2d7eeb56110742395aaa133a357439d94e48`  
		Last Modified: Sat, 13 Dec 2025 18:52:33 GMT  
		Size: 16.4 MB (16397879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa266f6685d3f68ad4e11e4c0e10e436e329038f00d7fb8e15d8d7b4a27fde9`  
		Last Modified: Sat, 13 Dec 2025 18:52:32 GMT  
		Size: 4.5 MB (4517795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb713f0cd22ef00ba52f038c47f5802640c61eb026845b85486018bb86020abf`  
		Last Modified: Sat, 13 Dec 2025 18:52:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eeb5883c511bb7ec0ed3d8fba1ad0adb286b4b96c0d2a5a24e62ac20b0aea01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2371997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cf4a5308e370d3ef57b93065c6fd24b4cadea099b760ed835296337da5cb5b`

```dockerfile
```

-	Layers:
	-	`sha256:45a813185dafe4e717e69be3837d9a6b128bf7176749e9a577677c80e34e8658`  
		Last Modified: Sat, 13 Dec 2025 19:35:24 GMT  
		Size: 2.4 MB (2353567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e6df7299b60d61099b52c2d99dde3330892a114530bb6601356f08cafcadf2e`  
		Last Modified: Sat, 13 Dec 2025 19:35:25 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:66773a9fcfa3dfa73801b615a3411371a1d0630c44af81100b9e78e49c29682c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.7 MB (185694618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b48a07d72c81cb78da63baaa5a873b3bc877b576cff581143c25856e2ae76b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 02:02:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 02:02:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 02:02:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:02:49 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 02:02:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 02:02:49 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 02:03:02 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 02:03:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 02:03:02 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 02:03:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 02:03:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 02:03:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 02:03:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d897bdc1fa613e96ab09f619b299b82896bea52ad484e0bad5fc9aba413ed88c`  
		Last Modified: Tue, 30 Dec 2025 02:04:01 GMT  
		Size: 134.9 MB (134859069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2545f476809a0307f0d561da4aa7362ade1d2eaa252f08d51e1fe218834eacb6`  
		Last Modified: Tue, 30 Dec 2025 02:03:38 GMT  
		Size: 16.5 MB (16482960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351fa2187a60abfd75ae772d1ccda43366dbea7fde9147d5307d5628cb606acd`  
		Last Modified: Tue, 30 Dec 2025 02:03:36 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd60a1c88777c1402e93f0f3f113a67f47911fb5d8d65bb0a99c208952366c90`  
		Last Modified: Tue, 30 Dec 2025 02:03:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:265a804d3d627aaa60a01ad008a62b374702a04609a4bb9dad6db7f21131a8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbc8523a093c9fbb01d16ef0bc06bc074cee745dcbe171858d32fd604ea3d41`

```dockerfile
```

-	Layers:
	-	`sha256:cde79fc43086919b6cb5ec784d07d5b05e8b1b835c4eca9cfd690fa02ac6665a`  
		Last Modified: Tue, 30 Dec 2025 04:41:22 GMT  
		Size: 2.4 MB (2359865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c6ecafb26dca0d35c7dd0a5848aadfd7d1a45990969d971bf08b2e412e57f5`  
		Last Modified: Tue, 30 Dec 2025 04:41:23 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
