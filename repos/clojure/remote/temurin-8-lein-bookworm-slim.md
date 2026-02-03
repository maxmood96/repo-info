## `clojure:temurin-8-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:2a1170227a5d11707cd300ab362910af90be254b2ca88c46ebd07d82d3716b6e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c5470bd06d410cf4a8f673bf920537ae2981e6c2cbbb1ecf6777491f38382fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105238452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e6322a157845df8b60f79bf69a478f836628741a2d2b38558693aea77b0342`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:17:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:17:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:17:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:17:19 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:17:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:17:19 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:17:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:17:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:17:33 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:17:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:17:35 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e80e84ba0f7b19efaf7b73628c4862a1ac713f885b2d346e89460d0ff9e09b6`  
		Last Modified: Tue, 03 Feb 2026 03:17:50 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817ff3c00e7f136770c93a5e70e00f22c06c26a4b1836d67092f5fb244298ee3`  
		Last Modified: Tue, 03 Feb 2026 03:17:48 GMT  
		Size: 17.8 MB (17758816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8f827c0850f75622c9644dc088bb9124016c93604cc4524045ea43711c4d64`  
		Last Modified: Tue, 03 Feb 2026 03:17:48 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d6bbcda6dd7f51e66dfe7ca9e0ab437bedbb8a701e5029f5e70ed0ba5e1bcb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c43a119c416811555d33a417b7ed27b61bb3f095b7289f86b5ee3abd85ffc3`

```dockerfile
```

-	Layers:
	-	`sha256:419761afde337e1c59165efb01079d379710ec74637b00295043c1a82368d779`  
		Last Modified: Tue, 03 Feb 2026 03:17:47 GMT  
		Size: 2.9 MB (2850408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:291db09efecee29e7e92af31e9ecd4c3b19020287ab7d2d7d65e42d467d60e19`  
		Last Modified: Tue, 03 Feb 2026 03:17:47 GMT  
		Size: 16.4 KB (16399 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8e1754bda011554adf5f84175d60f843f97f1aa045b9a30d350676c306030450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (104032301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f4059fe5b91d2399cf12fc3039c6d43241d9a4cd6208caa389c81c9731fd23`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:20:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:58 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:20:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:20:58 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:26:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:26:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:26:31 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:26:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:26:32 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f588ba761977132d2ecf6506e1a07635b1a4ce296a2020cbae117c592719d3dd`  
		Last Modified: Tue, 03 Feb 2026 03:21:29 GMT  
		Size: 53.8 MB (53814976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1ddfe74616b3e97849b19abf4c473beca80998811ddaa7b2e5f173ef8cede4`  
		Last Modified: Tue, 03 Feb 2026 03:26:42 GMT  
		Size: 17.6 MB (17591772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0c15c1a3842f484da237e88f30d5cb575dde7f9183dc5ac45417436af34d42`  
		Last Modified: Tue, 03 Feb 2026 03:26:41 GMT  
		Size: 4.5 MB (4517698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ae16b813daeaaa1e8b9603b64d89e2102c193df80f22a3935e43c39fc0b92c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4028b8dbadce6c6e5a8045c8106ed74086d0652af98056e56902a17a26c6a8d0`

```dockerfile
```

-	Layers:
	-	`sha256:44bf8b32b7a4fa6c4a8d1723b282c559c0de38792ce8d0e7a4237dbd01ddac56`  
		Last Modified: Tue, 03 Feb 2026 03:26:41 GMT  
		Size: 2.9 MB (2850721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e83d6d140041c552fb038ba99b7815815f2e90dc4c5e22545c4a0754575b3b08`  
		Last Modified: Tue, 03 Feb 2026 03:26:41 GMT  
		Size: 15.7 KB (15721 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:701d7c395164f3fc1a71d001be162901e8d3d35347b1371dc9ca3fe29a62f8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106722610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0dc5402bee4fc329ce1b57d65860d28caad34f7ad4c5e3d03a041dfb94d257`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 09:28:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:28:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:28:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:28:56 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 09:28:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 09:28:56 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:29:28 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 09:29:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 09:29:28 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 09:29:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 09:29:33 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce017c8a49cb1ae866b2be346445f9e98394b0ee0a4cef0a2924bd7c8c7eb34`  
		Last Modified: Tue, 03 Feb 2026 09:30:02 GMT  
		Size: 52.2 MB (52175144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3858091832ba4c96e058ff4b4c9e035db55df0f4c67e994d5650ee1db872c284`  
		Last Modified: Tue, 03 Feb 2026 09:30:01 GMT  
		Size: 18.0 MB (17960995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc3104dad90252db20bd2cfd919d56683ab327f28afcda8fc4a980c7c3d0d52`  
		Last Modified: Tue, 03 Feb 2026 09:30:01 GMT  
		Size: 4.5 MB (4517727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e670cb852f4ae3ef43e531bfc22de6ad0a94c92b9c6fbacb5d9f4089e5129527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a549c878afd79e777e6f8f62efe3d4a8fd78d9ec0617754d343c7d9df8e3887f`

```dockerfile
```

-	Layers:
	-	`sha256:ca2edd83f97c80cd05de34180ed360a83304ab27e87e2c2475e2325ef2ab2849`  
		Last Modified: Tue, 03 Feb 2026 09:30:00 GMT  
		Size: 2.9 MB (2852834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33262529431d2b6de201c09ade86e47e4cca45229b0c20f9cd2d450dbb5b4722`  
		Last Modified: Tue, 03 Feb 2026 09:30:00 GMT  
		Size: 16.4 KB (16444 bytes)  
		MIME: application/vnd.in-toto+json
