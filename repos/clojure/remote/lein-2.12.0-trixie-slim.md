## `clojure:lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:a200ca245f19922f88645a7184a9e40a034fcf6c67b1731aea66da07fd390c1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3fc8787de83c0ac85208092d0a4b32e9436f5be0b088e789b751508f2abd9c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208543830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd37d38dc3d0467bf467fe96e492e2d576793f6b74cb9ac14969e94a10a37eb9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570de40485d2cf767e369327b9948c0459dc7812d9ef1ae4b00def51be0e0752`  
		Last Modified: Sat, 13 Sep 2025 00:04:12 GMT  
		Size: 157.8 MB (157804796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0fa7121f8adcb71c892bbf06ba442e990f0ccaa69e21ee3d0c2171fb882a49`  
		Last Modified: Sat, 13 Sep 2025 00:11:33 GMT  
		Size: 16.4 MB (16447353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796b0ddc1bf7db139b0890757fead70979436f489080f3fbe2b1e991676539ef`  
		Last Modified: Sat, 13 Sep 2025 00:11:33 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846c50870c362d5ba3d9e71f6d6eaec0da37a9575f96148985401a3e080e7704`  
		Last Modified: Sat, 13 Sep 2025 00:11:32 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:45713dbea2bf3763f4231fa79f94aeadd906109429aa0fbb2b7a0f17ff92d8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5163f20034617c90a0fd599822a26ab15ca689acaba05b63a956d79ed2f02e34`

```dockerfile
```

-	Layers:
	-	`sha256:ba8407293e1b9c86dd5a345977b001b3cf7d6cf9ada307905372e83d759cdffd`  
		Last Modified: Sat, 13 Sep 2025 00:35:22 GMT  
		Size: 2.4 MB (2367144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ecc7cb74ec128908157e672a49ab715fc98bf173a2b7d1d6a1cb15630f3c383`  
		Last Modified: Sat, 13 Sep 2025 00:35:23 GMT  
		Size: 19.1 KB (19084 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:644c8e835b8a6a6a9ba5cfc13fdc3d5cadc2ee0058f5b675e1e1593811564013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244821940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540df847aed23bf0145a2e09fb3f2b7f9f20997d498ac52f5ae76b960fbb1169`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 17:48:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 17:48:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 17:48:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 17:48:33 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 17:48:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 17:48:33 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 17:48:33 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 17:48:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 17:48:33 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 17:48:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 17:48:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 17:48:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 17:48:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489f94fd88b06de71876d5dab65108a07ceb681f80db09fdbcd7d7f2cbe223a7`  
		Last Modified: Fri, 12 Sep 2025 23:44:06 GMT  
		Size: 156.1 MB (156081181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ab70750fab61724d93b659f9d82e577e2412e0ea1849877411eb8c46682d9a`  
		Last Modified: Fri, 12 Sep 2025 23:44:40 GMT  
		Size: 54.1 MB (54089558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ca98ed1d08d1a1b7ca790d85f209326bcfe7df47e5cff408238fb8aacf8b72`  
		Last Modified: Fri, 12 Sep 2025 23:44:29 GMT  
		Size: 4.5 MB (4514143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ccb49fb4b3baf5ef06a6c6a9887e85621d52b27a2c8bf36a4c3f2a335ef8f1`  
		Last Modified: Fri, 12 Sep 2025 23:44:28 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:91315bb1a5e29518091f640d1ed50cdca2eeb216650b5c49da886316225184a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5057bb3e9a6f758523dac551873038dab46e3f080f24c9c029766bc503abdd1f`

```dockerfile
```

-	Layers:
	-	`sha256:23ba53726a72c93463954a79fc761a377e5c580f7ba717e9c8b8643bfd9a4d9f`  
		Last Modified: Sat, 13 Sep 2025 00:35:27 GMT  
		Size: 4.3 MB (4287262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921f420477a18d053f7662b8ec1b7f7bf9251a1d6ddecabe10779dd09691f77b`  
		Last Modified: Sat, 13 Sep 2025 00:35:28 GMT  
		Size: 19.2 KB (19237 bytes)  
		MIME: application/vnd.in-toto+json
