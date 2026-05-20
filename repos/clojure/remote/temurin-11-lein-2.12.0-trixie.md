## `clojure:temurin-11-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:19efa8e18c7e4ce30dfacc4f7bf69a6aa012f2e927d522992aae55f0700718ec
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

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:f2783b631b241f531a75442f05d1a5c67d3ee9e14540b4e59ac792445c910a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218304058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d11216452aa73a8d0c2f973db6c8f024057ae47a4eb95c804192252036a605f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:57:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:57:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:57:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:57:41 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:57:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:57:41 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:57:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 19 May 2026 23:57:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 May 2026 23:57:56 GMT
ENV LEIN_ROOT=1
# Tue, 19 May 2026 23:57:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 19 May 2026 23:57:57 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e302cb804e7cb984b8bf300025b140521508f9c5c336ebcb1dafb2a6fd3c5504`  
		Last Modified: Tue, 19 May 2026 23:58:16 GMT  
		Size: 145.9 MB (145886262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce4c759786d57ee9622fbb6541c03bfef535425ad6f2349ca2ef5ef946a72c3`  
		Last Modified: Tue, 19 May 2026 23:58:14 GMT  
		Size: 18.6 MB (18589436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0850426dcee687ce3fe5298641064db006814ef3476b04b21bab9af1129413e5`  
		Last Modified: Tue, 19 May 2026 23:58:13 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1ad45afd4d5c6418b04560eea1909aff8e05d1dec8b5927552301ccb4c32960a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd82199051713a991ecc09e695de1876e832d9e0a86c1507aaef0ee22cea8971`

```dockerfile
```

-	Layers:
	-	`sha256:771e6ad1bbd5e363fe81aeee090cdcfbd157308bb68cd11b2faf13d9805adc75`  
		Last Modified: Tue, 19 May 2026 23:58:13 GMT  
		Size: 3.8 MB (3835712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c043a8f39778659a1f0674443cab6fa7798195d0907ceae5acfaae2b2d3c08`  
		Last Modified: Tue, 19 May 2026 23:58:12 GMT  
		Size: 16.5 KB (16517 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5d16c46441df08926fcc5a1ef15b57c8da25c0bafa2c16a460e6d4a9f82e0bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215319803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231ebc0341cde0d479822ae7c5d770500632738cd15e250b3c892b2922bee663`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:04:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:04:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:04:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:04:39 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:04:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:04:39 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:04:55 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:04:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:04:55 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:04:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:04:57 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725ae0c5aef96817122bcecd9b790f02a5d70ded02a22fbfc6e5dcefc13ecdb7`  
		Last Modified: Wed, 20 May 2026 00:05:14 GMT  
		Size: 142.6 MB (142582234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafd39b71a5fb9c4cc2244467f4d9653c9047cd44ae60b0a6bc69727c12ede7d`  
		Last Modified: Wed, 20 May 2026 00:05:14 GMT  
		Size: 18.5 MB (18547565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc6e7cd14eca5e1756ff4649a15e25cd4ae822c1e5a5107284512eeb148caab`  
		Last Modified: Wed, 20 May 2026 00:05:14 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7317100b33ed8491729dd6cb78b7e48a1eba0417f94d6708faf975eb5cd402f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f7a8c7d1b8a785cf4fb92478b3cdc2794a5e8a688d643e4801b5e7f99caeb3`

```dockerfile
```

-	Layers:
	-	`sha256:3d30ef1d44c8e681eaa5c597054b1ac68650c2354584793e6475cf1de909eb08`  
		Last Modified: Wed, 20 May 2026 00:05:14 GMT  
		Size: 3.8 MB (3836570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f53dcf5654279f45759d25b1ec4e2ba38600d04e1444195baee9813c1b07a2`  
		Last Modified: Wed, 20 May 2026 00:05:14 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:528f4bd7979b0889754f95bde9b6904c33fe20e212f5a7107e1751be8b06c776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.4 MB (209392118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367a1ab62172ebf3b4ee71bdd0f8dfeed36a2718cf860cc46a748099d49b5d26`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:26:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:26:20 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 09 May 2026 02:26:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 09 May 2026 02:26:20 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:26:50 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 09 May 2026 02:26:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 May 2026 02:26:50 GMT
ENV LEIN_ROOT=1
# Sat, 09 May 2026 02:26:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 09 May 2026 02:26:53 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6819a6f95dd2e4192ab6b7dae90a40976321dcde2fda4665eb71bbac73d5122`  
		Last Modified: Sat, 09 May 2026 02:27:27 GMT  
		Size: 133.1 MB (133110167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f506d4c8c4f2046dc22e4a52e3389658ffe7dbe1cd5c02c370997da5803b15`  
		Last Modified: Sat, 09 May 2026 02:27:24 GMT  
		Size: 18.6 MB (18640994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7056bc111a59aa3385107d1b4adf98074024ec9a4428bad0be8fc32c2bf7d7bd`  
		Last Modified: Sat, 09 May 2026 02:27:23 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:af99f6b7613cced4cf2b826cc4e719eeb95b7defcc8f67ea01241c96c21f2707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19403bb8cad2bc2b7df00059e594ff58bf5c9f5dc7c5d9ece977eb667fdb8c2`

```dockerfile
```

-	Layers:
	-	`sha256:516fe59800c8eddb90514893f2f385fedda7368a861e46c3930c4672aa254167`  
		Last Modified: Sat, 09 May 2026 02:27:23 GMT  
		Size: 3.8 MB (3836055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e72b524fda22551526127d0f6495e2b3f6bd8d9190b72ff6ba0c28dff561e35f`  
		Last Modified: Sat, 09 May 2026 02:27:23 GMT  
		Size: 16.6 KB (16561 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:8229423696ff4f442956f4f35766d09516f4c2a9f1a77b7893cfe1652f790746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199179781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9afd1c5b14f954242494769ec67e707441330d259acd219c5d829e2498f8bdbd`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:41:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:41:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:41:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:41:36 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 01:41:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 01:41:36 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:41:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 01:41:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 01:41:53 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 01:41:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 01:41:54 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e6016d4ebf4c94d6542085c791df63dbd93201c2c8fc6d05dc6abacf51ce4a`  
		Last Modified: Wed, 20 May 2026 01:42:15 GMT  
		Size: 126.7 MB (126651716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f06e69ba0084445429a2293453396f24dbc7ce9414e5718fcc2c1d975322b10`  
		Last Modified: Wed, 20 May 2026 01:42:17 GMT  
		Size: 18.6 MB (18630553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1831eab4bada5c0542dc318182c69813f2f83d23e262e21aa73f06cb5ec47af7`  
		Last Modified: Wed, 20 May 2026 01:42:17 GMT  
		Size: 4.5 MB (4517700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c0418eda7adebe45044803ef31ee07558e364faf56b9a1555527b816760c9a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3848661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa14ce2018b2fa9899dd654efd753ebd7810e1d11723e2155e31fe6872838358`

```dockerfile
```

-	Layers:
	-	`sha256:b549364a294f07d86f74a38f3d880d1c7ea5fdc8799c8069030184177288b382`  
		Last Modified: Wed, 20 May 2026 01:42:17 GMT  
		Size: 3.8 MB (3832143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:714181237091acbc0165c7a34b781b7885e59004ab81f15c6b57b54b690b22b3`  
		Last Modified: Wed, 20 May 2026 01:42:17 GMT  
		Size: 16.5 KB (16518 bytes)  
		MIME: application/vnd.in-toto+json
