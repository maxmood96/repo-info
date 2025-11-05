## `clojure:temurin-11-lein-trixie-slim`

```console
$ docker pull clojure@sha256:cb606d9086dc88aeebf8697b75178708a1c0633f4e4a1fae91943a7ff306d7df
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

### `clojure:temurin-11-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8e13667d87670d62a1b0d9afebfe2853d9063d052c75a84f43e305baf542b0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196401577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf83ab19f15fb2110d350becde3adfbba1f860a787f5814c6cbde5a641a659a2`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:30:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 04:30:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 04:30:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:30:11 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 04:30:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 04:30:11 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 04:30:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 04:30:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 04:30:27 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 04:30:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 04:30:29 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3ccfde141bb267fb5453aa39d1eb32dce472676d132407f1d776bd52f408a1`  
		Last Modified: Tue, 04 Nov 2025 22:42:27 GMT  
		Size: 145.7 MB (145658325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb39f30c0121aa65622fbee75bac7a8b931c01d9a6955b491d59f628f2e4c36`  
		Last Modified: Tue, 04 Nov 2025 04:30:55 GMT  
		Size: 16.4 MB (16447374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef901f3f9b69addd05244b91c33a23990f42c0a7792fca423e024ff8b0c32f80`  
		Last Modified: Tue, 04 Nov 2025 04:30:54 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6011450f0e6f6316fa06d99eb80f76f0d875272f47e4a34bf637b9608675d908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75bdded5d4f448fa0525be8e82ebad5dbf66dcbcd1aad6368f969f64c1218ed`

```dockerfile
```

-	Layers:
	-	`sha256:5ffafeb703477e4ad51f7b4b2572bc7a14f848a8247281e5d2ab933f29ac3b08`  
		Last Modified: Tue, 04 Nov 2025 10:37:34 GMT  
		Size: 2.4 MB (2383583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0803e10cf3522998a1fc1f82c5f6364c880b80ab21bf84a77a8916a792e6dbb5`  
		Last Modified: Tue, 04 Nov 2025 10:37:34 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fc337b2781ab1b8a4f6e5555897d62e7a937e718be6ebbe829667aa8afbdcaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193534169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79dd3226e46284567e5f9b9dfb849df2072288adb2971fdf362a95e67b3eb4a0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:43:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 01:43:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 01:43:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:43:52 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 01:43:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 01:43:52 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 01:44:07 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 01:44:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 01:44:07 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 01:44:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 01:44:09 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6a9cad07579db6aa11011ed8521e330cc30280180912fd1e295ed0dcc7ef0a`  
		Last Modified: Tue, 04 Nov 2025 01:44:28 GMT  
		Size: 142.5 MB (142460584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9b66acbf92be5314ea7bc2703c6a51895a4d2542c17252306412bc118690d3`  
		Last Modified: Tue, 04 Nov 2025 01:44:34 GMT  
		Size: 16.4 MB (16413530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfb07f77e92c3fd621c478f72174e161ce3aa19e1b2723a4f25da07551b43c3`  
		Last Modified: Tue, 04 Nov 2025 01:44:35 GMT  
		Size: 4.5 MB (4517725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eb2beb54f19edae769ac7e7d9d3548accff040ebd2a4a3e49260fb889aa29ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c899ff4efab09ed9a5d3fc4fc1cd9509580222182df6443afbb6105c6a264b1`

```dockerfile
```

-	Layers:
	-	`sha256:deb345a407b619235fcfa56bf11e6db69a56702559a6c5e97c19c13ebe11f1af`  
		Last Modified: Tue, 04 Nov 2025 10:37:38 GMT  
		Size: 2.4 MB (2383819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25321ae49dfc717c6d484ebfc4fdf75f77e23c75ab89e1ff1a08cc8da5cdc6db`  
		Last Modified: Tue, 04 Nov 2025 10:37:39 GMT  
		Size: 16.5 KB (16515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:74decf56aeba2f3ed3a9a4280a84819c5fde300a8cf216fa938780a46dea55c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187455969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e58671e0aa92f4b6e49537b3b5f14e02013d30a9142ec0bb9a549e9312c336e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 13:15:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:15:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:15:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:15:05 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 13:15:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 13:15:05 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:15:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 13:15:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 13:15:34 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 13:15:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 13:15:37 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075756bad78719f88f0199918d09009fc2e6e1986052db04c6df7dc01db38383`  
		Last Modified: Tue, 04 Nov 2025 23:01:26 GMT  
		Size: 132.9 MB (132853177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506637606c790ee05803d46e3539e45f04773318a538762cd8cbfb227c93bdd2`  
		Last Modified: Tue, 04 Nov 2025 13:16:24 GMT  
		Size: 16.5 MB (16486354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e633bf85a34c99bf32de759d96a240179cdd18ca67da185172ad97eacdc7c02c`  
		Last Modified: Tue, 04 Nov 2025 13:16:22 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:890791ee5a80e61c4a08452b03878ab7cf8d206e41d12be9d68ed124ef2f6cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17a53150a7143ce30b639797fa52af79bfcf82d66bfc06cafcbc133d3dab3ed2`

```dockerfile
```

-	Layers:
	-	`sha256:6943910f880a51ff6c371fa9a8fd21c7a981c14f76371107c11483c6d97a4c32`  
		Last Modified: Tue, 04 Nov 2025 16:35:34 GMT  
		Size: 2.4 MB (2383948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:375d11870336594bddfe8e38ee8e11526ff357e4df7386331a229f76f4023b18`  
		Last Modified: Tue, 04 Nov 2025 16:35:35 GMT  
		Size: 16.4 KB (16438 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a6bf1890042814eb2db3b2cc2df1fc9caf270fe3117237f52e92eb4146be3ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176461040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edf09cd67d5e4d6005e2a978eaff5d357dc46ff3edacd7fe93962af80e6b89d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 12:56:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 12:56:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 12:56:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:56:19 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 12:56:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 12:56:19 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 12:56:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 12:56:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 12:56:31 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 12:56:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 12:56:33 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b642dac8b5169c88c346b13e8b1a9342f34959618791aa4ee459f45519f5ef4e`  
		Last Modified: Tue, 04 Nov 2025 12:57:26 GMT  
		Size: 125.6 MB (125622161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f721ed19d9c425baecf4ed1606ed4eb5e020116d28b25c8bdd998843aeca31a`  
		Last Modified: Tue, 04 Nov 2025 12:57:07 GMT  
		Size: 16.5 MB (16483732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ea05ecdb7aa0b518d55b945a66c6f0b48afb6d757c32e633b2f935be98e7a8`  
		Last Modified: Tue, 04 Nov 2025 12:57:07 GMT  
		Size: 4.5 MB (4517723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:da3859529f3d09b6fc15d86d7533a678326ecea5d2c413d55ec38e7770d7cd37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2396408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506a248d50f711c6dc4dd01bb11b7268e96fb43d8d2d75f3d9952caadc99204f`

```dockerfile
```

-	Layers:
	-	`sha256:cdb2b1d694d2adbbbae24512060e55199ddef793f056924c3c29839f7a5644cc`  
		Last Modified: Tue, 04 Nov 2025 13:34:52 GMT  
		Size: 2.4 MB (2380014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13a8674495a1a4861fb318f4ce1f2383aacbee34e4802d5fcd7e96859215cdd8`  
		Last Modified: Tue, 04 Nov 2025 13:34:53 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json
