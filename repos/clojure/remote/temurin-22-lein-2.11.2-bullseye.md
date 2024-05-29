## `clojure:temurin-22-lein-2.11.2-bullseye`

```console
$ docker pull clojure@sha256:ce5b86f87af991e8c29a55c29d989cb6f292f2524ddce6e9965cc671e39a2b29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:temurin-22-lein-2.11.2-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8887537bd984e25aff2aa05e1aae6bdf32148ef10afa6868fba7705510ac8473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232361166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecd52c47182a197f49f4a7507f5b3f763344d669b411724e92981fa5dbdd90f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 15:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a3def59c4f8d3f1625eab8567e011fda2691f6a553d8e2bc3527fa097d80aa`  
		Last Modified: Wed, 29 May 2024 19:58:18 GMT  
		Size: 156.7 MB (156715496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ab22eb6d0298ee1ae3efe0c750e2ea2a0afb5bdee1fc45295ff092ae3c6a5d`  
		Last Modified: Wed, 29 May 2024 19:58:15 GMT  
		Size: 16.1 MB (16147747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09738c845852f2c3ba027ecaa394cf691962478994464892f8aa93a795e7371e`  
		Last Modified: Wed, 29 May 2024 19:58:16 GMT  
		Size: 4.4 MB (4398092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3b7acec77671ce4ed851c7d6dfc859b11c5a3248dcac7ac8f955462a473315`  
		Last Modified: Wed, 29 May 2024 19:58:15 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:75a30083a599a4762c2ba287e225877156ed81f2f1da001f94fff7dd9c1bab94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55813705fcce06c4222270eee10f21f2828b99945149052e9f303ba003b823a5`

```dockerfile
```

-	Layers:
	-	`sha256:e1c20587671e62c01614f62b797d785773379eb08224cdf014acf0532a7ed699`  
		Last Modified: Wed, 29 May 2024 19:58:15 GMT  
		Size: 4.2 MB (4151304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8feaa859912d7927589e9fc7712a4364928e18dfc38a987eac708bad87c0990`  
		Last Modified: Wed, 29 May 2024 19:58:15 GMT  
		Size: 18.0 KB (17980 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-lein-2.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2e37f1776bdcf77abc74d4bf9c3d5eb337037924a21ab7a303a4392179c0f784
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229219195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec08809299734255dcec2acc77f75f63cb057d912068266b9a31a754323339fa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:47 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 14 May 2024 00:39:48 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:44:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 20:02:43 GMT
COPY dir:8db4aa7d00469f3c784932412aa95caf68b05146a02559362a91df21ce463ad4 in /opt/java/openjdk 
# Tue, 28 May 2024 20:02:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 20:02:47 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 20:02:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 20:02:48 GMT
WORKDIR /tmp
# Tue, 28 May 2024 20:03:01 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 28 May 2024 20:03:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 20:03:01 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 20:03:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 28 May 2024 20:03:04 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 20:03:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 20:03:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84a1f76b155da5c15c43207f175b35e0a21820d0d8c424cae5b958fe3956aa4`  
		Last Modified: Tue, 28 May 2024 20:22:14 GMT  
		Size: 154.7 MB (154737692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d46bf9904bf94ee5768a39c23b508bf3a5f29045d325983d74009dad5ee543c`  
		Last Modified: Tue, 28 May 2024 20:22:05 GMT  
		Size: 16.3 MB (16344007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5952a80001255918c097335cde5c9818a498b727ad5336ac8fcad323b23dcae`  
		Last Modified: Tue, 28 May 2024 20:22:04 GMT  
		Size: 4.4 MB (4398108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97e9f8d5b0a2656f1fe13c99c5764e0192746940b85e1fb38c530e4e9de19fc`  
		Last Modified: Tue, 28 May 2024 20:22:04 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
