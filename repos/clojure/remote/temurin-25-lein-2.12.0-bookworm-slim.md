## `clojure:temurin-25-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:3b91db7be4b069001ad189f8a66107eb6e9d10bf75edd60d54334611b4e051ca
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

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:205b054a58f32183ebf7691c7a8eb501c9085581c055b85623c7836d4cdb12dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142550737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199936cd37a2d6937692943617cbf5d39a91fb95247c43d64b24ad3751c2b11e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:22:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:26 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:22:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:22:26 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:41 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:22:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:22:41 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:22:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:22:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:22:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:22:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befe45831f0d527879960b8fc7717491ccfa538b21006eeeb8e8702e9e4a6b72`  
		Last Modified: Tue, 03 Feb 2026 03:23:01 GMT  
		Size: 92.0 MB (92045301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d69bf1cd329a7542680ffcb3c8eaa2e2290c89289d20cb06384a63defb1eb1`  
		Last Modified: Tue, 03 Feb 2026 03:22:59 GMT  
		Size: 17.8 MB (17758819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3e6b8ac55bab4ad1413a0e5b343e327268e734e0ff776e51100ce110d5f076`  
		Last Modified: Tue, 03 Feb 2026 03:22:58 GMT  
		Size: 4.5 MB (4517698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5531edee49955baf5632aba79e7fb8d5e4549d7aad2c68661bef0cc98b00369`  
		Last Modified: Tue, 03 Feb 2026 03:22:58 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:44db8c9302aa90d4314e93fe75e48c1103b6e0438e9bc33720587136bcdc491c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68c907a688d7b71e96135d118a02d2ae62ec4e27855b309ed62e193f183e41b`

```dockerfile
```

-	Layers:
	-	`sha256:0500d2668d7d11af5d4e2534702c1c405beda70bb6f1f3e479d0744111627ccd`  
		Last Modified: Tue, 03 Feb 2026 03:22:58 GMT  
		Size: 2.7 MB (2680122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80a7025131f71f84ae32243e531139a3fbaf6607af7b476f5527f04b5c7631fa`  
		Last Modified: Tue, 03 Feb 2026 03:22:58 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d64916716a80df415d2c7dde0488c412f1fa9ab8cbda7bc7d06c92246c62670c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141270643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9483f7211e794e7455a502c5120b4671d449e5464a0e972a96f185cb2a78efdc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 02:08:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:08:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:08:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:08:17 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 02:08:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 02:08:17 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:08:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 02:08:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 02:08:31 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 02:08:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 02:08:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:08:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:08:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36d081cf3e2fecad5e60b4ae649fedd0d2b222796021f7069d368ea0262ac6e`  
		Last Modified: Fri, 16 Jan 2026 02:08:52 GMT  
		Size: 91.1 MB (91052479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fa051b5605a8b4b69738e7e0166f9ba829b311baf60f03f0164e2a03560e84`  
		Last Modified: Fri, 16 Jan 2026 02:08:50 GMT  
		Size: 17.6 MB (17592093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ca6c3b03cd668d7bb1d0616292d02d470470d809810b99ac00b07f4f2f31e7`  
		Last Modified: Fri, 16 Jan 2026 02:08:50 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171772e3075047015cb5c9ec0d1e3debbd24dd0ec1317506dc757abb8fcb8824`  
		Last Modified: Fri, 16 Jan 2026 02:08:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e8fa0bb7d12c210bd17ad878870a53ba01c1614781321e3de469068dd4bb712d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5daac36cea5aaa45bcd5b6efc36e52094b585be559dba9af0f89873a7d357c`

```dockerfile
```

-	Layers:
	-	`sha256:f606571c08fec2a42772a474089c4b51e9c7986c7e6528ea2b2ec6efc2958dd2`  
		Last Modified: Fri, 16 Jan 2026 02:08:49 GMT  
		Size: 2.7 MB (2679758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13a385ba9a2386547217df77e0888d0ea969f1a36351179d42dd061ce90fadda`  
		Last Modified: Fri, 16 Jan 2026 02:08:49 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:328bec1055aacb00459745b9ee6fad82377e5759caf41a9f96c9091706eee83a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146158381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6b93cb00f694876d45f01f49d0c725d9360044e9e442d79f1bd0044460de42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 03:42:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:42:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:42:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:42:30 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 03:42:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 03:42:31 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:43:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 03:43:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 03:43:27 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 03:43:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:43:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:43:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:43:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:03 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3b35e93b96e6ec97e655f2b0ad366e3b2cfef00f6563db06ed66b91aa30cf4`  
		Last Modified: Fri, 16 Jan 2026 03:44:17 GMT  
		Size: 91.6 MB (91610755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfc42b6a0171c70fe6556b28243e4d819cffb2b8ca83caa8ecd7c66b801c622`  
		Last Modified: Fri, 16 Jan 2026 03:44:13 GMT  
		Size: 18.0 MB (17960731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e8309fb5adeecdfc0547095bf708ec7ad24fa1d8d8d30c4a9e4c60b22734b7`  
		Last Modified: Fri, 16 Jan 2026 03:44:12 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80fbe9ba9a4d9708490d42d5c4441f91046f032d2c8dd3feee90311063ac047`  
		Last Modified: Fri, 16 Jan 2026 03:44:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7565e2cf75c11ab2827e4e4f4ae19ebefef95191ea0e65f7f6bb8c592c11e094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2702379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d05022736da6d0f55e98cff37e5f38a73a014eb351fa86bbd7cc521d4ab04ab`

```dockerfile
```

-	Layers:
	-	`sha256:dabffd47e903ca7946cfcc0ff815e900816e8f9a7738ba5b0063c6d2dd876f4c`  
		Last Modified: Fri, 16 Jan 2026 03:44:12 GMT  
		Size: 2.7 MB (2683265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68861a8f7d5e4b41739b13f2dd018bc43dca1f6162106ee0fcc5c848f56a5afa`  
		Last Modified: Fri, 16 Jan 2026 03:44:12 GMT  
		Size: 19.1 KB (19114 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ecdcb88c6e3d81c2b1133a10d4eeb27b2f0e551249529cd1f40353cc6689a994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137033986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8394d2ec56ef879b89fd4b948a59e478160579ef6b7c5c563be04eaa7f09addb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:21:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:21:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:21:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:21:50 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:21:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:21:50 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:22:00 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 15 Jan 2026 23:22:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Jan 2026 23:22:00 GMT
ENV LEIN_ROOT=1
# Thu, 15 Jan 2026 23:22:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 15 Jan 2026 23:22:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:22:02 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:22:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:08 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1410d0213b1f16b5eccb65857935df6be807f0646e4bd0d5835726aed96ddb31`  
		Last Modified: Thu, 15 Jan 2026 23:22:27 GMT  
		Size: 88.2 MB (88210681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32717a24cea4e7fc653f7a6781a779b620a195f26576b4dbe3f6ea1e191840d7`  
		Last Modified: Thu, 15 Jan 2026 23:22:26 GMT  
		Size: 17.4 MB (17420745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d623b1f0397247e8cd81322b11fecf7cbd8207a9cdff980724af45a9a11208`  
		Last Modified: Thu, 15 Jan 2026 23:22:25 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296161ca4e05af37a3eb2f72e0696c5b7c1966b5aca0477637552c0c2dd9872b`  
		Last Modified: Thu, 15 Jan 2026 23:22:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f7c9a71a91a2d3d6bc1e162ec16060d7fe8a666d94aa15bba01bd80cefbc5aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3a4629b1f1eea7c6bd4f2956af48324145ceeb7c46bc47cceecd092b7e0ef8`

```dockerfile
```

-	Layers:
	-	`sha256:b98c3d480fbc75af34c33dd09b3ff2a497f370bd1aff11b0dda12f37de92a6c7`  
		Last Modified: Thu, 15 Jan 2026 23:22:25 GMT  
		Size: 2.7 MB (2674484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31e098b93984d198c8016a34cc4d8f55c904323db2719a41886c4782a62a8c27`  
		Last Modified: Thu, 15 Jan 2026 23:22:25 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json
