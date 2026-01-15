## `clojure:temurin-21-lein-bullseye`

```console
$ docker pull clojure@sha256:ff55a100e90f27408cfabb579adce3c6a74dbd8c4cb45dadc5bd963f00eac2ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:04c748df1def227341a8d08bb3f5b9179386d2c30624ddd4b74f9c7bc51cebaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232708165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16bd683e36cc9ae141b60208021f59c92aa9746faac6d751b3d7b50fda9379f9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:34:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:34:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:34:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:34:08 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:34:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:34:08 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:34:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:34:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:34:23 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:34:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:34:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:34:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:34:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:36 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dee15a4bf2b4b0170c42dc596918941f44c30216cf03e8847d469cc586c61d`  
		Last Modified: Thu, 15 Jan 2026 04:19:33 GMT  
		Size: 157.8 MB (157825976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cd7755a5ee5c0d0b27c96d1e23e539cf5bcf5359be9d7fe7c24314eb107750`  
		Last Modified: Tue, 13 Jan 2026 03:34:53 GMT  
		Size: 16.6 MB (16607561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6206af380cebb96a67e7101d298bab99c4f2de0399f225ab2dd8f41a2c635ec9`  
		Last Modified: Tue, 13 Jan 2026 03:34:57 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2119565ceec99c07c8c537b6201f7e229328d9e803d4770fba858df0b08ee2`  
		Last Modified: Tue, 13 Jan 2026 03:34:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:10b70d0b0152ff0f7fddf6c7c2d71343acb1fcd379929883cb1c707931857449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95915fe2c30ba3bfa3acc523cdb97ef335a3986f6a90c686426a423e32e85781`

```dockerfile
```

-	Layers:
	-	`sha256:57c41aeeba096f2281d83f6df974da2ba9704df0e9054d7cc6941b614dfdee84`  
		Last Modified: Tue, 13 Jan 2026 07:43:17 GMT  
		Size: 4.5 MB (4479292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae5ea8c6b741aed96839727c8285550f21189e7573d1708dcf7dba5395f5f401`  
		Last Modified: Tue, 13 Jan 2026 07:43:17 GMT  
		Size: 18.4 KB (18367 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:32a8bbdfd85a2d184c826bffc0b0c943f20ee12cfe06eea4f47fbc9d26fff0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229478658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66827eca3267d1bf7ed61ff91f7e4af76b21f1bfaea54ac771aa14d17a9a490`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:37:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:37:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:37:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:37:48 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:37:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:37:48 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:38:02 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:38:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:38:02 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:38:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:38:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:38:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:38:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:52 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da16d75d94140c74c674d1b57a85bbbd44ffb10e0c0805919323048e9af925b`  
		Last Modified: Thu, 15 Jan 2026 13:21:13 GMT  
		Size: 156.1 MB (156107672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7f2857f7936e42244b891c739365f434a4ce3beb62e10dff1d5fa2cc7e55be`  
		Last Modified: Tue, 13 Jan 2026 03:38:37 GMT  
		Size: 16.6 MB (16595037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff87b6c0da63ee35b24c8684e7c8f5e41477f5bb1599faed882b86cee80fa96`  
		Last Modified: Tue, 13 Jan 2026 03:38:36 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207a690015864791af7e6bff8e6d9210778b9fa827af0f8c508dec4ddebc81d6`  
		Last Modified: Tue, 13 Jan 2026 03:38:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bdf605a4106f8e241a32be516c166b405a86aface21664ebc8f95d372eae12db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4496754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02fc7285ca71c4b1eaf6bc770fed1cec05b1b52edc7a9079f785021a69a524f`

```dockerfile
```

-	Layers:
	-	`sha256:ed74a33a02d558040b8937df99cdd4d981098a1f3337a5b678b490c417fd86a5`  
		Last Modified: Tue, 13 Jan 2026 07:43:24 GMT  
		Size: 4.5 MB (4478266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84fbe186a57df774d9014a449a8692e8f82c47e5a69f1f370e31de4c71eb5f74`  
		Last Modified: Tue, 13 Jan 2026 07:43:34 GMT  
		Size: 18.5 KB (18488 bytes)  
		MIME: application/vnd.in-toto+json
