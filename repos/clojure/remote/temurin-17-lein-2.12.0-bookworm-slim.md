## `clojure:temurin-17-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:983258fce01d9d7b7441b70bf23fc7cf5e80944eec5a00a3be0f70215e1a0a29
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

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6295a0aee42a0ca92807f6eff3c3b3c3b26d9cc50584f0f9e54b8c9a82aebde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.4 MB (195353128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8134b49848042998348990762e28b48a9afa3180523f79c2be8ece7152339650`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:29:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:29:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:29:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:29:51 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:29:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:29:51 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:30:04 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:30:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:30:04 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:30:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:30:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:30:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:30:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c3758da1c260a4d02960c13e152ba8ef3450b1ea5e58746c75baf08fdfd023`  
		Last Modified: Tue, 13 Jan 2026 03:30:58 GMT  
		Size: 144.8 MB (144847951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae76d6513b2e425d23256752f901965487f8b959fb7750c78ae7eff8bf3a8b9`  
		Last Modified: Tue, 13 Jan 2026 03:30:33 GMT  
		Size: 17.8 MB (17758424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143a008d348534803830a3f5c93794ace3bb22ebb487615756babb4064362ab2`  
		Last Modified: Tue, 13 Jan 2026 03:30:31 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da0dbaa661f30f359a9547216d1dfbb25653bcaeef5e222ca20b188844717ee`  
		Last Modified: Tue, 13 Jan 2026 03:30:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:283273293feb0d6ff0f03ad0cb93a9ea77f28a538dea2b18472444422b51bafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2747201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf235ec118747e152899f64874f95611366a485020fbcd981fb4b18266dceb9`

```dockerfile
```

-	Layers:
	-	`sha256:531a6c9aef83a60f248ad823e0b10c6db0d6edb78c031e39491a9e3154543cb7`  
		Last Modified: Tue, 13 Jan 2026 07:40:08 GMT  
		Size: 2.7 MB (2728798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9952272e1cffaf09d7dd53b1afbd61d4fd87142c7e469178ace13ec929b34cc`  
		Last Modified: Tue, 13 Jan 2026 07:40:09 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8a9f51b55b287ace1ba2cad0036821c28719f5d2c270736fdc3f2c887b35751b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193898069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399ea93755b33cd288308175158fde56100c4af220c2ab6c8c7772f7702662e1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:33:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:33:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:33:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:33:33 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:33:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:33:33 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:33:47 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:33:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:33:47 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:33:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:33:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:33:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:33:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b9cdbeae0246f35c6d9285a119e3c4853580e96cf1c2e76eed9262f5936ec3`  
		Last Modified: Thu, 15 Jan 2026 02:07:02 GMT  
		Size: 143.7 MB (143679920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4907c0ee96a7a34b3a336607f6792f9d19d76cf58e6b149c7ba17ba820b1108a`  
		Last Modified: Tue, 13 Jan 2026 03:34:18 GMT  
		Size: 17.6 MB (17592085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a856e9f944695a75e81f1eb94f610073463d6d287227fe213272850761323df5`  
		Last Modified: Tue, 13 Jan 2026 03:34:16 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e35ea87e1b10f82d4b8171bb7b748f76e21e3abb870bb0b61901d3bae46e84`  
		Last Modified: Tue, 13 Jan 2026 03:34:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3a45a959710ecca49032f2682eafbc232a9ee80da01a6b20e47a3cd7fa9a3bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2746937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84db65bdcefd137e243e4a818630019da021aca2ed046b01b45e730803926bc1`

```dockerfile
```

-	Layers:
	-	`sha256:30c0574a10d7eb50d187f7eb2b7977fc2e7bfdb16604d497fde90310e957a701`  
		Last Modified: Tue, 13 Jan 2026 07:40:13 GMT  
		Size: 2.7 MB (2728413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16d7e0590598a8b61aad076d45cc78f955bc684fb048e65aeb39c6d1d48afcbe`  
		Last Modified: Tue, 13 Jan 2026 07:40:14 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:180c7c3b44d4b642f8702a01ca87b1aa87afda8e66fe51a8a3bf67d765f2439c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199072745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3caf1973a02d8cffffd7f8536591f2fa20cd292316d3189b46fbef5b2e0ff3e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 03:00:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 14 Jan 2026 03:00:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 14 Jan 2026 03:00:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 03:00:09 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 14 Jan 2026 03:00:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 14 Jan 2026 03:00:09 GMT
WORKDIR /tmp
# Wed, 14 Jan 2026 03:00:54 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 14 Jan 2026 03:00:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 14 Jan 2026 03:00:54 GMT
ENV LEIN_ROOT=1
# Wed, 14 Jan 2026 03:00:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 14 Jan 2026 03:00:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 14 Jan 2026 03:00:59 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 14 Jan 2026 03:00:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:24 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060dc17fe3569d7989208ce114c5611a9d7911a036596dcd186541c714f43aaa`  
		Last Modified: Wed, 14 Jan 2026 03:02:10 GMT  
		Size: 144.5 MB (144525181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7928aafd66b51141d6751d049689ba7b44fad50857ade6b8a10512c4d70b1af`  
		Last Modified: Wed, 14 Jan 2026 03:01:57 GMT  
		Size: 18.0 MB (17960669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e7d84e73c25bf64ddc232e7037b370f9c7f2ba8385c23bd409576ac9fdeccc`  
		Last Modified: Wed, 14 Jan 2026 03:01:55 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fe5c5f803399f1e965d18dbfb2e868edc72094acad8573774d0b568e50ccc8`  
		Last Modified: Wed, 14 Jan 2026 03:01:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:962206eb4c4098ebc50b647a3b067e65161a031d0151d1fc1980fafda38cb392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2749078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2766c4c3728cb97c0207119942d08050a3f88b02f418b97d97652d6a556f9612`

```dockerfile
```

-	Layers:
	-	`sha256:361627419e5e69378777cf8a2eac9e97207aab2ff3b83d0f8e97c946f0974662`  
		Last Modified: Wed, 14 Jan 2026 04:35:48 GMT  
		Size: 2.7 MB (2730631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbb5870206195307a33e523d647188e3a2f6c65b72dc2444a9dc0d26a9beb61d`  
		Last Modified: Wed, 14 Jan 2026 04:35:48 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:aaa8e29375109b007d8cd6272ef0642f54a1cc1611d166ccf443806e60496e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183683119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2965f5eaf62dd01599cd4206598cae43cc8f48bd7456fffa2f4361ee9d7b359e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:14:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:14:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:14:15 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:14:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:14:15 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:14:25 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 15 Jan 2026 23:14:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Jan 2026 23:14:25 GMT
ENV LEIN_ROOT=1
# Thu, 15 Jan 2026 23:14:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 15 Jan 2026 23:14:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:14:26 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:14:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499182964acbb7a6f7acaa4f23aaad30ee7cbc97ce9848f38909ebdaca216d40`  
		Last Modified: Thu, 15 Jan 2026 23:15:08 GMT  
		Size: 134.9 MB (134859713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a331b268feb0cb6eb9c20821ed9bd26f4a665cbee0e9f5620b9f048296af2ba1`  
		Last Modified: Thu, 15 Jan 2026 23:14:58 GMT  
		Size: 17.4 MB (17420845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ed11886ddbd9fa993f626f354de1382aa5ff377ae9ed08254a70486bef6100`  
		Last Modified: Thu, 15 Jan 2026 23:14:57 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c8d1af6a390695a6aa18eeb2a33fc8e7af4211204da13464a626fb13479089`  
		Last Modified: Thu, 15 Jan 2026 23:14:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2517780c5482b2088e8525632f6e432fbc03c68662996b8cd1ca8fe40356778c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2739014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd530a057eaad52e261c70d8954ef0f78cea21e109d8e46fc8a846672a1038e1`

```dockerfile
```

-	Layers:
	-	`sha256:5d44f267401bcb01a6812d3be57cb937c18a159002f2c82c1d9b06f4b74ebc13`  
		Last Modified: Fri, 16 Jan 2026 01:39:27 GMT  
		Size: 2.7 MB (2720612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ae3eabdd440be8495fced7d352337e69404e00a49e60700591c546beee11013`  
		Last Modified: Fri, 16 Jan 2026 01:39:28 GMT  
		Size: 18.4 KB (18402 bytes)  
		MIME: application/vnd.in-toto+json
