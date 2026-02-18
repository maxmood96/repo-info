## `clojure:temurin-8-lein-trixie`

```console
$ docker pull clojure@sha256:7d3034b8cc127fac2b52f8441a28b89cc0e6b2f5e75a1d23b1480690248ba059
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:79b1e5ea5d26b5c353d67b516f323930e28cf8e8aad8990dcf154418bb5208c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127560858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fcc77617fc56156db8ed5cd757e64b914bf1302229e995c9d4c1cc05df89975`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:40:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:40:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:40:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:40:35 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:40:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:40:35 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:40:51 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:40:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:40:51 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:40:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:40:53 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da9f36d4c42ace50c2181040e969a37743ce42ce001a157a4e240dca2dbd0b`  
		Last Modified: Tue, 17 Feb 2026 21:41:07 GMT  
		Size: 55.2 MB (55170109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3584bf20b8cb128902d2fe9a44005ee581ad8a11660331a3adf2d9349f7c1ff6`  
		Last Modified: Tue, 17 Feb 2026 21:41:06 GMT  
		Size: 18.6 MB (18580047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c39b373eec3c05449845a3c85d279bf99ec9edc008ed5f8149688845a769c60`  
		Last Modified: Tue, 17 Feb 2026 21:41:05 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ffde3250dfbce11c81f49f0b1b45674584027c2601a83ef3ae95dd5b4086f10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baef67e24c7c4f486ffb4a895c528e2f78be59c5b5db29d5b0a24db41dffe419`

```dockerfile
```

-	Layers:
	-	`sha256:e3de3315d75d2d23bb51bc6281c0333cdc579f00a4411f5c868dc1e865f05840`  
		Last Modified: Tue, 17 Feb 2026 21:41:05 GMT  
		Size: 3.9 MB (3936480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:218d1461eda4ecf02a0dfdb59dac6db4756603289c8ba51b2eb64ee55292865f`  
		Last Modified: Tue, 17 Feb 2026 21:41:05 GMT  
		Size: 16.4 KB (16352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:79a2a3e6c0bc5cf1bb64d422cac9aca50ce0bdf5f5d38a2bc1a7514d798146f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (126962754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1446c0b4c73db869fae7422459e7306cb8e9c6899ed2f63f9c7bda983c05cf4`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:40:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:40:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:40:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:40:28 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:40:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:40:28 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:40:45 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:40:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:40:45 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:40:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:40:46 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3959ea49351b463b7ec9c28c898cf64b383144394bf7f7f647b1a7b632be1088`  
		Last Modified: Tue, 17 Feb 2026 21:41:02 GMT  
		Size: 54.3 MB (54251611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb052ea82280608b6d23bde293d6d5e45a5269a338f1c5fd58510742cff8776`  
		Last Modified: Tue, 17 Feb 2026 21:41:01 GMT  
		Size: 18.5 MB (18541389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fb510523f3a237fa72d24eec610f5e3cf93dcfb6c36d1f12eb272d33875e66`  
		Last Modified: Tue, 17 Feb 2026 21:41:01 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1c1d5c05909b13a5c43dfc24f8fbece4ec87dfa30b852cffb946a032e6a4aa27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc3d153fc1d825d846edebcaa4e5f5451ee65a501f484465b01ed5689cbc15a`

```dockerfile
```

-	Layers:
	-	`sha256:c2c3819a6c8c68557d32aa01395ff0dc006fbefb59eeda4f9d54a8808a3c0f76`  
		Last Modified: Tue, 17 Feb 2026 21:41:01 GMT  
		Size: 3.9 MB (3938057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96221a427d1f7bf7f5dbdfc66b8e92af2cddd2218eb15be1e1af1175ddef8039`  
		Last Modified: Tue, 17 Feb 2026 21:41:00 GMT  
		Size: 16.5 KB (16473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:3ac6bcd206438fd548bb38c463a0ddb1b29d4a71dbd98666375f735a8cba0953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128917990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a819b95672d84ad342b71a1ed13e49aff7515c6139d21173732f8078d5d94fc`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:59:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:59:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:59:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:59:16 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:59:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:59:17 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:00:49 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 06 Feb 2026 00:00:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 06 Feb 2026 00:00:49 GMT
ENV LEIN_ROOT=1
# Fri, 06 Feb 2026 00:00:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Feb 2026 00:00:54 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e31da8e0f9e130c166e97ec3b0c716f0ac97a7e8894e13f7961b61b37819485`  
		Last Modified: Fri, 06 Feb 2026 00:01:40 GMT  
		Size: 52.7 MB (52650394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa010a11b688da9781b56f422ad99dde4a8add90881bcff6ff236bed92cbc1d`  
		Last Modified: Fri, 06 Feb 2026 00:01:39 GMT  
		Size: 18.6 MB (18637698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcf7bd0b0a0061a1aed36fa7b5145e9fbfd8ec01e3ee4a37d4225e60a4f9793`  
		Last Modified: Fri, 06 Feb 2026 00:01:38 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7805f28dd08797083ba2d09da86851693fdc380cf2d14f0789672936213ae034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4159a60de0154493b4d30b4d37ef1841b08944a5ca640d77ab807cde4fc219`

```dockerfile
```

-	Layers:
	-	`sha256:1d7c532bcdb38c22993c1a648a29e8a6587880f088ad35d9bf4cf73f6e2da182`  
		Last Modified: Tue, 17 Feb 2026 23:29:09 GMT  
		Size: 3.9 MB (3938075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37590b8f031e0ab1bada12b9316dfcf49880b90159d9846006be27e96903a6a`  
		Last Modified: Tue, 17 Feb 2026 23:29:09 GMT  
		Size: 16.4 KB (16396 bytes)  
		MIME: application/vnd.in-toto+json
