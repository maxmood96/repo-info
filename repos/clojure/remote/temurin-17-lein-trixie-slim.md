## `clojure:temurin-17-lein-trixie-slim`

```console
$ docker pull clojure@sha256:9f79188d02254b0519715e24f1390dd78fef78ceb7dc07d18bb484f90534b272
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

### `clojure:temurin-17-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6d79d57599c62cb90e3609ca54df2abdc162468c06b2b30c2c5da703589ba986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195591634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a508fdb5e3bdf4a084ccaec7afbabb26ac284179f67bc137a61862f942198ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:52:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:52:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:52:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:52:51 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:52:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:52:51 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:53:05 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:53:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:53:05 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:53:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:53:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:53:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:53:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec673831a72559be1cd0fe46da8925268bbcf6231edde409c156b2e5bd92b8b`  
		Last Modified: Fri, 14 Nov 2025 03:33:46 GMT  
		Size: 144.8 MB (144847978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00dfe637b124c66ed6b3b2728a7fe65e1e5eb9265d79c3366bc142a207b6bc27`  
		Last Modified: Fri, 14 Nov 2025 00:53:36 GMT  
		Size: 16.4 MB (16447373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8023e3ebdd824cb52261e92a32d29e705f148a3324880ec424cbd7f0d836ab9`  
		Last Modified: Fri, 14 Nov 2025 00:53:32 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee68af5a13d7e94d72f4059c200a9e6527f2155976bb2bde3ebf24e48590def7`  
		Last Modified: Fri, 14 Nov 2025 00:53:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:06ef592c8c1060111cd10bfc20806428d9fd79e29a0fc7becfaa4059f2c5945c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befc895f9a092092b32157355d76360b9fbfe22a7ebefbe7347765f7f17639db`

```dockerfile
```

-	Layers:
	-	`sha256:ba460ca8655a176136a710fd2138fb2ead762437271695070e08874dd3acde15`  
		Last Modified: Fri, 14 Nov 2025 01:41:13 GMT  
		Size: 2.4 MB (2363444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9a0534160055292cec2d07ee0efd49d1b2323ca7c25c768676b71b86637553b`  
		Last Modified: Fri, 14 Nov 2025 01:41:14 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:17e4e94043de3f6fa9253214e4d045bdd78cd668a7c2c79092889d6dcbdf2277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194754000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a990f8360a577df1466d3ee1c99c64c4c3c07f95532928d2e82f5a522b023a74`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:54:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:54:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:54:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:54:49 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:54:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:54:50 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:55:06 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:55:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:55:06 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:55:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:55:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:55:08 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:55:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c3a32d03fec3724c12032668ee73749a8d15ea4d5435559abe8501f4e6f00d`  
		Last Modified: Sat, 15 Nov 2025 09:41:15 GMT  
		Size: 143.7 MB (143679959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9a21dfd388e9f701528dba70ba2d1b277dce367e4663f10afd32d281b28f77`  
		Last Modified: Fri, 14 Nov 2025 00:55:35 GMT  
		Size: 16.4 MB (16413564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6f3f55a10a2c5734531a8bb3fae2ee4722b3b504559902ce3c1cafb112ed2e`  
		Last Modified: Fri, 14 Nov 2025 00:55:35 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71dbc7d3bcf1899977136009a55775c6e5e8af4f87a4c6ff909d8a4a8e4c967`  
		Last Modified: Fri, 14 Nov 2025 00:55:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cb8bf57344fdf692911b1f64d6d050e11aefbba80e7d6e0bcacad1ac55059af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e745de198576a9472e0fa368b4f4fa29a078f131444d419807214827d1858424`

```dockerfile
```

-	Layers:
	-	`sha256:72a0fc83bdd9ea01976b2cf1f1028ce895141d5537bfb5e4822c5ac3d0f6e9cd`  
		Last Modified: Fri, 14 Nov 2025 01:41:18 GMT  
		Size: 2.4 MB (2363062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca80266490b30bec5473603adadba58d04e621c277851858eb7e858851973dfd`  
		Last Modified: Fri, 14 Nov 2025 01:41:19 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:97d08a67193360c50fd14f70da4ef3d8a24f970bdd53a3ab76d8e255e4640877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199128453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a2a8ae100b4cff66d15f153b0c294c1caadc7a6cab0975070577cbf1ad0247`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 07:06:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 07:06:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 07:06:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 07:06:07 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 07:06:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 07:06:08 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 07:06:36 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 07:06:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 07:06:36 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 07:06:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 07:06:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 07:06:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 07:06:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87c0b8920d1145986dc2b1ab28b2f1ed0575573627003c05e2df1cf5f419dcb`  
		Last Modified: Fri, 14 Nov 2025 13:33:40 GMT  
		Size: 144.5 MB (144525213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b42cf550a3767b7465699ba9244c73603a57e4032673af63048800fb5617a6a`  
		Last Modified: Fri, 14 Nov 2025 07:07:30 GMT  
		Size: 16.5 MB (16486411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977716fadedb9bbce9f4087348b3ff0e575b4e1e3944714b97d5ef6a2cdb12e1`  
		Last Modified: Fri, 14 Nov 2025 07:07:30 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3354d38cc29f4c14b20b8e1832c784994e9d3e4476dde014ab4f5836df178d2`  
		Last Modified: Fri, 14 Nov 2025 07:07:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b3a890ce42a0f9e60061511eab1ebbc678de40dcc5e00e136e4b3b546dea80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e3eaac7f147ee7218a0d6669a260876119c6f238503f79dcb2a036925eb8cc`

```dockerfile
```

-	Layers:
	-	`sha256:bc5a2dd5cb89ebb4f113521670c1cfbd65ea3622db0d2c777479050bd5615b5c`  
		Last Modified: Fri, 14 Nov 2025 07:37:40 GMT  
		Size: 2.4 MB (2364424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fa1a4e39449864d1654e447f7efb3db65e5fc875d51d4275b384739c703cbaa`  
		Last Modified: Fri, 14 Nov 2025 07:37:40 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:bfecdc29ea84a5e74e4c1349a01058c3fab1f1d2b150e9e94bb793ae40b2d42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193699912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b333a9767cbd41c72a650208288fd4287a513a86ee9ef1642617f39d728e6a90`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Sat, 15 Nov 2025 21:06:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 15 Nov 2025 21:06:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 15 Nov 2025 21:06:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 21:06:58 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 15 Nov 2025 21:06:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 15 Nov 2025 21:06:58 GMT
WORKDIR /tmp
# Sat, 15 Nov 2025 21:08:36 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 15 Nov 2025 21:08:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 15 Nov 2025 21:08:36 GMT
ENV LEIN_ROOT=1
# Sat, 15 Nov 2025 21:08:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 15 Nov 2025 21:08:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 15 Nov 2025 21:08:52 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 15 Nov 2025 21:08:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f51565c831843416c90e1d3853acceb5a5e8eed70cd002dda98e47bceb3fa63`  
		Last Modified: Sat, 15 Nov 2025 21:30:14 GMT  
		Size: 141.9 MB (141889552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a8c5a5c0c77e9e0526d54c3b5a4d838902b70045f2bb2de51860b3a576f31e`  
		Last Modified: Sat, 15 Nov 2025 21:13:00 GMT  
		Size: 19.0 MB (19016341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af65baeab029b1f765b8033f276ce792969c7d1da4b7fbbb9cc1a0445df63f02`  
		Last Modified: Sat, 15 Nov 2025 21:12:59 GMT  
		Size: 4.5 MB (4517802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21907d5a87ccd081ae6ad86c3e1235afb8bdced5f0219c0dd5024e9166b3d98f`  
		Last Modified: Sat, 15 Nov 2025 21:12:58 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bb23f8d59bbb4a91a04521e015d2823587abf6b887f5eabc6c6781d3c6119119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2371998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed001cf13a25671d935ba9bbf582ae85e30ba2cfa1662391f19059c42fadd5c`

```dockerfile
```

-	Layers:
	-	`sha256:e4833de9bd03f885d776610677faacf7b8bfc5bdb054d2a932201b3d2244b7a8`  
		Last Modified: Sat, 15 Nov 2025 22:35:32 GMT  
		Size: 2.4 MB (2353567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e6abf5164f0fb704971e92a67ecd7070403a2050d53e7c84a358ab74733192`  
		Last Modified: Sat, 15 Nov 2025 22:35:32 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:36e06751ecd0c02625331140c950cbfec6ee4ff3a4d50afd4448ea7eba538f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.7 MB (185698338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec22c7c578331f02521d64199f1079cd304714dd1bf1dbadba56187dd971cf7b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:56:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:56:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:56:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:56:25 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:56:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:56:25 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:56:37 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:56:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:56:37 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:56:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:56:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:56:39 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:56:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f13d1771014468c2762b50fac444775ee212cfc03b2579f1c62f791ba963ecc`  
		Last Modified: Fri, 14 Nov 2025 00:57:03 GMT  
		Size: 134.9 MB (134859068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0234927ee71b8ea18db260e7285cf5d80d3beaef1509cf9e6f473ee883a343ff`  
		Last Modified: Fri, 14 Nov 2025 00:57:18 GMT  
		Size: 16.5 MB (16483706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65a6e359ae4475520dbe21ef04fdbd675a9cf5636a82ff5104bebd70c7591cd`  
		Last Modified: Fri, 14 Nov 2025 00:57:17 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773802bcce4dfb5c416697032c467f0ff5af22c6b4157aecb84495bfc6bf65a3`  
		Last Modified: Fri, 14 Nov 2025 00:57:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2dbb30ee05beca24e5044d86065b0ca0b27da2dc608becfcc4718b9f27791fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38087c7e2f22f4ac3ce316077a74a8465e1006b3eee2debb17bfd83b02dde7b`

```dockerfile
```

-	Layers:
	-	`sha256:7b7a92e0ab883ed0dbd0e33c6f317439bffd2b5c3bf8aa7d9248f68416872514`  
		Last Modified: Fri, 14 Nov 2025 01:41:31 GMT  
		Size: 2.4 MB (2359871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9c1673ef4778c851c1fad75e5b9cf44528aa39fe34b0b6b3b122c7ae4c29404`  
		Last Modified: Fri, 14 Nov 2025 01:41:32 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
