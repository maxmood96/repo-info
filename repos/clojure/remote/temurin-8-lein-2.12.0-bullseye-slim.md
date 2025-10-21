## `clojure:temurin-8-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:6b2af195ece13a233f358727a9965f71f14f784036eed4933763fddd7a378996
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:97371162f234488e9164b30d8324707b44864ae45b7e8e88c3769e7a367574f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104826204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0cb5c8dce2cafa065d51b21c71119f09823836f7da169823c650dc0cc6eac0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9ceb41845848af33db2593ea85b55da735b9204516a747efb4e556b8b174e1`  
		Last Modified: Tue, 21 Oct 2025 02:18:45 GMT  
		Size: 54.7 MB (54731351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35bcc9da33f1ccb9e5a693fa73b1387afd47c8db53bc144a8b7af1f671c64c9e`  
		Last Modified: Tue, 21 Oct 2025 02:18:41 GMT  
		Size: 15.3 MB (15318695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac9ff56c82708321b5b27856fbbbdc8b835f040cd6cd7e46a52a667aaf63594`  
		Last Modified: Tue, 21 Oct 2025 02:18:39 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:623545f7558000ca2034898f0406f3ceccc3c66326cf601bad7c4e9a38e6e173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b183da14bbe393db3b6344a3e25eb55412b8c533b983a1e64879a575e7a4400f`

```dockerfile
```

-	Layers:
	-	`sha256:275698be9c3e7f0266107fd9241baca760548f4923e879ef450197ccf4a7f374`  
		Last Modified: Tue, 21 Oct 2025 09:47:05 GMT  
		Size: 3.1 MB (3139520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a89d6d5e81738b27b376c43f96ed1345224cda6e1c963a3c153feaf6c64c7fc`  
		Last Modified: Tue, 21 Oct 2025 09:47:06 GMT  
		Size: 16.4 KB (16442 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dad079d4566816a37f04cab0ac69c288232e5b345d35b4ed01ebb3efba2707ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102407556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aeaddcf270ef6eb30466cec4163b64e6e452345b43487409f4c25577d5c4dbf`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78bb8b23aa40a72d09832914ca296478039e473fdff77faec20a1d8ba3f0251`  
		Last Modified: Tue, 21 Oct 2025 02:24:50 GMT  
		Size: 53.8 MB (53835606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf52063284705682f4a9cf43cf4e67f64614016a36f17ee69e9407c2bfb2234`  
		Last Modified: Tue, 21 Oct 2025 02:24:48 GMT  
		Size: 15.3 MB (15305769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4197b6d0f8bc6a1bd182e7a3abc2b7a446005237209f24e363658ffe3038f70`  
		Last Modified: Tue, 21 Oct 2025 02:24:47 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:287b404b1ba50a0980c00c9b250c948537b1e9bc5c87d65ed8fbf76e9c4b405c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc35bf13dd45d3d65ec74f84ceb92ba64b46d41dc3bc99ac013badb7494436d`

```dockerfile
```

-	Layers:
	-	`sha256:361d64d3c99270c935c17830123b79a49ad0caa00e92f1b1f1847f58bbd37b20`  
		Last Modified: Tue, 21 Oct 2025 09:47:11 GMT  
		Size: 3.1 MB (3139827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5dbccbe5f1ec064ebbc3bf2b6af60901060da9d4d7f65382411d01cca811866`  
		Last Modified: Tue, 21 Oct 2025 09:47:12 GMT  
		Size: 16.6 KB (16563 bytes)  
		MIME: application/vnd.in-toto+json
