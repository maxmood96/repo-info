## `clojure:temurin-8-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:1379f8b17231906943b10ddffa0d5dd72653a2163b9ea350b766a48e79350a76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:2821b89cbe105247e85f6975d266551f6ca8ee7b072e3a924b751866d6fc5eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127532557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ac398bcae4e383904958f891bb2f353964f96bf07dc450d95ccd6739aedecd`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63afd79bfce7fd355a924fdc30ff4109eb6be66e01290cddeccbe35ed3d4852`  
		Last Modified: Tue, 21 Oct 2025 02:18:15 GMT  
		Size: 54.7 MB (54731351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628c9c6a66b67489d6f98c9e0714b222eedc803b881a04fffc02c8eced96073e`  
		Last Modified: Tue, 21 Oct 2025 02:18:13 GMT  
		Size: 19.8 MB (19802896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a38a24a5aa1a09a5a572f69cdda1acd8f50e3d7c48b0586f2e0dbddf2c04ce`  
		Last Modified: Tue, 21 Oct 2025 02:18:12 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6e9638fdb8809c5a8d4c4b8156a9fdf5cbcf1f75d77a674e04a5b39c03055577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4417859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ead6e7e7389f11b9f65a8493b713d23ab6371ac72ca858f3531846359dbad7`

```dockerfile
```

-	Layers:
	-	`sha256:4ded15f4de772eb79fd3daedacdd572440d081d62178a30d8cb0bf7d3f3e3390`  
		Last Modified: Tue, 21 Oct 2025 09:46:40 GMT  
		Size: 4.4 MB (4401446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54f138e95f0e2528abef26265541a48f8fd87bfac4a9f607011cd76e51b8ae68`  
		Last Modified: Tue, 21 Oct 2025 09:46:41 GMT  
		Size: 16.4 KB (16413 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4b21f46faa25e41eb0625a6b5ec5fff3dd26c635742f14127e396b135c5f38b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126344500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5fc10b77b70d7bfa79675919f18979f57d536074b4b2ca963ff79ae403a565b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5e30e31fbc8c13550dcbb80f0f3b4ee815488071ed974e4ec5892dba5a4d44`  
		Last Modified: Tue, 21 Oct 2025 02:24:25 GMT  
		Size: 53.8 MB (53835606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cccae72bb2f837161d23b0b5048a163363da43a71a79e5632e59807486c07bb`  
		Last Modified: Tue, 21 Oct 2025 02:24:21 GMT  
		Size: 19.6 MB (19632104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f463f536dddd20d29e9faef26dfb37d2917e911d144caa3c794601feab76e0e5`  
		Last Modified: Tue, 21 Oct 2025 02:24:17 GMT  
		Size: 4.5 MB (4517762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:da377a21e405f63f779d54863952cdb0e4eb068b70bf8ced3223385788fdcc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4418291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5f05a1497a769178b75ccf84b999f852407bb24f5ca857e446aee0c867641c`

```dockerfile
```

-	Layers:
	-	`sha256:be288d46283f63a780c373092b8b0daef32e036c5d36a7cd6b609c3dba5c5210`  
		Last Modified: Tue, 21 Oct 2025 09:46:46 GMT  
		Size: 4.4 MB (4401759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7100d64b55677e97c8a61c4d837dcbfda70dcb69275ee78b0a87d35eb9c17855`  
		Last Modified: Tue, 21 Oct 2025 09:46:47 GMT  
		Size: 16.5 KB (16532 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:f239c661a6bd2fa7a9e6bb4bd4b26a723f9264cf1fa4202a599a3ca34eeb27f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129031678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201e63e4867f4c6099cb58f85868a9f6a93ec09ddd6e9c6c8f49fae9a985f6c9`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401ddd0af0f7ebbdbb14517b608732ced7b77f026bd12e988950f03c5eea95a4`  
		Last Modified: Fri, 10 Oct 2025 04:42:10 GMT  
		Size: 52.2 MB (52165400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be10b58aeca4a5d60e4d2cd3538084aa00318113c229c3819d9a583f40cb91e`  
		Last Modified: Fri, 10 Oct 2025 04:42:04 GMT  
		Size: 20.0 MB (20021727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da4ea0625b84f92038ee535ea0cf86985bd4ac996313303bc29837dac5c62fd`  
		Last Modified: Fri, 10 Oct 2025 04:42:02 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:56ceeb6b1cd6287329085f01fb008474dc5588c357aa1933cde258030b3f3d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4420355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef920a6c09f86c24aeef2605baa86870fc51f4912985b37d863e3b119ce19f04`

```dockerfile
```

-	Layers:
	-	`sha256:304d07be5ba60b8ca788839125c5c53688451ad76452da0d238a6791f1fc8d0b`  
		Last Modified: Fri, 10 Oct 2025 06:50:59 GMT  
		Size: 4.4 MB (4403898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a9296b9cfc7f3d05faefbd911a70f62459de37f4777f8e86791d22effd03541`  
		Last Modified: Fri, 10 Oct 2025 06:51:00 GMT  
		Size: 16.5 KB (16457 bytes)  
		MIME: application/vnd.in-toto+json
