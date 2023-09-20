## `clojure:temurin-11-lein-2.10.0-bullseye`

```console
$ docker pull clojure@sha256:c774c0a3d88fb1f730be897ca7c54e951eb7e3d1129a28ac1f74a5091dd50778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.10.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:33a449ca941458247f8059676febd264982dc7c8b62973e05459a2309632acc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218143256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee90a0bba6970030adc42dc51eb3b11d9b588f2c7ded08857c3fdfa4ad2a24f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:51 GMT
ADD file:85db4f4c5016f51f7112a5d09cb7d4620f565a1379ae4b8a03c5ffc23886a876 in / 
# Wed, 20 Sep 2023 04:55:51 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:21:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Sep 2023 07:24:52 GMT
COPY dir:3e9b1d3d54369337872a2b8aa8c30068d69b28c2def3ec3bf07ba34bd69d48a0 in /opt/java/openjdk 
# Wed, 20 Sep 2023 07:24:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 07:26:06 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 20 Sep 2023 07:26:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 Sep 2023 07:26:06 GMT
WORKDIR /tmp
# Wed, 20 Sep 2023 07:26:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 20 Sep 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 Sep 2023 07:26:20 GMT
ENV LEIN_ROOT=1
# Wed, 20 Sep 2023 07:26:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 20 Sep 2023 07:26:23 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ddf874abf16cc990e0fd75a154a34ca0a03ee310ad895a18fb62ae15bf4171fb`  
		Last Modified: Wed, 20 Sep 2023 05:00:41 GMT  
		Size: 55.1 MB (55056714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d2593b379fff1802970ddf266f34d6bd5d13fda962a549ac1b0e11020096b1`  
		Last Modified: Wed, 20 Sep 2023 07:35:34 GMT  
		Size: 144.8 MB (144826046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8541c00432d76e113a7135ed6440c9de1fa6ccb19c823d8be8ff24ed221f3e`  
		Last Modified: Wed, 20 Sep 2023 07:36:07 GMT  
		Size: 13.9 MB (13861219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac6faddb4ef2de0aac260c354677cdcf6014a5381c14f07aa5a41e2d3c561bf`  
		Last Modified: Wed, 20 Sep 2023 07:36:06 GMT  
		Size: 4.4 MB (4399277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.10.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:16b01984e8eb64a18a7abf16a15eb86ac3266f76f8031502e031b5c47d316cd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213523814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e408826d72fb4ae61125c0348b71170b009ec200a9ff1be5c94f4452a9e05150`
-	Default Command: `["lein","repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:45 GMT
ADD file:6bc001e951ef1280f566a92e65fcff57aefb8a280aa3510b7cd4b4e0a54c5cff in / 
# Thu, 07 Sep 2023 00:39:46 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 09:03:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 09:06:37 GMT
COPY dir:68819d2d348aedadecb99120d7ca4a63dcc1e3aa0bb526ecbd9925396c38234c in /opt/java/openjdk 
# Thu, 07 Sep 2023 09:06:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:07:40 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 07 Sep 2023 09:07:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 07 Sep 2023 09:07:40 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 09:07:54 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 07 Sep 2023 09:07:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Sep 2023 09:07:54 GMT
ENV LEIN_ROOT=1
# Thu, 07 Sep 2023 09:07:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 07 Sep 2023 09:07:56 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:61c16b7975697b00760ff9536c09eed29b6a76923d4d98be38e9cdc749506417`  
		Last Modified: Thu, 07 Sep 2023 00:43:21 GMT  
		Size: 53.7 MB (53704716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0526516c15ab59c896bde61f8cbcc3d733f5b792e340106528fab44ad40477`  
		Last Modified: Thu, 07 Sep 2023 09:16:03 GMT  
		Size: 141.6 MB (141570385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79015fc993bd4ac11928839e72c354ee4827dea7b6f71df201f6326f00d1af2`  
		Last Modified: Thu, 07 Sep 2023 09:16:28 GMT  
		Size: 13.8 MB (13849448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790ec8d89720cb9e781ca858fb9f94a69cb22a630b2579c0800ee2c4e022e777`  
		Last Modified: Thu, 07 Sep 2023 09:16:28 GMT  
		Size: 4.4 MB (4399265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
