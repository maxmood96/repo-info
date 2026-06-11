## `clojure:temurin-21-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:8af398bd8572c61fd83ca23588b2074949fa46df95c9ce25d063a62c27283bca
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
$ docker pull clojure@sha256:6edcb7e4cda44c5cbc4878599e3ec07250efdb671bfdc62729240e4b447d7981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208918735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aee600cd3e5228027ab627e46bb7fe2d1433bc94c84538ed73b643110284247`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:19:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:19:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:19:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:19:46 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:19:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:19:46 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:20:02 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:20:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:20:02 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:20:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:20:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:20:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:20:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310662c7eeaf08565c827577188d24d93248725aa51a1dab7f5d7323ff3b7123`  
		Last Modified: Thu, 11 Jun 2026 01:20:25 GMT  
		Size: 158.2 MB (158166958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7625fc07d76286e41396924869a9ec9d628fe7674b73f3dcc443d0f5356262`  
		Last Modified: Thu, 11 Jun 2026 01:20:22 GMT  
		Size: 16.4 MB (16448181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87f04c0d66a2b16e0bc1f1a31dabcd0459cf25ccd8bd10b51bc5e16c3589d58`  
		Last Modified: Thu, 11 Jun 2026 01:20:22 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2925d1248f15ef47a952ad85101c131ba055821d8fe5205fb40d7b2dffb88959`  
		Last Modified: Thu, 11 Jun 2026 01:20:21 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bdcbafa89ef4d5d45363b7be050096d489fb159d48ceb6cff3078f332713c43a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ba6e892d94d6ad5cb9ce5907e906b3d36e498d1157f5053b3c3d583271c444`

```dockerfile
```

-	Layers:
	-	`sha256:6161e1a582e26e77a473dda3235f4ab7613b7462aa36c0218097e75203fa08ab`  
		Last Modified: Thu, 11 Jun 2026 01:20:21 GMT  
		Size: 2.4 MB (2367309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d8c45f3d6bbe170563759ddc00b72338c6aab2694f65eb6c9cc08445fa7614`  
		Last Modified: Thu, 11 Jun 2026 01:20:21 GMT  
		Size: 18.5 KB (18541 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3bdf11bce7e377295c153ed10d4e63b486384c2b98aaf298cba25e66f0644bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.5 MB (207542200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b21cc46f7ad3636d595c43dc8df56d2edf6191d14bedf7ef759fcc34cab0a65`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:23:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:23:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:23:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:23:40 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:23:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:23:40 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:24:04 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:24:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:24:04 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:24:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:24:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:24:06 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:24:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c747f81abfbf41742d9faf4fcfa57cbdf8ba693fdce73d7a7aca94b1eb0f68`  
		Last Modified: Thu, 11 Jun 2026 01:24:27 GMT  
		Size: 156.5 MB (156461323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eee841c875e78901a18f0153522ec41c2ede2f250a23254bbe236b0060c529`  
		Last Modified: Thu, 11 Jun 2026 01:24:24 GMT  
		Size: 16.4 MB (16414171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6800803966e7e1c3a29c359f888882e32c7954378e9d423781f8e7ca7014f23f`  
		Last Modified: Thu, 11 Jun 2026 01:24:23 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65d72ed953202f225e784a1f037de42b62d574c227648ff347a2ea09414eeed`  
		Last Modified: Thu, 11 Jun 2026 01:24:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:490521a196596d042d1d3dc7c12dc8b7d321932294fedae80214b315926b646e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7240b64178775f862ced9550f9f555c74f7f08f2ed341e849f8ab59f4341527a`

```dockerfile
```

-	Layers:
	-	`sha256:e0ee5f5678ec1efb2db3dc57a216f3afa9393e60c66a9271a95867a8a38f2be2`  
		Last Modified: Thu, 11 Jun 2026 01:24:23 GMT  
		Size: 2.4 MB (2366919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28caa738ba2085e2d2750f6e5c38f167afd7b5b74e4248e0f89a9619e27a385c`  
		Last Modified: Thu, 11 Jun 2026 01:24:23 GMT  
		Size: 18.7 KB (18662 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3ebfdadd9cfebbf14469c51c5facd5dbca360ee6b6ea33286660ecab41457769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212947931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f948e3d292463cd615e514574a7fb0f07d35b7c16d03e88ad4e4549200d266c0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 06:02:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 06:02:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 06:02:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:02:25 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 06:02:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 06:02:25 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:03:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 06:03:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 06:03:20 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 06:03:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 06:03:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:03:24 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:03:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b629dc606e724e659e7094cdede449bd2fe74e4594977f7749e2b2b2395027`  
		Last Modified: Wed, 20 May 2026 06:03:43 GMT  
		Size: 158.3 MB (158343282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3145b6015b779ac8895a2bafcc23e87d1b9b7067bf210f20ba38e91d4637f3d`  
		Last Modified: Wed, 20 May 2026 06:04:00 GMT  
		Size: 16.5 MB (16486024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00670779496d7d395c4e7bbb6526404152dc8bce0189f5d2bdca7bbe1b7a2674`  
		Last Modified: Wed, 20 May 2026 06:04:00 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c772f4328e553577400c127e3059a6e0363c6dc65eb24f42eaaafec82c76d4`  
		Last Modified: Wed, 20 May 2026 06:04:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a0b4abb93bd6361ea2aa29273f7f5c78a085bf37e0bb0561732ff4d24933940b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62977f581bfa2a1f6d6ac877f8691527c3e113c26d775654ca5aa5955f0a79b9`

```dockerfile
```

-	Layers:
	-	`sha256:90851571f9e3d0e9339dd4198a1bdda1947ce7d1340d9f15c2f7c7c4de756383`  
		Last Modified: Wed, 20 May 2026 06:04:00 GMT  
		Size: 2.4 MB (2368289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4244105ecca1f847ccacf8c57a171e3b0e5432dbae3347ffc47422b505d0da98`  
		Last Modified: Wed, 20 May 2026 06:04:00 GMT  
		Size: 18.6 KB (18585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d7e837077834626e1c928a47dfb4eddfc5c083ad662194777eed3e22ea209e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198242180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8859c8f87d5c208a050e9c959ca5409aa85544e66b215b8f4fb5f2c6b6b63da6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:12:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:12:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:12:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:12:07 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 03:12:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 03:12:08 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:12:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 03:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 03:12:20 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 03:12:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 03:12:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:12:22 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:12:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fe9d476bfc26aecb65233f2a84a64c452218d93474e5ac0581302972abb9cc`  
		Last Modified: Thu, 11 Jun 2026 03:12:49 GMT  
		Size: 147.4 MB (147388365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2119bb64f9c4e7e2dc3cb600ce560ec762a861be986ba51e278b42a720d136`  
		Last Modified: Thu, 11 Jun 2026 03:12:46 GMT  
		Size: 16.5 MB (16484280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12e7b520cb5aedb1eaf8299f90ef153db9dca02f6add59cd8102441900aa0cf`  
		Last Modified: Thu, 11 Jun 2026 03:12:46 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c205ad7fb0b2761b984d3f43655d6d5bf60d859353551641588ff80b4616985e`  
		Last Modified: Thu, 11 Jun 2026 03:12:46 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8d0898ebdf3abe8dc5b1c7ec2338d5339eba26fe497998fb1bbe9e1642a642be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf32c20cd3ee1be4d2a5574fbfcda916135b014e21dd56603031c18b2a93edf`

```dockerfile
```

-	Layers:
	-	`sha256:5c493231f28e66d926285233eb72f469120f975c54329c7b546792a9e3b03cb4`  
		Last Modified: Thu, 11 Jun 2026 03:12:46 GMT  
		Size: 2.4 MB (2363736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:420c470d1153c2b73933e46e92e6943855bcb98145d161b720cb4274aaa7e8d7`  
		Last Modified: Thu, 11 Jun 2026 03:12:46 GMT  
		Size: 18.5 KB (18541 bytes)  
		MIME: application/vnd.in-toto+json
