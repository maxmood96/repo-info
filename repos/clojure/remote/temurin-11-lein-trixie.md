## `clojure:temurin-11-lein-trixie`

```console
$ docker pull clojure@sha256:0f98d9df96364c1352ecbcdb0f933280e113f1e372c9b474484db8d1c89f9992
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

### `clojure:temurin-11-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:3d759245ea9e823c21fc1a1442502ca4f91d2540378df7e1086fac8aa4ac2ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217353568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f1c8e052522e32c0361faed33e49beee047bc8d495009ec4abe969273c88a1`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:55:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:55:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:55:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:55:01 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 00:55:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:55:01 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:55:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 00:55:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 00:55:18 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 00:55:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 00:55:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bd2513d316c3de979863613b697f25f9fd113b6e1f06712a21924bcac57849`  
		Last Modified: Tue, 30 Dec 2025 00:55:58 GMT  
		Size: 145.0 MB (144966651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70ffe16420b0596954ea3089a6e9f2c3b116e8d25233f56fc8fd32a670484f3`  
		Last Modified: Tue, 30 Dec 2025 00:55:52 GMT  
		Size: 18.6 MB (18579576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c976d14b40feb31a9c1782e6a70c5ae3fba70635cc42a6146cd476ade20db1`  
		Last Modified: Tue, 30 Dec 2025 00:55:49 GMT  
		Size: 4.5 MB (4517722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a0098b6431226a5a4760b380cdbcb768320fe0eae372b98f91f23cbd927c548d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5291d90b6be7e41bb157203723a7b2848f6dd5b00c6975d62cf6cd2fbdaa1c50`

```dockerfile
```

-	Layers:
	-	`sha256:83972246a1c3dfbda0d66754241a8cf107d6af5b9445466a82f7a0f985853e70`  
		Last Modified: Tue, 30 Dec 2025 04:37:43 GMT  
		Size: 3.8 MB (3833519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1c9476c3d293b48f7f5d4c0283ed8a5901d08725d139450209f616c85e677fb`  
		Last Modified: Tue, 30 Dec 2025 04:37:43 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6338aacd2e4d4afca9b5270c75cfbb3c6388cee061fec7433e71df53dba8730f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214440093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84797d7a6300ac87992c1fef1048d9c3ffead7cde00915db253cc8392f4165af`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:56:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:56:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:56:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:56:32 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 00:56:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:56:32 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:56:49 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 00:56:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 00:56:49 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 00:56:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 00:56:50 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20d643f9467d1a7cbd673f2ea7017c6da014950c1af77080e7255fb26ac8af7`  
		Last Modified: Tue, 30 Dec 2025 00:57:25 GMT  
		Size: 141.7 MB (141731577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe26e67381d20a79f1dbbfff08cd7f9d323009d660ed72cac8af03271a4c0aa`  
		Last Modified: Tue, 30 Dec 2025 00:57:19 GMT  
		Size: 18.5 MB (18540573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2747912f0aa9e6f62cb21f7720d3b34da6f6cdaeab62e12f2945fa3a1bc3d9`  
		Last Modified: Tue, 30 Dec 2025 00:57:18 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8cdf8720f63340b061b7a710ababb857b310235e0b97caf401bd358ff6653600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3851499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c41b428ca6f9e833e378debeb79af31fa405eb3b2feb2ef01c6ef54022abff7`

```dockerfile
```

-	Layers:
	-	`sha256:3a7ceb08f6fdd61c87156151c8dd4cc2a4b97166dba56aa7207ae6a4a9935ec6`  
		Last Modified: Tue, 30 Dec 2025 04:37:48 GMT  
		Size: 3.8 MB (3835014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da23f3d959a93271125c9e7fc9ea82205a6e38c2c00bfdcf18f2833794b9cbbd`  
		Last Modified: Tue, 30 Dec 2025 04:37:48 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:3484ff3c58099b0babe621fdd782f89e308cfb2ee5e3356b6a0751681bd4e4ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208345222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51792fc73346d5b2a9ee187ba4c8d52795f7d34085a1d8973f2d8906ec27aec1`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 05:15:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:15:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:15:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:15:55 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 05:15:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 05:15:55 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:16:41 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 05:16:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 05:16:41 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 05:16:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 05:16:45 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac6c6730eaba1ceb02f2452db48e2462e345b11bc91b812b8459fa6340514af`  
		Last Modified: Tue, 30 Dec 2025 05:24:31 GMT  
		Size: 132.1 MB (132081947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a42e20d3be523de003ffcf2a4e3e6932acaefc5602b6b75ccda3799a4c237c`  
		Last Modified: Tue, 30 Dec 2025 05:17:34 GMT  
		Size: 18.6 MB (18637049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ff851eac9d5285a564e1c51de1143652e046302472e4eeb5689e6fb949829b`  
		Last Modified: Tue, 30 Dec 2025 05:17:33 GMT  
		Size: 4.5 MB (4517709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fe9b2efd32879b5aa9b1efa6d79ed89c9f2904910cc9a2d49c82109965841bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ff57c0ce0e98a2b123b803e33c2471d880115c7aa11d520c4b5a2ff1eb5d3c`

```dockerfile
```

-	Layers:
	-	`sha256:f8a548584049db5eaa2928ba7c0927f6041631ab6bc5f2f1fed48657ee622a82`  
		Last Modified: Tue, 30 Dec 2025 07:35:19 GMT  
		Size: 3.8 MB (3833902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e107cdb1578d0c329065d280da5b15d298b2f96bab2553313888de640167561`  
		Last Modified: Tue, 30 Dec 2025 07:35:20 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:32e36c5166cb436de3e9ded6d90094a06b0c4136bbf9cd65a899705da00ae068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198178711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2870f04b283024273d54ac1f18f9d36296d4f4674c3a9819246b87dff7ec91`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 05:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:46:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:46:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:46:08 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 05:46:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 05:46:08 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:46:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 05:46:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 05:46:23 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 05:46:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 05:46:26 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:85bc4a4d1f4e52a33d42907057e0ab87c5eb2560b332d94f6e9d7da79c0c76b8`  
		Last Modified: Tue, 30 Dec 2025 03:26:29 GMT  
		Size: 49.3 MB (49345959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b01d36ba1f6a1190b4da37280aeb379ded8c4027b73808d2505bcb4c0320029`  
		Last Modified: Tue, 30 Dec 2025 05:47:05 GMT  
		Size: 125.7 MB (125694405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54bf32fa0c45bb3c7a31dc0147b9b5c243d37987bc7d0611e1dcb271326b885`  
		Last Modified: Tue, 30 Dec 2025 05:46:59 GMT  
		Size: 18.6 MB (18620560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1f31a89a356f6caaf74ca7de475e5c9c3afb76ee3aaa05c5d610faa4a2dfb0`  
		Last Modified: Tue, 30 Dec 2025 05:46:58 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c19dc2fae27bedbbc46e69a6908e9f4e7b1c83cefe574c3a9ec797dafcb2154e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3846314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c632317a78409fd901e45ba0ccf713286806a935f3821c52e7c800bc8c8a487f`

```dockerfile
```

-	Layers:
	-	`sha256:7d08888da276e1fb32a55ca52d4a0f5cfe64fc94d7882234da7cda2d1a208500`  
		Last Modified: Tue, 30 Dec 2025 07:35:23 GMT  
		Size: 3.8 MB (3829950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b75ae8172e9d2009113f5087d2557755be9ce6722ca05ace453f3911eeab7e6b`  
		Last Modified: Tue, 30 Dec 2025 07:35:24 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json
