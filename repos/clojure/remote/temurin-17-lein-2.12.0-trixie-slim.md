## `clojure:temurin-17-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:6c3a348ef0077741d53cb95a0292d96f982b612d10e018430babbcdb8d1638e5
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
$ docker pull clojure@sha256:8e0a6a4fda86a173ef3a367ceb7de2d0137c6ddd9618f848c863f73d7eb8902d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195589707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf1af860ad7cf6810a1b9196d1745019bbd4b4d3ef997493adec708a41c74d3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:53:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:53:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:53:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:53:17 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:53:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:53:17 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:53:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:53:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:53:33 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:53:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:53:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:53:35 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:53:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bf45e9c56c31c00b25ec0ded6c31a5c14de6ffdf972c0b4635e19122614ddb`  
		Last Modified: Mon, 08 Dec 2025 23:54:14 GMT  
		Size: 144.8 MB (144847946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434940ae3633702fdfb8ad75128d604936f9d1f4dbab6e40697d1a725d48e5a3`  
		Last Modified: Mon, 08 Dec 2025 23:54:01 GMT  
		Size: 16.4 MB (16447095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4231eaf679bd0a037b37d342e835cc8611cfd681880b3235319a87c1376f51b5`  
		Last Modified: Mon, 08 Dec 2025 23:53:59 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff3e04a1e60e526b48f36a9eedfcf7503bce4212409fb73f4e6511fe1b62ecd`  
		Last Modified: Mon, 08 Dec 2025 23:53:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:df4043f204fdbbdacbe434b815d22cd25ab32b31841182095268d997a527e65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab89d1dc7ef191d3b368eb266bc92125d768e5b47b1e19dd9a85205e8642af2`

```dockerfile
```

-	Layers:
	-	`sha256:178e501911e45c4003d9886d03b824e06d405956776147dc45ce9867e7524333`  
		Last Modified: Tue, 09 Dec 2025 04:40:42 GMT  
		Size: 2.4 MB (2363438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a9c9cfeb08072e9eb0a046782cbf4d18ea5cec6278c459c7cdb44d8d43b719a`  
		Last Modified: Tue, 09 Dec 2025 04:40:43 GMT  
		Size: 18.4 KB (18384 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b41cad3f42c8df758c8028db0d842c9511134ed0d963cbb82a82cd300eccc911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194750471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873549a2eefe94ac5eecef59dcbb3d28fcb44c8f83a0ba68de388dcd3146e040`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:00:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:00:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:00:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:00:42 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 00:00:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 00:00:42 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:00:58 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 00:00:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 00:00:58 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 00:00:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 00:00:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:00:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:00:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7729f7607dd19bdb70713313992980a86edf47836b7e54fb38f2e630e94d48f`  
		Last Modified: Tue, 09 Dec 2025 00:01:20 GMT  
		Size: 143.7 MB (143679910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bc1ab636cc90ac0fa35005e19a1aef2ef77842f7c9f888c8d803ee21dbc181`  
		Last Modified: Tue, 09 Dec 2025 00:01:26 GMT  
		Size: 16.4 MB (16413794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6668142cf244de001f28a3d39b3cb1a3b30e8aa27e0a3d5cebed9421d58cd7eb`  
		Last Modified: Tue, 09 Dec 2025 00:01:25 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e248b28d3b77926214286b5402b52cd58dd181745a5740798abf9896364114db`  
		Last Modified: Tue, 09 Dec 2025 00:01:25 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c31d57eb927b3cfab7502eb4a467801bcad6a93094eee93f1847bd20a6f77771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e866d5a9aa628ed46bd1de26e37b9e62c9f33fdce7b8d4943f96323d11bd3bb9`

```dockerfile
```

-	Layers:
	-	`sha256:31208108dc9a5160f9663b779d66cce45f8e11a8ae3b02b2fa53bc5b33d13197`  
		Last Modified: Tue, 09 Dec 2025 04:40:47 GMT  
		Size: 2.4 MB (2363056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfee042816db2f2be65217514c6b11fa480693a9d326a685d29f6adfa93db01d`  
		Last Modified: Tue, 09 Dec 2025 04:40:48 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; ppc64le

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

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

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

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:b1a80a8117dc04fc5be6c5eef6fd975dfe5272451b345a44d5d58c3d7419093c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191078777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6b0e21464a7df63ca6d4417591b1f14e574806c96de1ca0e62b7ddb4fd1b46`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 17:58:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Nov 2025 17:58:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 20 Nov 2025 17:58:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 17:58:06 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 20 Nov 2025 17:58:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 20 Nov 2025 17:58:06 GMT
WORKDIR /tmp
# Thu, 20 Nov 2025 17:59:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 20 Nov 2025 17:59:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 20 Nov 2025 17:59:34 GMT
ENV LEIN_ROOT=1
# Thu, 20 Nov 2025 17:59:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 20 Nov 2025 17:59:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 20 Nov 2025 17:59:50 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 20 Nov 2025 17:59:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d74684f217d805ec7013972d089a9baa3e158cc8603592f0e9ad77ff195488`  
		Last Modified: Mon, 24 Nov 2025 10:03:10 GMT  
		Size: 141.9 MB (141889576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7d70e98f969d860109ed6f2ecfd566bc9476ba24cd78021946b677638e57e1`  
		Last Modified: Thu, 20 Nov 2025 18:03:51 GMT  
		Size: 16.4 MB (16397848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd61d43029dfc2e57a4c10d9515b742a50cd51f77d8bc2ddbb17a069710a6313`  
		Last Modified: Thu, 20 Nov 2025 18:03:57 GMT  
		Size: 4.5 MB (4517797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c772892cded581cae2d9cb440de63a40ab8556113e3ebd34662454a71abca3f5`  
		Last Modified: Thu, 20 Nov 2025 18:03:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7148ceca45478fb8e7a07ce85b52370be491f39de7a808d77e0f7cb49855d628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2371996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c030b9005fda5df9d1a153ae5aaab64374dd55d3f462bbed93cf56ee7d767fd6`

```dockerfile
```

-	Layers:
	-	`sha256:6eec10e416a7770b0f8ec56a30e004ea476567022090a7b02aff9a7634d9bc19`  
		Last Modified: Thu, 20 Nov 2025 19:35:40 GMT  
		Size: 2.4 MB (2353567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90d8fe1d817dfcfc7e2352cff1ea6c92f28741ecba5347aacb9633519a4604f9`  
		Last Modified: Thu, 20 Nov 2025 19:35:41 GMT  
		Size: 18.4 KB (18429 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:60875199727e2316e3a6d9ecc1e92c298be1c1ea3b48ff90afbcd382f861c6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.7 MB (185694621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454f8dc0e44cfee3d3957e4e2daa9a5e6c7cd717e283d8f611cdd1cfeec06117`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:28:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:28:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:28:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:28:50 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 01:28:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 01:28:50 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:29:07 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 01:29:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 01:29:07 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 01:29:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 01:29:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:29:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:29:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3260fdadccc7546154b4e7a7be47bf1049c46ad309ddf771b36f324535df05`  
		Last Modified: Tue, 09 Dec 2025 01:29:54 GMT  
		Size: 134.9 MB (134859033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7c8845a3331340f8debd16593a48858cd4cf3af52e3781d3998f33926a92f9`  
		Last Modified: Tue, 09 Dec 2025 01:29:43 GMT  
		Size: 16.5 MB (16483033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3076c47296552b6dfb7eaf5e0c5fb9a91e11960d74c4ee4c2656cc39144e53`  
		Last Modified: Tue, 09 Dec 2025 01:29:42 GMT  
		Size: 4.5 MB (4517727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0bcf211eb2d1f6fc198f7fbe313b162572b25d42e369bb31a4cfaf5012505d`  
		Last Modified: Tue, 09 Dec 2025 01:29:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b353b5d68e81909f9b72fb056181d299b34b6fac0c42acd000b4be5320e1bff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ecd7aa5bf194d5201719e388550e4ef8c31825aac75ce9c3d7eb4174371321`

```dockerfile
```

-	Layers:
	-	`sha256:c2af029685f7d4b0c8cebd138bad4e25c8b1220266e7335fb2f2c264ceeb9d42`  
		Last Modified: Tue, 09 Dec 2025 04:41:10 GMT  
		Size: 2.4 MB (2359865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aa3f79534a9dffb01588915ec9abe37a00938aaf16b8733e2cc6dc95f76cb6e`  
		Last Modified: Tue, 09 Dec 2025 04:41:11 GMT  
		Size: 18.4 KB (18384 bytes)  
		MIME: application/vnd.in-toto+json
