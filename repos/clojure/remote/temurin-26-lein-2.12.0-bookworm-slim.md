## `clojure:temurin-26-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:7ad4e101f651a997b59c1a97eb1b6352602d61b485833f5a2b6a0bc2ce35cb5b
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

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1828c197ff05dcc4dcdc631cf90902a2981797963bfbbb212af9f108a62163d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (145038348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ad3be09dc56cb566875819ff7d2b26c11a825ce140863d3bbb0037344370de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:35:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:35:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:35:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:35:58 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 20:35:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 20:35:58 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:36:11 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 20:36:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 20:36:11 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 20:36:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 20:36:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:36:12 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:36:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beb66aae2a3010cf959df724ce1558d6f43e469d67c48538b0bf0001178a5db`  
		Last Modified: Fri, 15 May 2026 20:36:32 GMT  
		Size: 94.5 MB (94524372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21175e98f410cccdaafe737cabd102a801a73beb78be4ad2fbc54ab2ff3ab144`  
		Last Modified: Fri, 15 May 2026 20:36:29 GMT  
		Size: 17.8 MB (17759550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f75024492684d0aca374a40f61f022097a721fddd04706419814f98e007a68`  
		Last Modified: Fri, 15 May 2026 20:36:29 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13691ce8374d0cd6cf8db14f5743f27cbb4397b3c93ca455810ca0bb93ede0f9`  
		Last Modified: Fri, 15 May 2026 20:36:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4acdbee364276047478dcaf096e84d4e5ab4fc7679ce08cd061093aa539c36d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2714118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b34ce100ee776ce076b28dec0efadfe31300a159808a5561d34ed8fd86deea`

```dockerfile
```

-	Layers:
	-	`sha256:4209def457f094147930049f0139676e5a93c7cf07379703c6998854bfb20230`  
		Last Modified: Fri, 15 May 2026 20:36:29 GMT  
		Size: 2.7 MB (2695568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee706a9ef59f9b803a87d03a6126a9fc630be10a72996f4bb7eaf2c6691491dd`  
		Last Modified: Fri, 15 May 2026 20:36:28 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:25c14a291a421a0a2fefecb16f036989663ce07f3f88da01959172882132fcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143731775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f069226f0100d4fe3c6089235f9bd43128d232f3d394fb66609a8709b610be`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:35:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:35:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:35:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:35:57 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 20:35:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 20:35:57 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:36:09 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 20:36:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 20:36:09 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 20:36:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 20:36:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:36:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:36:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7405bb9216868a405b56cc0634aa51965443ef7c830610334ab92583fa3b7e64`  
		Last Modified: Fri, 15 May 2026 20:36:30 GMT  
		Size: 93.5 MB (93504390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ccbd3fec687fa1eddba8f914359b2ffbc1d93d0298bd5cbe93ea547130b3da`  
		Last Modified: Fri, 15 May 2026 20:36:28 GMT  
		Size: 17.6 MB (17593061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e766bf8d6de26f7bab7e8a01ef9bd3f19e27ac285c642bf6111a9b7b56e94de1`  
		Last Modified: Fri, 15 May 2026 20:36:28 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b648f622f8c1606f8218ed7c5465237d7eafb1405418f64c44665f459a6860`  
		Last Modified: Fri, 15 May 2026 20:36:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3d55502fd9b4162d3fcc1c755d12d2da97f4ed914797540d453889c940efaf72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2713851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a844a99c110bc2a10bb222b6ea7c97da3847dd94dbb165efba92286cddbd55`

```dockerfile
```

-	Layers:
	-	`sha256:e72b0dcbe28b16c51e45c4bc6a64178695efaa700a051e14e45168b323ddee42`  
		Last Modified: Fri, 15 May 2026 20:36:28 GMT  
		Size: 2.7 MB (2695180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01a12648baba25b0156cecb7de09552f501c3054e8d97b70cd8a5ab2316290c0`  
		Last Modified: Fri, 15 May 2026 20:36:28 GMT  
		Size: 18.7 KB (18671 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e8efb270dc63a01450fb2c2e670782a5a1a6ff36731142bbc51d721ef89b9032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148460010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcacc4a6981defd88b55930dd0d588f2714e4a7f7e909148660dfbc8fff98ca9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 21:45:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:45:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 21:45:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:45:51 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 21:45:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 21:45:51 GMT
WORKDIR /tmp
# Fri, 15 May 2026 21:46:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 21:46:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 21:46:31 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 21:46:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 21:46:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 21:46:36 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 21:46:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fd299d196bbbb90b619a2efbdb555a0daabbf409ed235c488e800b3c6f94e4`  
		Last Modified: Fri, 15 May 2026 21:47:13 GMT  
		Size: 93.9 MB (93902030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b74426afd6f23fda8046029dab28bd6bc6dde70d5848b4a834850681a7a3873`  
		Last Modified: Fri, 15 May 2026 21:47:11 GMT  
		Size: 18.0 MB (17961389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2cc3f8f0bad6135352d2c3a053849add47844a0e3717ddd9a19d389a7faddd`  
		Last Modified: Fri, 15 May 2026 21:47:11 GMT  
		Size: 4.5 MB (4517708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eac2175226431ed76ae9d12f17a26143857b854f8eba499aeedffb61db5106b`  
		Last Modified: Fri, 15 May 2026 21:47:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ba5b155c859649a5e1101b3dcc2d625b636fde33e3040032c3afb2638be45c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4cb7d1bca29ff996b9228050f49dc9091f78b8778e16fe83fce4ccf9e09708`

```dockerfile
```

-	Layers:
	-	`sha256:b584ef35b11547f100c52a1babef679991838429f8033167200a3a31ad5a9512`  
		Last Modified: Fri, 15 May 2026 21:47:11 GMT  
		Size: 2.7 MB (2681337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31d87baa6eed9903296b85f450881c7b8e090046ad38e3110ef916b5b047e71c`  
		Last Modified: Fri, 15 May 2026 21:47:10 GMT  
		Size: 18.6 KB (18594 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ecb4fce938025fcf8d9d72a692a684ccc2113d57f0108af24365ce2fa597ce13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139368921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68cec53473cf6acba4a7590c4528f5dacc6e011bce136a01f05f0cd19afa380b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 21:29:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:29:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 21:29:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:29:10 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 21:29:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 21:29:10 GMT
WORKDIR /tmp
# Fri, 15 May 2026 21:29:43 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 21:29:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 21:29:43 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 21:29:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 21:29:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 21:29:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 21:29:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfab53db9f0cc17ffff5864e26eda68d07663829af4b95b63bc4073b1f3451c`  
		Last Modified: Fri, 15 May 2026 21:30:23 GMT  
		Size: 90.5 MB (90536962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99f0711eefaf572bcb5beda5a8e1edfb348d39bb3369122e85415783e8c46f4`  
		Last Modified: Fri, 15 May 2026 21:30:21 GMT  
		Size: 17.4 MB (17422176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b889ad88f2d74a31d16f1ff40a27c51358b18e987c4e015db94ae61cf48cb0bb`  
		Last Modified: Fri, 15 May 2026 21:30:21 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288ccad30bad04a642e07a86d5de64acd62662cc9822fa8e48e20a8b74c213c2`  
		Last Modified: Fri, 15 May 2026 21:30:20 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8e91642347d2bbf721d7a5ee258d0980480f75313e4f18a2928559ec4a5bb88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b01ec5e77168b13f6d5b1a29a9b37902928fde00b2731ce1c5ae319bf3a51d4`

```dockerfile
```

-	Layers:
	-	`sha256:6681da9b9fd6d8b2b5b8136f4d2a1dfbca1d53dfd50dfdd3cac286b557af89b5`  
		Last Modified: Fri, 15 May 2026 21:30:21 GMT  
		Size: 2.7 MB (2672568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7aca18ffba3f9647f3e3685f2ff8249725b3b7e58eee770e2bf5e44bceca621`  
		Last Modified: Fri, 15 May 2026 21:30:20 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json
