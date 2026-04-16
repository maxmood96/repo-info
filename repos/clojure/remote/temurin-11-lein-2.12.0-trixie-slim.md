## `clojure:temurin-11-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:d63b33acc91c2eabb2fe8cab43a5b7e213fb18d01028c5e884bb7251f9f2c48f
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

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:32fa618c69dbab4b3481c2102aed10451c5104802c8d9bb3c74296e328d8beee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.5 MB (199502167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e13719579e86c50370ebb5810723fb684281baf96cc72481948ac09e2319e0a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:02:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:02:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:02:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:02:41 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:02:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:02:41 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:02:57 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:02:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:02:57 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:02:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:02:59 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e7014cda1faeab0b963d54d6ab3f00b59624bbf5b3a6bf51e02acf6a093f3c`  
		Last Modified: Wed, 15 Apr 2026 22:03:18 GMT  
		Size: 145.8 MB (145806793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09ae8377277824f9bbf217101e434fd5f7c59feca600142a83b91e70df88a17`  
		Last Modified: Wed, 15 Apr 2026 22:03:16 GMT  
		Size: 19.4 MB (19401963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b5f74fb90d7be2c8a790f35f60ebf392549779b7c0f127b8a5e415510f613f`  
		Last Modified: Wed, 15 Apr 2026 22:03:15 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f44a0a201b5abb9836d5303ded2437d2d5389fb89ed2a5442550e7ac639ceb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b8a833e2fb9fa5352ba7a740ab36e750417a504cfb9e2adbd04614b8bccb7e`

```dockerfile
```

-	Layers:
	-	`sha256:5da6641860d764a906e4da2ca31a5eb15bfbe7e197f1890832402314092f9945`  
		Last Modified: Wed, 15 Apr 2026 22:03:15 GMT  
		Size: 2.4 MB (2384929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc15b27c732d6afc7390d8f60a34d77b5d95f87d4ab0812ccb473cf7e4d57673`  
		Last Modified: Wed, 15 Apr 2026 22:03:14 GMT  
		Size: 16.4 KB (16393 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c2dd314c02c62f71cf50c522f723a3cd0a33a39aa85d5ab7c54bb71cdd11ea23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196891993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b63144c4e001c2580ee2fc75b1c05aeafa05ee964759b88961f5680dbd24f1c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:13:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:13:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:13:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:13:58 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:13:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:13:58 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:14:15 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:14:15 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:14:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:14:16 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76a727088c9cbbee2b741f4ecc6bcd62131ef123d61e4193467695fa8d91a44`  
		Last Modified: Wed, 15 Apr 2026 22:14:38 GMT  
		Size: 142.5 MB (142500803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646e4b27b158989eb35b01fbd9fe9952592e0754c4b15830ca17f7564b211d59`  
		Last Modified: Wed, 15 Apr 2026 22:14:36 GMT  
		Size: 19.7 MB (19734905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f859da95d57c730c09198777989239572432c291caccb63b59a30b8b8b7d39`  
		Last Modified: Wed, 15 Apr 2026 22:14:35 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aee1a135d418e613f025d08d8938082daa972305bf45bf2fcf9aa06f1cdf4e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24d868fc77945a368fae99f2a169657ba58eb86a6f12c115d279b74809d369c`

```dockerfile
```

-	Layers:
	-	`sha256:d385d8c4f74a58e5668554a958d7ddc06e02ee275c4c086d20517bbe7bef453f`  
		Last Modified: Wed, 15 Apr 2026 22:14:35 GMT  
		Size: 2.4 MB (2385165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f632f7b146cc5a0385177b931ba129a3ad11a5281dab7cec880fcfb1cb817dcb`  
		Last Modified: Wed, 15 Apr 2026 22:14:35 GMT  
		Size: 16.5 KB (16515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c0372d89be4307d0cdd1ea7fbf3eaf20e8d72f424fb0b3fc02c0e45e76037be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187593908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bc5e0652fce5861f67f4e75a5c2160c8c011bd8fe35bc2ef2e3b500ba933174`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:31:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:31:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:31:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:31:54 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:31:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:31:54 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:32:38 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:32:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:32:38 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:32:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:32:42 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e26676b8fc5a07c40bb71da4c5066413b10ef71e116aefba94d4275fc936247`  
		Last Modified: Tue, 07 Apr 2026 14:33:19 GMT  
		Size: 133.0 MB (132997689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cc395b73a7a7e2ecca458bd2d469fb94b1dac2e77f4c803ef84c10291b7cf0`  
		Last Modified: Tue, 07 Apr 2026 14:33:15 GMT  
		Size: 16.5 MB (16485411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae24e776432d5b9bf19093c9b41c0241667c1e22429ec03ab5aca6a3218a0ef`  
		Last Modified: Tue, 07 Apr 2026 14:33:15 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:968de93d22ef4afdef39d4bb486c038f1c221e92d6ab9b46ac06d5120ae46095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b76ab07818a79c4467331caecf29ee9b76fe330d239d10e74e4213d8442625`

```dockerfile
```

-	Layers:
	-	`sha256:fffcd8af9bdc6e87c030f277665817798fcc7fd3c096d7712206f2ff5c27d380`  
		Last Modified: Tue, 07 Apr 2026 14:33:15 GMT  
		Size: 2.4 MB (2385294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b24c110740455ee8b5e4fe200c46b021e359c39558823eae807e23911666ad7`  
		Last Modified: Tue, 07 Apr 2026 14:33:15 GMT  
		Size: 16.4 KB (16438 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:fbb2f81f4ee74b7862a8fd85999dcafa31b258405fd1f29c7cd5c475e4903fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177399314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4715fd0a290a54a91ae95a6798e15d36d0b671fffdc22bf5c6e6b3457261820a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:40:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:40:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:40:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:40:00 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:40:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:40:00 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:40:13 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:40:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:40:13 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:40:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:40:14 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9166190ba17c367d077fe9e36dd0402927522edea9133f6d301c45a7bf95699c`  
		Last Modified: Tue, 07 Apr 2026 05:40:38 GMT  
		Size: 126.6 MB (126562240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391f5f728abf61c633253d361d581703c6946640df8ae98847804d84e57d6b36`  
		Last Modified: Tue, 07 Apr 2026 05:40:36 GMT  
		Size: 16.5 MB (16483903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3ead82e98c0cbae289018cb5f96b2b5345a1047c416d3c4ce9b3593a87fc42`  
		Last Modified: Tue, 07 Apr 2026 05:40:36 GMT  
		Size: 4.5 MB (4517721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1037e0c7a25e5080fb654d6a308dbf7888f997d3d959af09cea18f7d93ec6b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e84a0793f7151fb411a23822fb88000113c504cb6644b45d8ec5c6fac1eeb2`

```dockerfile
```

-	Layers:
	-	`sha256:b974e1615472311bafeb49314b4b8f17df7811dce68357c13facb847f23738ca`  
		Last Modified: Tue, 07 Apr 2026 05:40:36 GMT  
		Size: 2.4 MB (2381360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3fa278e6b0d65f0f749d1beb7845ad95597f8537555bcba04abcc6fb5e32dcf`  
		Last Modified: Tue, 07 Apr 2026 05:40:35 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json
