## `clojure:temurin-26-lein`

```console
$ docker pull clojure@sha256:5c8035594c55e817d4acd3cc02e7499c624382bedb57886c2578a308bf3d14f9
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

### `clojure:temurin-26-lein` - linux; amd64

```console
$ docker pull clojure@sha256:417175b99726bb96f02ebed08581828f1ff819e716d27ba523aa38f7b2ca56f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.3 MB (167268963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e06d8977f2cb88e977ab8b6cfcd9beda28fabbf8d8394cd04b3ccd3d2c4bdc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:21:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:25 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:21:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:21:25 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:38 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:21:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:21:38 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:21:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:21:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:21:40 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:21:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a7f93b4d00762ffd34bbb0552e63e327a367b1b4654c8f6f2311e66cf1e2dc`  
		Last Modified: Wed, 22 Apr 2026 02:21:58 GMT  
		Size: 94.5 MB (94455691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3269c96b2d3f476e1160e52d91413576951f99afe6bfb2e729b8ccfe9dd6d6`  
		Last Modified: Wed, 22 Apr 2026 02:21:56 GMT  
		Size: 19.8 MB (19806478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e94083377043aa1253afa9e85c02459423f43cce270b737411cf1652d7f69d`  
		Last Modified: Wed, 22 Apr 2026 02:21:56 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524ffeafbfef5ce66aafb17a83b5f42f9042c3381ca340ed18a9ac7cc01879d9`  
		Last Modified: Wed, 22 Apr 2026 02:21:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:81064688dae50af6501f942153f26c7c11b30e1d4814ea718baca7afadf01bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fb1bb83ed9e40ff62b12833708547e7efe986b4d451df28227c107eb6a2777`

```dockerfile
```

-	Layers:
	-	`sha256:90fc22c39c7967d32f6dabc0a98fadf6c00d116489dc7b9af803ce80d9203b5e`  
		Last Modified: Wed, 22 Apr 2026 02:21:56 GMT  
		Size: 4.2 MB (4247885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:621b046c9a67e977f304536f5fa88912ff3a02ee7c61546ee7698edf43d2e888`  
		Last Modified: Wed, 22 Apr 2026 02:21:55 GMT  
		Size: 19.0 KB (19010 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5785d2c1731aeca2a7a8b1660be0dbd98fbce25cf2d869aa64028e8195cad145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165923373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed7f92f181d0dd8df6b02c888a0ae91014dd3d169035d6bb4b0d0c15caf2939`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:24:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:24:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:24:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:24:29 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:24:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:24:29 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:24:42 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:24:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:24:42 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:24:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:24:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:24:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:24:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7571dbf296500a5621b38b6962b45d1182063361707cf5507c81eb0d4d627a0a`  
		Last Modified: Wed, 22 Apr 2026 02:25:04 GMT  
		Size: 93.4 MB (93395200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d351462fdc3bd284598a53de32613b378f153f7c7572d6799c7fa9374f5dc5`  
		Last Modified: Wed, 22 Apr 2026 02:25:02 GMT  
		Size: 19.6 MB (19636960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9355e20eb4dff4a0a99931929f6f3819734aed633752cbde19c856d31c525557`  
		Last Modified: Wed, 22 Apr 2026 02:25:02 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fe006782eac835cec57bdeee01678236c89e429bc0d5d2ed96001cd90a0be4`  
		Last Modified: Wed, 22 Apr 2026 02:25:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:f38c602d63f6e34f7def2dacd81cb72a0cfd1d580de4c8fbec1fa8dc1b199440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9d5c22b3669b6a5fb5cbeaf8cac0cab5da2bd2c7618977139f31733fb54967`

```dockerfile
```

-	Layers:
	-	`sha256:c0621252e058deedea2a13a7456461b1d25f64cff2242b10532be5d239df5072`  
		Last Modified: Wed, 22 Apr 2026 02:25:01 GMT  
		Size: 4.2 MB (4247521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:840fc64c0a54e634b39d9cf67ee9dca93da7fe9ce15902e08b5cdff7283bdb5b`  
		Last Modified: Wed, 22 Apr 2026 02:25:01 GMT  
		Size: 19.2 KB (19156 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein` - linux; ppc64le

```console
$ docker pull clojure@sha256:ad075878a20814e06762a82cbf02035b1e33f127a61fa540fd618790f0d5b447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.7 MB (170667057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a1dfb784fb041146054add29bed7f109d2189b7d1f4fbf709ed53e643f3f48`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Fri, 10 Apr 2026 00:49:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Apr 2026 00:49:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 10 Apr 2026 00:49:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 00:49:05 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 10 Apr 2026 00:49:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 10 Apr 2026 00:49:05 GMT
WORKDIR /tmp
# Fri, 10 Apr 2026 00:49:32 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 10 Apr 2026 00:49:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 10 Apr 2026 00:49:32 GMT
ENV LEIN_ROOT=1
# Fri, 10 Apr 2026 00:49:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 10 Apr 2026 00:49:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 10 Apr 2026 00:49:36 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 10 Apr 2026 00:49:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5bb937b64e28b9440675ccbc228210a99b8d8484e299953df825953180b5f5`  
		Last Modified: Fri, 10 Apr 2026 00:50:20 GMT  
		Size: 93.8 MB (93781433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213dbae337a5455dbabf0e4151c608eab4dc2d1b81e9706f56314a65150c6b1d`  
		Last Modified: Fri, 10 Apr 2026 00:50:19 GMT  
		Size: 20.0 MB (20030503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c4198fff1b6a249f71f7f9d6ecea50f6deb671380a8ca8c1c5215373bbf9b5`  
		Last Modified: Fri, 10 Apr 2026 00:50:18 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f206a180a19dc4d851f0188da0462b6f41c0aa4db076257034717d005bdb42d3`  
		Last Modified: Fri, 10 Apr 2026 00:50:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:abf40be3ddd0670adfc69acc217f25ae61618f06137f075095992bc80c80279f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50eea03f972e7c100533e04289a4df680870355f12d1b59e9603fa522e554a69`

```dockerfile
```

-	Layers:
	-	`sha256:1d99c3561a52f78272e14d4f40d5e7ca4b1e0e84ba09155c09235b7dbf20a305`  
		Last Modified: Thu, 16 Apr 2026 03:15:24 GMT  
		Size: 4.2 MB (4233694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43ea9cad4756ef84090191466e2f826c88307d6dd114a2836e14ef169195c719`  
		Last Modified: Thu, 16 Apr 2026 03:15:23 GMT  
		Size: 19.1 KB (19067 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein` - linux; s390x

```console
$ docker pull clojure@sha256:e189fc5c2206dcc373df266cf3bd620c5414e9de5e9ca3d46bb110d88ba4ae0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161680653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d8d2b526bb756a43434aef7b81a8e2e8bef906abb369835b257df3cabd7fe6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 04:06:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:06:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:06:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:06:50 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 04:06:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 04:06:51 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:07:02 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 04:07:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 04:07:02 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 04:07:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 04:07:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:07:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:07:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76be733848ad2e2341b4747388067f625f269684e93fbce48b752d101175e95b`  
		Last Modified: Wed, 22 Apr 2026 04:07:30 GMT  
		Size: 90.5 MB (90547745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5a390abf637304f071d7322eac7a7917481cb82a71a9c1e4348e603e22acdb`  
		Last Modified: Wed, 22 Apr 2026 04:07:29 GMT  
		Size: 19.5 MB (19466766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8269b2fa4a1c848d7d43f20db2b903c7075848c48bf19cbb630639bb2791f874`  
		Last Modified: Wed, 22 Apr 2026 04:07:28 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af41df4c2b9cd2afa2c6947eea990ba74e0853a021f64f50c74d2f1fb288602`  
		Last Modified: Wed, 22 Apr 2026 04:07:28 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:6e521722f108db7727900fe6faa8a7fdf3abc9538b9757d9563166b8577e59b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4243895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322c3e31ad3062300b703afeecac975bd12f6073ceb3b842923837cae056f04a`

```dockerfile
```

-	Layers:
	-	`sha256:c916d441c18e12cb973e7944f2dc77be8394a77888d96c4a2b859cd616cac8a5`  
		Last Modified: Wed, 22 Apr 2026 04:07:28 GMT  
		Size: 4.2 MB (4224885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72a11838e3e099a67b5adfecf81026b223857dcda7bd76e647ee785fa5430607`  
		Last Modified: Wed, 22 Apr 2026 04:07:28 GMT  
		Size: 19.0 KB (19010 bytes)  
		MIME: application/vnd.in-toto+json
