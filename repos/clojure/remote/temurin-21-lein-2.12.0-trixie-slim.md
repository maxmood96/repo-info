## `clojure:temurin-21-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:0daa73abdb1dcc272538e9ecdda2cc02903322fa9da8c1dafc9d5340a71fc137
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

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3fc8787de83c0ac85208092d0a4b32e9436f5be0b088e789b751508f2abd9c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208543830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd37d38dc3d0467bf467fe96e492e2d576793f6b74cb9ac14969e94a10a37eb9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570de40485d2cf767e369327b9948c0459dc7812d9ef1ae4b00def51be0e0752`  
		Last Modified: Sat, 13 Sep 2025 04:59:15 GMT  
		Size: 157.8 MB (157804796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0fa7121f8adcb71c892bbf06ba442e990f0ccaa69e21ee3d0c2171fb882a49`  
		Last Modified: Sat, 13 Sep 2025 00:11:33 GMT  
		Size: 16.4 MB (16447353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796b0ddc1bf7db139b0890757fead70979436f489080f3fbe2b1e991676539ef`  
		Last Modified: Sat, 13 Sep 2025 00:11:33 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846c50870c362d5ba3d9e71f6d6eaec0da37a9575f96148985401a3e080e7704`  
		Last Modified: Sat, 13 Sep 2025 00:11:32 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:45713dbea2bf3763f4231fa79f94aeadd906109429aa0fbb2b7a0f17ff92d8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5163f20034617c90a0fd599822a26ab15ca689acaba05b63a956d79ed2f02e34`

```dockerfile
```

-	Layers:
	-	`sha256:ba8407293e1b9c86dd5a345977b001b3cf7d6cf9ada307905372e83d759cdffd`  
		Last Modified: Sat, 13 Sep 2025 00:35:22 GMT  
		Size: 2.4 MB (2367144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ecc7cb74ec128908157e672a49ab715fc98bf173a2b7d1d6a1cb15630f3c383`  
		Last Modified: Sat, 13 Sep 2025 00:35:23 GMT  
		Size: 19.1 KB (19084 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0d0b3836951d773731dd5d836ff63f2a2032307bc9efe2cdc0d35193a58fd908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.1 MB (207149506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f7651ca7d7ecf02c1174e97825644418d4e2f1ed9961a95bc273e969307e19`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed6c705219127c15e4485cd83d07a5d15bb63e212a342a3f2537761d913f1cb`  
		Last Modified: Sat, 13 Sep 2025 00:16:16 GMT  
		Size: 156.1 MB (156081182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bde23b48e0532d48278cda144771505741d40bb760dcda5035a13f490a2e14`  
		Last Modified: Sat, 13 Sep 2025 00:16:34 GMT  
		Size: 16.4 MB (16413555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8956acf464f72707dee2125398b0ea58d47f92d47df240f14b3322ffe3737a48`  
		Last Modified: Sat, 13 Sep 2025 00:16:33 GMT  
		Size: 4.5 MB (4517708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e04f7b7be8d8902442d86899afeb88d11cedecbdc380512ce37b479917839c0`  
		Last Modified: Sat, 13 Sep 2025 00:16:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:015d7dbc755252f04312e9e79d9c1e5ced9d941d26ece51d6f321c1735e02d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a96553130747bf9c6a97c27bc11781c175bb466f3177696d6b4f1b7efed9b7b`

```dockerfile
```

-	Layers:
	-	`sha256:f3e68f9a3eac5f789d9a65e442eed080a8205b4a69bb3a259e9f4086820f2f76`  
		Last Modified: Sat, 13 Sep 2025 03:35:05 GMT  
		Size: 2.4 MB (2366786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da77eae6774ce385fa04b9cbb883846406226e84e702a352e80e239dee29e897`  
		Last Modified: Sat, 13 Sep 2025 03:35:05 GMT  
		Size: 19.2 KB (19229 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:444eb1fc4fb4710c4a289074e70c25a80298cb7732f538443d035494a2daa377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212562453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c389b001a6ef7c7fc3ed1d1cc56fbdb0c50583bca6410ffa53d14538ac2ca3b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961eb7ebf0035f6d398671677d350eb2f03bf73e15b167f039f8bd38980355b5`  
		Last Modified: Sat, 13 Sep 2025 03:48:15 GMT  
		Size: 158.0 MB (157963461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393a4e28236da5f0446d478e6d39c4c47b617fb5654b726f15f914154f5127a8`  
		Last Modified: Sat, 13 Sep 2025 03:48:37 GMT  
		Size: 16.5 MB (16486473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08157687d48ceb2d99c05cd37503ed47b3f1f7a8ddd6ab8d282f9034d4d9568`  
		Last Modified: Sat, 13 Sep 2025 03:48:36 GMT  
		Size: 4.5 MB (4517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f399506c8fac0dca5921c17008277b895b8d57d7097d36680c88f88af89cc167`  
		Last Modified: Sat, 13 Sep 2025 03:48:32 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8e5bbca825a2817011bdae81dc7c61b751106d79fd4b94f69ff4a61084573a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31dfedc67938330c1ac719f97d2c1f6417cae5802ce318cb6b8fcea100d37ddb`

```dockerfile
```

-	Layers:
	-	`sha256:c608973c61e9d584fbd9f410fa443fd555d403ed5db9bb07e48e20cea3454128`  
		Last Modified: Sat, 13 Sep 2025 06:35:05 GMT  
		Size: 2.4 MB (2368136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38fb4d5aa46a931d9770965c1ed9a5a4ff69cef04a5e1aa0f3d6956f70d569da`  
		Last Modified: Sat, 13 Sep 2025 06:35:05 GMT  
		Size: 19.1 KB (19140 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c1c9c5a659751e8744e31787cc8954d150cb83baa2c5a39f3a7c6ef554850f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197861820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977403ce7940c7c7a94dfbb9ca896c39425bf596cba3fd4578d14d601a23af15`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4c284aa571e77182f2d698660ed6e8ab6e5fbf5fa1bcbcf0017032e82225f4`  
		Last Modified: Fri, 12 Sep 2025 23:59:48 GMT  
		Size: 147.0 MB (147027059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770fca43264be177f9f1190393562db105ae606abaf3dd8e7393eb1cd34af6fc`  
		Last Modified: Sat, 13 Sep 2025 03:16:40 GMT  
		Size: 16.5 MB (16483718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d97e2114f086e798cc71ca26d3ec7d1f6c0d86a0210dacf725e656740e71dd`  
		Last Modified: Sat, 13 Sep 2025 03:16:39 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a34132ed266e7f432ae6461f5f994f25a1c9162dcdbf3e5b5ad62f2ce32d960`  
		Last Modified: Sat, 13 Sep 2025 03:16:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ce3b7ec7b5e657671323527f9a407a3f52f2650a621f3e4830b6d14df776f272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddd2104ec01b7fd1243abe052f69d7cb4ad7accc97050bef59f4f4724a8152e`

```dockerfile
```

-	Layers:
	-	`sha256:9573cb80603b17fbdfd8a7674f25c2229bef33580ff83b9a0956a7ec61759116`  
		Last Modified: Sat, 13 Sep 2025 06:35:10 GMT  
		Size: 2.4 MB (2363571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3426292e9823555e797d8ecae782ebb52fdd27ff704dc512e3b2ee8309d4a90`  
		Last Modified: Sat, 13 Sep 2025 06:35:11 GMT  
		Size: 19.1 KB (19084 bytes)  
		MIME: application/vnd.in-toto+json
