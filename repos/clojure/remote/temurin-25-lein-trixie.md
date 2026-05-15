## `clojure:temurin-25-lein-trixie`

```console
$ docker pull clojure@sha256:d0f8d89ea5f46624922fba929ea258644f1b75d05fa6381c0ea91ed3826e932f
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

### `clojure:temurin-25-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:93a6619c1beb14f4cac88190ab44cc1d6d745abf2c27bb13aa87da9b224acf2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164980594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a0562bfaaef801630626a10e4cf1238f986021d2d709ca519483de7d1bd483`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:19:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:19:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:19:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:19:17 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:19:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:19:17 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:33 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:19:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:19:33 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:19:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:19:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:19:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:19:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe29d8d7873e11f75edaacb59da63bf713ab8d7c140a334ba91fdd9b4abb25b`  
		Last Modified: Fri, 08 May 2026 20:19:55 GMT  
		Size: 92.6 MB (92574588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc02ff1241751bb6b6d2eda87521f7c3ac4d4a33a1f9d7adba52cbd474143686`  
		Last Modified: Fri, 08 May 2026 20:19:53 GMT  
		Size: 18.6 MB (18585541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ba20a5be5db1944c780fdea658098a8c4cdaad23532a1c5908b7afeb0469e6`  
		Last Modified: Fri, 08 May 2026 20:19:52 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4544b716fb67ffe0e70ca6ab7e7653bae47416af2bc8edb8a1c6f39ce9055d98`  
		Last Modified: Fri, 08 May 2026 20:19:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6043cfe682bb47a7c473c26067f04db29a3e8fbcf4ac545d1d0712749ed7b477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978e33bcc653a936ef47dcc70f22951b69cfa888324c712dbab8acd65bf83331`

```dockerfile
```

-	Layers:
	-	`sha256:7824c5d63d89d62b767ccb57e9e1cd1724104613f5bb94ffd75a3a2786d14f26`  
		Last Modified: Fri, 08 May 2026 20:19:52 GMT  
		Size: 3.8 MB (3784182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11bf833fee6bd87ad5661f67f937ce5e8113fc485226011a07d1ad90037398ae`  
		Last Modified: Fri, 08 May 2026 20:19:52 GMT  
		Size: 19.1 KB (19132 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ab111993276685b0211f274531bfe3ed10a9e56df68f7f5a390a158b98728ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164275376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d7537cb60d51c2f87f9fd7ca1d950ce499eb6db42989b69ff129d485cda9544`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:23:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:23:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:23:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:23:22 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:23:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:23:22 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:23:38 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:23:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:23:38 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:23:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:23:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:23:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:23:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b818ed24ce5a487fdf4cf17cc0112019c18201d4da6249b92b9f7b5cb39282`  
		Last Modified: Fri, 08 May 2026 20:23:59 GMT  
		Size: 91.5 MB (91542245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db2b006acb08b53bf736aa643f664c62ca02c826b583ca96f1f9fa9853c3ad1`  
		Last Modified: Fri, 08 May 2026 20:23:57 GMT  
		Size: 18.5 MB (18545533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7452882be6388e6f11e952461d577f7d8c6f74a175ae76010e4355574c05b8e`  
		Last Modified: Fri, 08 May 2026 20:23:57 GMT  
		Size: 4.5 MB (4517724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cd92f1e26217cbaa66698ed2de0cdc7ba4dc542e08e8135f5017c33586dbf2`  
		Last Modified: Fri, 08 May 2026 20:23:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ef7bef57cb4c31b0c10e72aee0fe78ac6c7aa73db0a245d975f2f9f0f8c7adcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3804358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765749ed681734ab287d8ec5c8e05b5fe90b24f2e6b47cf21b82f82738071c45`

```dockerfile
```

-	Layers:
	-	`sha256:7149a70686a65681cfd73d4cba5cb92d422d0687352f638c9152e749e921aa2f`  
		Last Modified: Fri, 08 May 2026 20:23:57 GMT  
		Size: 3.8 MB (3785080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcd8b583b6c2783a2446e969edf895a8111edf41a21a92c19c11c992a1f0159`  
		Last Modified: Fri, 08 May 2026 20:23:56 GMT  
		Size: 19.3 KB (19278 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d151b62e6d90e0e5a3038e312873b835381d723cd236d27edfbb74d0415adb6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.2 MB (168196415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6dcbb2fd21f017a6b04ecb5011eaa686924fe93b731e97356ac60211c53918`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:42:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:42:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:42:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:42:40 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 09 May 2026 02:42:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 09 May 2026 02:42:40 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:43:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 09 May 2026 02:43:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 May 2026 02:43:14 GMT
ENV LEIN_ROOT=1
# Sat, 09 May 2026 02:43:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 09 May 2026 02:43:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:43:18 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:43:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2325345b811e94f6ff3ccd6a646a97c3cc4365dd97daee1fdfcb79b03cec8cfc`  
		Last Modified: Sat, 09 May 2026 02:43:51 GMT  
		Size: 91.9 MB (91914029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98aef2466aad75ffbe921f2435a872374e52df3453679c1d2f38b09de72706dd`  
		Last Modified: Sat, 09 May 2026 02:43:49 GMT  
		Size: 18.6 MB (18641066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c975f85023f978bb164a1f6e6ddbe73b5e82668e80b57a7aec93d64e1a111d3d`  
		Last Modified: Sat, 09 May 2026 02:43:48 GMT  
		Size: 4.5 MB (4517726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff19bbff073692a7f5595b1925b09635c23e2d66dc8eb71637ec1b8ffa742c0`  
		Last Modified: Sat, 09 May 2026 02:43:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:513dd01ebe0b242fb019bc6c66bcb23c345f13318be47d81f0d57f51e070c427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3787695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257d7b924caf08c095f68bd34eec38c5e66061da6c3d00eee15f39b87f681e88`

```dockerfile
```

-	Layers:
	-	`sha256:4e46bb7ad763f65b0ca744166d413a73953a30d5d8c6fbda82c0dde65e178d83`  
		Last Modified: Sat, 09 May 2026 02:43:48 GMT  
		Size: 3.8 MB (3768506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ca98a5e0800333542aaba55fada4c89b8f5e09aa8e8e66c866e030dbb85d0df`  
		Last Modified: Sat, 09 May 2026 02:43:47 GMT  
		Size: 19.2 KB (19189 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:fe4c46ee3b93f7231bc239e14cc3aea915f83c92a4882ade0088993ee8d2e98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160937388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed7100b89969ea2424eca7d26bbcad6618a1bc2974fcbc922928889c46b8578`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:19:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:19:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:19:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:19:24 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:19:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:19:24 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:19:39 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:19:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:19:39 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:19:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:19:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:19:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:19:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471b7103dad7afe52bf3fd88bcc3c26d834f21822aa6fcd3d73af3c901b4545a`  
		Last Modified: Fri, 08 May 2026 22:20:06 GMT  
		Size: 88.4 MB (88420329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5800df0428d27cd242fa0c00f1f4dbe1b28024b95f36c94c5cf7652a1375e3c7`  
		Last Modified: Fri, 08 May 2026 22:20:04 GMT  
		Size: 18.6 MB (18626624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3a1183857cd2870a70fb9aa42d92529e20751d0669078e95fddb8abbdf45ba`  
		Last Modified: Fri, 08 May 2026 22:20:04 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc100201c38b4f472da6dc2cfe6a5583006b7fc92f697f651a5df5b863417080`  
		Last Modified: Fri, 08 May 2026 22:20:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ea49470f631e19c812e6495ffb1e76222409ca100fd12c08e03a469395b08612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1245445047eeb5d1a55478e16c36019957684e95442c668c10a33bf6d1b72478`

```dockerfile
```

-	Layers:
	-	`sha256:6ee44efe98145b5b28761663755280ac4ce32563db12b01d8ddff5674a1f220b`  
		Last Modified: Fri, 08 May 2026 22:20:04 GMT  
		Size: 3.8 MB (3765171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea18619d6375ce44cf2c5ce353fb63c6c2e1addf7a866e19162f7c423a7999c`  
		Last Modified: Fri, 08 May 2026 22:20:04 GMT  
		Size: 19.1 KB (19133 bytes)  
		MIME: application/vnd.in-toto+json
