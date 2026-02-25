## `clojure:temurin-17-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:7859cec12fad132381f4beee0a5cba99d2c09b45f9ac0363ab1b7fbdbf829881
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

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7305b9ef84064d3e7158593525c5de3adf7a985fa6ab78358a7ce1f253b7f529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196141882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300013298a0669769632a5362e11b3e0f8a2081a5941d1ebe086434fb5a756c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:54:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:54:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:54:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:54:35 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:54:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:54:35 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:54:49 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:54:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:54:49 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:54:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:54:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:54:50 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:54:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc6bbc0cbc4349fcf3471289b262b127fc4cccdfde6e3ded6f578901f602056`  
		Last Modified: Tue, 24 Feb 2026 19:55:09 GMT  
		Size: 145.6 MB (145628715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427a6f5c62a7fe3743ca32d87c6c9c0bd638e1d3407b713bf1387c827e18f3e5`  
		Last Modified: Tue, 24 Feb 2026 19:55:06 GMT  
		Size: 17.8 MB (17758758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4688bdbbe080f208c0be59a1ea8a14afdb522d3b445ecdbff408cbee88039ce`  
		Last Modified: Tue, 24 Feb 2026 19:55:06 GMT  
		Size: 4.5 MB (4517700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19f0fde8d050e70a3f4b8d756553d5f594508679d63297041db63084b87a750`  
		Last Modified: Tue, 24 Feb 2026 19:55:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:be02fd0cb7e2b6c05737511c55522ec44f728edbee6d7d11b1407600cabd8574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2748453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544585145381c2d2d0439e2ecf1b231f1e86a94e71001c81eb491fe0b44d08ed`

```dockerfile
```

-	Layers:
	-	`sha256:47bfeb5fd22e671bb23349b96d1e5d8ba10b05b2c001610b1c033f2c4284df56`  
		Last Modified: Tue, 24 Feb 2026 19:55:06 GMT  
		Size: 2.7 MB (2730050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d811069c7d16a12c282b45e0465270b7da458177e721edb509ed48753fc1d88a`  
		Last Modified: Tue, 24 Feb 2026 19:55:06 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0a3d576bd3fcfa6abeb4f27f9c9758ded4e82253731db2206be0c2980fbec92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194662192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9306b521ce066a665c1501fe75c3010b7fd3bc841dbd0fc01917ad364f97c90b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:05:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:05:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:05:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:05:04 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:05:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:05:04 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:05:17 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:05:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:05:17 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:05:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:05:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:05:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:05:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916efda5ec544349a54235d2b3e19c970b64655fd3df3e3dfecb21b4f3f942eb`  
		Last Modified: Tue, 24 Feb 2026 20:05:38 GMT  
		Size: 144.4 MB (144436198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c2070f51aa2864bbd27fac39a727e20b9e8c7a04656faeb5059fb9e33ce039`  
		Last Modified: Tue, 24 Feb 2026 20:05:35 GMT  
		Size: 17.6 MB (17591780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5dbafb9276d15fb53f1818ee5a924bc26fb877d06f3ee81ac6c6796e074da47`  
		Last Modified: Tue, 24 Feb 2026 20:05:35 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5471dde53a4a500f08ec1ad7e166a1336ba60cb81c3f194c1bbf04655d30842b`  
		Last Modified: Tue, 24 Feb 2026 20:05:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a80037096dbf3d312eebd621991954296a318e1bc555385f93f8e3812ad98053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2748189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90793875ca2e5a1952b4e1d6aebf5c5c6e80357cce6352c85cdece69ab70bf89`

```dockerfile
```

-	Layers:
	-	`sha256:5ce8756d7a5d11c07aaef23d722aad1daff71566d4b839c1580dc52ac1af3132`  
		Last Modified: Tue, 24 Feb 2026 20:05:35 GMT  
		Size: 2.7 MB (2729665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26888c9f2528b334e7937346d45dccf0d7e231eaf08a149264946e4d0089c684`  
		Last Modified: Tue, 24 Feb 2026 20:05:34 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7bb0b122fa4aaca27a831b5f50514a1211954c61cf334597d29f929c2e25b622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.0 MB (199995821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9b4aaa59870f485c4d574da37f6804725e209387eaa29ccf878cf44fe318c0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 01:57:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:57:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:57:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:57:33 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 01:57:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 01:57:34 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:58:19 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 01:58:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 01:58:19 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 01:58:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 01:58:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 01:58:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 01:58:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5dce4318783a0719a116da2642ffc1e720139258359bf09a330578610611a0`  
		Last Modified: Wed, 25 Feb 2026 01:59:10 GMT  
		Size: 145.4 MB (145438176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1100db94cbe411e2cbf065c2d2bcffcae8ec65b61c6565c9ae52096e4c6cad`  
		Last Modified: Wed, 25 Feb 2026 01:59:07 GMT  
		Size: 18.0 MB (17961124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a011a6f301777ce9d5640c8b7eb106191449c26d1b481cf798fbcfae3d7348a`  
		Last Modified: Wed, 25 Feb 2026 01:59:06 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f07e9a1665858cd2792afcb3f3b74ee89093f6c0e5489ca24145603e5c3667`  
		Last Modified: Wed, 25 Feb 2026 01:59:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2cf1ce5364b6ac45ad0786e2373f4a09d553735555aa3fb411effb99e663ba88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa757b8c70b0b009f81b8e3578ffdf4cceed29a3dad4023d48baa55566d62efc`

```dockerfile
```

-	Layers:
	-	`sha256:191440072b0bb7c81cf7cf4c3cc657d58ddd0ee378f093a036637156ffd54ee9`  
		Last Modified: Wed, 25 Feb 2026 01:59:06 GMT  
		Size: 2.7 MB (2731883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00513addc0f9c642f8a7111e67125fd0a2856d2877e61908876b237579bbf1b8`  
		Last Modified: Wed, 25 Feb 2026 01:59:06 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a304f4e9876adf64ac3a57d98987045d4d34ad91a0982a44732bac5e677b57e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.5 MB (184457944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c054c2c7941dbcb43085b4dd593dbee7c642b372836f03737cde8e2113f583`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:15:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:15:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:15:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:15:05 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:15:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:15:06 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:15:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:15:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:15:27 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:15:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:15:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:15:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:15:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f803dd7bc2d733b564da46ba5a231113967783e3416f03d86ef7ca2b792f6a`  
		Last Modified: Tue, 24 Feb 2026 23:16:12 GMT  
		Size: 135.6 MB (135627087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9f849315cad4bfc3ce38de0466c844273c9d26095bb7b4ab692f89f6551750`  
		Last Modified: Tue, 24 Feb 2026 23:16:10 GMT  
		Size: 17.4 MB (17421153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacff39a56e7b6a3fa02e049114b5ed2c6f0b47134237b07deebf351e98dd6a8`  
		Last Modified: Tue, 24 Feb 2026 23:16:10 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94364cbc8a48b89d0ceb7ae134d350b516e8797a3eaf3581460d152ebb5f7f51`  
		Last Modified: Tue, 24 Feb 2026 23:16:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:62cb5490b27c7ff395b58c542b2e27aa05a029a11a2e38933a14b423b4d04cae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2740267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e73d522a444253cc6b73af4417b595ba0ed10418f35354dac4a9b63951a9c8`

```dockerfile
```

-	Layers:
	-	`sha256:9b2187264985e310d10d60a3fa080aa9d83e44411906d82698ee0aec45502fbe`  
		Last Modified: Tue, 24 Feb 2026 23:16:09 GMT  
		Size: 2.7 MB (2721864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ad8e664d3c4225e912ae7b5c67f0a91f8a469602328cf03cffb15aa7040f857`  
		Last Modified: Tue, 24 Feb 2026 23:16:09 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json
