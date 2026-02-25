## `clojure:temurin-11-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:bf9c0d30dd022d3f0ea25e92eb8f7b9840bae99c2a89a1856ddf2f1050f30450
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
$ docker pull clojure@sha256:4e3b73d340fefeac0a285ca1c919ffec7286f2702e66f0a1031a2a9f152c0831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196319499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e10d08961a2e90c990c50e90964c4af178178682b6d94740fef9c6ead6c452`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:53:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:53:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:53:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:53:45 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:53:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:53:45 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:53:59 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:53:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:53:59 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:54:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:54:00 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c41970dfa7371b9fbe267ea251c9269a33d70adfb94fe8f8316fcdb3622d2b6`  
		Last Modified: Tue, 24 Feb 2026 19:54:19 GMT  
		Size: 145.8 MB (145806748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8230f11ec3e76f08bf526a0b4501be451ee863c2710c45c613e6f6eec41b08d`  
		Last Modified: Tue, 24 Feb 2026 19:54:16 GMT  
		Size: 17.8 MB (17758739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cc10aa8e7f5a5cd1c68299f58c9a0b19d4ccf65e62a899128bac19c1b5415d`  
		Last Modified: Tue, 24 Feb 2026 19:54:16 GMT  
		Size: 4.5 MB (4517701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cf6fbb06247e7df9d7ec8a5989e3c92dfed3459c90e0160ee2ee68c9177550e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2766603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce1c0ab657901addf93032b14f9efe35b0b63984cd5a92aa65b4d3e25aa84f9`

```dockerfile
```

-	Layers:
	-	`sha256:8dc6840a024cef201d95ab2119e69ee3b6782ce4bab6a95c6672c2dcbdd35531`  
		Last Modified: Tue, 24 Feb 2026 19:54:16 GMT  
		Size: 2.8 MB (2750191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bb6c6d0e2fcd59c6dc44f4d3797e87ecad7e071fed7a565377b28ee021c5768`  
		Last Modified: Tue, 24 Feb 2026 19:54:15 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cd68ba74bd6e83dd7482ef0cf05a56e63878214f5009a0b00f71d5b67dd18e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192727064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f944d68850750e37788b0d491ae910f250df4b8728ec96ba0d4156efec39a9d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:04:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:04:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:04:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:04:15 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:04:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:04:15 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:04:28 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:04:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:04:28 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:04:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:04:30 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2640af19aa6f1d4357dd92dfe2ff171cad48ace966763c1767b48f4e6463b8aa`  
		Last Modified: Tue, 24 Feb 2026 20:04:50 GMT  
		Size: 142.5 MB (142501442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c0f5856c40b9718152de03b2b813f36ca23d168615f59184f2be25431d3937`  
		Last Modified: Tue, 24 Feb 2026 20:04:48 GMT  
		Size: 17.6 MB (17591780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567097d55bab73ecf76b2c5adaa59f481c0d2cd9828ea3f8747250f8e080876d`  
		Last Modified: Tue, 24 Feb 2026 20:04:47 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ad286858f96d2ae4487cc81b0a7df96f862349de47b592a13b96e3a326f3684f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2766957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1800c0a3e413b5ca333342d4b10720943eed568808d25b4f87e8dd1748f4b18`

```dockerfile
```

-	Layers:
	-	`sha256:a168e0978572c03ce075520068dadd4c5d101f370c8f3c74514eee9ef667c68e`  
		Last Modified: Tue, 24 Feb 2026 20:04:47 GMT  
		Size: 2.8 MB (2750424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7b505262cb4fd363124044db838d743b78d07ad2b073791978d489c4ac191c`  
		Last Modified: Tue, 24 Feb 2026 20:04:46 GMT  
		Size: 16.5 KB (16533 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ae2e9748c42b1ca2b57c62069a52166b0fc2e627a165656b1ccff4f907ecbe45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187555087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5664449c257c849bd7e6c3904f7fcc57f72afe9873ac345612286baf142b66bb`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 01:49:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:49:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:49:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:49:21 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 01:49:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 01:49:22 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:50:05 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 01:50:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 01:50:05 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 01:50:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 01:50:13 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9bc5a19266700a831a5467cc408599b98ef115eeaac770a91b7bf3a370d120`  
		Last Modified: Wed, 25 Feb 2026 01:50:54 GMT  
		Size: 133.0 MB (132997811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141c3f26e8bde611c7333ad466c14f692337e80a911e1fd9aa778c0e009852f0`  
		Last Modified: Wed, 25 Feb 2026 01:50:52 GMT  
		Size: 18.0 MB (17961141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa69a31717175f1d3638a8cb60afd3a35cc135298c2c8c5c51a6549b9e604b33`  
		Last Modified: Wed, 25 Feb 2026 01:50:50 GMT  
		Size: 4.5 MB (4517769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bfc11db0064de8e77230c10e6f50fcbb3de2c4fdc1987a1cacac7d1c4d14e7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2767865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71359fcd5390804c5b7e9c5bf7f934d1b3524816c61a8c162e828212dd780158`

```dockerfile
```

-	Layers:
	-	`sha256:9483d6c0ce236d319670a744282e36b81dd7005b46fb9497c44c5f20dd9481dc`  
		Last Modified: Wed, 25 Feb 2026 01:50:50 GMT  
		Size: 2.8 MB (2751409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cbc2123c108556a8fbbaeecd92a556def822491e92d7d64c30ed74395d06c3c`  
		Last Modified: Wed, 25 Feb 2026 01:50:49 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:960f1e2c3c21345ca9f02cf096b43222db8f210d570ee2fe561ab17d76dfb5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175392571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ae0379c5edc8f9c4ffa61ad6f903a799c848ba0e42f2a33ab0f4867c36410b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:11:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:11:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:11:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:11:21 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:11:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:11:22 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:12:08 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:12:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:12:08 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:12:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:12:10 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88825d23886aad7630f698fabec26ff327fb5cc56e608c0be4067ab5b8f57c4`  
		Last Modified: Tue, 24 Feb 2026 23:12:49 GMT  
		Size: 126.6 MB (126562035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4752e09360ef316984a21934f8604389cff03c29aaa543bbc98950c5249d34b6`  
		Last Modified: Tue, 24 Feb 2026 23:12:46 GMT  
		Size: 17.4 MB (17421227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f2148f6359550c014e4e4abf2719cb752f8ec99a1129a128c839c54e416a7`  
		Last Modified: Tue, 24 Feb 2026 23:12:46 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9b4c85c514940952234187a4e3adabab2ae93e028f0138ab7ff5a1aa8a402ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2758419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf41226fb485edcba623149005c8c73e49696b66405d9aace80efe4789ccf0d`

```dockerfile
```

-	Layers:
	-	`sha256:ae4cca4800ccab75e8c3d46e69331cd336e943021953ff8840928f4b7bef89bb`  
		Last Modified: Tue, 24 Feb 2026 23:12:46 GMT  
		Size: 2.7 MB (2742009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1358cb7e7e3143b236786bd93c9921c717f878b64981be3a05215585591f53e`  
		Last Modified: Tue, 24 Feb 2026 23:12:45 GMT  
		Size: 16.4 KB (16410 bytes)  
		MIME: application/vnd.in-toto+json
