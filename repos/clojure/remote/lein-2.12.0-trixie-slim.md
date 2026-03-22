## `clojure:lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:4f6280a6cfb772c5a6092e7e77d05a7ac61a50fbbbbdac9ee0ec09294402aeef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:827c1e177795bc9bb4ef5d39ecb95450f56598e09a6bd0957de11a704aeff82b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (142998035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b0df7d774eb9d3f54e44e9c8d80d5f327f92c1d4af8df2f323cce0012afdac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:01:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:01:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:01:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:01:11 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:01:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:01:11 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:01:29 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:01:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:01:29 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:01:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:01:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:01:31 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:01:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2db9b55987c8b20ff7a0c9a02f422557cc8f8e2c5ff3bcc2d9d916276ae0d8c`  
		Last Modified: Tue, 17 Mar 2026 03:01:51 GMT  
		Size: 92.3 MB (92256328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82039fd364019cff6d8ec1b2231ca961210fa5a1436f77686e41d13873e67fa8`  
		Last Modified: Tue, 17 Mar 2026 03:01:49 GMT  
		Size: 16.4 MB (16448061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5231cfd87361f1851e025ecfc00f4ca72c6c0de47b1447907bac91e27781c46`  
		Last Modified: Tue, 17 Mar 2026 03:01:48 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba28eb741d7c91ab8900af845cbd08ffcc3f400a9e294626c1f0e6ec3f4af3`  
		Last Modified: Tue, 17 Mar 2026 03:01:48 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4d307dc6f52e917cc90b796db9c7b3235d9a3dbe235afe7ddd8826e0db1f7238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2351874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750ca2b50a93fcead5f54af4b50f05e234cf63f9949d158a9802ffd3d1f41476`

```dockerfile
```

-	Layers:
	-	`sha256:a6607a30d213e089367cf1080e15e2b5b1aa653c687576f6101736561a071ed5`  
		Last Modified: Tue, 17 Mar 2026 03:01:48 GMT  
		Size: 2.3 MB (2332840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:505faa4f5bb29dd4d0233fceca106145fb4349203c4fb6829672445f045f76d6`  
		Last Modified: Tue, 17 Mar 2026 03:01:48 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7e624cab703bb456047cf8ab2c7486917ed7daa1a6825d96a49786b7de324e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142358879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c7b0a2d03cf0379abb55cbcc2abf7627063bd820fd3672ba68ee7a45bf49a2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:05:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:05:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:05:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:05:30 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:05:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:05:30 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:05:48 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:05:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:05:48 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:05:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:05:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:05:50 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:05:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeae329513ba2056ab9833802db15281e988afba41cfe0447418f7f93d26491`  
		Last Modified: Tue, 17 Mar 2026 03:06:09 GMT  
		Size: 91.3 MB (91288273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23de0546b3a99195b47d2760199b59c1fdbb09ac27e4c18a879a647f0668683c`  
		Last Modified: Tue, 17 Mar 2026 03:06:06 GMT  
		Size: 16.4 MB (16414024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9f4813372dbf525eb9f3fee0b2044c45f05aa3ae454377f5dfc10d79c34f34`  
		Last Modified: Tue, 17 Mar 2026 03:06:06 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece7bd89d24f2616a8475dfb85f33ee2b8ede0c3bf6f325d0ad9aae4834db65e`  
		Last Modified: Tue, 17 Mar 2026 03:06:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a2c73e137422e2535e7ea3a40f04718c5b60a30e04401dce1b7eb391486ac71b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2351658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:287b87cc90740e5636706a7b18ffc5f6fd53e84e31c5a7fe5a44fcc3f253bf5f`

```dockerfile
```

-	Layers:
	-	`sha256:14208d3f84548664f28cecb44e16a3450ab11ddb9f5a842c896dbba58ed7df7e`  
		Last Modified: Tue, 17 Mar 2026 03:06:06 GMT  
		Size: 2.3 MB (2332479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aa66a96ec1247fd79801f4c7e64ffb4b64f8e9e1428fbb35938e57621dbc947`  
		Last Modified: Tue, 17 Mar 2026 03:06:05 GMT  
		Size: 19.2 KB (19179 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:41277915c85e519288c0ab9c7ecc6d68f6fa8bdc85e06a17a0eb5329d85094ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146229286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5ed5db79ccd939d16b908c5409f546ca024307fb744b11f95f02aca0b836bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:46:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:46:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:46:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:46:17 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 18:46:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 18:46:18 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:46:55 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:46:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:46:55 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:46:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:46:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:46:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:46:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210f0f2228872d076d4a64e5b33affbf6841048c0c771e1ab74cea434ead7212`  
		Last Modified: Tue, 17 Mar 2026 18:47:33 GMT  
		Size: 91.6 MB (91632916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2f377d15cbed8e5d5df61fc68245d179a37bca02c22c72b45ab827ec705c74`  
		Last Modified: Tue, 17 Mar 2026 18:47:31 GMT  
		Size: 16.5 MB (16485353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a81e11d1305abbb39205bc724614bf089b437850a3200f4abbb6b28f6ff3ee`  
		Last Modified: Tue, 17 Mar 2026 18:47:30 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33caa070e3d1da66ee4571a60b4f66cbdd29eea006fa51737e83d16da1a20b1d`  
		Last Modified: Tue, 17 Mar 2026 18:47:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:da0aeec959a96b884750cea9b6de4206e4a9c09d04cb0de34d07ddc11473ef22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b01386daa9668c72d869283921fd0cb4bed508692550629f9a1ba9b240486e`

```dockerfile
```

-	Layers:
	-	`sha256:6a844435ab7103d7870ff6db52cbb036a4d475ce21406c75b2fef13c60a1b262`  
		Last Modified: Tue, 17 Mar 2026 18:47:30 GMT  
		Size: 2.3 MB (2317144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:856dceefe4b2ef668b3baa199a16d0532918a9cea3937a1834008fac2d8505f2`  
		Last Modified: Tue, 17 Mar 2026 18:47:30 GMT  
		Size: 19.1 KB (19089 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:14ccddcb594f39b73ed40ff6cdc2282afb82d0be5c8072a49b95a7cf396c0a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139965463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d9b275a700ff2aed2144da6facfc127fc49e265e048b3753ba26589d12a1b0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Sun, 22 Mar 2026 19:34:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Mar 2026 19:34:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 22 Mar 2026 19:34:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Mar 2026 19:34:05 GMT
ENV LEIN_VERSION=2.12.0
# Sun, 22 Mar 2026 19:34:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sun, 22 Mar 2026 19:34:05 GMT
WORKDIR /tmp
# Sun, 22 Mar 2026 19:35:38 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sun, 22 Mar 2026 19:35:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sun, 22 Mar 2026 19:35:38 GMT
ENV LEIN_ROOT=1
# Sun, 22 Mar 2026 19:35:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sun, 22 Mar 2026 19:35:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 22 Mar 2026 19:35:54 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 22 Mar 2026 19:35:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0b5164900a4737bd8c71921f9d6095f2a9499d5081755c56a4aa46d8f37e9865`  
		Last Modified: Mon, 16 Mar 2026 22:10:41 GMT  
		Size: 28.3 MB (28275636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18130382227055943bc69d00df6af55a8fd9d543ffadeb9c5060d81d2d5b4bfa`  
		Last Modified: Sun, 22 Mar 2026 19:39:25 GMT  
		Size: 90.8 MB (90773437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2028c8e6fc011e77710120cefa1a98052ddc93d20dc25da2809b9918bb16b64f`  
		Last Modified: Sun, 22 Mar 2026 19:39:13 GMT  
		Size: 16.4 MB (16398172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41aae351c671748355fcdddc8f2f62b879745872696e5d71cbaa8f3622a7de1`  
		Last Modified: Sun, 22 Mar 2026 19:39:10 GMT  
		Size: 4.5 MB (4517789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb29e433e622e72a0d5cee10404e91ce919f078ad03a9edc59790112957dd6`  
		Last Modified: Sun, 22 Mar 2026 19:39:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1fcb2d39f44508e533d65d74006de605ce8a9767705d862ee31f7fae6fc074d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2326000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1cf905d9a19944273760bcbc0643b28bbd756f9b0a40f0a13d74319003d3ab`

```dockerfile
```

-	Layers:
	-	`sha256:589f25123532543e6603db61fa4eeab1b12328aaab6d3919fdbc83061ca42b0a`  
		Last Modified: Sun, 22 Mar 2026 19:39:10 GMT  
		Size: 2.3 MB (2306911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e74a7764800dac3ea8d14143f36821e53be591aeb679bcd0536e7b98785028e0`  
		Last Modified: Sun, 22 Mar 2026 19:39:08 GMT  
		Size: 19.1 KB (19089 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:aa1af5af2b81a5ca540365de289e8b4c8d3e18772011aeb796699759fdb27ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139071236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09459e5575da8b282427149c7dcddd350a0b1e3526a84b8a183a8b60bf8892c9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 11:44:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:44:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:44:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:44:36 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 11:44:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 11:44:36 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:45:17 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 11:45:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 11:45:17 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 11:45:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 11:45:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:45:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:45:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb62fc097eaac184da503b941c60f97ec5e455a5301ecef6716aa9c41ac21b33`  
		Last Modified: Tue, 17 Mar 2026 11:46:01 GMT  
		Size: 88.2 MB (88233795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd976f29fb71af1884527d52d956299bc3396574700a911da1ba87a7ee57b4`  
		Last Modified: Tue, 17 Mar 2026 11:45:59 GMT  
		Size: 16.5 MB (16484007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170417c1688b1d4e0c0815dd5bcc640b7fb65012cee3e237d1cc852c8540bcb8`  
		Last Modified: Tue, 17 Mar 2026 11:45:58 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3971fb34765dc8b3615bd7627a187f50fe80a775b4752a731d3f38b6b7d641`  
		Last Modified: Tue, 17 Mar 2026 11:45:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:18f9b102a0fed949fcbde9abbdf53b55754026eced723b4fb390f6562e7e23c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2332863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4f05de4b73030ff163aff95160d4783b2ecac4942aee88d0d6c53ce1ea7efe`

```dockerfile
```

-	Layers:
	-	`sha256:6cfee29e9e91f09f94d73481f8641446a8ab9aa1cfec610b81b406093bafd162`  
		Last Modified: Tue, 17 Mar 2026 11:45:58 GMT  
		Size: 2.3 MB (2313829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2c8fa69e6b39fb361073db53b6e513985c4575e4062ba6dea5e713ead8901da`  
		Last Modified: Tue, 17 Mar 2026 11:45:57 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json
