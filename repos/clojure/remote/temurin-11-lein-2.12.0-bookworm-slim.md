## `clojure:temurin-11-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:80ebaa573ca267f1e34422c749b6df9c65c10bf1a3d7cfed157c5d21042800a7
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

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8d5072dc840d820690d23d3ab6030a5440e8c973606a5a38289168c7936bf25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196320511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384d2ddd28b08b8282911ca06f7fe2a105e32b51f9b889f83abb9a37d796e73a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:02:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:02:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:02:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:02:10 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:02:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:02:10 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:02:25 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:02:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:02:25 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:02:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:02:26 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68b348288f592db1b2069e93d1cd0473f8b37355800ec37267a4d9969c6aed2`  
		Last Modified: Wed, 15 Apr 2026 22:02:45 GMT  
		Size: 145.8 MB (145806832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cc2f394383ec97f32f4d2c61a0f6e93c84508d4f960ad31bf827c14393679a`  
		Last Modified: Wed, 15 Apr 2026 22:02:42 GMT  
		Size: 17.8 MB (17759600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f62ad3878c87a082c3b4a35b60b430a55e448bba42d7e6cc5b1eb6854b80d7`  
		Last Modified: Wed, 15 Apr 2026 22:02:42 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9838168ee740b2ea24b838dbd67b3091b81044a7ae9259070f3bcdcd70fef6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2766602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02a64acc2164ea8ba43aa4bf06b5b04810687d8f68de12dd4fb46a75186948c`

```dockerfile
```

-	Layers:
	-	`sha256:05e7c9b33dad63ab342f55d7442f52bfef69a881ef8dfa55fda05befb3086f7d`  
		Last Modified: Wed, 15 Apr 2026 22:02:42 GMT  
		Size: 2.8 MB (2750191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d4617f891b2d6d2dc24a79638e0f387aac4f0a357e2b9131ab726da111cc775`  
		Last Modified: Wed, 15 Apr 2026 22:02:41 GMT  
		Size: 16.4 KB (16411 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e21682f805d5d5ca0a71f6b63add7156737791f6d0c110b307a786be253a9e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192727821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d9db0a8a3669a833dcec55389b3bfe768c8b08d78fc3dfa1638a7c314440f5`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:13:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:13:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:13:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:13:35 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:13:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:13:35 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:13:48 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:13:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:13:48 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:13:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:13:50 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5851c3aeff5d985d89b5b3f01b405b93021f26a6d7d650f4d91860e18d0b9f8f`  
		Last Modified: Wed, 15 Apr 2026 22:14:11 GMT  
		Size: 142.5 MB (142500803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b8ab7d9869ee96bcc933ab9e97c71706de6370d4471719b179548044bac033`  
		Last Modified: Wed, 15 Apr 2026 22:14:07 GMT  
		Size: 17.6 MB (17593065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89331b0675a1530685cb0d2b18e4068dc6c1e3f65b75d333bfc6ee2d2a359c7`  
		Last Modified: Wed, 15 Apr 2026 22:14:07 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ddf84e95ae665552ac58fe490f6c0712a7f54ad718c15889560822b2e3b9f674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2766957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faad4a86901cb57cc93086110122b910546e87f1f36e6256f7f64494b4930838`

```dockerfile
```

-	Layers:
	-	`sha256:8dae33c03b6ffe8d924ac8147e92a435bbd3fce1ea0c47d4ce15f901db7394bd`  
		Last Modified: Wed, 15 Apr 2026 22:14:07 GMT  
		Size: 2.8 MB (2750424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08c58d7c7155c4bd8ff1846c7b6ed356cbaa4ea30747fe340183a610f8f898eb`  
		Last Modified: Wed, 15 Apr 2026 22:14:07 GMT  
		Size: 16.5 KB (16533 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:81f005f241d3527a23a5a03c58092374041babc3e9cf1ffdff3d05447b8595d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187555002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b994fb470f463fa3d79671c9c16bb291167a9b505ef0ef006722aef31bbcaf`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 14:30:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:30:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:30:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:30:20 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:30:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:30:21 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:30:57 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:30:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:30:57 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:31:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:31:02 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3239a667025d854bea5c185db151e78d7d54c70792c78737dc5abe529056f1e3`  
		Last Modified: Tue, 07 Apr 2026 14:31:37 GMT  
		Size: 133.0 MB (132997659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4ee323fcdf48d12047143773fa8f5c1478de30398802b3bbf739ca2de92bdc`  
		Last Modified: Tue, 07 Apr 2026 14:31:35 GMT  
		Size: 18.0 MB (17961090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1048e3e97e4d050882db7f9bd2ad88def7cfffafe62fc18b76d2a159e775080`  
		Last Modified: Tue, 07 Apr 2026 14:31:34 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a7702f330e2cea471ab43bac3fffb56901b6038640e0b62cf0a3c623a0a0854a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2767864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439e3d353d3b21cdd04db80b5b554277015b19e0fa89cf34d47e032ec5ceac7f`

```dockerfile
```

-	Layers:
	-	`sha256:cf771a82b04d8bc2bff188a82535a08945e1565e669ea13d48814ae120fcb2f8`  
		Last Modified: Tue, 07 Apr 2026 14:31:34 GMT  
		Size: 2.8 MB (2751409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c6bf8023b8a8aea6638ca50fd9d820bfe04d01345c5ff72dadc5e4ed3ae286`  
		Last Modified: Tue, 07 Apr 2026 14:31:34 GMT  
		Size: 16.5 KB (16455 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:786074430f0a613e4cae95e1beba13ae21932654550d1fd1c1a4c744762e8dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175392693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b30f24cba2e8d8a7a8c4e9167f9a5dd812d03fa2e2d55d451fe4c305038002`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:39:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:39:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:39:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:39:16 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:39:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:39:17 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:39:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:39:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:39:27 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:39:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:39:29 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e385f726bab54d70ecc51bad16d60533bc9b6d182b632879bc3c86a7da9d89`  
		Last Modified: Tue, 07 Apr 2026 05:39:56 GMT  
		Size: 126.6 MB (126562190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafa6a9582fd75b84b80a45c6b1573591fa2afb9383c760a2ec7d8ad2e01a777`  
		Last Modified: Tue, 07 Apr 2026 05:39:52 GMT  
		Size: 17.4 MB (17421084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69bb5b93eaee5f4a7e807174461c29e5ebf73c713fc8c68f56d6d15d4b3682b`  
		Last Modified: Tue, 07 Apr 2026 05:39:51 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dd18fef376277924e9f4b6e1d52882890f41f4576390060c09c8ae9e379dd25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2758421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb49a66074f26d587f7a545831d9bc5247051a4ae9223a4e690e1e034539d4e`

```dockerfile
```

-	Layers:
	-	`sha256:f32dee42f8019f43c67a2d0a2f72d1d935a78a959c11de4a3f233260db978b07`  
		Last Modified: Tue, 07 Apr 2026 05:39:51 GMT  
		Size: 2.7 MB (2742009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:851570905604d2098a5d074740a932eac52a467e0099505a0014977144b6fd22`  
		Last Modified: Tue, 07 Apr 2026 05:39:51 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json
