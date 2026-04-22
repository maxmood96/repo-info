## `clojure:temurin-8-lein-bullseye`

```console
$ docker pull clojure@sha256:8744bdc86e5664cee8ee4f719c856dbdd1d81a4db5a13127b3ce36d9df2c3a84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3005d5f5165fb6d82b1c3b344d8f65fbd5346dbd70c663cea4de8d7dad687952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130080474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db9fe85ba92e41669dddf65f0954ebabfcb4f9dac7ba24d82b3497f92d936c1`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:15:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:15:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:15:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:15:06 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:15:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:15:06 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:15:22 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:15:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:15:22 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:15:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:15:23 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220416585f7568220ad0cc835cd34af63785acfa0a96af0fd7849731cec24116`  
		Last Modified: Wed, 22 Apr 2026 02:15:39 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72cdd6c2551fd276d7b3b93307ca92ee7ee2981c52a3abbfc6228d1ceb86433`  
		Last Modified: Wed, 22 Apr 2026 02:15:37 GMT  
		Size: 16.6 MB (16629513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6639ec549a3de5e24661e18c3de5ae82ceee1f572c536679a6ebc7e3d8423e`  
		Last Modified: Wed, 22 Apr 2026 02:15:37 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4d7677b316ca921bc7b68a6b982e47077dc9a74f8ba10da75f7cf082cc3e5a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4623221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54fe57b1c33fb0c9536ceae7e67368796c1c9bce953ec0b446dc97ed2c8eb07`

```dockerfile
```

-	Layers:
	-	`sha256:a0d31163def97ee7874fc2d71bada1bed13f3c9771a972238bac7c41b46a1f7e`  
		Last Modified: Wed, 22 Apr 2026 02:15:37 GMT  
		Size: 4.6 MB (4606851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6b047f47b45bcfe40d0a0ef9b2b6876beb6cd6b900065a96082162db775a5a8`  
		Last Modified: Wed, 22 Apr 2026 02:15:36 GMT  
		Size: 16.4 KB (16370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2df2c2536a1b65cca5e7923a5f7f224dcc5fadb6aafb5658e50b483f5c417822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127638867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0319c2378f7f068693715e10319b8a009a3ffb8d3fe6f5915fbcc941ed264f6b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:18:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:18:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:18:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:18:56 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:18:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:18:56 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:10 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:19:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:19:10 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:19:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:19:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc9e2daf87d570e7e17e66a484c9dcb113fa3b2faf09639a0d88a17f53177e8`  
		Last Modified: Wed, 22 Apr 2026 02:19:29 GMT  
		Size: 54.3 MB (54251612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b081df9db5e3646243bd4ddfa4b8e170ee44af42afc4912139e49e90e20f011`  
		Last Modified: Wed, 22 Apr 2026 02:19:28 GMT  
		Size: 16.6 MB (16616509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f9ed37726f5b467539aadd8ef013c752c51ad24a354c143ce303582e72b75a`  
		Last Modified: Wed, 22 Apr 2026 02:19:27 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a3572c3260ba0648d83cb88f99cfbc7071005de293ca13f96b9b4511226deff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4623016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b302b068339f5eed7b0e6bb3cdaecd89111f36dd89a8fd52e6ab7ca80624d955`

```dockerfile
```

-	Layers:
	-	`sha256:2c0545cfed01820c77de78cb9894dd29aa505d68d1e83e60fc786e9a99040884`  
		Last Modified: Wed, 22 Apr 2026 02:19:28 GMT  
		Size: 4.6 MB (4606525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e5c2198d46162244ad38e457090d4d9738ab962032ee2367dbc078ed55a8d5`  
		Last Modified: Wed, 22 Apr 2026 02:19:27 GMT  
		Size: 16.5 KB (16491 bytes)  
		MIME: application/vnd.in-toto+json
