## `clojure:temurin-26-lein-trixie-slim`

```console
$ docker pull clojure@sha256:4931bc7ad4acbd42d6bf17037ecbe25492803282c5e52dcd38dc05586e8d218a
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

### `clojure:temurin-26-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f95c6c06d4891bf1996d0897b5e8269f50387d3a5ecf669375f9eae8e381f6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145202047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452a668f00d7ef676821bbf405ed857c9868627d3cbac39c59dd7508730de6ad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:21:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:48 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:21:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:21:48 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:02 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:22:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:22:02 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:22:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:22:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a45704b26ca05e732d6744b57a78e687b0cd8b3ca952c60e465dc2be0935d9e`  
		Last Modified: Wed, 22 Apr 2026 02:22:22 GMT  
		Size: 94.5 MB (94455697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf993fa3f4a0001f9e06e7e60f51c51b8d964b8e3a96e0edde7062088e7b8e4`  
		Last Modified: Wed, 22 Apr 2026 02:22:20 GMT  
		Size: 16.4 MB (16448016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d21e035fb9f46605bc3670e30fb89ebdb1fe78c6f0f5a4af6edb6a2e51a250`  
		Last Modified: Wed, 22 Apr 2026 02:22:19 GMT  
		Size: 4.5 MB (4517731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de993dedd434faacee782f8dfe0a81dea594377abcaf70fd8679653f5c820304`  
		Last Modified: Wed, 22 Apr 2026 02:22:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8b0a73ae9c168eea016999dc3951da2e08db0e350d068d4e8adf4ee86f89cd4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2348672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34ab558c77db81b2dfce9144d55e29cf08f93a5366ec54356723ef13ae4a75a`

```dockerfile
```

-	Layers:
	-	`sha256:5b90aa433ef537ac74aa6832662cec0bcd03377a9354636bc200c8bef1c00b8f`  
		Last Modified: Wed, 22 Apr 2026 02:22:19 GMT  
		Size: 2.3 MB (2330292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c8e531c17296c6cee268dc82baf0aa30e28fa6c679543b710430afb4fd08696`  
		Last Modified: Wed, 22 Apr 2026 02:22:19 GMT  
		Size: 18.4 KB (18380 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2ffe4d79c788462189b7a9356e5f9de7a8d29b61ce63c520efe246df6ebd28e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144470881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beaf21909ab7b0febae310b924ec691069dcf7a81e6a6d6068deef332eaa868d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:24:54 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:24:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:24:54 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:25:11 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:25:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:25:11 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:25:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:25:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:25:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:25:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158a2817c61e7c1e7df62a2e5f22d279e02c4d2cc07cf8871dfa4f89f31757d6`  
		Last Modified: Wed, 22 Apr 2026 02:25:31 GMT  
		Size: 93.4 MB (93395201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15e9a0b7c13bb02590e0ef77d158ad61f303f4c5dfab87a7f522ed20c82655f`  
		Last Modified: Wed, 22 Apr 2026 02:25:29 GMT  
		Size: 16.4 MB (16413956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093c8dc02255f02abf6990b45fe1a8a7ce14a1adb78f2c16f021ad399cd7ad09`  
		Last Modified: Wed, 22 Apr 2026 02:25:29 GMT  
		Size: 4.5 MB (4517691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4958af48176da23efbf8281467ec68e9a6c2897d5c0021fdd119f45c1750941c`  
		Last Modified: Wed, 22 Apr 2026 02:25:28 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bee9002433db1903f71ea65556a5bdc1a4fcc969875715fe0ef57b6b7ead6f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2348408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50089b8eca6c04194e829247c0ee1f1f78610c1715009424cd846b4455d9bbd6`

```dockerfile
```

-	Layers:
	-	`sha256:cc60165058859cebc143a1b8f71bdb054876b1e616ddefe1487654606bfd0196`  
		Last Modified: Wed, 22 Apr 2026 02:25:29 GMT  
		Size: 2.3 MB (2329907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b67e53b0bced4a01ea09b2549171480a634156a35386e22b794b9ebbf7f4f05d`  
		Last Modified: Wed, 22 Apr 2026 02:25:28 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d60d7ef221fa882a39b4bc6ce081a64f07e81d04f6ffb1764f82ade64f808522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148382992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6257e81e663fe057be208b10405cd6bf21dd2aadd672adc90022dce648f3dcc2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:52:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:52:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:52:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:52:30 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 08:52:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 08:52:31 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:53:03 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 08:53:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 08:53:03 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 08:53:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 08:53:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 08:53:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 08:53:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e771730505306c65b920a33ea03d87b316b140e1fe4d13ec6a98c1278d920c3a`  
		Last Modified: Wed, 22 Apr 2026 08:53:41 GMT  
		Size: 93.8 MB (93781494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70882fdb2e099b41e0b4a582d98ec6c1db5455f1bd7e9212946596a4e4b74230`  
		Last Modified: Wed, 22 Apr 2026 08:53:39 GMT  
		Size: 16.5 MB (16485326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9819a938c9bd7b2a5bbcb17f61e0c4a46f78bbef8a1e39aa4f0772807cd953`  
		Last Modified: Wed, 22 Apr 2026 08:53:39 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcca2714f58cb10fcfbd111af384e2e5530e845bc90f559199f9d272dbba045`  
		Last Modified: Wed, 22 Apr 2026 08:53:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cf12d646d763f1b1d19fa05046fefddd904b8297dd743d2659fc7501af3b8cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4dc48ad69862b09ab1e148bf8fbd7a75d79a9c186e400ee0052d545d220794b`

```dockerfile
```

-	Layers:
	-	`sha256:e8a54ea82529ced9e1401d86c7508244bd375b14436b9a6cfbcc6f7ea3176ecf`  
		Last Modified: Wed, 22 Apr 2026 08:53:38 GMT  
		Size: 2.3 MB (2315208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13c312c7d6dc583a799c2f0127f6a00440cbc400639dfd5fa2b6c2057fcb6a70`  
		Last Modified: Wed, 22 Apr 2026 08:53:38 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:060f4fcfeb21d4e2d0ee854841c802cc9d1e61c5b6fce9cff9785748b81d5c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144820161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476d4762802700c1947f3bc1984c2d225e761688306c1cb19be0d167cecbc60e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sun, 12 Apr 2026 18:55:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 12 Apr 2026 18:55:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 12 Apr 2026 18:55:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 12 Apr 2026 18:55:33 GMT
ENV LEIN_VERSION=2.12.0
# Sun, 12 Apr 2026 18:55:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 18 Apr 2026 05:58:19 GMT
WORKDIR /tmp
# Sat, 18 Apr 2026 05:59:53 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 18 Apr 2026 05:59:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 18 Apr 2026 05:59:53 GMT
ENV LEIN_ROOT=1
# Sat, 18 Apr 2026 06:00:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 18 Apr 2026 06:00:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 18 Apr 2026 06:00:10 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 18 Apr 2026 06:00:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7fc246f5e32984af9b4236c90104244f3679fa7192854d7e61221c59edbfc2c`  
		Last Modified: Sun, 12 Apr 2026 19:01:08 GMT  
		Size: 93.0 MB (93008131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc28cb33cb7a7eefcc013f41eaf996cdcc65c65b43cee38c16eff1e37e97ac5c`  
		Last Modified: Sat, 18 Apr 2026 06:02:05 GMT  
		Size: 19.0 MB (19018040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fb8f4bfa51e3cfb690879cb983e4bcde926575bfb034ac525b27653a3f40cd`  
		Last Modified: Sat, 18 Apr 2026 06:02:03 GMT  
		Size: 4.5 MB (4517783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095fc2b5519a2fc089038af1c26c56f0684f016e0516b5fc436f17aa90910db2`  
		Last Modified: Sat, 18 Apr 2026 06:02:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:87bd0f7bb9102437eda4fd9d9efe045be2d1c6d46bdb39ab39802117735bee8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2323399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aaa7e2ee3e946efd7b123bf13bc23a2f1b1be7a5406bc9fcfab69bc7f8dd7dc`

```dockerfile
```

-	Layers:
	-	`sha256:acd7be5ff5bc8f699bc094b74671205c7dcc693191a66827725613b7ae8ee6cf`  
		Last Modified: Sat, 18 Apr 2026 06:02:02 GMT  
		Size: 2.3 MB (2304975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2439836ca6cc6295db1cdd32728f0bb286fc9f7874413f7e2a3e45aac57f110b`  
		Last Modified: Sat, 18 Apr 2026 06:02:01 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d38d804dad6d474c2a17f3109847978bd6929f3469dfd4ef35aa689dc61dcc04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141390063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26527cdb0d42e2fd2b022ae0ea006d9eafe3d0a23856700769234c8f812a3dc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 04:07:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:07:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:07:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:07:17 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 04:07:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 04:07:17 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:07:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 04:07:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 04:07:31 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 04:07:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 04:07:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:07:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:07:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6552167c3fb921ccc494ee3bece04b6397bc0c70a2295fcbb0589332416e0edd`  
		Last Modified: Wed, 22 Apr 2026 04:07:58 GMT  
		Size: 90.5 MB (90547693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fa790cb57a6a413a1892e2adaa1bbdfc15dc75a1a3d592137befaf06ed5112`  
		Last Modified: Wed, 22 Apr 2026 04:07:56 GMT  
		Size: 16.5 MB (16483889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd510d1fc131bddfc7ca1675c6945e19322295442fdb02b074dc7f707a7581d0`  
		Last Modified: Wed, 22 Apr 2026 04:07:56 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd4aef0861e7c1ea8d43572366b8d2a69250f9648afa60d9d5fa43f875468e5`  
		Last Modified: Wed, 22 Apr 2026 04:07:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:69f58307f76b00879ab33099b5ebe5f694f9112e9f2787e056645e24b4d5ab52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3e95de42d6b4e8d760ad192f7f12e7cda95eb59b41af64173abe1c01f48a35`

```dockerfile
```

-	Layers:
	-	`sha256:c163609264565014a067422e48776b1b5a025d2f9e18db69c67f0dd9bc79e2dc`  
		Last Modified: Wed, 22 Apr 2026 04:07:56 GMT  
		Size: 2.3 MB (2311905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e1ed4c63c4642eb57b66b3673a999d043fb2911ad1267ef12839f9493fd793e`  
		Last Modified: Wed, 22 Apr 2026 04:07:56 GMT  
		Size: 18.4 KB (18380 bytes)  
		MIME: application/vnd.in-toto+json
