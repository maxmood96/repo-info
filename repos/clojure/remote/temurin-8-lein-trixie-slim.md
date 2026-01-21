## `clojure:temurin-8-lein-trixie-slim`

```console
$ docker pull clojure@sha256:7049d0b8b49aae444a76fb6ad587991fd28a3aae0f1b39e103afa4ecc3a313ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6d783a80934ab3d2731196eb11fb60aa47ddaf7170469039ef40f060c8588219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105472086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b6056ad46e67a7a6f828aecc5958a93a8176ebe4a88945c805aca189dfd883`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 01:42:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:42:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:42:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:42:37 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:42:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:42:37 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:42:53 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:42:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:42:53 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:42:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:42:54 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3756f6cd80888bb832c6fb9b5c96b88e3a50239c2cae3fe87b84195b3073a36`  
		Last Modified: Fri, 16 Jan 2026 01:43:21 GMT  
		Size: 54.7 MB (54733367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1fc60d7d7347a77db9274a7c4f5305218ee8f1ad50db60dd1b4e9f8076776f`  
		Last Modified: Fri, 16 Jan 2026 01:43:16 GMT  
		Size: 16.4 MB (16447285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d775f1091a69fda71fceb80a1ff39fd91513902ebe3e128aa13abaf4194238`  
		Last Modified: Fri, 16 Jan 2026 01:43:06 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:39a74b90946ccef25ea55baebd1c7ae8fc5d6629e9020a0908829499c6778413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0062522a58490dcb1a4d6823fcd93f8dec880e4908d813f128dea1094ee14f`

```dockerfile
```

-	Layers:
	-	`sha256:cce932378977515b0d8090d2587c7580a565e8d4906dc30e9967e2fb5769f1f2`  
		Last Modified: Fri, 16 Jan 2026 04:54:09 GMT  
		Size: 2.5 MB (2485110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58abb5ea895fa0f6ed8accb58db64cf366b567d8d7c5388a624c9e449e125ee7`  
		Last Modified: Fri, 16 Jan 2026 04:54:10 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:275ac6fb2eaa7c1af59f9c3c018f4a927e43d9694340abb78ffb0803a4fba64a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104880763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7d9a8e05f199f99dc9ae625725a04e0272f92395e485291be6ae512001ee25`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 01:46:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:46:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:46:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:46:33 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:46:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:46:33 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:46:49 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:46:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:46:49 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:46:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:46:51 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb5079c707709670959515870c5603254eb31e1301f0bb241a184f7c95b1600`  
		Last Modified: Fri, 16 Jan 2026 01:47:08 GMT  
		Size: 53.8 MB (53814998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290ae6af55656d33c45a230ea89d725a0a5f7bfe4bec800f783ce185cc1ba409`  
		Last Modified: Fri, 16 Jan 2026 01:47:16 GMT  
		Size: 16.4 MB (16413941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20ae8b12d9655b3d3c425aef28279b70dc3f9fddb7ddba3c7c15d10b6b6cb92`  
		Last Modified: Fri, 16 Jan 2026 01:47:15 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ff4fedbda9abc15c4d6713959027bff6d65ed4404bb1f678cdb24bca02a7b027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125349d629c471a4012168a792a36c156121560e3f40110d5cc8c458f8f947e3`

```dockerfile
```

-	Layers:
	-	`sha256:13ea756b7476551787b4e84004f30ec53182133596bdd8b72acf71830edf892c`  
		Last Modified: Fri, 16 Jan 2026 04:54:17 GMT  
		Size: 2.5 MB (2485426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3943795ef8f0f728309df5cbc7390582c1bfbe361f11f33490b10e67d6ce55cb`  
		Last Modified: Fri, 16 Jan 2026 04:54:18 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c80a0aa42829bea72279b1055eba2945c93cc9c5cfddb48ffbf01010d245f23d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106774017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:297886ddd55b14d9d232a52a90333680af4b860d15b2b388b999a67b4fc2d015`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:49:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:49:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:49:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:49:44 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 02:49:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 02:49:45 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:50:37 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 02:50:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 02:50:37 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 02:50:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 02:50:42 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b120fe6bca491b5d43488fbe9708b684a36bfbedc4a0256ac7fca0cabd7b42ee`  
		Last Modified: Fri, 16 Jan 2026 02:51:23 GMT  
		Size: 52.2 MB (52175136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158dc72ef6db8b1485d3ad58d69e155206e6d0d4318adacc50af8029d4d0b274`  
		Last Modified: Fri, 16 Jan 2026 02:51:13 GMT  
		Size: 16.5 MB (16485503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97319fe678bb1f9e7faa9ccc6f3e8292991028524864571334fdd6e48b0c8f4`  
		Last Modified: Fri, 16 Jan 2026 02:51:20 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:da91a169c95c125de97495b8858c32a1545064e12c458ed422e938639594c78b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499e108283c8a434b97450012b3a06324df55e120a0279ddcc3f31afb77b274d`

```dockerfile
```

-	Layers:
	-	`sha256:1ca4b3a3153007cf6b466589516de3ca645ef79cb62faa29fea31f82469ac429`  
		Last Modified: Fri, 16 Jan 2026 02:51:12 GMT  
		Size: 2.5 MB (2486683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e2409926ec6096639c32d685872cb1d9eb219de61be01e5da032b101233e90b`  
		Last Modified: Fri, 16 Jan 2026 04:54:23 GMT  
		Size: 16.4 KB (16425 bytes)  
		MIME: application/vnd.in-toto+json
