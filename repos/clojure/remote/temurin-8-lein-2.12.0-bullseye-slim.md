## `clojure:temurin-8-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:0f954696c52057652e1bd7c0e2b15826cde652948e795bf6b809e36d0b7cd93b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:67e27278b188587e0e2934b296138e211f074ed98c07b79e766d3d3d42b4b264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105284528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6570b6c7dbedeaf21aef3c67daa83859dd847eb67bf4d9121736695debd1d7db`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:15:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:15:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:15:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:15:29 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:15:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:15:29 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:15:43 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:15:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:15:43 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:15:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:15:44 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5678eb6522d78cb257e20d04f4c7a263f14ebd5d070b5893c631a1037475901`  
		Last Modified: Wed, 22 Apr 2026 02:15:56 GMT  
		Size: 55.2 MB (55170083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda9b15f8844ea43b574ef00d763355728d8ff6fac97021c3dfe59154d902d0b`  
		Last Modified: Wed, 22 Apr 2026 02:15:55 GMT  
		Size: 15.3 MB (15338755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7d48388f0e2503983dac818e6169b21ee48298ca14bd2d053fe57cde6887e3`  
		Last Modified: Wed, 22 Apr 2026 02:15:55 GMT  
		Size: 4.5 MB (4517724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bfc9e628903f2936986445928ac52cdcf837128f21169f2324fef143dfc3f269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3164969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd9cb863034c4e1bee11ab6f5d717a20c156f4772dde7dd67d9fe555c3ba1d6`

```dockerfile
```

-	Layers:
	-	`sha256:ad7a54ac6091515d7690d735a1c066fffd3ce14640071f031ca6ff5287b8922a`  
		Last Modified: Wed, 22 Apr 2026 02:15:55 GMT  
		Size: 3.1 MB (3148571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81b8703b67acc57231b374978a890032cd336303361a3cc6b6f48c94dabe1391`  
		Last Modified: Wed, 22 Apr 2026 02:15:55 GMT  
		Size: 16.4 KB (16398 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b1e2aba5cf1ef302dee8e334ec5625cda54c3793af63436a3b69f90f8721cb9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102839050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e996b0e05e6d9e843f57d811ca5588fe8ed50e85c5e18b4aa6dbc40b8ea994`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:19:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:02 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:19:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:19:02 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:16 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:19:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:19:16 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:19:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:19:17 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e987a1751168f0d5cf46e7c6ee11ad761c27c87ec025093d6aa6de5b9a5c67`  
		Last Modified: Wed, 22 Apr 2026 02:19:32 GMT  
		Size: 54.3 MB (54251622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cff6a304fc3a6f5902006d028b1b72528b3d8531e1eefc6a9fb374b46a2b52`  
		Last Modified: Wed, 22 Apr 2026 02:19:30 GMT  
		Size: 15.3 MB (15327174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03aaeaa0ad6b302804a3d93610fa8114560e51250da4deec5cabdeca3e2e39e`  
		Last Modified: Wed, 22 Apr 2026 02:19:30 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:449693157560bc33aec74f0ea8b3fd52fdd804ef30a79435ec0ec45471604c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3165401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0dee52d888e71387e3feddc093191c08b324eb3f5bebea89509fdfcb350848`

```dockerfile
```

-	Layers:
	-	`sha256:b858b00ddcc1d507a632d2bf191c055f0ec797d587b1d9605a1e7ed233bb61d9`  
		Last Modified: Wed, 22 Apr 2026 02:19:30 GMT  
		Size: 3.1 MB (3148880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ccf971a489856fbb3242bc3257dfc50ec584934c422e33533b273c4ddadcdab`  
		Last Modified: Wed, 22 Apr 2026 02:19:30 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json
