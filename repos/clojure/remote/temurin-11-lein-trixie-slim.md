## `clojure:temurin-11-lein-trixie-slim`

```console
$ docker pull clojure@sha256:f8602703b3080abade68c15712a0d9d46dd18d60129b973f0eff50e1495097a5
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
$ docker pull clojure@sha256:b03f97ed3cbd1ae8df56ae6043c44edaa006f88d24ad56847e40d26481006b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196632266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57300e03316b957536b1865bfcb42376b1fb78baf3ff662185b807de727de78`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:15:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:15:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:15:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:15:55 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:15:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:15:55 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:16:13 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:16:13 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:16:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:16:15 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098c31a09d33921e034b83cd2839e41e3fcf86a2116493134692dc1af526dfdb`  
		Last Modified: Fri, 08 May 2026 20:16:35 GMT  
		Size: 145.9 MB (145886254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843eddb449a92e49e8cb9d437ebe55b821af82ac48a6ea5297c553b994c1798c`  
		Last Modified: Fri, 08 May 2026 20:16:32 GMT  
		Size: 16.4 MB (16447997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e725156685cec4fa3f6be66a68059a9c4c71fdc5419025cb0651e8fcbd08cdd5`  
		Last Modified: Fri, 08 May 2026 20:16:32 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c928f4745f623937b881558eb8cc58ed49faa906760ce333bf3c7c100da7524f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f031f52fe4b4c4e7c439a48aa7f7845d33bc6eebdb1afd5854e17707388f0f3`

```dockerfile
```

-	Layers:
	-	`sha256:2804d102a46d08e755717b33d90f5ade5a0223f25b94606cbf80b399284ab60b`  
		Last Modified: Fri, 08 May 2026 20:16:31 GMT  
		Size: 2.4 MB (2384931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abbfcbf0e4ffec417e205a99c30ae3adcbb0db214e41de9871060335e96860dd`  
		Last Modified: Fri, 08 May 2026 20:16:31 GMT  
		Size: 16.5 KB (16548 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:17ee8be8d7403bb71e80357da0f1bf82c6381bb7d6cb231160840383d0cc030d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193657538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45416ce03d91c22b27b9affc6cbfa918eb45bb58e7385da37957ea62ea6efdda`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:20:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:23 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:20:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:20:23 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:20:39 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:20:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:20:39 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:20:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:20:41 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8869a605edc468970ddeda3843e1c5a1b457f6e3633d0433d19902a1f2dcfc9`  
		Last Modified: Fri, 08 May 2026 20:21:01 GMT  
		Size: 142.6 MB (142582199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43979f9b650b555c863cfd9af5899e56a10708a84cf3c88afaf6b464d77c64cf`  
		Last Modified: Fri, 08 May 2026 20:20:58 GMT  
		Size: 16.4 MB (16413921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b5fc5ae2fd470d335ec987717eb477a7b2e21f34fb4902acef1510a0fa8b06`  
		Last Modified: Fri, 08 May 2026 20:20:57 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8fd49cc53984f7549d3c73dd298e44921e23cfbe5dcad947faab30eefc8a6cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954578922aac0a598ec6e9bd153d4d601769ba6755495b378a85d4cda2695075`

```dockerfile
```

-	Layers:
	-	`sha256:6584607e60a3848cc2d7076cebf2b7ca47820c37116c1686f659ea16c8bb6eef`  
		Last Modified: Fri, 08 May 2026 20:20:57 GMT  
		Size: 2.4 MB (2385167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:161a03daedffc347faba649a8e7a7448faeb13fc9eec465fde73302894a2d055`  
		Last Modified: Fri, 08 May 2026 20:20:58 GMT  
		Size: 16.7 KB (16669 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:cfe8f5971d10fdfe9e509ef457233030fdb8852598804ecccbdc07a6f95daf80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187711351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d0f0ed8943c21a8385e5956767a7fdc8d64ba09eee5924bc918ea5e207ea11`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:38:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:38:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:38:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:38:54 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:38:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:38:54 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:39:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:39:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:39:32 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:39:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:39:35 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd298a1e1654753929706776995581c6d8e0ae8db97ccd3dd0cbc779069c0bd6`  
		Last Modified: Fri, 08 May 2026 00:40:09 GMT  
		Size: 133.1 MB (133110194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765279a3db3dc6d0d205aab3aa3b72c0d59a9c9c3618844103d69b72e76df610`  
		Last Modified: Fri, 08 May 2026 00:40:07 GMT  
		Size: 16.5 MB (16485334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c672b3d21d1f5bb26cc043cef3593ec31d3497fcdc5e63a9e4307ef90bd6ea3`  
		Last Modified: Fri, 08 May 2026 00:40:06 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5dea9ee18fccccb5e5ce19a532e55b08eb1bcced42fd18ee0dbbf9e761873168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a160e7d3332a03bd191807ab576305cca27e24993dff325646c61307f45e132`

```dockerfile
```

-	Layers:
	-	`sha256:fbd1acf98acfda98e24398a24709f66638833fc6846f3471823b6c992d3286d5`  
		Last Modified: Fri, 08 May 2026 00:40:06 GMT  
		Size: 2.4 MB (2385296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e310edf03514575c047e29c6c547af44350a885c54eb00af55a3350c1817323d`  
		Last Modified: Fri, 08 May 2026 00:40:06 GMT  
		Size: 16.6 KB (16592 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:25ac6a8abd2a4364539f7c2b442fc4eff943530d5f24258cef0a460375e8c215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177493661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f283cfbe5c63b145081c082f63dc3020e53ebfac25f2118a5146e2dd78ccbfc`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:13:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:13:50 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:13:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:13:50 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:14:03 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:14:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:14:03 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:14:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:14:05 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f616beb9fa3f85be0df9ff578c65c04793648f333a4daf9843ed26118d89ab38`  
		Last Modified: Fri, 08 May 2026 22:14:29 GMT  
		Size: 126.7 MB (126651715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4d1f7763329292ce7ce4481fd864337c7f84a14038f64b8362d331388f5086`  
		Last Modified: Fri, 08 May 2026 22:14:26 GMT  
		Size: 16.5 MB (16483823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da56935f719049b77156c24232ea86e2697e369700dba2052fafd8fd101bb962`  
		Last Modified: Fri, 08 May 2026 22:14:26 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:80f2b762b9da1907dec275bb778ae7760e955e97d28c3fec4631875f2b4fce9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa36492d8bc32e93131af44b8a08f377fee75d17df7341935484cf9ee0d30d0`

```dockerfile
```

-	Layers:
	-	`sha256:2d73ae2a3c7cc30e65036125df754a65219881e651bd186176cb29eff1b90418`  
		Last Modified: Fri, 08 May 2026 22:14:26 GMT  
		Size: 2.4 MB (2381362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b44ecd5bb125e39050b12b6a29ec7d144c6205211cd90042cacc41708634fb7`  
		Last Modified: Fri, 08 May 2026 22:14:26 GMT  
		Size: 16.5 KB (16547 bytes)  
		MIME: application/vnd.in-toto+json
