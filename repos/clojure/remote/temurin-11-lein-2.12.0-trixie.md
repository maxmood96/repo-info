## `clojure:temurin-11-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:898729c51d4c5b7d4aa0c5a584797687a58b5d127fa0eb008ea14098ff593ea4
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

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:c0c7181f72ef73bf9eae28798d5c7cd35af2759a7ce7479835f1f78b62956444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.0 MB (218040874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a548538a559f5dc0d2d0cd0aca3a5e25d891d6723898574e13cf652132064d81`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:30:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 04:30:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 04:30:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:30:08 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 04:30:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 04:30:08 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 04:30:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 04:30:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 04:30:24 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 04:30:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 04:30:26 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db43675f8624903db9ce47b5c4c35ce2b59962715058eaf64d8cd63f7fb92bf`  
		Last Modified: Tue, 04 Nov 2025 04:30:45 GMT  
		Size: 145.7 MB (145658350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744b68290d5b1648aa55d1478e4a15d6e64b28e1120a7de7a19b8a8f13b8f3be`  
		Last Modified: Tue, 04 Nov 2025 04:30:51 GMT  
		Size: 18.6 MB (18579126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51adf6e63d2bc68f5162c73786a16de2f62bc86ddd4657cd4310b5f79267392`  
		Last Modified: Tue, 04 Nov 2025 04:30:50 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:44b50527596db1a12d1212946cc5c12e3ef67a7b2ea09885a58a1a9c41180e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc17428e79b9345aa3d7787e18ae5d9ec0a299bbe4f9da3f60be762da5de9823`

```dockerfile
```

-	Layers:
	-	`sha256:92ce10d87b33f22da245edaa7fcc6d657bc989687da880c27dd4ad435696f8f5`  
		Last Modified: Tue, 04 Nov 2025 10:37:24 GMT  
		Size: 3.8 MB (3833525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61519da8a66b5533f3d0c867c15c8a1fdc94fcfb2c2ab8bdfb443fc601e16fd4`  
		Last Modified: Tue, 04 Nov 2025 10:37:24 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:85c4a04169c3ab76da5669769960788c32aecc39b85c39263644065fb7a5d192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.2 MB (215168650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5330eff2e0008d61cf63a03979c5e66e87800761905968fdf7d276372ce996b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:43:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 01:43:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 01:43:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:43:44 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 01:43:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 01:43:44 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 01:44:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 01:44:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 01:44:00 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 01:44:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 01:44:02 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bde7315d390090bbc8b1e62be16bc27a13d740611b7852110e7e31d09193d6`  
		Last Modified: Tue, 04 Nov 2025 01:44:23 GMT  
		Size: 142.5 MB (142460584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7792fdb47a65d24641219f24f7f129357ac84841dff1da0b555542d1c13fe34a`  
		Last Modified: Tue, 04 Nov 2025 01:44:30 GMT  
		Size: 18.5 MB (18539898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97242474ddca5c581529853d86014fa6cde0ffcfeebc97187c974f4d02fc76b`  
		Last Modified: Tue, 04 Nov 2025 01:44:29 GMT  
		Size: 4.5 MB (4517706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:409b478c9358d02391c62500b0b462ff2c46e5782678a2c5cc341c77619f1199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3851505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83e7c8a5e07849ee9c6f939694fa877c62a7ac5a0a187af6d31184c2b609fab`

```dockerfile
```

-	Layers:
	-	`sha256:b49df038ab10c5051ec5e28502503e26fc8e1040acde7c1c9962ed0f9005ccb5`  
		Last Modified: Tue, 04 Nov 2025 10:37:29 GMT  
		Size: 3.8 MB (3835020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55232d3a58e0b5638a52f15fe4280b8e654967f934f01425fbfe30177ded409`  
		Last Modified: Tue, 04 Nov 2025 10:37:29 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:8601569279df640fb91ae679373fc95687026697a5563d47c431b05361925fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.1 MB (209116971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883738d914134a97183491865c5443df31958c2889f77ecb0bfb7f39a54671ae`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:047d1b265d8a7d20ef8b3ccb9f133c3c5f1e4f9c92089889756590b7f20452b5`  
		Last Modified: Tue, 21 Oct 2025 00:26:24 GMT  
		Size: 53.1 MB (53109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05657968b04d89b7505c556f928a437efac01def053a76ab254d7cdcdf932a85`  
		Last Modified: Wed, 22 Oct 2025 21:58:42 GMT  
		Size: 132.9 MB (132853184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57b205467b39c747a2da8e1d00f9c307bd2c478f5e2f7c6a8745a6495ddbbd4`  
		Last Modified: Tue, 21 Oct 2025 15:36:30 GMT  
		Size: 18.6 MB (18636520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0887b3826bbcea453bcc0da3a5f512acdd8cc9ab7220e5407641574ad52bfbda`  
		Last Modified: Tue, 21 Oct 2025 15:36:28 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:255f7b2adb67c735e9cf66cc942f08fb355ebfb05566347bcf423fa29ad39dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15fff049e460d6bfc9110a182b8755eae51766116cc0da610a1a5ad800bf7e43`

```dockerfile
```

-	Layers:
	-	`sha256:798051b3a983e8fa2b1cbfd1b5855e930317631df0dc826856af8943be32baf5`  
		Last Modified: Tue, 21 Oct 2025 18:35:45 GMT  
		Size: 3.8 MB (3833908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55830ea6e4b11e50647a7ab860ad0c48eaaf968f1304a6baea8b1baed4055d90`  
		Last Modified: Tue, 21 Oct 2025 18:35:46 GMT  
		Size: 16.5 KB (16451 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:d4ce36076d040ed8536a180f2e51a3256f023f3bb352580cb7ed4d1a5398df6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198112453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb8e6b64e814d5bf12329d269744bdc8ac4b0377aa4bc274a8463b1ff0a4106`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 12:55:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 12:55:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 12:55:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:55:15 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 12:55:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 12:55:15 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 12:55:29 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 12:55:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 12:55:29 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 12:55:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 12:55:32 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc69aeb6f642e24b91c8abc7db1d688b36af067eb53670762bc030a8b22aca20`  
		Last Modified: Tue, 04 Nov 2025 12:56:17 GMT  
		Size: 125.6 MB (125622121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d905cd6a73a68b80335593dcdad25d4165699eb79bddc73164f6fd70dd06c7f4`  
		Last Modified: Tue, 04 Nov 2025 12:56:07 GMT  
		Size: 18.6 MB (18620242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a787bdcbed9ebb326f14af71abad03317a36e1061153d0127b5d85033e919856`  
		Last Modified: Tue, 04 Nov 2025 12:56:05 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8e1ae9b033cc773ffe1a6e1df113a80a83dc6f2a8399d29b31e49d90e5cb289e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3846320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21614fe2cf455b065b7fb3815df4178c3120c2c87c4a3cd34ce55ace9f64575f`

```dockerfile
```

-	Layers:
	-	`sha256:aaa6a72141cfa60a9b0891c274418e269ff8b4796ed154fc53e29d25b51d1e17`  
		Last Modified: Tue, 04 Nov 2025 13:34:48 GMT  
		Size: 3.8 MB (3829956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13449244038f2653bc59dc35c685055a856b0abfcbfb56a00b7c892ccd9397d9`  
		Last Modified: Tue, 04 Nov 2025 13:34:49 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json
