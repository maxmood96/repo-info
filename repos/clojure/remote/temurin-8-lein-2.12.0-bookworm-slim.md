## `clojure:temurin-8-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:068f90061e5786813b30a407a17d100ed595792492645a272dd0037e1ec04dfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7574ba4f26fa41564f1b0d4d68b4c744d3c76ac37c13dcc0c2c5a041e58154de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105238135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477e5ae0dfe02ae68a9b9d3da41a925eb407a267c8894fa1aa2ea73369758968`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:19:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:19:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:19:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:19:43 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:19:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:19:43 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:19:57 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:19:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:19:57 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:19:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:19:58 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ca1d1fc7388b9754feb325e1381fdcf97da057f3de65129712fe5c1ab44596`  
		Last Modified: Tue, 13 Jan 2026 03:20:23 GMT  
		Size: 54.7 MB (54733370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28aeb33438bef541fd0fa7ae92906c4fb22ed6a30ef7d5989c4c97bf6a261da3`  
		Last Modified: Tue, 13 Jan 2026 03:20:18 GMT  
		Size: 17.8 MB (17758435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b57f62761c1d6b063279d2ca77bf9709139990b49fb224d1301a8b38902d1ff`  
		Last Modified: Tue, 13 Jan 2026 03:20:17 GMT  
		Size: 4.5 MB (4517726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6fd672c3abb6fac67c0bbac94df950615de2ecb2083a9f779861793315c9be56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1429ec688d1cf9e22893529e0d50dc8f9d8c2b78ca296aca8fda7ff18e2287c`

```dockerfile
```

-	Layers:
	-	`sha256:6fc658081a48122b7c16dd157f90c373d917ddeb14d6b598750f76949c1ee886`  
		Last Modified: Tue, 13 Jan 2026 07:48:33 GMT  
		Size: 2.9 MB (2850408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85873c4e09df7fb9d1e3c07ad9580e3182747c46ffd73085e1f46f74c4ad3eb7`  
		Last Modified: Tue, 13 Jan 2026 07:48:34 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ad1e1438fca12edddc88743d4813acf18e6422fa218eff9a20e41e6f9a41871a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (104032675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a4a1eec6541758baea5ad3317577a2ccdfe1774bcfcdd4e3a3e4ddc09287e3`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:26:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:26:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:26:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:26:57 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:26:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:26:57 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:27:11 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:27:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:27:11 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:27:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:27:13 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0958bc686db803a0fa893a1f79d44fa9fd89cc0ad75edc8989057fdbbcf584a5`  
		Last Modified: Tue, 13 Jan 2026 03:27:40 GMT  
		Size: 53.8 MB (53814993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca983d910e42f277baf39fea48bf734120e66da082fd11bbfc4febff2984b2b`  
		Last Modified: Tue, 13 Jan 2026 03:27:36 GMT  
		Size: 17.6 MB (17592008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45f0c01f1567dbbe8cb3a704433c5717b4cba7a2339a10c4f1d61ee550beaa3`  
		Last Modified: Tue, 13 Jan 2026 03:27:34 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:80a27d9af46ca793233ee382bdb5dd753a2add5ac873724a2efb633f7ee3ebda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7b5cb8e621a7cd723f253cf34f33f32b0d6e8a398174cdb2fd7f0df940e6cf`

```dockerfile
```

-	Layers:
	-	`sha256:c7670baf1f1e5e6b45aea69fbbbc41214c754e915282e837cab0cdb0dabdd8e8`  
		Last Modified: Tue, 13 Jan 2026 07:48:38 GMT  
		Size: 2.9 MB (2850721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3875c4cb91251a252238fb358e5ec51edd7fa4192758866ab6e8086e6338c8a`  
		Last Modified: Tue, 13 Jan 2026 07:48:39 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1990ea49cca41e2765f4d723c9e71b173eddc830d6639ec327d92da5583bc22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106722343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325ce4d24dd6a96a8089e5dfc6d570f5f4779f8600588a9eaf0b7a27c350fb00`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 02:55:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 14 Jan 2026 02:55:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 14 Jan 2026 02:55:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 02:55:56 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 14 Jan 2026 02:55:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 14 Jan 2026 02:55:58 GMT
WORKDIR /tmp
# Wed, 14 Jan 2026 02:56:46 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 14 Jan 2026 02:56:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 14 Jan 2026 02:56:46 GMT
ENV LEIN_ROOT=1
# Wed, 14 Jan 2026 02:56:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 14 Jan 2026 02:56:52 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:24 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e347cbd2e91bcb301cef8b394f60db373b540ede97dc905d61207646be4178b`  
		Last Modified: Wed, 14 Jan 2026 02:57:40 GMT  
		Size: 52.2 MB (52175137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f993bedd87d9d7cec5214aee5dcdba9156b9b5068d96758375b55b82e0b92b3f`  
		Last Modified: Wed, 14 Jan 2026 02:57:31 GMT  
		Size: 18.0 MB (17960685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5965547035b54ba7972abb5b0f67b549de77a7966e27186614d7f493db58f4c`  
		Last Modified: Wed, 14 Jan 2026 02:57:30 GMT  
		Size: 4.5 MB (4517780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c4000ac11c1d2c629c4a21b83826729a1d711e026277e8ab39b584a15a989b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72921dc642bf6b7718c586f437b1dd4a904046f966fa433f156d7fc04105fbe3`

```dockerfile
```

-	Layers:
	-	`sha256:4e9f86062eb3ff72d9bdef86a63e280274888f341a288cd919ade1ad744ccd3c`  
		Last Modified: Wed, 14 Jan 2026 04:38:08 GMT  
		Size: 2.9 MB (2852834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:047427e6d2d5d2d66cc261ccf1f203cac9252091cbfa9a5db6c8b64c965b3e23`  
		Last Modified: Wed, 14 Jan 2026 04:38:09 GMT  
		Size: 16.4 KB (16444 bytes)  
		MIME: application/vnd.in-toto+json
