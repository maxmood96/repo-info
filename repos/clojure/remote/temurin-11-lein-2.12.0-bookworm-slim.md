## `clojure:temurin-11-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:7aea8683e82e16995ed150470bce41723be56049a85af52c393ee3dfdd32a278
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

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d7a41eb29276a401251507564364c62509b8320d40f126af5221ea5bb0ee3865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195471673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08846edcbe3e86d0805ec51a9109d29c65911ab4c5fc8880ca67b15c30102e3e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:19:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:19:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:19:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:19:09 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:19:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:19:09 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:19:24 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:19:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:19:24 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:19:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:19:26 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46eceb889c0b92092a11c3b2c0a9b6929a3f80c4a8a5aed21c5c57e1dace17f5`  
		Last Modified: Tue, 03 Feb 2026 03:19:49 GMT  
		Size: 145.0 MB (144966643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e940e316b022d6563ca4cfe98319baec74498618fd18ceb487a6ae4dd73a199`  
		Last Modified: Tue, 03 Feb 2026 03:19:42 GMT  
		Size: 17.8 MB (17758777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c2919db560218e9fa8d80f5cb27a41c9b55e3bc7ccb64278fe300a1d86de43`  
		Last Modified: Tue, 03 Feb 2026 03:19:41 GMT  
		Size: 4.5 MB (4517734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ba7070e6e373c854d57cc9f46891ea6f41bfcda99fab997dbe2aaa1cc607210c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2765349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9237f7eed502c7494e4196b0dc1cb6ed18bd8ccd50bd2856fb6dae360398a2`

```dockerfile
```

-	Layers:
	-	`sha256:176af286d7fc28bd0332598b756ef4956b380e327ad539129608e7832aff78d9`  
		Last Modified: Tue, 03 Feb 2026 03:19:41 GMT  
		Size: 2.7 MB (2748937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e3b00a7ba31cfa74b28340d5f8d298d372204dc8c0af9be61f6f05d6a9c492b`  
		Last Modified: Tue, 03 Feb 2026 03:19:41 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0bc4011c3cff566a731a4bb91a71d9875e427b1f11da7cb4311440ce692dc08f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191947332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf197de8e6c555acea5a07a068d3d2db8258c96babe56b019a945182d5e9168`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:21:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:21:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:21:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:21:40 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:21:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:21:40 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:54 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:21:54 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:21:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:21:56 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7ed0634e986d0a9b11badf9ea7437c306dc960f1aa0a7f1d4c3fbbf8e47873`  
		Last Modified: Tue, 03 Feb 2026 03:22:15 GMT  
		Size: 141.7 MB (141729934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f73a6d70a9dc5939715ad61cde97296895aef42b8a0ec7b0e4c019023b6b52d`  
		Last Modified: Tue, 03 Feb 2026 03:22:12 GMT  
		Size: 17.6 MB (17591795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226da2bc04e59193708574ea1b056bffd477b140475f0cd3e896a0667a59d922`  
		Last Modified: Tue, 03 Feb 2026 03:22:12 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b042a791446d3d8849b4981353fb92c97399d0101eff8f7d97a625b8c8d0787f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2765703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a865c683720d83b6f4fdcbe9e5f20c05d21d8a4ef04b799d4da890fe51535b4`

```dockerfile
```

-	Layers:
	-	`sha256:d46e11cc15bdf5ad82fdbf06cc92ab9b26845f03b81b53f571f58aacc7604d61`  
		Last Modified: Tue, 03 Feb 2026 03:22:12 GMT  
		Size: 2.7 MB (2749170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2fa160b60ae939722d335138c5949f9061f8d48ed7debdf319553ceb2898a52`  
		Last Modified: Tue, 03 Feb 2026 03:22:11 GMT  
		Size: 16.5 KB (16533 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:14b414ee2bb4e2cde87d05370a1b54179baaa4c3caa0507fee75fbda56313932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186627328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18ec7d8c61b84011391a369f602f71954bcef395acd374c84467bc85a3bc570`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 09:34:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:34:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:34:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:34:50 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 09:34:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 09:34:51 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:35:25 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 09:35:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 09:35:25 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 09:35:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 09:35:28 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91775ea6b360b47d3003bf9fce8b6bfafc6000ef76da1b159098b664cbe3f91f`  
		Last Modified: Tue, 03 Feb 2026 09:36:05 GMT  
		Size: 132.1 MB (132079761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c85740e817bac213bfc6140632e4eacd1e96e322f737afea625aeabe0ece51`  
		Last Modified: Tue, 03 Feb 2026 09:36:03 GMT  
		Size: 18.0 MB (17961062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ec57e9e8a6a8c6e33fc10d82ed339f9d2f074823b8f0a8eff94d4d5c9d878d`  
		Last Modified: Tue, 03 Feb 2026 09:36:02 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5a6fb25a9c897bfdb1b8c131e066091e969276a184fa33ae956924d6397190b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2766611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef5f63d9e1eee8e630d9931938ba0df9b5330e3682a4a374261d9783502eb8a`

```dockerfile
```

-	Layers:
	-	`sha256:3538d04dd4ebb098d5c7850a5e42c6ccef4f7bb936a0c97f2a44ae9ec647dbe5`  
		Last Modified: Tue, 03 Feb 2026 09:36:02 GMT  
		Size: 2.8 MB (2750155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cfdbd7b935bf00e189b3c23aca7143a1b02e8c81ad28e80ee9cd2415c66a1f7`  
		Last Modified: Tue, 03 Feb 2026 09:36:02 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a9b51114b10fcf56a3c5fef3f7bf8477aaf319600bf3043eb0906b254d2040c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174518140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8091a649682dd906d9f04d839db36c034169388bc874ad32551c99e980875e2d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 04:59:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 04:59:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 04:59:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:59:45 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 04:59:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 04:59:45 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 04:59:55 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 04:59:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 04:59:55 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 04:59:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 04:59:57 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0f29c1a622a9cb30cf548aa4e36533f197514e0885ba711dcb1d8f48584cee`  
		Last Modified: Tue, 03 Feb 2026 05:00:24 GMT  
		Size: 125.7 MB (125694849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29aff0df444cc497d00f35b18d291b03781b84c647255d822e2e26a21e0dc59`  
		Last Modified: Tue, 03 Feb 2026 05:00:20 GMT  
		Size: 17.4 MB (17421130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0515c0b250040bb4892b7ff7a10d0a2aca0f7ab60072dac1f035404bb22804f7`  
		Last Modified: Tue, 03 Feb 2026 05:00:20 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:829d96ba410ac10a43918fdca5ed13482f0ece93d2081c1dbdbed559d90b208f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2757167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e919a456c82c3d1e1ecdff4f4f013d1379967f39671e6099dfa9cb68c95cc704`

```dockerfile
```

-	Layers:
	-	`sha256:ccf2eec8e4b7bb80458bdcbe69423c712b0cd7fab777b59f4b92b5b17c291ac2`  
		Last Modified: Tue, 03 Feb 2026 05:00:20 GMT  
		Size: 2.7 MB (2740755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0763d2931d3be5fb84b08fdfece476b1055321225a8d6035a1a1b43628c9241d`  
		Last Modified: Tue, 03 Feb 2026 05:00:21 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json
