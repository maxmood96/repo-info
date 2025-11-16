## `clojure:lein-trixie-slim`

```console
$ docker pull clojure@sha256:9fa9d27952ecdf72dc7f7163217653de07115aa26e5cd9307b90641cd4ae1a2a
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

### `clojure:lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5391d4101ce0a4344f541f203cfbae5450f1687c8c77b5ecc5b6010e55d85300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142789072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb261d3fd0d7048ab928d2426cf554c60ab0e07cf2b21adb920d015ba7dac24`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:55:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:55:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:55:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:55:42 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:55:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:55:42 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:55:57 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:55:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:55:57 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:55:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:55:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:55:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:55:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88e4ea9c7610eae94c40db25cf311aa715f53cbd47ae73b7b39fd221c3dc316`  
		Last Modified: Fri, 14 Nov 2025 00:56:31 GMT  
		Size: 92.0 MB (92045298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8691373b699d3d4d3ee6ae0596e8462dd2d03795b949dd28e455e45a355f578`  
		Last Modified: Fri, 14 Nov 2025 00:56:24 GMT  
		Size: 16.4 MB (16447482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831326fc8d96f564db5fcdb0931008a3b9629ea2cc75d77a1d3d2dcae2b288fc`  
		Last Modified: Fri, 14 Nov 2025 00:56:22 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcde40df2ccc94f6211102d41c020e0d4d2918a653aae7c36336e79c633bb1ff`  
		Last Modified: Fri, 14 Nov 2025 00:56:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:84916ff737ce03442fb28b66d213d443c0ea35a607a1d0a2b9c6f60ac4865521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510cead42c7ae7fc595362f1fafe62731938db789adcc7a1c3bc46c3da62b503`

```dockerfile
```

-	Layers:
	-	`sha256:6961aa062be330e2795b7433f6f8843310cf22c409b81bc425d6e42fb8fca345`  
		Last Modified: Fri, 14 Nov 2025 01:47:18 GMT  
		Size: 2.3 MB (2314760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0981a73497c3a091d70bcd2e27153d56491919b17e550edb5d4e0be52120fb2d`  
		Last Modified: Fri, 14 Nov 2025 01:47:19 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:280e4bdcdc42dbbdeda6c6277ad0de781d3591542172fb570849f0cb7a216580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142126520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84dece784f2bf218246a1cb74ac6927bdc63e815d110b59ce7aff0afb7eb8688`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:57:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:57:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:57:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:57:59 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:57:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:57:59 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:58:15 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:58:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:58:15 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:58:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:58:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:58:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:58:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262cc0685394031f6ff3f3d0a86490a12fae03ec5c20c9024d342feed10288dd`  
		Last Modified: Fri, 14 Nov 2025 00:58:54 GMT  
		Size: 91.1 MB (91052512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0dc4cb261b42faa272543273d93e02a679029af51157ee72b89960e9d14d87`  
		Last Modified: Fri, 14 Nov 2025 00:58:42 GMT  
		Size: 16.4 MB (16413536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61e52f972a53978c4f3f1ec875e6c0d44ce7897898f7dfe855e12d66b2a520a`  
		Last Modified: Fri, 14 Nov 2025 00:58:41 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507cb8cf59539e896fbb4754b66cad54c669652925f17b30f71b34a4550b2fdf`  
		Last Modified: Fri, 14 Nov 2025 00:58:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5771c05fcfdc0b79f50a684ba5019e73c176095d19d80190332d0e92abce6d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ef99681b64dcf270cc3bf9b257a18e77baffdc1b463d793ba4689806b45d6f`

```dockerfile
```

-	Layers:
	-	`sha256:0eb83cbe39ead97c820e2fc5a2dd9a822ffd2086f77f2d3281c4e00cf50e5083`  
		Last Modified: Fri, 14 Nov 2025 01:47:23 GMT  
		Size: 2.3 MB (2314399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cb9d0ab2246f4e887ce746ed0d5c0ccd522a13a1eca1c020a5dcda2067049bd`  
		Last Modified: Fri, 14 Nov 2025 01:47:23 GMT  
		Size: 19.2 KB (19178 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:fe5aa5541656b85e316a052c6c278ba204db5bab6eb750ca05c065730831d7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146214011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e0add9146c7e4feab0ecb4d2b93b808b3373d89923f3f3c00fa16f20a7351a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 07:38:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 07:38:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 07:38:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 07:38:50 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 07:38:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 07:38:51 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 07:39:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 07:39:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 07:39:18 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 07:39:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 07:39:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 07:39:22 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 07:39:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e214a9e01b759d7b08b8557e73d24cd420e1a0095fd9ed8d25175ebdcd1470`  
		Last Modified: Fri, 14 Nov 2025 07:40:17 GMT  
		Size: 91.6 MB (91610774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73041d2112f5e22071d66a770670cb410ce10c03a81d54eb3fd02de311b1d9b1`  
		Last Modified: Fri, 14 Nov 2025 07:40:09 GMT  
		Size: 16.5 MB (16486405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9479135b2efa860ce182bbc17d5909ae27f6dad8b751689949a99199dd770e8`  
		Last Modified: Fri, 14 Nov 2025 07:40:05 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8c7ab422819c96a6ba68f204c1c71a8f5749fda050c2fd62e9386b196132c2`  
		Last Modified: Fri, 14 Nov 2025 07:40:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:413c059cdc0e404198fce1b8badca7d5e88b26abf01cd30a0395d12f019c6e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6bf2bfedbd047912d7abff3ef739a26f6790e8ff0eedad5d53b15b206086de`

```dockerfile
```

-	Layers:
	-	`sha256:9e6126e25e818978d3fed88b2a7b1f958b41acfb2772e8299c44bb673403b400`  
		Last Modified: Fri, 14 Nov 2025 10:34:52 GMT  
		Size: 2.3 MB (2317050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c22db576fc9e5ca53d1b24464c62c6e36e0398966162622c3d6eaf7c9ce4d77c`  
		Last Modified: Fri, 14 Nov 2025 10:34:53 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:c9019ae3f473516e8183cc91990a5930c36984d229ae0eb7fb10c56757a66310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142563117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b18ed75006e5341400052b36287e7df9dde571259e4dbf81a66bd60b872265`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Sat, 15 Nov 2025 22:24:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 15 Nov 2025 22:24:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 15 Nov 2025 22:24:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 22:24:51 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 15 Nov 2025 22:24:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 15 Nov 2025 22:24:51 GMT
WORKDIR /tmp
# Sat, 15 Nov 2025 22:26:24 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 15 Nov 2025 22:26:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 15 Nov 2025 22:26:24 GMT
ENV LEIN_ROOT=1
# Sat, 15 Nov 2025 22:26:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 15 Nov 2025 22:26:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 15 Nov 2025 22:26:44 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 15 Nov 2025 22:26:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de331da7b5fa32193d37464667be79a9514eefa9df4d5a7f8b711124d7538b6`  
		Last Modified: Sat, 15 Nov 2025 22:30:37 GMT  
		Size: 90.8 MB (90752790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d775b8f46d7e2e95e241e64454f9e1ae7622d38b9e907634fd9ba9a33894c75`  
		Last Modified: Sat, 15 Nov 2025 22:30:38 GMT  
		Size: 19.0 MB (19016318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0628391fda317ced03a4ab9dce763017e8c59118c529f5b630f08ce887561c24`  
		Last Modified: Sat, 15 Nov 2025 22:30:29 GMT  
		Size: 4.5 MB (4517791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7314f02e8b7a15b9a1579bb58bf0334794afd7f2fa820f66ff6f29c2915fa3a3`  
		Last Modified: Sat, 15 Nov 2025 22:30:28 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2d36e178f88db65b0710c34e589daf70c3c19b40c163e80773553008365caec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2325901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38bf0ddfdf55801ca847f5fbc369a8c39d7bf6ba4c0f30c727edb2b40232dcd0`

```dockerfile
```

-	Layers:
	-	`sha256:fe7e39f4407ffb61deca1d5ded5b7615a305f54d6cd10dbb743ed8d140cb534b`  
		Last Modified: Sun, 16 Nov 2025 01:34:36 GMT  
		Size: 2.3 MB (2306811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590a1e60b79e15a4468713625bc6927268390365a9bfff1becc6ff40800ab00c`  
		Last Modified: Sun, 16 Nov 2025 01:34:36 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d39b8d98022c00176aa312f4c751de9ecdd09ee9e7104b80b68749b98234ebf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139050051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6865925defa4c2c701d75099f7717b0b0cc5ea42818b64820241a2a35172be05`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 01:03:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:03:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 01:03:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:03:58 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 01:03:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 01:03:58 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 01:04:15 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 01:04:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 01:04:15 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 01:04:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 01:04:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 01:04:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 01:04:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68938204a636f823d8b918e7681930804615472d355c8f63462626916e8c77d3`  
		Last Modified: Fri, 14 Nov 2025 01:05:03 GMT  
		Size: 88.2 MB (88210741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d48a0e42f41a603f4157f708814c5b3efc370de7fe84d135ab1a4de25a99c75`  
		Last Modified: Fri, 14 Nov 2025 01:04:48 GMT  
		Size: 16.5 MB (16483743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1edcaf3bf8c2643d28260aa4d4a7201ddc01c68b728f875670b5b33bcbd773d`  
		Last Modified: Fri, 14 Nov 2025 01:04:45 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9513280532d676da26d67afa8a35c4e72828b70be0c767300fd5373a9165f0ad`  
		Last Modified: Fri, 14 Nov 2025 01:04:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f36ee78bcfe6a6b739a97899d4ba539eba219c8e5cceb480e527c0044d105881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2332769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8988e16620a64647238fbf29b7d0992df6fefa10e26d037ae918c2145ea8c2e1`

```dockerfile
```

-	Layers:
	-	`sha256:3a5cc379c09b8a7bb2adc2fd8723a9c3ddc1b9a9e90586e5854c49e1d05d207e`  
		Last Modified: Fri, 14 Nov 2025 01:35:18 GMT  
		Size: 2.3 MB (2313735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7baf2f06185ee34f06ae943f175c5cda0d6bc32389b6564e42ae3016f84a614e`  
		Last Modified: Fri, 14 Nov 2025 01:35:19 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json
