## `clojure:temurin-11-lein-trixie-slim`

```console
$ docker pull clojure@sha256:d6a676dd71e2c763ec5966f9d9e4ca26ea9081b9e6474f55d91f98a1a58bdbb5
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

### `clojure:temurin-11-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ddd6f469285e19edbd070dacef7303f70ff9f5b27e7bfb47bf3b884158827814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196548399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1645b3b1ae343512d6130c225fe1e585f5a655a855bf821a21f61233cbed71b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:13:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:13:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:13:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:13:48 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:13:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:13:49 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:14:05 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:14:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:14:05 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:14:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:14:06 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a2deb3ce74d8380367b610740fb18d397c2dd4b6d040e9b7cadc0e980eca10`  
		Last Modified: Tue, 07 Apr 2026 03:14:25 GMT  
		Size: 145.8 MB (145806914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60990bd747b9fed440932833f72b2d356ec48f417e4d6c6cacf1309a0bb32c02`  
		Last Modified: Tue, 07 Apr 2026 03:14:22 GMT  
		Size: 16.4 MB (16448050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9693c23e6d149fcc2de2a0b3a2a57cdd940c4ffa109787e08b14c63b3ab1ca70`  
		Last Modified: Tue, 07 Apr 2026 03:14:21 GMT  
		Size: 4.5 MB (4517763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:62394436313f26528128ca5ae2b4926573e6b32748c8dc72de65e7cdde145bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f541fa2da9725d04446b6cd37f8c129a1051ab8a761dddd5c5ee42a87485fc0`

```dockerfile
```

-	Layers:
	-	`sha256:aff55be1ddeac7960187505d301c798a92247b107c540fba88c2a80266fb5eb2`  
		Last Modified: Tue, 07 Apr 2026 03:14:21 GMT  
		Size: 2.4 MB (2384929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99e41d8b4cc0b4e0078e0b0d4b13b1a78642f895d287cd567fc9281d2c595562`  
		Last Modified: Tue, 07 Apr 2026 03:14:21 GMT  
		Size: 16.4 KB (16393 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c9486f1f68f14c0786d550159cad438ebb3cfefaff32608624bce3a59d8bee24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193570504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1e70935930c769acc70ef7a66e498f0530e9c2afe98ba9558ffe1d20bd8409`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:24:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:24:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:24:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:24:12 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:24:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:24:12 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:24:28 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:24:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:24:28 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:24:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:24:30 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bec000b8c51d641ad70625e6709b178a1f342640b122744f30dc2de641fda`  
		Last Modified: Tue, 07 Apr 2026 03:24:49 GMT  
		Size: 142.5 MB (142500070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12f569e0dc75b1d6cb40b1b0299c1a64b8931b6554d293ddb37f483b25db01c`  
		Last Modified: Tue, 07 Apr 2026 03:24:46 GMT  
		Size: 16.4 MB (16414082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dd541e758cb4eff7ad5540810e6046fbbfb1e228eb2da7746188f2430320ce`  
		Last Modified: Tue, 07 Apr 2026 03:24:46 GMT  
		Size: 4.5 MB (4517769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:01143515c3de961e3542679ff2a9f650d9f31326fac66241e917b821dd6cb258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cfd79597f2b5d3e3359695c9cb8fad2e5a779023c012a80bbda441c6c3eafb6`

```dockerfile
```

-	Layers:
	-	`sha256:b8064e33d515d4e02377df8bdb2845ecfb6c4de47da58f62c5c6326ce4a46319`  
		Last Modified: Tue, 07 Apr 2026 03:24:46 GMT  
		Size: 2.4 MB (2385165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17f68daf2a04990e2554bdce2c47642be03aa6789505d80b243f966b0621dfd3`  
		Last Modified: Tue, 07 Apr 2026 03:24:46 GMT  
		Size: 16.5 KB (16515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:158f2ec50b2d9738a97ef275424d98bd5ba435ee1e068abf639fafa3d431cc08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187592669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28cf8be22c792320a36d496ffa86db3479fe75b25ee1da3d3ef5a1d1e8726ff2`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:18:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:18:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:18:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:18:16 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 18:18:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 18:18:17 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:18:58 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:18:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:18:58 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:19:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:19:02 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6d8bc187d9d77c2b576c45cef2edbe313dca76b0d35a49ca751f0587487fda`  
		Last Modified: Tue, 17 Mar 2026 18:19:41 GMT  
		Size: 133.0 MB (132996714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a8b7d6b8e91457324a8f05f9a8ccaaf540006612f0d3b9765432e086c9d98d`  
		Last Modified: Tue, 17 Mar 2026 18:19:39 GMT  
		Size: 16.5 MB (16485374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd33dda0e24b165064dd68dc40f0381dec8c601c0df3edc4429da453ded8b476`  
		Last Modified: Tue, 17 Mar 2026 18:19:38 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:59d2089f3c4dabc6dc40ae02d81348cfd747a66ebaf8246cebc9d801b06f06c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e67277d85e1e91f3412226af57b396e3a43eb8951b16d22104f117baf3f41c`

```dockerfile
```

-	Layers:
	-	`sha256:957014fb3ba556adf698cddb32c1418158e3d746573632c720398da63a2e0c07`  
		Last Modified: Tue, 17 Mar 2026 18:19:38 GMT  
		Size: 2.4 MB (2385294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b350cc736a1a6ad39fdbb748df704b52a8f6266215c233059be2d3581cfddc09`  
		Last Modified: Tue, 17 Mar 2026 18:19:38 GMT  
		Size: 16.4 KB (16438 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:fbb2f81f4ee74b7862a8fd85999dcafa31b258405fd1f29c7cd5c475e4903fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177399314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4715fd0a290a54a91ae95a6798e15d36d0b671fffdc22bf5c6e6b3457261820a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:40:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:40:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:40:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:40:00 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:40:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:40:00 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:40:13 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:40:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:40:13 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:40:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:40:14 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9166190ba17c367d077fe9e36dd0402927522edea9133f6d301c45a7bf95699c`  
		Last Modified: Tue, 07 Apr 2026 05:40:38 GMT  
		Size: 126.6 MB (126562240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391f5f728abf61c633253d361d581703c6946640df8ae98847804d84e57d6b36`  
		Last Modified: Tue, 07 Apr 2026 05:40:36 GMT  
		Size: 16.5 MB (16483903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3ead82e98c0cbae289018cb5f96b2b5345a1047c416d3c4ce9b3593a87fc42`  
		Last Modified: Tue, 07 Apr 2026 05:40:36 GMT  
		Size: 4.5 MB (4517721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1037e0c7a25e5080fb654d6a308dbf7888f997d3d959af09cea18f7d93ec6b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e84a0793f7151fb411a23822fb88000113c504cb6644b45d8ec5c6fac1eeb2`

```dockerfile
```

-	Layers:
	-	`sha256:b974e1615472311bafeb49314b4b8f17df7811dce68357c13facb847f23738ca`  
		Last Modified: Tue, 07 Apr 2026 05:40:36 GMT  
		Size: 2.4 MB (2381360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3fa278e6b0d65f0f749d1beb7845ad95597f8537555bcba04abcc6fb5e32dcf`  
		Last Modified: Tue, 07 Apr 2026 05:40:35 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json
