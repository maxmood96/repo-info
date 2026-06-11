## `clojure:temurin-25-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:25c23a80ad4e27566f9d289739c5d4aab0b1279724ecdc689cde3d38853954fb
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

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f04c0911adce6ff124d0bfd0e576e524ee552435b5bad99d5c52f035abef320e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143326275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e476a4357a86e670fe992112f0dbadf45c9bc5351fd0b592b28d19560260b22`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:20:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:20:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:20:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:20:48 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:20:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:20:48 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:21:05 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:21:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:21:05 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:21:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:21:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:21:06 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:21:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99e94753806732a59bc4b23e39e4532d886a7d4f0fa5083f9d375b756cdd162`  
		Last Modified: Thu, 11 Jun 2026 01:21:24 GMT  
		Size: 92.6 MB (92574564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefd14e16a08ad396d78bec0a098fa9bc6dff2a43770fb2a078242d7a50d46cb`  
		Last Modified: Thu, 11 Jun 2026 01:21:22 GMT  
		Size: 16.4 MB (16448155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe1d61a048fa045483c8ea58ce1d8e80e6cff3dacf92679571c8114156d6e50`  
		Last Modified: Thu, 11 Jun 2026 01:21:22 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f5934b9a171aee4933f3a7a0723a04776e5d949f61b1d1518e86a7273178ee`  
		Last Modified: Thu, 11 Jun 2026 01:21:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3d69b746cb0e49aa9522408c2d703b51c9901c713d60c9f987c43e5cb304a034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2352693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fba84223e2e2eb1ee3cd95c0a83c80ebc94bd5b049a66fd509867c7e195277f`

```dockerfile
```

-	Layers:
	-	`sha256:0e99b5cc6d23b733a1b329f112c904b9bdff860a201765e51d675d31792eb972`  
		Last Modified: Thu, 11 Jun 2026 01:21:22 GMT  
		Size: 2.3 MB (2333505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:498257df3ed1e55a91a452499742eda487080ac7985b465059f09c7f197d3af5`  
		Last Modified: Thu, 11 Jun 2026 01:21:21 GMT  
		Size: 19.2 KB (19188 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ef792c9d7a8fc812b62e8b6fc746824cb639a8b380490f267149ef3a8654d972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142623203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c961de4e205b7a42ffbc0a3d85ee00d6f0b6bc3324fff8772c803cc54548dbb4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:24:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:24:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:24:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:24:58 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:24:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:24:58 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:25:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:25:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:25:20 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:25:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:25:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:25:22 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:25:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b96afde525a724c077eb2ebc2872f4ef25175462dafe84becd258091225e77`  
		Last Modified: Thu, 11 Jun 2026 01:25:40 GMT  
		Size: 91.5 MB (91542260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d48df6e8956d6c5f04a5e5707ff8c9198b2e89cfe25f859e49d6140edaa2bd8`  
		Last Modified: Thu, 11 Jun 2026 01:25:39 GMT  
		Size: 16.4 MB (16414248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8d8a94b33550d6b0a40182790cea139333e37f8c51f6c33dbc6abb659e65c7`  
		Last Modified: Thu, 11 Jun 2026 01:25:38 GMT  
		Size: 4.5 MB (4517736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f270d52703414555d34c32df730c92ea6733565291d7877ae7ae000a3096169e`  
		Last Modified: Thu, 11 Jun 2026 01:25:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4ef211ee3ee5126d20e0686e4326f5bd58899d38c986728279ace781b0726e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2352468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63097864ecad6f12bbf3ca6e52fba9df4c4c4a4d10f56bb8f1419b397fca689`

```dockerfile
```

-	Layers:
	-	`sha256:500be00bb320c38a8bb8ebedc9e2f0a656aaa9b3a1d1e4f116669358c0e6dd4e`  
		Last Modified: Thu, 11 Jun 2026 01:25:38 GMT  
		Size: 2.3 MB (2333136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7b360dc348ba86580049ed5afef89c659e772ed5d7dec8236f315d5fc23dbf0`  
		Last Modified: Thu, 11 Jun 2026 01:25:38 GMT  
		Size: 19.3 KB (19332 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6645d8255f69b38380805140b22bfd316177a6f3be5e5f0e36b444747eceb748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146518663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2bd88e73933570bb4534511a00ba357256add9ff68924fce558217e7d6fd5e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 06:06:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 06:06:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 06:06:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:06:59 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 06:06:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 06:06:59 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:07:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 06:07:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 06:07:27 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 06:07:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 06:07:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:07:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:07:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe901bdfd8966081270b7ee3a299c954c200a642ef0bde8cc9488b26992dfc68`  
		Last Modified: Wed, 20 May 2026 06:08:03 GMT  
		Size: 91.9 MB (91914021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d24295425e23fe335db7051b75a79224d5e28f8d5ea93707a59f0001cd01c2e`  
		Last Modified: Wed, 20 May 2026 06:08:01 GMT  
		Size: 16.5 MB (16486031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e662017a3d5a92dc7470210e45a46407458197ff13b6b9a854540c1257371f0c`  
		Last Modified: Wed, 20 May 2026 06:08:00 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f8ebcf16720b4be819f5a2bf430926bdb0c266ef9949c686c9c4119f7790c2`  
		Last Modified: Wed, 20 May 2026 06:08:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7e586ed3cfcd960622773b1b471b0419751167e058d0ffcf5dbb4af920982a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2337053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17f9f619624ecc3cf632a3d6c8efc8e0ea1ae8c9050925e07143e9c0ebe18c1`

```dockerfile
```

-	Layers:
	-	`sha256:6b700f00214e965bbda2c80bc15fb86519a1d79af45ec791631280f7cf100c74`  
		Last Modified: Wed, 20 May 2026 06:08:00 GMT  
		Size: 2.3 MB (2317809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12e2679fbeef64c463d261b9f150a4e1c983537e13821a7fac0231675e1d3e0a`  
		Last Modified: Wed, 20 May 2026 06:08:00 GMT  
		Size: 19.2 KB (19244 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:68623666db225d0fdc8dbb9dffc653d60553d530c6ab0058e0d966aef868468c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139274105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89aeebe672a4146b11ae5248dca1f0ee715faff76dbd98c399bf037447543e1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:14:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:14:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:14:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:14:23 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 03:14:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 03:14:23 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:14:35 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 03:14:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 03:14:35 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 03:14:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 03:14:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:14:37 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:14:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876cd0a7591fab967735e6927a8216404c62c6b59b6d3f16292123c17f4d06b1`  
		Last Modified: Thu, 11 Jun 2026 03:15:02 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5dd2b34a1d60fc6a4b7213e02af3fe4e5e4f542c817b2809c2f54e760535199`  
		Last Modified: Thu, 11 Jun 2026 03:15:00 GMT  
		Size: 16.5 MB (16484257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6552514d9e6c57fcb31c6f004ea0f5e63b45f091fde107171b9f87386a374a4`  
		Last Modified: Thu, 11 Jun 2026 03:15:00 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bc6b6fb455e38d2f4d3ec57c991e44681f9eba236a02b04a680f5a61125dfd`  
		Last Modified: Thu, 11 Jun 2026 03:15:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ccc6f280a6b138cb827c1285d298370a93074946d05c210e2975c4d95aa06daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906bd8e74498f50ef71c18dc8fc9f0db47d98370521433081941e6191805514d`

```dockerfile
```

-	Layers:
	-	`sha256:27d55f67de04215b014b8aaf6948f8363b39ef540239a5d956f259d8a18a2e2c`  
		Last Modified: Thu, 11 Jun 2026 03:15:00 GMT  
		Size: 2.3 MB (2314494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2ff72a2e9fab66b96928d1197a59591113a994e446d67e12fefbbbbcfea3feb`  
		Last Modified: Thu, 11 Jun 2026 03:15:00 GMT  
		Size: 19.2 KB (19187 bytes)  
		MIME: application/vnd.in-toto+json
