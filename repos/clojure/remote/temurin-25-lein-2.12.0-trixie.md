## `clojure:temurin-25-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:566779b8dd267eec2c95d2fb8e2e59d12a5b75797a6f94ded6f3e6ec62e84ffc
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

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:64115677c98c0cee5b5796ffc7f58f0297083e3911d60ee9def6ebcd88ba5084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164992749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5d9424518c6a010c4a80f0117496534ce74a4208c23633c97b5a0dd6e43011`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:00:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:00:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:00:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:00:47 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:00:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:00:47 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:01:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:01:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:01:03 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:01:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:01:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:01:05 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:01:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d24d871fc8bf96d43663799f4f296f97196700667aa90a933fbe208a0b5a84`  
		Last Modified: Wed, 20 May 2026 00:01:37 GMT  
		Size: 92.6 MB (92574574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e0d1a2150d8b54cd50e5d78c93247239ce9e9b1d7bc0cd2d3b0e307f8ee177`  
		Last Modified: Wed, 20 May 2026 00:01:35 GMT  
		Size: 18.6 MB (18589412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44b307d0a6bd49704baa7b2e0a39ab28ac9ac1489d56b3ee27266e3e4420b85`  
		Last Modified: Wed, 20 May 2026 00:01:35 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22684ed83e7dbd72a7676699ca67bfeb68fb2fc6b18e48aa69324a12ef2fe391`  
		Last Modified: Wed, 20 May 2026 00:01:34 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:42bbc07d04c2d0c349ee042abf0166d4ef7a36652f9f948bdbeb5f37976cc54a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b352377784b637e10972c157b9e6bde3257ef4c2236ea771a105bc670f16e073`

```dockerfile
```

-	Layers:
	-	`sha256:49478dad5c668627d4571f8d28d589bef783d85227b4647f9abd26095bad31e4`  
		Last Modified: Wed, 20 May 2026 00:01:35 GMT  
		Size: 3.8 MB (3784224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2beb86fc370b1d264e9cb5bf02edb91058b5a14f51ef1477cf98111e7004e6a4`  
		Last Modified: Wed, 20 May 2026 00:01:34 GMT  
		Size: 19.1 KB (19132 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8c84f6360d8294313d5c6f616c3c5ac2c06120775bc3014ad3c76b2612f90884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164280079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cda97af24d2d9e783f708002c1f47bbb74d9d7a633cf7b80be3d7972c411828`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:08:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:08:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:08:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:08:02 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:08:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:08:02 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:08:17 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:08:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:08:17 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:08:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:08:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:08:19 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:08:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f5f0158da6c1e07ce4cfe2f77b744223c4693b467d6de9945a7aa64bfac6a2`  
		Last Modified: Wed, 20 May 2026 00:08:38 GMT  
		Size: 91.5 MB (91542245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b6b1a6c4ccf0272d0fa72fb7ce80009f21d99bab842786734cae42aad594f`  
		Last Modified: Wed, 20 May 2026 00:08:36 GMT  
		Size: 18.5 MB (18547429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edec91048558f68e59c58101f30cab7586c8d92cf46dbca55d96e3267222285`  
		Last Modified: Wed, 20 May 2026 00:08:36 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fa38b9b1da5f7006331de3a689d00e98ba0a3775c5b4816fd33be1a4a54611`  
		Last Modified: Wed, 20 May 2026 00:08:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7f3f560b074dba5246ebb33d9d198cca6d80aee254dc308db23c22ecac2a077e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ff420a06a86e12a68177d62c355867306c7aebd9533ed53060e3e6e1b51911`

```dockerfile
```

-	Layers:
	-	`sha256:9f89a3112ec77025749b125cc77ae02ce265a02f5791a0d1b77bc39ac7fb581b`  
		Last Modified: Wed, 20 May 2026 00:08:36 GMT  
		Size: 3.8 MB (3784485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2bfae8a2dbb3921ec69c85f1acb250ed03c695ddd7a982dcbfe77c3daf19954`  
		Last Modified: Wed, 20 May 2026 00:08:35 GMT  
		Size: 19.3 KB (19278 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; ppc64le

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

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

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

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; s390x

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

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

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
