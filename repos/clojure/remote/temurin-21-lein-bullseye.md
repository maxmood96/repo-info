## `clojure:temurin-21-lein-bullseye`

```console
$ docker pull clojure@sha256:f20d31565d02d5e345860c95b7d9eca234402b6cfe1ccc30709c7a632778d5e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1558229955890ba161b46fef80bba16ef6f0a607df1a31ec921ca59598ae8c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232767589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aefe83e4ad908cd15c1880ea713ac061e8dd52b5ea787b450aa9aec30f9be15e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:15:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:15:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:15:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:15:38 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:15:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:15:38 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:15:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:15:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:15:52 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:15:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:15:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:15:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:15:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037add3cdf569c5bb1d5a3358cd99a53bd3f7a123b4a71c5201d20befffbd8c6`  
		Last Modified: Tue, 07 Apr 2026 03:16:15 GMT  
		Size: 157.9 MB (157857048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4580805ee5835cf58ad5c70dc0d9a0cca12e802ba577c5234e63cc48c614c1b6`  
		Last Modified: Tue, 07 Apr 2026 03:16:12 GMT  
		Size: 16.6 MB (16629571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3066362b25be9387178f9dd1cced6d3c73ceca7013c12594140b449ac446d4`  
		Last Modified: Tue, 07 Apr 2026 03:16:11 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3990c0264d8b8624639fef354e50098e583d7711a01ea4484eeb74b64fd934ab`  
		Last Modified: Tue, 07 Apr 2026 03:16:11 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c639241ff71e2908dd56247e77a34753b8294f791868c0584a84ca8712790710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae021a02ec834064f6e9b47453ca854efaf5c5e71a1c45071470c48b6b666c9`

```dockerfile
```

-	Layers:
	-	`sha256:91dea46892777db0ef278a6eeb5ea84d31c2e7cb2482f1ebefe9a43026975558`  
		Last Modified: Tue, 07 Apr 2026 03:16:11 GMT  
		Size: 4.5 MB (4487714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31222319e64b4d64d865aca2db4fff107dd31abd18c111e4df79ec94723d54ac`  
		Last Modified: Tue, 07 Apr 2026 03:16:11 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:04561e362ba8e513f99d45d55d6a8586317bc701211b65b86f10d6a942b49ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229515358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc5219c632d6bec36c4b72adc6b1de67dfc64eb105188cb8605f02739f24c94`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:26:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:26:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:26:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:26:35 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:26:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:26:36 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:26:51 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:26:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:26:51 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:26:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:26:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:26:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:26:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad129a3c72737bff1e40a94c2ecb98b306d5757bb14d06da0db1798d29f03de`  
		Last Modified: Tue, 07 Apr 2026 03:27:14 GMT  
		Size: 156.1 MB (156133049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d599abb498f6c15eaede2713b50487af3cf9e7d930f8c997aeaef0ebd3bc12`  
		Last Modified: Tue, 07 Apr 2026 03:27:12 GMT  
		Size: 16.6 MB (16616565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab6a8a5e34e39de84d83e00efa17852a6eaabb4d9b7e2e92da39f531e24e2d5`  
		Last Modified: Tue, 07 Apr 2026 03:27:11 GMT  
		Size: 4.5 MB (4517701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4134e4082fbe45ca1f8ff2ad771b6d1ed83a3d17a862655151cbf9785a3e2bd`  
		Last Modified: Tue, 07 Apr 2026 03:27:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a1a2508009ed8d6655d81b63a63ad459bfc637139e3fe7f30f66d6d65ef04831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4505177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133f4cd677f4f1943ed609a29232b332edaccf7f5bf36d061c440598d2410e7`

```dockerfile
```

-	Layers:
	-	`sha256:7e67721d6fa58b3e6c777fa2b0e0966009b132f648a00ef67af822761668d0a5`  
		Last Modified: Tue, 07 Apr 2026 03:27:11 GMT  
		Size: 4.5 MB (4486688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:935f86d3c2b02f1ed1d32eec8c369089fcb22107d1f982520f85aad7093c0336`  
		Last Modified: Tue, 07 Apr 2026 03:27:11 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json
