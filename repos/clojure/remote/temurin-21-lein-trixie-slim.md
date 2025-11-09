## `clojure:temurin-21-lein-trixie-slim`

```console
$ docker pull clojure@sha256:38d8eb4bb5bdd0f6ba8b9005b708081cd27a82dda7b8c602d45526d2420fb6bd
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

### `clojure:temurin-21-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:06e897dd504980013273e40a8c72eb1622eb7a5ca70074287d448c37680ee7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208569663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc09a9c0b8bbf6e072ccb0fe4181f458748f5febf0fbf730611073cd33cd94c7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:44:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:44:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:44:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:44:33 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:44:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:44:33 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:44:48 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:44:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:44:48 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:44:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:44:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:44:50 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:44:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5ac102dda8cfc39e3d55a3ea1d2d641bb0a191916dffa94e421662d987dae2`  
		Last Modified: Sun, 09 Nov 2025 04:26:04 GMT  
		Size: 157.8 MB (157825965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0453b860447a35a7cf5d00a66d8e37bb537bd137b1dbaee071baf353a9f3705`  
		Last Modified: Sat, 08 Nov 2025 18:45:35 GMT  
		Size: 16.4 MB (16447425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fa9cf617734a4540100bf14aeea149a06d45160e95af981478fdba86ee738b`  
		Last Modified: Sat, 08 Nov 2025 18:45:34 GMT  
		Size: 4.5 MB (4517740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9216e1062e9f744eb5aaf50a259e6b0880152910d322c1ee21eed18ad5a6c4b2`  
		Last Modified: Sat, 08 Nov 2025 18:45:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:25d043379cae0d24556c0869dcbcfa6100fb5518d8401137793430a4d0ddd744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed81eb7a6d147d45f59ec572b00709fd405a22430aa9f6aecc4be0f0bd6c83bf`

```dockerfile
```

-	Layers:
	-	`sha256:56b0bfe92454e65df687a6e411cd39b7d3ca0766811e81130313b12653181eee`  
		Last Modified: Sat, 08 Nov 2025 22:48:39 GMT  
		Size: 2.4 MB (2366546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aac9520f2f27a556cfbc08d49c44d44c3132a7a2b920ab5804f41fecb622ecb`  
		Last Modified: Sat, 08 Nov 2025 22:48:40 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1caeddbd6ae4713bf368dbd1027644d45a38b40247324fcaaafdc46f789a15f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207181603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aeb5aa483b25f40234cf81ba32a508fad9a377db8cd08e0b680af53e2c53f1e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:44:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:44:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:44:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:44:02 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:44:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:44:02 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:44:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:44:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:44:18 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:44:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:44:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:44:20 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:44:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc9fd1684d2e79c9f2337ebf3a0033d27a922264344e343b4391decb596189c`  
		Last Modified: Sat, 08 Nov 2025 18:44:42 GMT  
		Size: 156.1 MB (156107603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cdf930334a6b65678c793ab0c4c58246f7ccb34c3ac577e98ef8f5181e949a`  
		Last Modified: Sat, 08 Nov 2025 18:44:57 GMT  
		Size: 16.4 MB (16413517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78996e61169bb4a493b7b3b20d7386976d4c2ac5a927b00b134bd8892ca66f6a`  
		Last Modified: Sat, 08 Nov 2025 18:44:55 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c70f731fa1d0c65e46d1704a17a013788623771288829e8347b453aea69a43`  
		Last Modified: Sat, 08 Nov 2025 18:44:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b2aec3282fd59677109f68da910c3554a98274eab1eab8582fa987bcc5d4c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd02fac6af57f487b359307337e8835cbfcbb5bfb2550142c2b46800ffd44111`

```dockerfile
```

-	Layers:
	-	`sha256:096196474763179c9c8b3a02dd57d51257a862c0056064a353ce45532a548fd4`  
		Last Modified: Sat, 08 Nov 2025 22:48:44 GMT  
		Size: 2.4 MB (2366164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79e8bec0e7cf75d31df5dc99f45a9c123de12c9c9d848daeb8e1e15f6e72b708`  
		Last Modified: Sat, 08 Nov 2025 22:48:45 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:da5dc37e5f34cd223ef14db75ce7466e101f65278e094f64e400bdd009232218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212546135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b1056abc771e340ecced6cbc0054fed717b3f9ca0694756de4e763c2bb84e4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 21:36:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:36:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:36:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:36:25 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 21:36:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 21:36:26 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:36:55 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 21:36:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 21:36:55 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 21:36:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 21:36:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:36:59 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:36:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415390733088512f768bce0a8253b48875f9511f6c4dcb6f7f3efc679d791f76`  
		Last Modified: Sat, 08 Nov 2025 23:04:04 GMT  
		Size: 157.9 MB (157942893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99d85b6b052d90c224163ce3894f2163e9a1c59d2ebf1ccacc3bd82c5ed845d`  
		Last Modified: Sat, 08 Nov 2025 21:37:45 GMT  
		Size: 16.5 MB (16486428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab494078ec2a29c3e1f85648eaf96811296428a52b34de00f324772749c9dfb1`  
		Last Modified: Sat, 08 Nov 2025 21:37:44 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b7f84bdfdb05dfac5de1b8f0a887cfdcdd742b2f921212caafa668457ad90c`  
		Last Modified: Sat, 08 Nov 2025 21:37:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:87db32c61770f281bd39fd7aed7c77c8d76f7f93a058f8a98c2591b74614417c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd8449be558e5b99e5b8a286595beb24a9990d16acd5ca60c40575716936fd2`

```dockerfile
```

-	Layers:
	-	`sha256:cc6d6ec89e5ec74c1d0b3937c8bca272ca92638f47efd884efea92cc300c5f36`  
		Last Modified: Sat, 08 Nov 2025 22:48:49 GMT  
		Size: 2.4 MB (2367526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b824646c184ee638d1801c82bbd8df1ab9dcbc9c1629fbe6bdda4eed1029abf5`  
		Last Modified: Sat, 08 Nov 2025 22:48:49 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:7889818db082b9e44ce0eac45e8c55b1283f42d037fd847786d7c9a9e44cc157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.8 MB (202785614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8196c8faa402c81327b3dc78ff59f8bdcc7942b16eaa238962b4df0f4292877`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Fri, 07 Nov 2025 06:39:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 07 Nov 2025 06:39:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 07 Nov 2025 06:39:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Nov 2025 06:39:40 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 07 Nov 2025 06:39:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 07 Nov 2025 06:39:40 GMT
WORKDIR /tmp
# Fri, 07 Nov 2025 06:41:09 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 07 Nov 2025 06:41:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 07 Nov 2025 06:41:09 GMT
ENV LEIN_ROOT=1
# Fri, 07 Nov 2025 06:41:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 07 Nov 2025 06:41:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 07 Nov 2025 06:41:25 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 07 Nov 2025 06:41:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0db3eb8e5337e5bca5167ab6ffe6048420e62d22a7ed6f5b99c7f187ac58dcc`  
		Last Modified: Fri, 07 Nov 2025 22:59:41 GMT  
		Size: 153.6 MB (153593538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04eeb2232647e702a831003207c488170fe5926961743c13ba06a4f5530079e3`  
		Last Modified: Fri, 07 Nov 2025 06:45:52 GMT  
		Size: 16.4 MB (16398084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da31dbac25fd0ad46543c5cd3c30e95a2fd2ac9ca6b19808772acfd366a1ee9`  
		Last Modified: Fri, 07 Nov 2025 06:45:47 GMT  
		Size: 4.5 MB (4517776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41865be74a49f8eb23c7a6fd05ce6b9ea2aab2ba1fd67e8c8bb130eed59b571`  
		Last Modified: Fri, 07 Nov 2025 06:45:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a5e4ca58ddce1146990b4a2f93d4c230dc11c63238101e227648d8b77339fb88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1618169625a6af5af081637f08d49808adc244e859d99e5c0a14e6ac805e04e`

```dockerfile
```

-	Layers:
	-	`sha256:01e20be17699e83148cb595fe855985bc77c50f0906195336e5b076371613b9d`  
		Last Modified: Fri, 07 Nov 2025 10:37:00 GMT  
		Size: 2.4 MB (2358592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:900211808b8622c829578d0feb794811e73cf44efcd7d8284326322f0500655c`  
		Last Modified: Fri, 07 Nov 2025 10:37:01 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:400d47467601c0ddad8ca344e84bda850f136b756c78d2eeccf42dbaf214ae91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197909187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f228e8247c62afce2f84fd41c33b82b489c5a04e4030450ba41d29a48dff75`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 20:31:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 20:31:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 20:31:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 20:31:19 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 20:31:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 20:31:20 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 20:31:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 20:31:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 20:31:31 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 20:31:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 20:31:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 20:31:34 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 20:31:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b891b02a41c144ad667375203af22ef67797f89fef67b5503aca8b9fb1eeb108`  
		Last Modified: Sat, 08 Nov 2025 20:31:59 GMT  
		Size: 147.1 MB (147069879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16abb1346e17c79c40ac4da3aa13a70dbad20043a8527f4248c1d11172ddd04`  
		Last Modified: Sat, 08 Nov 2025 20:32:05 GMT  
		Size: 16.5 MB (16483734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efefceffb328e4fa2ac82f25c87395d87447f816d64ad53379af97c61694818`  
		Last Modified: Sat, 08 Nov 2025 20:32:05 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b6644093d23135b78963ea4e2fdc4aaac57a9578c368656766e7fdf799b7bc`  
		Last Modified: Sat, 08 Nov 2025 20:32:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2a4f354ee257ba0a2c45200e10b9e18608f1becbf2a2be7cd8634c7248ac9890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f195a6c8f2a03c099b77180c111507a3ec075c842cea410cefb4fbc1c4ba1f6a`

```dockerfile
```

-	Layers:
	-	`sha256:22a2c62bf96092f5fcaaa41325e6a256f0535a4dc1173f77d2b426b6d184f468`  
		Last Modified: Sat, 08 Nov 2025 22:48:56 GMT  
		Size: 2.4 MB (2362973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aec3a08e7caad2423bc154e258824991c58503e7fded8d67739aaf7111aacda5`  
		Last Modified: Sat, 08 Nov 2025 22:48:57 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
