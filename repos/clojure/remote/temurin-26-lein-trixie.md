## `clojure:temurin-26-lein-trixie`

```console
$ docker pull clojure@sha256:3595dc0649f5de3d0cab2c66f15e9ae974e066e21a6d67efaa3740040dec0d6b
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

### `clojure:temurin-26-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:43ee95ffb600ea84030ca43dbf64ce34666a871c31883a1d90c8b2312ee8fb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166861485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0621876769a275842734e04e9cc745b5a0a6a8ae09e648ae44400ae543054bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:21:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:52 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:21:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:21:52 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:08 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:22:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:22:08 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:22:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:22:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:09 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a2baa2ab541dab5d585354ba3229388686582f5edab3c11f4f639c2171bb9d`  
		Last Modified: Wed, 22 Apr 2026 02:22:29 GMT  
		Size: 94.5 MB (94455691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51696d54979af5ad60097b88807b3ad69ffbdc61072c8311e726cf3a0aa24d8`  
		Last Modified: Wed, 22 Apr 2026 02:22:27 GMT  
		Size: 18.6 MB (18585565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523dee10cbbd6e113d25d5e8d7e4ef7f876ae6a836c19a553af64d47a682ccfe`  
		Last Modified: Wed, 22 Apr 2026 02:22:27 GMT  
		Size: 4.5 MB (4517699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36ceabb14d7e9930eb10c18b135f0650595e8275d2c9c7ed36be79e941b45dd`  
		Last Modified: Wed, 22 Apr 2026 02:22:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7390ba9c534f395f28057121dae9d0d57fe66290fae652f01a3197dcdd8ec7c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc1be9ffb94053418c859b7b92d1fbfac3f837537e2e006107093576230c56f`

```dockerfile
```

-	Layers:
	-	`sha256:adb63d2f801cd035cc3484aaf3956541e3469a9fdc487eaeb1b8975fb0afe708`  
		Last Modified: Wed, 22 Apr 2026 02:22:27 GMT  
		Size: 3.8 MB (3781031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0a0d1b59ac59af485b2d90fafd4da7bf0cbfee4cac757571c2d217e7cd1a2b1`  
		Last Modified: Wed, 22 Apr 2026 02:22:26 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5f52051deaf33890b1233d7964207adb55a3f41b618d49f97ff210ceff81dcdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.1 MB (166127996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d950d390cab5d0552059acfa6cd762434cd8e40dc25806d10b46b5bad97f2f66`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:24:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:24:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:24:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:24:44 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:24:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:24:44 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:25:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:25:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:25:00 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:25:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:25:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:25:01 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:25:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64ec9bd3c225b4559d3b951c3bb892075be0a9cadd29154dcc04d7d3d68931a`  
		Last Modified: Wed, 22 Apr 2026 02:25:20 GMT  
		Size: 93.4 MB (93395169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72584a8f8103e8aa24fae9eeb8b43c69d46d370f264a19bd6cae5331b0a4eceb`  
		Last Modified: Wed, 22 Apr 2026 02:25:19 GMT  
		Size: 18.5 MB (18545445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5201003bc864112539d9403f74e758e2ce3ea9eb02ad302cc069af51a8fba5`  
		Last Modified: Wed, 22 Apr 2026 02:25:18 GMT  
		Size: 4.5 MB (4517709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e22e4c8466b79fd348fb989559b85c1da5990af733a19f905b246386e9daf76`  
		Last Modified: Wed, 22 Apr 2026 02:25:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:63a0689eee396ff0c09dfcd940d2e337b25814a35e39d75dc836005231aecd9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789cf802eae90e56d7a0eb429f1c77a0d66aa2489398730be2c9e95274c3fdd0`

```dockerfile
```

-	Layers:
	-	`sha256:0262f52cf7c4b922991da4b457efa62ee5e3c0de6f164c394b397156494b4aca`  
		Last Modified: Wed, 22 Apr 2026 02:25:18 GMT  
		Size: 3.8 MB (3781905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebc929173cc42978d2230ce8b01ad0f94df93002079d74799a49312444ebb9fd`  
		Last Modified: Wed, 22 Apr 2026 02:25:17 GMT  
		Size: 18.5 KB (18466 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d610ec23f876dcdfc94e4a1872c90ea576bcfcd5c493812966cd5751ed43d652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173809975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5e5e907f2cbad4f1e604cd875e6203b1c4c80a37634e185943c9f0ce725954`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 00:52:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Apr 2026 00:52:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 10 Apr 2026 00:52:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 00:52:59 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 10 Apr 2026 00:52:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 10 Apr 2026 00:53:00 GMT
WORKDIR /tmp
# Fri, 10 Apr 2026 00:53:41 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 10 Apr 2026 00:53:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 10 Apr 2026 00:53:41 GMT
ENV LEIN_ROOT=1
# Fri, 10 Apr 2026 00:53:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 10 Apr 2026 00:53:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 10 Apr 2026 00:53:45 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 10 Apr 2026 00:53:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfcead13693a6857ab51b621e372876765c71adf46e88c3448e530a15832886`  
		Last Modified: Fri, 10 Apr 2026 00:54:22 GMT  
		Size: 93.8 MB (93781469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939f9b59dcc310bae2886a3e5b887d515998e62f1a67fc9485867652470543d7`  
		Last Modified: Fri, 10 Apr 2026 00:54:20 GMT  
		Size: 22.4 MB (22391662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e0880bb9273b3389fbaca34c3c3adafdeb8f78b6f06f93cb5c2e28b9544746`  
		Last Modified: Fri, 10 Apr 2026 00:54:19 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7ed19e2a8c8930045aed379951930b0d583eeca80929513eb43ef936e60997`  
		Last Modified: Fri, 10 Apr 2026 00:54:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:12fbde7cdc265274fdbb66c2644f446c2547bf54da85d32eed10555352a1ceb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0a23cb3a8ebd6e4995efe182dfa1f4b9c3f81001dc8bd33940cebf68652ff5`

```dockerfile
```

-	Layers:
	-	`sha256:8e507514efe3f8524adbcdc02d3858d0bc2d2f49409896853c62777e71f729e1`  
		Last Modified: Thu, 16 Apr 2026 03:16:15 GMT  
		Size: 3.8 MB (3765967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ddd7b1ff76881a5a776f0928c79e45cff6ea6052725d6a19b9e08797e705aa6`  
		Last Modified: Thu, 16 Apr 2026 03:16:15 GMT  
		Size: 18.4 KB (18389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:e250cf8e28a191465eb8f239b04007d7e72f98d34797dbab43f600881d3d3e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167015124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93c81816c90e0a5c79f8aca38630af8fafd9a96b7ce8826df26fc35e2ca6b48`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sun, 12 Apr 2026 18:49:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 12 Apr 2026 18:49:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 12 Apr 2026 18:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 12 Apr 2026 18:49:16 GMT
ENV LEIN_VERSION=2.12.0
# Sun, 12 Apr 2026 18:49:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 18 Apr 2026 05:53:46 GMT
WORKDIR /tmp
# Sat, 18 Apr 2026 05:55:21 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 18 Apr 2026 05:55:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 18 Apr 2026 05:55:21 GMT
ENV LEIN_ROOT=1
# Sat, 18 Apr 2026 05:55:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 18 Apr 2026 05:55:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 18 Apr 2026 05:55:38 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 18 Apr 2026 05:55:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90d8e4f2f94de58856173d1d55466c632c6602bdea8fc895ac0398eaddfdb2e`  
		Last Modified: Sun, 12 Apr 2026 18:55:02 GMT  
		Size: 93.0 MB (93008107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c8d2818d0ccda06dcd9dc2c6bbda8ad949e0a88c075e3cf64d8b08bf9e8083`  
		Last Modified: Sat, 18 Apr 2026 05:57:52 GMT  
		Size: 21.7 MB (21696168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0501baec3a9f6bbc72c98f346731ade7b5110809770e6f338af973ecd9e85898`  
		Last Modified: Sat, 18 Apr 2026 05:57:49 GMT  
		Size: 4.5 MB (4517792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89ed4a8d98316c2cdf06591315aeca84a1dc7e059ecc0a5818c5b427501da51`  
		Last Modified: Sat, 18 Apr 2026 05:57:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f8bed7596004292a2c142d11e4bafcb1c52325d8d5f50ac2cef793508ebee79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3772532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c8a9e5e50f45085da05caaa182cc70d7b3d391725f5d8dcf652c71fe037ef7`

```dockerfile
```

-	Layers:
	-	`sha256:e426d3eb2db03a01141ae7f4f26109bf6433dd274aac56b1e3b3a8561e9bbecf`  
		Last Modified: Sat, 18 Apr 2026 05:57:49 GMT  
		Size: 3.8 MB (3754143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aff1603d960cd5b7ab744367f3104b6f5a9549962dc7290cae6e61c9b8ea6144`  
		Last Modified: Sat, 18 Apr 2026 05:57:48 GMT  
		Size: 18.4 KB (18389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:de507be08c1015d582431895cb3b8b5c04fd32e78d5f6796e3f1ca0284d2ae1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166213208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12db328236e8004aaec428b29f7b91ad13d59c56fd93c7c4b9b95b85195336b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 23:44:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:44:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:44:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:44:06 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 09 Apr 2026 23:44:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 09 Apr 2026 23:44:06 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:44:19 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 09 Apr 2026 23:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 09 Apr 2026 23:44:19 GMT
ENV LEIN_ROOT=1
# Thu, 09 Apr 2026 23:44:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 09 Apr 2026 23:44:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:44:21 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:44:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e10aa2a41f6d7f1d361656c178853889e3348a51d3a809aed5aeaabd70ff55`  
		Last Modified: Thu, 09 Apr 2026 23:44:48 GMT  
		Size: 90.5 MB (90547693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e002a835553d257ad36383051fdc666a663ce06347df27ad0bd20d70f58af40b`  
		Last Modified: Thu, 09 Apr 2026 23:44:47 GMT  
		Size: 21.8 MB (21782250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db2c551e286858f51f8e9b7945d30b3bab5e1e1a67ac6800004a30ec5ed9e3c`  
		Last Modified: Thu, 09 Apr 2026 23:44:47 GMT  
		Size: 4.5 MB (4517731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7922f910b6838b0cbe8f35f1203acff61de1fbeb75859a6d5b570b6e47d43af5`  
		Last Modified: Thu, 09 Apr 2026 23:44:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:28c061521a3f9ba26d654dc57c2cdbe37f591981b882ee0e86fe4bb781776801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3780989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3d691bcdab4514d9989c3865bb2632fdf51e2e9899d9d364e2194302e7711f`

```dockerfile
```

-	Layers:
	-	`sha256:16344c28cc650d704faace2d02400ec9968d2df3c3b162436e8384baacb5041c`  
		Last Modified: Thu, 16 Apr 2026 00:46:48 GMT  
		Size: 3.8 MB (3762644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:837f8a7a0c1bcfc4c1cba340398b3b257338bcde4084ca39d97ff9e740676fcd`  
		Last Modified: Thu, 16 Apr 2026 00:46:47 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json
