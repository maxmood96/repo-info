## `clojure:temurin-11-lein-trixie`

```console
$ docker pull clojure@sha256:25b44c930fc1801a423664fc4adae0464d42fc581df7f179449078e2d0e97d19
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

### `clojure:temurin-11-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:96fd5f21ca9aed8142cfd7dbace27d04a15572e8c3b04d008f02683db7e5d959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217353536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b0b45abe3f6b9605dfb82634cd328632abb768fbf869e44c9a4efbf7c5934a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:07:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:07:04 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:07:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:07:04 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:07:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:07:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:07:20 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:07:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:07:22 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78db572841c71d3caa4f2f83b9f2b45604205a8b3e39ae88855a8a0b564f22d`  
		Last Modified: Thu, 20 Nov 2025 03:07:13 GMT  
		Size: 145.0 MB (144966633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9080a978362ad9aeecfd11ce702b8c5c2eaa2a0f677670ff1347f21733b568dd`  
		Last Modified: Tue, 18 Nov 2025 06:07:46 GMT  
		Size: 18.6 MB (18579558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef769b0213a43490df9a51c8ec36eff785349a0649dc83410a6f4da6d396ddd1`  
		Last Modified: Tue, 18 Nov 2025 06:07:45 GMT  
		Size: 4.5 MB (4517766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d5f665b80859745f9d72b7942052f0ff22ba22bc7fcfa93bbabdb4ccef19fd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb87748f584edfff28033f37a6618df5ff228ca280b150902c3a9e355b0185c`

```dockerfile
```

-	Layers:
	-	`sha256:df6468fce8302a9ee8a185048de1738d050763aa843d3739e0e7e3e7a24e3bb2`  
		Last Modified: Tue, 18 Nov 2025 07:38:40 GMT  
		Size: 3.8 MB (3833519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ab3ffec72957a3008565c997838ca96077ba21a4d3fd957f3c90521898e0518`  
		Last Modified: Tue, 18 Nov 2025 07:38:41 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:89faec196055a874139a1de55164cc9f3bd443e8ab04ac562242b9d24729beca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214440211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d61af1c2d6d4a3917a614c121eb19e0bf2b4cbcc56866f618c5388351ddf710`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:57:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:57:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:57:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:57:14 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 04:57:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 04:57:14 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:57:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 04:57:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 04:57:31 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 04:57:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 04:57:32 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11712c78fc976f496c6d9ee6d0d34f5c2b5b76604ed90999d8eaf1fe2c19593`  
		Last Modified: Thu, 20 Nov 2025 21:31:56 GMT  
		Size: 141.7 MB (141731579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0108a1ede633874996c92138e8a8edfb2f5ac0cde59ded7ba46205017c77391`  
		Last Modified: Tue, 18 Nov 2025 04:58:02 GMT  
		Size: 18.5 MB (18540655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690ae51cb282a4b9bd4f1a1f433058b5b219ddfd0cbdf5d169614f631e4b3b1b`  
		Last Modified: Tue, 18 Nov 2025 04:58:00 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7546bbabf56d311a732c40215d937c57d637898b925905e74bb841070314c06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3851498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0bddf0ae7d9ed5f67b0c048b95445e90c15b352fc5c1caa41bb23a9f2ac2e8`

```dockerfile
```

-	Layers:
	-	`sha256:23908bcc9ceaf9206cd77abd4596f0272c57f678964cfdf9c3c0707911095376`  
		Last Modified: Tue, 18 Nov 2025 07:38:46 GMT  
		Size: 3.8 MB (3835014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd25d1a3b8037e43b38b94c5c21e765c96f2cbadfb40123cf7cd4b3a6a5e3e71`  
		Last Modified: Tue, 18 Nov 2025 07:38:46 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:cc831335117ec737fe49a8fd5817aa4362f69619e2c084470d37a7864bdab057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208345276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8578cf144f7f011d475f4c7b7881373184e00ced8002ad3b8b5f334a9c0b15`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:25:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:25:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:25:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:25:25 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:25:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:25:26 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:26:01 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:26:01 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:26:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:26:05 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37d1cc451357decc266df875d9334bbd4504581a335e8cd24c32ce8844bcd57`  
		Last Modified: Mon, 08 Dec 2025 23:26:56 GMT  
		Size: 132.1 MB (132081948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b41cab6022c010fcde6e41c7222df8d7ea7b3dd556130153bc257b9e1fcb15`  
		Last Modified: Mon, 08 Dec 2025 23:26:49 GMT  
		Size: 18.6 MB (18637067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998f666a95871e79caf1b97796ac5953f1a565dfece2ca621ee576bdeb32715a`  
		Last Modified: Mon, 08 Dec 2025 23:26:48 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4b6fde99f61e51ad00234d3040db01d82b926a7dfdbf6bb53e2eee12dc8bd360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9ec16341fe4c0c549de141920e8a91deb511cbdf75ac46a2a9d30893534a2d`

```dockerfile
```

-	Layers:
	-	`sha256:33dc19e90993738b73a0bd05c5c2576efa97dfa0f3182f52b03af4355f85f19e`  
		Last Modified: Tue, 09 Dec 2025 01:35:40 GMT  
		Size: 3.8 MB (3833902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc62482b4a5067db8af21b84eec632303a4b29597ee98cf38e33b8879c52787b`  
		Last Modified: Tue, 09 Dec 2025 01:35:41 GMT  
		Size: 16.4 KB (16407 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:5e9748cbde7baab8298d4ea2927db6aac22bf043a596b166bf1d5855720ab441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198178801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33413a1ad8e9c97fe9bf48e46a48317342c411c3a5db540de78a52ebede1215a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:22:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:22:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:22:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:22:44 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:22:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:22:44 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:22:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:22:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:22:56 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:22:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:22:59 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:af4c50a2cf2848edb9e1797defa12d9a203416cf14b67469a37a418b1d0bb175`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 49.3 MB (49346014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a70cb1c823d5e23b35944c88065c13443837da05f853837830e64a9332d56c`  
		Last Modified: Tue, 18 Nov 2025 05:23:40 GMT  
		Size: 125.7 MB (125694435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cd8cedce4a4925458bd493ae3937ecd3dcc3df9376f754aa9dc92cae1f7fe7`  
		Last Modified: Tue, 18 Nov 2025 05:23:31 GMT  
		Size: 18.6 MB (18620576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7909e65bd9bcaa9aa24ce44063bcd27707a4b01f15bed8405aef2c370cf2b851`  
		Last Modified: Tue, 18 Nov 2025 05:23:30 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:248f2111f33c3d56e73f79f7eaf6b5182070c4d0cb4fd5c925ca5a6447d3f3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3846313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19764231282fa133314abefc3d1b0f71e7601192db0093dc18c5526d7595fe6f`

```dockerfile
```

-	Layers:
	-	`sha256:7e4b1f031f8351bfe655a17bde0343c7dcd8dd2bdec9ca21ee893b52227bc006`  
		Last Modified: Tue, 18 Nov 2025 07:38:56 GMT  
		Size: 3.8 MB (3829950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a689f43ecbc6a7e63b1767ccf5b8d6156a83e51ebe49914e89668d23eadf6bf`  
		Last Modified: Tue, 18 Nov 2025 07:38:56 GMT  
		Size: 16.4 KB (16363 bytes)  
		MIME: application/vnd.in-toto+json
