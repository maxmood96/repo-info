## `clojure:temurin-11-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:cc298602c232128700e3ec3ce95db949e3136d330b35a808bc372e08ba26266f
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

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:51788da950e14f5caa7853837b125afaba2818098dc0be3c7b677a795485194a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196550240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7753d5194a87c98ad5811744e37517aa196997275303d78ac16a1fe4c79db554`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:53:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:53:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:53:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:53:48 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:53:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:53:48 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:54:05 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:54:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:54:05 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:54:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:54:06 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bb0273b39ed9f306b154332a7a8948f2899d6b8cf06d5f26aaa2393003daed`  
		Last Modified: Tue, 24 Feb 2026 19:54:26 GMT  
		Size: 145.8 MB (145806701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed6fb8da63dda4e3d6d3aa9c34a4a63e2974c492025fed4afa112def624ab78`  
		Last Modified: Tue, 24 Feb 2026 19:54:23 GMT  
		Size: 16.4 MB (16447125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356b9f962a5912f7c6a6ebe723ea55e4966cba0b1490a230482525bfce2e0f04`  
		Last Modified: Tue, 24 Feb 2026 19:54:23 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7a4038282a6d30c3dc563a8a1dee4093f6b657a9c0684231a82d67f4b2107cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c62ac521b55345d058cdd058e50e1c64606107aedfe9416d8d1d51fd1db2fef`

```dockerfile
```

-	Layers:
	-	`sha256:3b0e7f927a767977fd528f2bb7037ef987ed7701cc9fb4818c66bbc5bbb7c268`  
		Last Modified: Tue, 24 Feb 2026 19:54:22 GMT  
		Size: 2.4 MB (2384893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f4244edd46703183d9dc85c4aa92d1d3dbee9befb41f7791e7ba4749ebe87c1`  
		Last Modified: Tue, 24 Feb 2026 19:54:22 GMT  
		Size: 16.4 KB (16393 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5de76252d27eba37f3c19549eb0b5bc69b80839179075899087941632e3a0690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193572894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb047d92e388b3f615f4b853f1c191b3ba424b3d2ac1358769920b5b1e48253a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:04:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:04:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:04:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:04:50 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:04:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:04:50 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:05:06 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:05:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:05:06 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:05:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:05:08 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a253c1be5b700a84d0f48a30ba654c71bd064cce2ef7d7791b572bac308190ed`  
		Last Modified: Tue, 24 Feb 2026 20:05:29 GMT  
		Size: 142.5 MB (142501412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecb2f56a47e8ec78c97451ef7449ce366cc3a8cda3aa756c9c138338c2d1463`  
		Last Modified: Tue, 24 Feb 2026 20:05:25 GMT  
		Size: 16.4 MB (16413621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fea4c292708afc90f1e68c211b6d1388ab9d12c572ac2ebaae838e59ff98e0d`  
		Last Modified: Tue, 24 Feb 2026 20:05:24 GMT  
		Size: 4.5 MB (4517731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:195bd880831036dd883a7152636fcb5bed1d87bec77bf6b14294d97d974040a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177a98c9ed3c33ae1fc6e3116131cb7971f7776224c8402bae37be9f079fdd4d`

```dockerfile
```

-	Layers:
	-	`sha256:8cb9738e193f001bfddbe5675712f255bb6a6c2f23d5ccd87dc67905c3cbd79e`  
		Last Modified: Tue, 24 Feb 2026 20:05:24 GMT  
		Size: 2.4 MB (2385129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df89a6ee81d6dc36770a4ed6774af84ec1b08c67640581451cdd0fbda6b06bd1`  
		Last Modified: Tue, 24 Feb 2026 20:05:24 GMT  
		Size: 16.5 KB (16515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b9d08be7ce75e897d0330d7b49209b9c4f7222a28574bdd740a1cf97a117cc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187600721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27bb8eb47e05f9919520d7e13b3fcb94599dd0ea6f0c7b0e06b8d45d789a734e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 01:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:51:09 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 01:51:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 01:51:10 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:52:12 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 01:52:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 01:52:12 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 01:52:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 01:52:16 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21426e09421bed3f9e9b43d31a1a5b3e053a0afe29ad9d5a421aeefd9dec6ac2`  
		Last Modified: Wed, 25 Feb 2026 01:52:55 GMT  
		Size: 133.0 MB (132997815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67eba9ef769962b6e662a08c1bee2cdde1db2162ed2b01e447da6e634d0abd8`  
		Last Modified: Wed, 25 Feb 2026 01:52:52 GMT  
		Size: 16.5 MB (16484888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e0fbaeb76022bd7891791d73298f83cf442e8674879572b0efbd9a5c438d68`  
		Last Modified: Wed, 25 Feb 2026 01:52:52 GMT  
		Size: 4.5 MB (4517770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b4b6c453392f717cf57e3b728de62deb5c77eae220d238bc77e31fc9276b8938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0721f0548d680a1bbbc54b62e8f4e623323697b163adb721686b1736db1071`

```dockerfile
```

-	Layers:
	-	`sha256:9fd90e6211db69c674d6e8fee6a956156792a9d4e11c3b2e0951aae1c7da9d32`  
		Last Modified: Wed, 25 Feb 2026 01:52:52 GMT  
		Size: 2.4 MB (2385258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c28f3b8a078420b874499d83e0b88dd7a52f7549bc4ad8ba487d97a029b1c64`  
		Last Modified: Wed, 25 Feb 2026 01:52:51 GMT  
		Size: 16.4 KB (16437 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:100d827a4da0aab28101b1104a02e73d67c1b2b3bd2e85616837704f5fcb4fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177401403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50458726018ee78e1b6c5337adf5fd209c5d7598bff68d34b613fcf164b37ed`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:13:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:13:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:13:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:13:08 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:13:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:13:08 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:13:46 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:13:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:13:46 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:13:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:13:48 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773136b18489da474dab6c335e3fb6d61644f01d540ea474ac9f79a4dfb431fe`  
		Last Modified: Tue, 24 Feb 2026 23:14:24 GMT  
		Size: 126.6 MB (126561996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981b90611ca498fc2c87915fd190d7eb75fc1e22b09719855a0a731c20610696`  
		Last Modified: Tue, 24 Feb 2026 23:14:21 GMT  
		Size: 16.5 MB (16483448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25788fd0764163ac3ca68267094c94e43ea5524490b29e2efdd7c3bd115198c7`  
		Last Modified: Tue, 24 Feb 2026 23:14:21 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1236e0bad527783026c262a5625957884bb5ec4c254a978633e1138a99937081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468a60a5ca892ff26a45748bf9c5267b62deb6ded32a421ab7e41c90764d2bb7`

```dockerfile
```

-	Layers:
	-	`sha256:8fe6d0fa050f862c9d5c9fd58591e7c986899eb4826f9cbbed5dd2f7c1db703c`  
		Last Modified: Tue, 24 Feb 2026 23:14:21 GMT  
		Size: 2.4 MB (2381324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b4ab527280ad295e537e8f54681cd097b08acfdadbed70f66c71565b62de4ca`  
		Last Modified: Tue, 24 Feb 2026 23:14:21 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json
