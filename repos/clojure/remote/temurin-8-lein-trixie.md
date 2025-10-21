## `clojure:temurin-8-lein-trixie`

```console
$ docker pull clojure@sha256:c9fe8b37c5f3bb1f3f01038638adefdab5cb647ee7286b6f47f9574f3587adf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:1aa4e6fad85a399910b5a179f4967c4e3b3eee7af5fdae6701e0e277d5a26122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127113140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57dfb7aa9b9d2a1e7d2558dd65c966e661259abf57abe645a80d0873fdd0e0d4`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
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
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30969089d0947c4346bc2b8f34c843d69e769b77e4ee73ae9886fd51d880516`  
		Last Modified: Tue, 21 Oct 2025 02:18:58 GMT  
		Size: 54.7 MB (54731352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30738b08555f6150dc0c6a790c0f71bdcaa425a1c080416a63f91347467aa5e0`  
		Last Modified: Tue, 21 Oct 2025 02:18:55 GMT  
		Size: 18.6 MB (18579026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6043af5421b5e81d7c9ad714841d5c60e79f1e9fa643976e2834befcc4202f3`  
		Last Modified: Tue, 21 Oct 2025 02:18:54 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cb2155e27475677f9c03d9a436ec67d9fa599d12e949bae28feb47fd4d8c387a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822ef7e9f8eb44f05dab11b5c69f3719d05e8cb889d9b095e851337a153c1ecc`

```dockerfile
```

-	Layers:
	-	`sha256:c66346129031a140b9a6d2c1f07e11d900a52662961ba6a5bffd7bfd424a149b`  
		Last Modified: Tue, 21 Oct 2025 09:47:13 GMT  
		Size: 3.9 MB (3934996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ae3472b0fbe808729bc96cc33d3429f6ebde3bda209dee89fbbfbd39354b11`  
		Last Modified: Tue, 21 Oct 2025 09:47:14 GMT  
		Size: 16.4 KB (16395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7bfe5293752cbb49b7edeac8827e1e3dc3bb675cc83641022aff21fdf1ee644c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126542930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9954f5ea88759e1f82f3624723020ee3a284c0f43ce7890c87d0b19d34319a4f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
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
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306dc464422d9e3026e1a44f8557173c9721b7a34a9cee04fe191f77cf098f8b`  
		Last Modified: Tue, 21 Oct 2025 02:25:01 GMT  
		Size: 53.8 MB (53835625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6f4a1fce2575846e6ffb0219d9e399adfe1b3204c6b3f05799a3221b68c568`  
		Last Modified: Tue, 21 Oct 2025 02:24:52 GMT  
		Size: 18.5 MB (18539810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93dae2a3a5637c19f9312c79cc044fdeeb87894a9a1037d15a440f530ed7b02`  
		Last Modified: Tue, 21 Oct 2025 02:24:49 GMT  
		Size: 4.5 MB (4517720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:43cb2d174cab2f4d998fd81494d14d1423bcb47146ccd74b1145fb9063a91644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a340dd97739b05f4d678a0beb72e55b2f6d5c0a40d102af85aa7e61e0390253e`

```dockerfile
```

-	Layers:
	-	`sha256:1aec0c31b070e1de1711b27775a4ed0a829631c4a4f8c34f620a5d398f8c50fb`  
		Last Modified: Tue, 21 Oct 2025 09:47:19 GMT  
		Size: 3.9 MB (3936571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:331a49e97697027e1b264c58807a4dff70b8e66b46a671d059dbbca6532e30a5`  
		Last Modified: Tue, 21 Oct 2025 09:47:20 GMT  
		Size: 16.5 KB (16516 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:2b1d4099472a2d9a293336657d0554150ab9e7fbf6f9bf3c03bec2b7f88403ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131639043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b863970b5291d1da28ecf9b786156db356c801e4e163a6b2dea422272b384d9`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc3f1eebf7bf9dd53e932366fac151524ad2e096efaf95dbc9c6f9b71a05479`  
		Last Modified: Fri, 10 Oct 2025 04:46:14 GMT  
		Size: 52.2 MB (52165419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9537142fb607356aabf6c181f6742a949cd41c2ea83d7459673c88cb55047f8a`  
		Last Modified: Fri, 10 Oct 2025 04:46:04 GMT  
		Size: 21.8 MB (21846616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febb0cdf816fb23a17c76c493b6b6c7e47caace1d6b806adfe5a7f8575af4503`  
		Last Modified: Fri, 10 Oct 2025 04:46:00 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8b8eab6a2df1cdb193000acffcb3b771362ffa75a3645484d13f081202b83633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b525db765a8762c905eaccd6f48d0cd8dac6c1aa27bc5789d84da2cae4c471e`

```dockerfile
```

-	Layers:
	-	`sha256:8ad4b3baff7bc8137a84496fed7a8895b1b07f8dfb459a3992324ee6df2c736d`  
		Last Modified: Fri, 10 Oct 2025 06:51:43 GMT  
		Size: 3.9 MB (3936587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0d6e6e49074a6d33abd112a9377e63a14205aa939777fba96e680484349873b`  
		Last Modified: Fri, 10 Oct 2025 06:51:44 GMT  
		Size: 16.4 KB (16439 bytes)  
		MIME: application/vnd.in-toto+json
