## `clojure:temurin-8-lein-trixie-slim`

```console
$ docker pull clojure@sha256:0fb6f1485d1986a2875f4c6cc30ead5c6e915ee883fd4c102e6c80e8b0693de5
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
$ docker pull clojure@sha256:62cc1fa93c40e7abf6d6c4bc9c7cc3228368f7fb7a42245ca1f3a004359ca023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105474571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becc60404076d9c0c794dbe0ebf59aa82531aa9152f8804a8f2a6e1c6417fd00`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:29:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 04:29:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 04:29:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:29:49 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 04:29:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 04:29:49 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 04:30:06 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 04:30:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 04:30:06 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 04:30:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 04:30:08 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b91391d1e979f1d5e7cda6960b2cbe7e4e4e85932fc126dbdd0620bedc67a1`  
		Last Modified: Tue, 04 Nov 2025 04:30:36 GMT  
		Size: 54.7 MB (54731291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45278ab8117f94aeb14f40a07de8297bf5ed8cb3c60d050d8c3f20ea79b3f608`  
		Last Modified: Tue, 04 Nov 2025 04:30:32 GMT  
		Size: 16.4 MB (16447425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba01f9c2acfb3a763ebb8c856de4bd94b8e66ce93cc0ebcb64dbbf4eebad80dc`  
		Last Modified: Tue, 04 Nov 2025 04:30:30 GMT  
		Size: 4.5 MB (4517719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c24211b2ca5eac965a9f7db59f1a8b9cbba5cde4721cab48ba683e28080e65ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5865c39a5c4c11c0a201f95c7990968f04ed48dc9c94c797cbc83a0b33760e`

```dockerfile
```

-	Layers:
	-	`sha256:97680c0e964ea8b83b203914f40aa76fe37ff6b723c2a5d77acdf6e8e08ec69f`  
		Last Modified: Tue, 04 Nov 2025 10:48:52 GMT  
		Size: 2.5 MB (2485054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29f4fbd670f3b80e69c6c56cebbf95dcadc864348f373484816c5bb9f047b0f9`  
		Last Modified: Tue, 04 Nov 2025 10:48:53 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:612fd7c44ab9b0dc7e7f07eda85364e60afb760a731ce056a8a5010ad122c77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104909138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104a0e9b33562d561dcbf5e2b3fbf7aa648636b3156575734b4a38927047320c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:43:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 01:43:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 01:43:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:43:24 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 01:43:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 01:43:24 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 01:43:41 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 01:43:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 01:43:41 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 01:43:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 01:43:42 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5bdb42897e2f1abfb792d3b20785cf855ea952a6b15e94f225eda38967036e`  
		Last Modified: Tue, 04 Nov 2025 01:44:05 GMT  
		Size: 53.8 MB (53835577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1236918abd6bb33368ad66add992e9464e592f56c0a28a9155fbc0d83abcd8e`  
		Last Modified: Tue, 04 Nov 2025 01:44:04 GMT  
		Size: 16.4 MB (16413516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3fd5bbb6d2269da353a7cc067c2550bfb81ffc918c95230783f8b1fc745ea2`  
		Last Modified: Tue, 04 Nov 2025 01:44:01 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7499b17edde3c2b52009fc276c88d8ccdd29ffa2cd84386e27313715e0be7c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184d32ad5ca6c71eee029ab09c38291c10f94f2249b014fa0d1999b392f959c6`

```dockerfile
```

-	Layers:
	-	`sha256:e796439f2472dcb13cea2cad1b0b163aa43f7824be443445ab13788a708e8506`  
		Last Modified: Tue, 04 Nov 2025 10:48:57 GMT  
		Size: 2.5 MB (2485370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb271641dbf4a18c4d3954fd3234de826a58ed76d31463566b605ca059b140d`  
		Last Modified: Tue, 04 Nov 2025 10:48:57 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4e248231b8ff721b4cc828226c0992d31f79ee79b321dcdfffed9b3db013d29e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106768234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92e560f7d9c7b9bc3a3c5a558e9b7f4e47b4bcae8165a5545b6b916e96643fb`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 13:04:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:04:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:04:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:04:05 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 13:04:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 13:04:05 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:04:40 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 13:04:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 13:04:40 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 13:04:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 13:04:44 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1238aaaad8882076b4c982f227415c87f083a64c6a1006f173b38c1418642696`  
		Last Modified: Tue, 04 Nov 2025 13:05:25 GMT  
		Size: 52.2 MB (52165369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4919e01d66399718f0880921fed4ffd21bf319f595ebefd9e5e1dc1eb069ff5d`  
		Last Modified: Tue, 04 Nov 2025 13:05:22 GMT  
		Size: 16.5 MB (16486427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eeb7fd1664d026ecf9db0d9fb5ba5dd811cf6ba3e3d5c2d26a9d3edf809e5a1`  
		Last Modified: Tue, 04 Nov 2025 13:05:20 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1d9cc062d40afc975f9512e9645ce76cacec9c8026138d6388585571594d0170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33e9b61e236642a8e1b73558df56754582f7d5b0b6d8428e91ead36f906e42f`

```dockerfile
```

-	Layers:
	-	`sha256:be186ed635b183640459b4e7912f277c57136e04d57868736900ca4c356d3a66`  
		Last Modified: Tue, 04 Nov 2025 13:38:48 GMT  
		Size: 2.5 MB (2486627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92fa056e4df3ed6ea069abaed1df492aa057926a31d3bca89f412a86cc5ead64`  
		Last Modified: Tue, 04 Nov 2025 13:38:49 GMT  
		Size: 16.4 KB (16426 bytes)  
		MIME: application/vnd.in-toto+json
