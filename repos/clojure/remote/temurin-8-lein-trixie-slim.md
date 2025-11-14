## `clojure:temurin-8-lein-trixie-slim`

```console
$ docker pull clojure@sha256:cb075d38165904e5f3cfe80d6790b8ddc716eea6263a202cf9bc8860f31fbdca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d2d4c170a9d1ab6c7dc0a1af226d6472b2a8a05ca6e519a4b3ba5ec595f94b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105476637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a75b07dcfebe72ff07a3ee4b58adf315d303cd8e3ba0402a9b11847f77846325`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:49:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:49:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:49:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:49:41 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:49:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:49:41 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:49:56 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:49:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:49:56 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:49:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:49:58 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b345508b52ebd9561c8ae42d6417e6f0fa616d55fdbd66751201694b003f48a`  
		Last Modified: Fri, 14 Nov 2025 00:50:25 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a239079c759faa4b758a32cb7bce7ae5625040eb3f4de10ebe43577c6ae1efe`  
		Last Modified: Fri, 14 Nov 2025 00:50:19 GMT  
		Size: 16.4 MB (16447378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783373f15c741f23fae35ea1810e059e246bf38cf17cdfab444f52b38ad8ae39`  
		Last Modified: Fri, 14 Nov 2025 00:50:18 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:08adf9470601c9c0a959681c4a5f53e08051fe6859bb8de6aad126a1681d62a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8593f4dcbbed5fb41a856fe1a1c68e4031baa5a8fb799a3d5e25060f230353`

```dockerfile
```

-	Layers:
	-	`sha256:43c7a443fbe2cb9fa24785d421aa0ee900db76c0c7f1d497620f650bda60e331`  
		Last Modified: Fri, 14 Nov 2025 01:50:45 GMT  
		Size: 2.5 MB (2485054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dca7cebb203a13584165e0f00506fee5c13ff54edf1f71ce7e73b8d0c3f0326a`  
		Last Modified: Fri, 14 Nov 2025 01:50:46 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c4333abf9724c7cf93cdd008deb67030e1cd7118436c921494ec6bd93a45e068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104888624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723b779d41dd7fc5d157d4d657c48b8c7b64741b44569ba42647165810b4a36c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:51:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:51:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:51:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:51:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:51:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:51:18 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:51:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:51:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:51:34 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:51:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:51:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b85b9b1a0b8938b79f275e12b34be8f0558c34dd0bf62e130debbd7f81fba9a`  
		Last Modified: Fri, 14 Nov 2025 00:52:03 GMT  
		Size: 53.8 MB (53814998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22086d1de766d3e90d54171ef0debc59f86c35c837669f01dd186af8713e3f6`  
		Last Modified: Fri, 14 Nov 2025 00:51:56 GMT  
		Size: 16.4 MB (16413554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228a150002e3fbac39fe6c765d3ca08689092d94c5aa6190c06c9a2766c27055`  
		Last Modified: Fri, 14 Nov 2025 00:51:56 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9301ad7e03769bf8f7b7b80cb3cccec713d4be7d80101ba53a8d5c5649bcc1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfa894946e03c42d2ce7d6fad3a3567568f025302085a5e3c380958185cc98b`

```dockerfile
```

-	Layers:
	-	`sha256:f3188d43c428059945c633e5c60ef693cb16cc1d785e06f79823bab0aa778460`  
		Last Modified: Fri, 14 Nov 2025 01:50:50 GMT  
		Size: 2.5 MB (2485370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87a77ce1e56bcfb92c09058020da56ca3e43493551b36880e054844238628e8a`  
		Last Modified: Fri, 14 Nov 2025 01:50:51 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e371dd04bef38ea4321950fd7f6380a04e4afc7bf85838b0016632ff024a0e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106778012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a049876b9a1135815caf1a613b9636a4f8d90bea1eea88db967adfb4d4a4d1a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 06:30:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 06:30:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 06:30:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 06:30:44 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 06:30:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 06:30:45 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 06:31:19 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 06:31:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 06:31:19 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 06:31:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 06:31:24 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99f9e4c12fa0931fb9cd121ca71dc57218e0b79e5b2195c44ff9a7397e58e1b`  
		Last Modified: Fri, 14 Nov 2025 06:32:06 GMT  
		Size: 52.2 MB (52175141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02670b0040e9ef2d74402391dc7d5f2320e627d9e875d69bc41ade546cd1a582`  
		Last Modified: Fri, 14 Nov 2025 06:32:10 GMT  
		Size: 16.5 MB (16486444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b0b0c8e67c5115003c36ee81333ce1be194b5f6d43c47609365b664f157aa4`  
		Last Modified: Fri, 14 Nov 2025 06:32:02 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ca1614b2bc98de65925d0cfc55febd010ff865064dcfba6565965f283fe1eb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c419c21b2e9b624043c41b80c74b78b10e0f51aa83f4274c9d895ffb2639391e`

```dockerfile
```

-	Layers:
	-	`sha256:bb46f9b16ac84b04d11ebefca9127d95237cdce6f7bfb0c777fb8c5b248a3450`  
		Last Modified: Fri, 14 Nov 2025 07:40:20 GMT  
		Size: 2.5 MB (2486627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:606b1a72e7766cdc7878fe1b4b417313d1465cf9b409ab4f671ceabd5142766f`  
		Last Modified: Fri, 14 Nov 2025 07:40:21 GMT  
		Size: 16.4 KB (16426 bytes)  
		MIME: application/vnd.in-toto+json
