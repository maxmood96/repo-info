## `clojure:temurin-17-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:c66532846d00c9fb73379314e52d82d0ad039b68b18d9773612b387249dbf54c
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

### `clojure:temurin-17-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7ab48c32e2b9dff8095e2bfe8ab7047a59c174adff7225e67cec898b6d6318b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228839286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd2c2a7edbeacebb7077254cfd65ffba4424043e9aa17a8b87eb736787fcab8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb64879df5fd9a9933136e63c0dbf2846c418108a04d45023eb2754175d5c6af`  
		Last Modified: Tue, 03 Jun 2025 14:59:36 GMT  
		Size: 144.6 MB (144635023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b5bcd71f50ca43398d1675ed92602b38ba8dc1252443e813244069b45ecb1f`  
		Last Modified: Tue, 03 Jun 2025 15:17:49 GMT  
		Size: 51.5 MB (51464332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178076ecd77350eb0909657625b9dbd0a11ed9c640630da00ff24fe8550005b4`  
		Last Modified: Tue, 03 Jun 2025 15:17:46 GMT  
		Size: 4.5 MB (4514173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55f4d5b1a68581e3a7475a3db5a303f79a012fe61eb4c8f1c19be96c5e0572c`  
		Last Modified: Tue, 03 Jun 2025 15:17:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:434ca3824e4d40f3001e3761fc75d31607bf364d9ee3a015d7e0e7f9b9cef0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4385211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe61b6a91652fa019da25551aa9fe6154ba8cb445686f283e986aa837bf8ea03`

```dockerfile
```

-	Layers:
	-	`sha256:26c9ca87971280be3a09eb08747682caf4117888f882a133b91287c23322cce4`  
		Last Modified: Tue, 03 Jun 2025 15:35:38 GMT  
		Size: 4.4 MB (4366753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90343e560ca424bdb7165a492929f6bb19fadb73f44086e07b8b0fdc739e78a3`  
		Last Modified: Tue, 03 Jun 2025 15:35:38 GMT  
		Size: 18.5 KB (18458 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:108b04cceb7238fae0bcbd3a9dcc3210536c3943d3b8fca87206b863967437a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227525663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba3b2031450cb30f6ab316a8c45de0d11132868fce697c90ccb960f5a633555e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbfa317a80df2e7dc3da8da387d9081ffa13f5e29daff53d5dcef29b40af4a3`  
		Last Modified: Tue, 03 Jun 2025 12:46:25 GMT  
		Size: 143.5 MB (143512643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1811d50188badff8bf68315651ee2745ba3ca16f6e568169a54ff1a3f027cc`  
		Last Modified: Tue, 03 Jun 2025 12:46:23 GMT  
		Size: 51.4 MB (51433125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4500facfebef0b0862be8dfa1606ac5ae965716dc9ad8109099378595760cc96`  
		Last Modified: Wed, 04 Jun 2025 14:51:00 GMT  
		Size: 4.5 MB (4514186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724e7ebcf80863b1634d420324bdf9e130fbca7009bdf272234263cc27867634`  
		Last Modified: Wed, 04 Jun 2025 14:28:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4f1c812c64718951d90b457deb56638afea2c971d6dfd98db9d31579e4f281d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4391024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9294cbef68540265e2b0293f76d34f922b218c82e175617860cc7a0f3d5ce6`

```dockerfile
```

-	Layers:
	-	`sha256:2e0414539a1856e350a2a702e83aa4a979f3fe4c90eed9ff20ee416cf88228be`  
		Last Modified: Tue, 03 Jun 2025 15:35:43 GMT  
		Size: 4.4 MB (4372445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64f850d0adae52e0093e4370cd3b30ef31a67726b928f18c7832a4f20a6cd09e`  
		Last Modified: Tue, 03 Jun 2025 15:35:44 GMT  
		Size: 18.6 KB (18579 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:39feef9c328c2d4258d525b7d380a1e6032727141d14fab7a6e0794cee6c0201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237540595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ea5ece2e62710a262a63fea8c8ed8fbc19aa141a3642dd40408148998a5ea2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07686e6fdd26baa61178aa1b8e90f5239ab4c91006e539b5fbf39feb82e0a434`  
		Last Modified: Tue, 03 Jun 2025 08:46:31 GMT  
		Size: 144.3 MB (144280562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0decee83afb24ecf7d37887ccac098a891c8d28c1a60a9b2bddc2b4a4d6180d`  
		Last Modified: Tue, 03 Jun 2025 08:46:32 GMT  
		Size: 56.7 MB (56678475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f2c8b93997aa5cf0e662f507dd40d83a3e60d858c495cb87aeb982b8c24ffa`  
		Last Modified: Wed, 04 Jun 2025 20:00:56 GMT  
		Size: 4.5 MB (4514216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa90108fa977aec48383a94a826d0fc8c93886744aad1ca23c5f6a429170b02`  
		Last Modified: Wed, 04 Jun 2025 20:07:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dadbae0f8fad34665bfc5af3303c0681bc8d57962729cf19fca2e4c640170848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4390086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623ac9d6bbf3830ce24e1da4054148dd4c0c9e46da5b394171cf22304d4b5eca`

```dockerfile
```

-	Layers:
	-	`sha256:434b2d64b01ff5611edcd7c69fd7b174067a4f4ca9896f033549cec54cd83e43`  
		Last Modified: Tue, 03 Jun 2025 15:35:49 GMT  
		Size: 4.4 MB (4371584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dee28bfe5ab790b427f62e82ead4d8ba3f23a00a6e9c67e05e57ba85160476e6`  
		Last Modified: Tue, 03 Jun 2025 15:35:50 GMT  
		Size: 18.5 KB (18502 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:cb8c5b72170397daf08a33962daa0c1ab8cae277e6844076533565f17ed26930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216544189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fcd3f916e60a0234c94fafc1e3f5066296ce9f3f389e3969d1b4c8aa29534c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad34fa5b937772a939247553d5da11fa707ffc251f370c152ab8bf4d478cc3f`  
		Last Modified: Tue, 03 Jun 2025 06:13:21 GMT  
		Size: 134.7 MB (134673554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7397fa411a4c1ed9c03f953714d3715ec49d3e4423e6b445fd5c7b65d59f4448`  
		Last Modified: Tue, 03 Jun 2025 06:13:20 GMT  
		Size: 50.5 MB (50473241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea053dd873e309ba3a0c3a4d8d35a32fe67a816b9b01526bce7b586a40396ae`  
		Last Modified: Tue, 03 Jun 2025 06:13:19 GMT  
		Size: 4.5 MB (4514158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58cbcde30767229eb078dd3911a66ac08d12cedac62cbf0562f3776c989223f`  
		Last Modified: Tue, 03 Jun 2025 06:13:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:067719904fbb6fc5a4f77475394245e26af5f56fafbd8dd873ece5ed46a383ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4379481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a2cae9e34e4217b05bc1eb53db2031baff83751faaeadd1e53c6f6a40ee768e`

```dockerfile
```

-	Layers:
	-	`sha256:b51276813ba074e2d240afb5e9cf37f35f3f57b10371b71d1308f7359ded8262`  
		Last Modified: Tue, 03 Jun 2025 15:35:56 GMT  
		Size: 4.4 MB (4361023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9487d180112f8f0d41c1f462a9bd449ed908196f28a1c6388834e95015e7b1f`  
		Last Modified: Tue, 03 Jun 2025 15:35:56 GMT  
		Size: 18.5 KB (18458 bytes)  
		MIME: application/vnd.in-toto+json
