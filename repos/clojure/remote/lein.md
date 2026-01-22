## `clojure:lein`

```console
$ docker pull clojure@sha256:af3ade34d9bce1539f78697c69ce6fb6bf5e06765b8bbee3c394a847457fe9a8
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

### `clojure:lein` - linux; amd64

```console
$ docker pull clojure@sha256:4472f4cc11fb806d0d3ee0f4b00fb25550ab068d3b9a3e437bc2354c4b2bfbd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164847478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7a734f20195145c00eeb81a0e8bc824b9b56506ef3693c62f3711907479c34`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 02:02:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:02:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:02:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:02:45 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 02:02:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 02:02:45 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:02:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 02:02:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 02:02:59 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 02:03:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 02:03:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:03:00 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:03:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164b494a12da7ff970d90e5da2cda60dff9ed8f6889a63344fee2624f616b08f`  
		Last Modified: Fri, 16 Jan 2026 02:03:20 GMT  
		Size: 92.0 MB (92045288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9cc54e54f6c5a6b7cfedcc71d9f64d8d05731a4f99ec17a514dc367bcdb4f02`  
		Last Modified: Fri, 16 Jan 2026 02:03:18 GMT  
		Size: 19.8 MB (19802428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0634370efd48dda361d0b2f2851dd1bc9af1b6bb4eefa109039c9f0f1c5a49d8`  
		Last Modified: Fri, 16 Jan 2026 02:03:17 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96edf77acb4b2223062ef42ca471009dbf395d9a3cc21222097997ec449862a9`  
		Last Modified: Fri, 16 Jan 2026 02:03:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein` - unknown; unknown

```console
$ docker pull clojure@sha256:7d98da0b853bbd577d72ca576d12f445771e9c30a1786c3d8c59bf15bf6b2c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4253298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6efe5be2d45d9174d27631299a3268ddf510025cca6c547d88fe4cb6f8dc6a2`

```dockerfile
```

-	Layers:
	-	`sha256:8b5440db11e0a279dae318ab9d411689fd44ac44fd8ce990ddb232110a853603`  
		Last Modified: Fri, 16 Jan 2026 02:03:17 GMT  
		Size: 4.2 MB (4233039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:656b565bd95b6f1b6135384d4147613af515fc2167ced609b86c9c21057c8615`  
		Last Modified: Fri, 16 Jan 2026 02:03:17 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ee57817d877a0bd72a4599a4f481be629d32121d3b67f77655937b07a2e49c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163569461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0451890ae13c95214c78ad6e94721e14747591ffd9781278015945bb9f95e7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:42:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:42:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:42:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:42:08 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:42:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:42:08 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:42:22 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:42:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:42:22 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:42:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 02:07:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:07:53 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:07:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed151cd1f87e92a724d9a48e309d58a18cd805ebf4483e572e60dfe7d0f8d36`  
		Last Modified: Fri, 16 Jan 2026 01:43:19 GMT  
		Size: 91.1 MB (91052515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118fb0333c17c4c6592a085efe7efc72ba08e3e07947ae9add0be953e073dedf`  
		Last Modified: Fri, 16 Jan 2026 01:43:12 GMT  
		Size: 19.6 MB (19632706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5b65a6273426c2f029bdbcdf4d516054f3cade5a35d7c0b3ae2c5e80480f79`  
		Last Modified: Fri, 16 Jan 2026 01:43:10 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715d75c569b5ce250c4dccbf39820625591ba89e07db04347dea4c90935027b0`  
		Last Modified: Fri, 16 Jan 2026 02:08:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein` - unknown; unknown

```console
$ docker pull clojure@sha256:7d9dac766e9422259ff9f2b925864235ebf41f60716b1c99d2126ced542dcb64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4253175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869fd30e0bce723fccdba2268e936841a372102a97fe1804c50a3195a1220fb5`

```dockerfile
```

-	Layers:
	-	`sha256:144fdc7fedab33f0cc3e6f153b19d0dcfdc4931933f41b1d25195643e4765aae`  
		Last Modified: Fri, 16 Jan 2026 02:08:04 GMT  
		Size: 4.2 MB (4232723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e846aaef646600c6dc6c684c48e74bc018782b262d76d12f0d38b627a81fc39`  
		Last Modified: Fri, 16 Jan 2026 02:08:04 GMT  
		Size: 20.5 KB (20452 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein` - linux; ppc64le

```console
$ docker pull clojure@sha256:ba30b9dd4328e3bce836b304e9bb9c4ca608dbda822ca06e014fc42d1d2b1c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168478858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bfa84eebce07fd4ecfe5f86a13d2255021d9118f82e4b2d2b8e42be3943ecd9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 02:43:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:43:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:43:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:43:19 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 02:43:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 02:43:19 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:44:05 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 02:44:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 02:44:05 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 02:44:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:42:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:42:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:42:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96a2bd88573c70d41d7945da863a10fbc76252e0180def2eb63f3e259f7f1fe`  
		Last Modified: Fri, 16 Jan 2026 02:45:52 GMT  
		Size: 91.6 MB (91610764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259c1135f98921991ae84772c0a37916fb368af39e47c22694bf0d3645512503`  
		Last Modified: Fri, 16 Jan 2026 02:45:49 GMT  
		Size: 20.0 MB (20022500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2caf94f89bf158a1e26bca0e2b0bc88a465abc44e79b816fc7248dc275efdfa`  
		Last Modified: Fri, 16 Jan 2026 02:46:02 GMT  
		Size: 4.5 MB (4517790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07e18eeaf2f582ed94d300b69b9b650fa1e5535d475c8b8177ab019bcc7ac1e`  
		Last Modified: Fri, 16 Jan 2026 03:43:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein` - unknown; unknown

```console
$ docker pull clojure@sha256:ee3a41ed1817aea73efc60eca0b67552f8cd6de370ded92bf0265101c80b2a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4256573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce34bed38a2727327dc6be725300801a42ab2c095daa33761eebcc2362cc2448`

```dockerfile
```

-	Layers:
	-	`sha256:a2947bdfa6059759e29f2861d4608e722d4be4b08f660902701f6be382e7e6fb`  
		Last Modified: Fri, 16 Jan 2026 03:43:01 GMT  
		Size: 4.2 MB (4236234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38a64f2b34a398675d7480157859250ec2ac19c6418117479cac1f153cbf9287`  
		Last Modified: Fri, 16 Jan 2026 03:43:01 GMT  
		Size: 20.3 KB (20339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein` - linux; s390x

```console
$ docker pull clojure@sha256:cb1ee1ab722928b65a83da409b258025463d7ff078e7b706275e660f32d41d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159329259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0526cdc796aaa00491c2b73c86050602a212ac3a84081e47c5c64b17af3521`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:08:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:08:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:08:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:08:54 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:08:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:08:54 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:09:05 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 15 Jan 2026 23:09:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Jan 2026 23:09:05 GMT
ENV LEIN_ROOT=1
# Thu, 15 Jan 2026 23:09:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 15 Jan 2026 23:21:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:21:37 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:21:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bcd3733e73d9ad16f59673e9b75fbd8e9079e28b7929234c36c4708a507416`  
		Last Modified: Thu, 15 Jan 2026 23:10:16 GMT  
		Size: 88.2 MB (88210681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4736bc87370c20e32ad01048119c977304c04bb19a3fae4f6c5c5d02c35f7d47`  
		Last Modified: Thu, 15 Jan 2026 23:10:01 GMT  
		Size: 19.5 MB (19462003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7d46bebaa2b51d5ebaa2a924db156b423750b481941ce4e238ea889ee99018`  
		Last Modified: Thu, 15 Jan 2026 23:09:50 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01469230179b14623bc5e1adb4593f6850cc3c4e7fe79e185cf5c96a2c30f131`  
		Last Modified: Thu, 15 Jan 2026 23:21:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein` - unknown; unknown

```console
$ docker pull clojure@sha256:78c89e2964659be1bc012b152fedcc0fd5b4f21e72bb2b49673e84078098ecb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a79ba1f5516f09d141521901d4e7fd21e1ce070e90c38047ccb035cecb855c`

```dockerfile
```

-	Layers:
	-	`sha256:609dc04570bb85f7d2462a34d87b50f99c94e0ebecb58d11d17979a6db5dc90a`  
		Last Modified: Thu, 15 Jan 2026 23:21:50 GMT  
		Size: 4.2 MB (4227401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e8e7665824e9f314b89eee23a68f35a8ba4b8ac8a1406686f7d75c67c0ca0ea`  
		Last Modified: Fri, 16 Jan 2026 01:35:57 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json
