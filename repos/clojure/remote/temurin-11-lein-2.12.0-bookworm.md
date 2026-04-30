## `clojure:temurin-11-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:28dd2b1a1e973bdb51b627a84a7a68bf7220e4cf9dc514977687a08f2ee2627a
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

### `clojure:temurin-11-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ef93852ce888e5b245a89f774766a24b61c15debf8aefbd575c0a35858129b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218699175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd441f82b9e7120a030ebd486b4095a49c7a9f2dccfcf107a7b31fb4dde6b3e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 29 Apr 2026 23:14:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:14:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:14:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:14:30 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:14:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:14:30 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:43 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:14:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:14:43 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:14:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:14:45 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd26557bcf385edf651f173d453300d97dd3eb461339bad7bc59dab88eec6a7`  
		Last Modified: Wed, 29 Apr 2026 23:15:04 GMT  
		Size: 145.9 MB (145886252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d7279be96e0775c65b2df730b1f0f7926fd27242848f9c69f2c7ece858a1d4`  
		Last Modified: Wed, 29 Apr 2026 23:15:02 GMT  
		Size: 19.8 MB (19806507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347b8aedb469c54981a3c063052ce702cce4ded8b773bdfffd6f7aa675b2ca32`  
		Last Modified: Wed, 29 Apr 2026 23:15:01 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2248a9143f368bb7e09cd69f573a96e97913f08f44a9b73b393c233cfe042252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4318256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f26bd1801d1dab46efac8e95dffb410a5d69cefade485f6c8f74618203c95c`

```dockerfile
```

-	Layers:
	-	`sha256:97ac6981c6fa629359d0ad6047f21ebebcd24382d4d16bc608b87871014c6a39`  
		Last Modified: Wed, 29 Apr 2026 23:15:01 GMT  
		Size: 4.3 MB (4301874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e044625bc76c4fad537af2740d91230e346e24d6988cdebea63c22a534e5427f`  
		Last Modified: Wed, 29 Apr 2026 23:15:01 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3c5e30d964b8b2f95062a1ea3255566e67158ea78908755ca9e62f65f6c1c408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.1 MB (215111799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b92df7870b05e347a208da33a24a41da31ce469177282bbe71c428efaca6de3`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 29 Apr 2026 23:13:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:13:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:13:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:13:36 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:13:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:13:36 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:13:50 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:13:50 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:13:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:13:52 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42b428d2d08ef94d02561ec304d09c1953cad0fa2c429f7f66788af9141ef30`  
		Last Modified: Wed, 29 Apr 2026 23:14:13 GMT  
		Size: 142.6 MB (142583978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622dcc7f598467e9120f9358d15fcc8d3967459105e0bc4f88ca0ccd4e4fc94`  
		Last Modified: Wed, 29 Apr 2026 23:14:10 GMT  
		Size: 19.6 MB (19636970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6c8bb6176bafea48a2228ab8495d9dafa42f88b332a56f5a37c5774936a884`  
		Last Modified: Wed, 29 Apr 2026 23:14:10 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a27550945d25799a3a250155bbd5a2e4ca21ca542a6917c7b8fdad01c489a50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4318610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6c5b42978fc9d8b604934355de7fe67b9ec7bcdb1ea0c22711e16805b40223`

```dockerfile
```

-	Layers:
	-	`sha256:5e37e2895f6eac72a52812edf0524c3b05b9af24d6dfe8dbdeb218d692a8a46c`  
		Last Modified: Wed, 29 Apr 2026 23:14:10 GMT  
		Size: 4.3 MB (4302107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c2893baca700be24da50b99a2326057cd51123bb2cc94659fd534d952cc1092`  
		Last Modified: Wed, 29 Apr 2026 23:14:09 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:1d089948ced20cf3d8c6ee5e4e59e90378dc43b6c4ac1b615df62f79d221c560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (209994654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2e372a23a86e2acc1e801632a8d95db2eee44b43d3eac4d95e8738bdb32b9e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 29 Apr 2026 23:23:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:23:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:23:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:23:09 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:23:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:23:10 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:23:50 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:23:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:23:50 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:23:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:23:56 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237ef4f7556b579838f856974008ca10a74407a11bb8a3d8ee66e54d2f440d6d`  
		Last Modified: Wed, 29 Apr 2026 23:24:49 GMT  
		Size: 133.1 MB (133109625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537274260f2f7519b72fc4fe74aa741a6d053ed68c49c49ff8da40708d10862e`  
		Last Modified: Wed, 29 Apr 2026 23:24:46 GMT  
		Size: 20.0 MB (20030504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eaba4d187484717187b5199fc70207d49da08dd776a2adcc4d91458169138dd`  
		Last Modified: Wed, 29 Apr 2026 23:24:45 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:74e161f95f9abdc62764857e03c7588ba537405a6c6829eb5c8fab85584645c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cc47079925a5cbdbffc91e1850326520d4a36406c65c0b1cb84bd08e247ad6`

```dockerfile
```

-	Layers:
	-	`sha256:871ce0f911d94db7e570c4c081ca36181ff628bd94e09eea7864d164c9f5167f`  
		Last Modified: Wed, 29 Apr 2026 23:24:45 GMT  
		Size: 4.3 MB (4303120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78334c9661f015ecc8984a41ab4f237ff463b335ea10d2c2b8d7919e71d829d5`  
		Last Modified: Wed, 29 Apr 2026 23:24:45 GMT  
		Size: 16.4 KB (16426 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:2ef1936fe922c4bceda29ecd7e85590aed9c4dce3c1e7189a9f212981cb7b3dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 MB (197785226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7674248285f423397a1c8ab0b00e4c58284e48646ee3f28d6579cf294531bf1f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 29 Apr 2026 23:12:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:12:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:12:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:12:54 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:12:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:12:54 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:13:06 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:13:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:13:06 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:13:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:13:09 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9877cfa317cb3a147f3af298dc6f97e96426f3a35ab1d50968ae58d675a805f9`  
		Last Modified: Wed, 29 Apr 2026 23:13:35 GMT  
		Size: 126.7 MB (126652695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dc324b5d56acff9577f3fe9d30cd5aaff0696920895572f609945290c5e955`  
		Last Modified: Wed, 29 Apr 2026 23:13:33 GMT  
		Size: 19.5 MB (19466783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8811dcedee0cce1b8a52a4f6234486e26e95e053b118f8800184bc726c9345a`  
		Last Modified: Wed, 29 Apr 2026 23:13:33 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6e1496c697484566b55f53bbc79f040aa691e3fa48dcfbf192359874d068e7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4310074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8300e8b11f1ca1145c159b4148291a39cb3eaf904d810fcd654c15813ae78747`

```dockerfile
```

-	Layers:
	-	`sha256:aa25aec1efc78a4b35edee1bfaf4a52cb01db404086793a18445407059ee3c61`  
		Last Modified: Wed, 29 Apr 2026 23:13:33 GMT  
		Size: 4.3 MB (4293692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33872a983cd9c762b527657e25cabc249ce64d7c4cfa86f89da393c47417ba02`  
		Last Modified: Wed, 29 Apr 2026 23:13:33 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json
