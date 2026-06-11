## `clojure:temurin-25-lein-2.12.0`

```console
$ docker pull clojure@sha256:db205425383e78a14bc92db226a990b60819295090a7a5cdda6ae07105ce69fc
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

### `clojure:temurin-25-lein-2.12.0` - linux; amd64

```console
$ docker pull clojure@sha256:6e61d98c2ad8d0c82be8b86f9a01b412470b5dd899e3262ad94ba426440f545b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165407987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03eae289249585e5b9185ce164dbf3b247f72c2c4aa225365657740c0258b7d3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:20:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:20:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:20:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:20:37 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:20:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:20:37 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:20:51 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:20:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:20:51 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:20:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:20:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:20:52 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:20:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85147c5f2117bd04b931199ec409a76fc936c63110a25f497330ba6b8ca1c68`  
		Last Modified: Thu, 11 Jun 2026 01:21:11 GMT  
		Size: 92.6 MB (92574599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3faa3c7ae0f0618d691bb1f01dc2de0d4afeca62ea7fcd3f618be02033162db`  
		Last Modified: Thu, 11 Jun 2026 01:21:09 GMT  
		Size: 19.8 MB (19813158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76190ede90ed606e6c374e31848f48987f50bc0822f2e1a463948bdb8215e09`  
		Last Modified: Thu, 11 Jun 2026 01:21:09 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e31da2b31515a4a486c8958148224851b6302805f2ed8428aad63e6ef9215a`  
		Last Modified: Thu, 11 Jun 2026 01:21:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:06ba07cb9cdc004dd60178004b3b3a369f2d0871594fe08ab6066dfc6bc6f3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e89bf0ef8291ba9c5da93d51e9eca04ecef8d1ea8e300c801b62ede744533d`

```dockerfile
```

-	Layers:
	-	`sha256:de63242d53c7f6b1ceef919dbef3ee87e98b79f6574eaa826736f327ff36fcff`  
		Last Modified: Thu, 11 Jun 2026 01:21:09 GMT  
		Size: 4.3 MB (4251686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bda4acf072455b82681eac6713babba7db7966135eda99c95f26b921e01e1b4b`  
		Last Modified: Thu, 11 Jun 2026 01:21:09 GMT  
		Size: 20.4 KB (20413 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2c6e57f159fc1fbbf8ce87aaecf665062e8a33306aaf84418e14118a71a73110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164092380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578a7e40eeb91dbd78f423032296fb0cc6a57225367defa7ce4476aa363684cc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:19:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:19:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:19:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:19:21 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:19:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:19:21 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:19:37 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:19:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:19:37 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:19:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:24:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:24:26 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:24:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a8a223e1e5b53167dea6c5cba0328181bdb1b8569b95271e7c51e65f08e493`  
		Last Modified: Thu, 11 Jun 2026 01:20:20 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e87f4d738adaddde2ff37024abeaa530d09ad20e4f55b14b5dc45a1d01dc3af`  
		Last Modified: Thu, 11 Jun 2026 01:20:17 GMT  
		Size: 19.6 MB (19642949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349ef78040f62a8f1cc6ec00c4397169978679ac08b71739800742ac25ec447f`  
		Last Modified: Thu, 11 Jun 2026 01:20:15 GMT  
		Size: 4.5 MB (4517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54293434749587a0b3a42acf113e8ab07fdae54f129b233e6e6819c16f51daf4`  
		Last Modified: Thu, 11 Jun 2026 01:24:33 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:8fb509227ccdfe2c6b2df55821f0b17a526036a40dc6f619bb7261f52b5f42eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc4f1dbd08ff6687f0761765ba2895bbf8b47a48c7fea361279bf9560159c7d`

```dockerfile
```

-	Layers:
	-	`sha256:b4d8862aefdf24dc7e6568d53bd1b8b02c0ec0465cc60d7baff11767d095be4b`  
		Last Modified: Thu, 11 Jun 2026 01:24:33 GMT  
		Size: 4.3 MB (4251370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1bf01223c45d6d58c19ee717847dcbf6758725e0c0c87bb01de4e8950df867e`  
		Last Modified: Thu, 11 Jun 2026 01:24:33 GMT  
		Size: 19.7 KB (19653 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0` - linux; ppc64le

```console
$ docker pull clojure@sha256:48b6bb7b9cccd7b9311a3f4f1b5912065c66e7fb1e6ee394f50243b44b8d097b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168805710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233c8ac37f69140d8454be13a2c099c31baec121f9d53b3a66d28969a6d4b6a4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 05:41:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:41:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:41:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:41:51 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 05:41:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 05:41:51 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:42:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 05:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 05:42:24 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 05:42:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 06:05:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:05:27 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:05:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9d252f0e38d109f9943592c87001ada39f271784191f398d66e991f1eda37`  
		Last Modified: Wed, 20 May 2026 05:43:46 GMT  
		Size: 91.9 MB (91914038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35d3313261f425bb57fe0ec2df94d71655d5cab502cf29befe49b7076ac4b95`  
		Last Modified: Wed, 20 May 2026 05:43:42 GMT  
		Size: 20.0 MB (20033270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583ae030626da8366bd7fd80799babfa8092b34004fc94d6d0e6d56dfb0b43b9`  
		Last Modified: Wed, 20 May 2026 05:43:42 GMT  
		Size: 4.5 MB (4517774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b93b4cf56521576bbc55413a47dd3cf10f21f074b68a96bd3486d9954b1b1d1`  
		Last Modified: Wed, 20 May 2026 06:05:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:71b9f89cc22dcc3aa17483fa2e52fae7e5fe8c38b60c530c53d86086b8688586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4257370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3995ee7f8a47733bed335a6a04420014b3ca1e52c6002d9f6e5e16612e96efa`

```dockerfile
```

-	Layers:
	-	`sha256:bd53a7dfe496b67b4fce4f802da9e96edb28075ad45afd898f679b3f326ff291`  
		Last Modified: Wed, 20 May 2026 06:05:45 GMT  
		Size: 4.2 MB (4236877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2792cfaec70394728932fc0a1caa540b01b82f9fd081601c87c80fe39cdcf02`  
		Last Modified: Wed, 20 May 2026 06:05:44 GMT  
		Size: 20.5 KB (20493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0` - linux; s390x

```console
$ docker pull clojure@sha256:9bfbaf3336cec5aa7d00be287dc0e3e254057437d9d13aa11428f23bcb34ea86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159575047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993c583925cc0b981ace8cba047d3919c4a646846982d413c23e8e251b97c871`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 03:13:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:13:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:13:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:13:15 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 03:13:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 03:13:15 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:13:26 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 03:13:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 03:13:26 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 03:13:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 03:13:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:13:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:13:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d5d28a9b892aa865b958e34a0eeffbccb54b6231b8f8f42d3512025b674cad`  
		Last Modified: Thu, 11 Jun 2026 03:13:56 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae6d0573e77ca9cc639e4290d813b3ffb6aba14b3706e0f784cea4114bc9c43`  
		Last Modified: Thu, 11 Jun 2026 03:13:55 GMT  
		Size: 19.5 MB (19475055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c697d5e928e2c45c6e7c24cdc74f200030570d1eee13ac615f6f2e8efc9c037`  
		Last Modified: Thu, 11 Jun 2026 03:13:55 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a6ffe98c189ae44972e944fe98ed57f0713abd0b918fb36b0a7e90bdd717eb`  
		Last Modified: Thu, 11 Jun 2026 03:13:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:afc0c7f2d3766f05791033c64d1740396a7706f2f9a791bec3e888664de3166f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64f93d7031a141a80039b7dbc4c44b0dff41fdd4f9ca4110cd28a8f4bff0477`

```dockerfile
```

-	Layers:
	-	`sha256:dd288f4bb1d5f6d69471abbaf4cd3cf0d916853b5dd4fa7f9c7df58e3333deab`  
		Last Modified: Thu, 11 Jun 2026 03:13:55 GMT  
		Size: 4.2 MB (4228062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88077fec7a56b69d9e86b3dc4f87dd2d68e179211eb1d9c4ebbc8492d4d42f5b`  
		Last Modified: Thu, 11 Jun 2026 03:13:54 GMT  
		Size: 20.4 KB (20412 bytes)  
		MIME: application/vnd.in-toto+json
