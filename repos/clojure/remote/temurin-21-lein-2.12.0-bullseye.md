## `clojure:temurin-21-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:4cc1c6bc0d82fa8608699d5e331271f94df1d4badbbc15b2183890354909da8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0b6b54474c4e4b5f0cd73f3ce88e5b058941c42c85973386402348e351826a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232739127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d249264be3f204c96d3118d1d29edb9d27df2a4abaa1c9b18311124b046a83`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:05:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:05:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:05:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:05:41 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:05:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:05:41 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:05:55 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:05:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:05:55 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:05:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:05:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:05:57 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:05:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0d85ee9eb9422df517b52418d0c1c001f4369038a21661c159bb95090a3487`  
		Last Modified: Thu, 05 Feb 2026 23:06:21 GMT  
		Size: 157.9 MB (157857074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f905fa31cecc7225bfc8d05fd47eb94db5a0d57ee9b57270813a2a83acdc82e6`  
		Last Modified: Thu, 05 Feb 2026 23:06:18 GMT  
		Size: 16.6 MB (16607629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36a9f555eb210f8b7a337b0ce998946a1b5c4db86f0119eb2c0ddc40eb458cd`  
		Last Modified: Thu, 05 Feb 2026 23:06:17 GMT  
		Size: 4.5 MB (4517735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f81bee9fb63bfcade3fd355e12edbc2e63c26ab940aa7d0aa7992bed4f47d0`  
		Last Modified: Thu, 05 Feb 2026 23:06:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2493becbec569b74bcf52174d18a26f84ab51f58f1bc32aa8c993a7c14ccc632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85b540b1482ab81c785afc66a1b44d67ec05579d17c0c48c41a8714f52de5c86`

```dockerfile
```

-	Layers:
	-	`sha256:11c778530311741cabee4ec3a33dcbc3891cd49cf3cc175075a7b1586cd89559`  
		Last Modified: Thu, 05 Feb 2026 23:06:17 GMT  
		Size: 4.5 MB (4479294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e7c4f9746ec1347735a741e71a9eff2a1719156a4325236b9f429fb2d241f03`  
		Last Modified: Thu, 05 Feb 2026 23:06:17 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:006e7d7e557f1f81abca54dd3d903c862f8a241947e3b3ff491e45433ca3c67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229504560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce997bcec5c03c702f7bc9e650648553b29458a3705c1479dccc39c4f513bfb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:06:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:06:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:06:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:06:40 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:06:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:06:40 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:06:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:06:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:06:56 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:06:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:06:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:06:58 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:06:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfd15c40f3c8c4c3320dfdf49df2760e7a4609aae5141670d7564e7d08d638b`  
		Last Modified: Thu, 05 Feb 2026 23:07:20 GMT  
		Size: 156.1 MB (156133069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3c3e4ea1cb058bc6324f45f4432cd4ff930a22ca3a48a32c1cdec1e278b344`  
		Last Modified: Thu, 05 Feb 2026 23:07:17 GMT  
		Size: 16.6 MB (16594992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a49ba80dea84ce4ced30dfa25d42144a29a74d0d6fd85c750aa0119c297346`  
		Last Modified: Thu, 05 Feb 2026 23:07:17 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1668b5fb20842c93dd1816ad327151cf439e9212de04abb85cadad138a0bb6c1`  
		Last Modified: Thu, 05 Feb 2026 23:07:16 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:88a38ecb7df7640631e7b28d4849c2d383db3ebcac0f91fddce6f15ed811cf62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4496756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04067eccb742cb276910057f82eb48fbf337a642e8872efca91b50cf9c6e8dcf`

```dockerfile
```

-	Layers:
	-	`sha256:e8795cdec002f90af944e7312bdca701bd8812d267b0c0dcc2704add2b6e8c44`  
		Last Modified: Thu, 05 Feb 2026 23:07:17 GMT  
		Size: 4.5 MB (4478268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d92c01241408a2c390e26ca926fdc8b9de80271c75c73eb421e0cc64f25625ae`  
		Last Modified: Thu, 05 Feb 2026 23:07:16 GMT  
		Size: 18.5 KB (18488 bytes)  
		MIME: application/vnd.in-toto+json
