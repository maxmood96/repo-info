## `clojure:temurin-11-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:0350a30dd4194c23b7d984a6ae57717d23fdcd1e965c2168f72b42184d859fc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:96a4449ab16a66d42a6d06f79dfd6f89757ec9753403d0ba5041990dda2ae923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196000807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4815172d6b693c3424711afbc849570ea5fb3e0ee216108037e3d3376d2b419c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 29 Apr 2026 23:13:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:13:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:13:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:13:40 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:13:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:14:32 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:46 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:14:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:14:46 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:14:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:14:47 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d451d88a5bc900d6c49b43ba1006ed561404bac2485abe612d41fd3803197fd`  
		Last Modified: Wed, 29 Apr 2026 23:14:25 GMT  
		Size: 145.9 MB (145886335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f266eb2d2962d179697628efda1be6d3e61ca5b63d13c90ef52630c8917d14`  
		Last Modified: Wed, 29 Apr 2026 23:14:56 GMT  
		Size: 15.3 MB (15338791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fe03fa50efb770374fc62280a1e8736062f4198df018386842638277617e58`  
		Last Modified: Wed, 29 Apr 2026 23:14:56 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7ec76919292f278db07b37d3e04c503c593f4d62ca2689d966cbfc47812057ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97da1620f080c9704fdb69476eae62023840b9ec1826b9f781cb26edaca8bb39`

```dockerfile
```

-	Layers:
	-	`sha256:2fad13e505f6cfb18219aefc13273382889250016a4dfed1b66928918cc73032`  
		Last Modified: Wed, 29 Apr 2026 23:14:56 GMT  
		Size: 3.0 MB (3047725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fd776a29401b1a61a507ff088bee9117bc4911966a58041329d8bf43799604c`  
		Last Modified: Wed, 29 Apr 2026 23:14:55 GMT  
		Size: 16.4 KB (16410 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9d87e5a53159e01519a9af45439bef874c7b6108763b4f59d73a5c07ad3ee8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191171482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313466272421b056e4d17e8f1530eb453ffa8b25c9ba5d169b659ae09e02870d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 29 Apr 2026 23:14:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:14:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:14:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:14:23 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:14:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:14:23 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:36 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:14:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:14:36 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:14:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:14:38 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cb1115507df2baba0f0764a8574bf2d105a1335cf26a9f020f3108053241cf`  
		Last Modified: Wed, 29 Apr 2026 23:14:58 GMT  
		Size: 142.6 MB (142583978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ef2e4008fa2dafde597709a9f11aee1d82512fd9aab2839dbe7f93bb473bc0`  
		Last Modified: Wed, 29 Apr 2026 23:14:55 GMT  
		Size: 15.3 MB (15327213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077cf4644880f2dc39d02abb19ab869a5a658b2faf0892a5de4a2170dc342bbe`  
		Last Modified: Wed, 29 Apr 2026 23:14:55 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:44b38437f71353998bf1a7dbc7d84cc8586d22ad3b548afe7c746bb5d64c3322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a67ce69c769b26db0ed5127d72b4c77a953a5f47f36a2e0e8061562c51e4cc`

```dockerfile
```

-	Layers:
	-	`sha256:28bdd896cbbec38803cf348c0121a5c63391617c3e735bd8712847c04066072a`  
		Last Modified: Wed, 29 Apr 2026 23:14:54 GMT  
		Size: 3.0 MB (3047952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75abacac5c143a0e0b5068a1f0ac2766caaada0c572daf8c7ebc0959185acf3`  
		Last Modified: Wed, 29 Apr 2026 23:14:54 GMT  
		Size: 16.5 KB (16533 bytes)  
		MIME: application/vnd.in-toto+json
