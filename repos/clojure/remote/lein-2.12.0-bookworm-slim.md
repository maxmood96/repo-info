## `clojure:lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:b362661ef0a34fb08bd13d070441f00e10dea6958d3bc3d5cfa591c16ef4996c
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

### `clojure:lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0b0c8d3c85983f2c361d2ed05bcf74089a533237671fdd55f4af10f222c98615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142550109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf7b91e9ca9a7054f3b0b5fe5c1fffcd99b25c072c16d47a8fa5a6081924ba1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:55:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:55:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:55:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:55:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:55:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:55:20 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:55:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:55:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:55:33 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:55:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:55:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:55:34 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:55:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5f3abccda65aa372061e93716f4831963739f62c8a5221aca6656f200510a2`  
		Last Modified: Fri, 14 Nov 2025 00:56:17 GMT  
		Size: 92.0 MB (92045316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49503a544838ac7bf365df78a197b8b6b5c34bf6527464500ede0cb5ede7532`  
		Last Modified: Fri, 14 Nov 2025 00:56:06 GMT  
		Size: 17.8 MB (17758092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282b668c6f378aa2bc0395ecd4089d2673b7198dd48e1fd953c970811d2254ed`  
		Last Modified: Fri, 14 Nov 2025 00:56:04 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708784f703aea8d199090fef4dbd97ac01a8a0981c741b482a5127aa204e9b99`  
		Last Modified: Fri, 14 Nov 2025 00:56:04 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aa30d8a3964c0548cc8e27dd0356941a4222653c026ed26be5947ddd5e70f813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49477b4ebbb23ac46339acc4c36d6b7c030c285377cba22ca62b82c376222b5`

```dockerfile
```

-	Layers:
	-	`sha256:bda28bffc79f307f475462612cd427669af42de29fe6234bec74e3e97eeb113f`  
		Last Modified: Fri, 14 Nov 2025 01:46:32 GMT  
		Size: 2.7 MB (2680112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f9d30851e8c2bc7306b5877e293589c662e70babcd1197de5217f2360df2634`  
		Last Modified: Fri, 14 Nov 2025 01:46:32 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:17c1df9b5bd7a60dc8bb4b8a12ec96a179b3d60e1d87bed1675f5778ff583b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141264180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f7b9a6ff20778fdea4cf2feeb827b83ed125430eadbe58e498d1e92dbe0eae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:57:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:57:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:57:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:57:53 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:57:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:57:53 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:58:07 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:58:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:58:07 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:58:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:58:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:58:09 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:58:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c4a6cc90b7bf9d72c9ce6a0829abd5bbbf3df244613c564167aa07c01cceeb`  
		Last Modified: Fri, 14 Nov 2025 00:58:44 GMT  
		Size: 91.1 MB (91052514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1e40f6b779e23a488fd038f8549411400834e32eb0ebd1b50c0b0c676ccd55`  
		Last Modified: Fri, 14 Nov 2025 00:58:35 GMT  
		Size: 17.6 MB (17591115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1596d8a67a8775a26a4a5836e6806f7b69b9f002bf4013936a6a6c0806e2140`  
		Last Modified: Fri, 14 Nov 2025 00:58:34 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08847c6cbfe32b9c002448e6087d8aae1cc02b1694119042a05a153e11ef40ce`  
		Last Modified: Fri, 14 Nov 2025 00:58:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7e62bb0700f5bd51d51d8696eb30a44a90e949a91ca057fe1c9b5f7c33aa1abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf1b9722aca1dde7cf1409657db4322446fcf0a638dcb19393b801b6a2050aa`

```dockerfile
```

-	Layers:
	-	`sha256:a2d8fe45b06c656b6025109d8428bc081e8c7dbc9d35219acd99c9b281ad503a`  
		Last Modified: Fri, 14 Nov 2025 01:46:37 GMT  
		Size: 2.7 MB (2679748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff04987c024f4fbf2b03a03c3b9c6f610107dcdeffa0649fb1da9e4c55fd8e4`  
		Last Modified: Fri, 14 Nov 2025 01:46:38 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3ac2209516f52889c4064a4f9e55b1766c6dd7c4dc38ce95bff14d067c7c6dac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146157428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0784334cfca3ba33cd59a3ffa4cb7f832728fb7e4d840bddcdc47feb11569c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 07:34:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 07:34:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 07:34:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 07:34:35 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 07:34:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 07:34:35 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 07:34:58 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 07:34:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 07:34:58 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 07:35:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 07:35:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 07:35:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 07:35:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8275b969478a67ffe36a38a5498d7d85493ce57ad435a9a48bfed04467f8497`  
		Last Modified: Fri, 14 Nov 2025 07:35:54 GMT  
		Size: 91.6 MB (91610774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e321b7d2a7af83a168d8a08fab8f836598338a887b4e2b3f64fdfd547470cbc9`  
		Last Modified: Fri, 14 Nov 2025 07:35:49 GMT  
		Size: 18.0 MB (17959591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb7d029afa7e7837f012e5b168d823cf275027e02d8c9e4d62ea3f6088b4434`  
		Last Modified: Fri, 14 Nov 2025 07:35:46 GMT  
		Size: 4.5 MB (4517730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6408e6843724886a731fcd9e9aaaa578f038d50000f7a84d3f278524b72c45cd`  
		Last Modified: Fri, 14 Nov 2025 07:35:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9fc4fe23e9674abc6b8b67977a71bdcc599720b16e4b3b45e40e773f42b30da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2702369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da73d8e4027082811a7f62cda43b0d029da8d28c0364477cd43f68ca4ae26e31`

```dockerfile
```

-	Layers:
	-	`sha256:4088d45bf2e398dcb9ffbd974fbca2b09158938f603e02e0ddabc5128af8104c`  
		Last Modified: Fri, 14 Nov 2025 10:34:38 GMT  
		Size: 2.7 MB (2683255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:485d73f21e7707f9b0f00b5ae2ad5ee952af165bcc5e457a704e7b0593293bad`  
		Last Modified: Fri, 14 Nov 2025 10:34:39 GMT  
		Size: 19.1 KB (19114 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:e09f512301137d50ebaec6ef01c7ad29b03f07eb6eedfd14d16e4446a2d892f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137033294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d1d52ef3e5e766b4b689a213af82e249524935aa73875f1d2e958967b23278`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 01:03:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:03:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 01:03:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:03:04 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 01:03:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 01:03:04 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 01:03:14 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 01:03:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 01:03:14 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 01:03:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 01:03:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 01:03:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 01:03:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde265baf46f3c8b33742759c5fa64bad12a3b3dd450ba515f29cda2827e7aab`  
		Last Modified: Fri, 14 Nov 2025 01:03:57 GMT  
		Size: 88.2 MB (88210714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f7f92a46707a0b5b4401a424877000e147ad3a3b2ffab45cc50156b1652319`  
		Last Modified: Fri, 14 Nov 2025 01:03:45 GMT  
		Size: 17.4 MB (17419845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5d99c23c532c2fb3306ab327c7deb2c877f537ff87ba3081bc526eda1c292f`  
		Last Modified: Fri, 14 Nov 2025 01:03:44 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e29f7ee6cccdbacf56ec3b46505982bd8950b34cbe69a28a53b6f4e834721e`  
		Last Modified: Fri, 14 Nov 2025 01:03:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2b78c08d0f27495b21de7987473363f7a89ca82fb295ffd9fa05f794ff4a3198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e40b664aedc87dd584ed0c84c8896b5d8cfe878046aa25cce6b988f3285ac9a`

```dockerfile
```

-	Layers:
	-	`sha256:65b0e208627bec6ad2ec6560c980bcaf223c4626bbceb87f284d6a7e2e209cb0`  
		Last Modified: Fri, 14 Nov 2025 01:35:03 GMT  
		Size: 2.7 MB (2674474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00dc12172aaab10b7d45b437f6f602994bde7ee94fbdbf0a950eff14e9df6284`  
		Last Modified: Fri, 14 Nov 2025 01:35:04 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json
