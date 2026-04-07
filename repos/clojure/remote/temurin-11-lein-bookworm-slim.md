## `clojure:temurin-11-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:ea24cc979912b3ee6760d277e9404f6d92e814b12e247abc64ee8166ee3a235f
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

### `clojure:temurin-11-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7a5d8e7ded7bf4e0e936db3dbbadac44363f18a7e1884a2f857bb521cb16b8eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196319742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243c45c60862d67cfb7b6353a8d88f4556c88209357dfc7c3e86883e6804df7d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:13:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:13:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:13:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:13:18 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:13:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:13:18 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:13:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:13:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:13:33 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:13:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:13:35 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c22ddb28e4b6619ed8b8037d73636be2962c549e13040f7805fe85afe95fdf1`  
		Last Modified: Tue, 07 Apr 2026 03:13:54 GMT  
		Size: 145.8 MB (145806872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3f19b21d76ac8d657375badafc7839294dbf547c4b5077769da41f0743f6df`  
		Last Modified: Tue, 07 Apr 2026 03:13:51 GMT  
		Size: 17.8 MB (17758763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a361841fb0ddc58b6f7e5d7ff49eb25010a89f1ddc6001656fb77a07841ddc15`  
		Last Modified: Tue, 07 Apr 2026 03:13:51 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6c0bc52fd86ed9539d5eb76bb379eab6df8c3958853a74576e929aa4b9929245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2766603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200a0c02bdc89252de96a591c7122ae18a295a53ab7cbd0fcd561a9e40ed2fbd`

```dockerfile
```

-	Layers:
	-	`sha256:7a815846d9bbe0c338da271c047f3eeba1befcf0ce145aee2bf72b39bb7569fa`  
		Last Modified: Tue, 07 Apr 2026 03:13:51 GMT  
		Size: 2.8 MB (2750191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868af7db30f3679903e0f805f1786798e2178b98bfc105078f4d033016cd0ec3`  
		Last Modified: Tue, 07 Apr 2026 03:13:50 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bd660f857a6a3a5855c01905378e65a43bcbc3509b3e593b2c2c95a1e5323d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192725712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22bfad8a57e94dadd265025e3f60a490efadf18053d542248f530c1fa9aee62`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:23:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:23:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:23:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:23:49 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:23:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:23:49 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:24:03 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:24:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:24:03 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:24:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:24:04 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015dec85e584445b377158665f9e919e7468a49591ab782e3ecbfe756ab745c5`  
		Last Modified: Tue, 07 Apr 2026 03:24:24 GMT  
		Size: 142.5 MB (142500071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8075a6df6658b025f9a056bd45d9536328b53642654279f1dbadc891b8c01583`  
		Last Modified: Tue, 07 Apr 2026 03:24:22 GMT  
		Size: 17.6 MB (17591738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc16034c88741fbeb9da30f07b93e76bffca1f8c3b6bb1b218311b2160cfa66`  
		Last Modified: Tue, 07 Apr 2026 03:24:21 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bdfefa237d9daa11c163c6c73027a354b795c87856683f4b19fb37bc2965099a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2766955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86403553f1b97f74fd121ca83644505aa394a64c75b1173a359e486ff1eb268`

```dockerfile
```

-	Layers:
	-	`sha256:d2d8b446b94c27a7ef63fa12d1992404cebe7bfb36ccc30a92ded7ca338a4126`  
		Last Modified: Tue, 07 Apr 2026 03:24:21 GMT  
		Size: 2.8 MB (2750424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b21d28dd5b186d83480c227d94c0be2ac9ad9e9156914861064a1600b7350c8`  
		Last Modified: Tue, 07 Apr 2026 03:24:21 GMT  
		Size: 16.5 KB (16531 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:8d1595cc5f268f6f7ef6a3eccbceb9424f375a194d85bcde563ac64594c98b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187553953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4965447b8b77b60db549eec98a6ddbac41008ebd4904a45ea6cd4dc5388fd973`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:15:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:15:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:15:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:15:40 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 18:15:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 18:15:42 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:16:23 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:16:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:16:23 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:16:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:16:27 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbecbf7ecf5689b9ec9a2fb7833196c9e479474539bbea61e477b10fa3c1a715`  
		Last Modified: Tue, 17 Mar 2026 18:17:05 GMT  
		Size: 133.0 MB (132996700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0186f3e36c49826de33a0fadf370565a7f0575c84d2b02ac3390d95c8d09a7d6`  
		Last Modified: Tue, 17 Mar 2026 18:17:03 GMT  
		Size: 18.0 MB (17961093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d20bd2c05fbf06d94672204b72efd3688e762ffde8e743ec18e7e92d890a769`  
		Last Modified: Tue, 17 Mar 2026 18:17:02 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1917e1eff84e832dbaa1563de32beff02906ae32cb3d9aaaedea1ac5fd9d6b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2767865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadfadb1a04689aeefcbe2164c6b018d88564ffa09b3b31c5a77b470cf26bd88`

```dockerfile
```

-	Layers:
	-	`sha256:104eb99fbf21594889e51483ac06adc10533f1fde61c81428bd75d260ba8b3d0`  
		Last Modified: Tue, 17 Mar 2026 18:17:02 GMT  
		Size: 2.8 MB (2751409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68bdb4816d5cabc4fa3fd0cb818bee102f01767e9d13652a595aa7f990fccf4c`  
		Last Modified: Tue, 17 Mar 2026 18:17:02 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:786074430f0a613e4cae95e1beba13ae21932654550d1fd1c1a4c744762e8dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175392693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b30f24cba2e8d8a7a8c4e9167f9a5dd812d03fa2e2d55d451fe4c305038002`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:39:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:39:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:39:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:39:16 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:39:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:39:17 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:39:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:39:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:39:27 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:39:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:39:29 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e385f726bab54d70ecc51bad16d60533bc9b6d182b632879bc3c86a7da9d89`  
		Last Modified: Tue, 07 Apr 2026 05:39:56 GMT  
		Size: 126.6 MB (126562190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafa6a9582fd75b84b80a45c6b1573591fa2afb9383c760a2ec7d8ad2e01a777`  
		Last Modified: Tue, 07 Apr 2026 05:39:52 GMT  
		Size: 17.4 MB (17421084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69bb5b93eaee5f4a7e807174461c29e5ebf73c713fc8c68f56d6d15d4b3682b`  
		Last Modified: Tue, 07 Apr 2026 05:39:51 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dd18fef376277924e9f4b6e1d52882890f41f4576390060c09c8ae9e379dd25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2758421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb49a66074f26d587f7a545831d9bc5247051a4ae9223a4e690e1e034539d4e`

```dockerfile
```

-	Layers:
	-	`sha256:f32dee42f8019f43c67a2d0a2f72d1d935a78a959c11de4a3f233260db978b07`  
		Last Modified: Tue, 07 Apr 2026 05:39:51 GMT  
		Size: 2.7 MB (2742009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:851570905604d2098a5d074740a932eac52a467e0099505a0014977144b6fd22`  
		Last Modified: Tue, 07 Apr 2026 05:39:51 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json
