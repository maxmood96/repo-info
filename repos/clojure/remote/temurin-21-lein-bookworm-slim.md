## `clojure:temurin-21-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:b9df9919693e9b1025b25437f42206e065d2bddd100103cb2c30cf42d417cb0e
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

### `clojure:temurin-21-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ceda12c604d09486d4eea867b5af0cbcc793ec3db97f13526e88668b02af45b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208330645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821ca55a927dd70c9dc86d7a7a1cdeb2885377c9c9b0d36c4ec1b2e24ce99253`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:01:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:01:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:01:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:01:34 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 01:01:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 01:01:34 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:01:48 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:01:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:01:48 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:01:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:01:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:01:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:01:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6cf382c16c655fedd4f828b50df8f00bfbb0ec3900a450af802fa62d310281`  
		Last Modified: Tue, 30 Dec 2025 12:27:15 GMT  
		Size: 157.8 MB (157826042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed6e6f1f50ba58eb13b5208cb69de85c3159f1199b248256283bf5280447e07`  
		Last Modified: Tue, 30 Dec 2025 01:02:18 GMT  
		Size: 17.8 MB (17758047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c601b38f692218953413802be5c607e80c295ef240e8916aea8d0467d302f7d`  
		Last Modified: Tue, 30 Dec 2025 01:02:17 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8542b74ab3d7412c54fb6e109a8e3a89115a59ab98a99e32cc7f55b7c62aebe`  
		Last Modified: Tue, 30 Dec 2025 01:02:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cb9a4f9652cd51e33899b3c2e797a377a6d4925ec80004d9e4e96f1f9154e6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9d6179025759e1c0c84d2573a995a13edacd4ef81004bad4665557e6fb4c96`

```dockerfile
```

-	Layers:
	-	`sha256:cd454abfacb3892ca81db4181db6c0ec42f0f7583a8102fc29d9b31116d209ae`  
		Last Modified: Tue, 30 Dec 2025 04:43:45 GMT  
		Size: 2.7 MB (2731890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db59e68d7272f7d4b62f4cedebaeab16622709768405528b8ddc75c3103a298c`  
		Last Modified: Tue, 30 Dec 2025 04:43:45 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6ab71500aa3ed53e676830c31ade1dadfc1ff4f3d6a617017590ce6cf094902a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206319058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3626f94c21c3b9ddf377415dbf40c6fd6d5ed93726ab354555d2498652766964`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:02:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:02:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:02:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:02:58 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 01:02:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 01:02:58 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:03:24 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:03:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:03:24 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:03:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:03:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:03:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:03:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95654e2d5c337261de59e2f1d322475ea810acfe5c760dc3daa42304d8a333cf`  
		Last Modified: Tue, 30 Dec 2025 01:04:16 GMT  
		Size: 156.1 MB (156107638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20f1cd775591ca8a415f99a8b304d6b09dd45da28de30a923b29c819c44d88b`  
		Last Modified: Tue, 30 Dec 2025 01:03:54 GMT  
		Size: 17.6 MB (17591080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7af2042daf66109abdff04ede4a36aab75dc25ca78fd09c8550e58685772e8c`  
		Last Modified: Tue, 30 Dec 2025 01:03:53 GMT  
		Size: 4.5 MB (4517700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2f5224a9cff70cfdf57a8ee7af348b267735c6efae8a97ed9d057c28aea02`  
		Last Modified: Tue, 30 Dec 2025 01:03:53 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e31447b9db7f191aeb3c6aea0036f5c33a62938c1a50ff38f8251d9d693d9a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3f692251947eaf95cd33deecf4f53f67cc967e0b81e6fcfcee2e7548b2586c`

```dockerfile
```

-	Layers:
	-	`sha256:ac24724602472de060509d0111a2c451044627457a37c1e5f02a8355b7ecb3e0`  
		Last Modified: Tue, 30 Dec 2025 04:43:49 GMT  
		Size: 2.7 MB (2731505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aa75080a7f2cfab4cf649b66f781c56e177d7cb174adf490ad1f942441db04f`  
		Last Modified: Tue, 30 Dec 2025 04:43:50 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:eb1355915325bb4abeb57d8bc1b882e24a90a6caf9d86daabe357e6ccf757d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212489668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6592d2152066d8533b1b21a9c7434ec25858faf92053f0ebb9a9677b7fff3390`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 05:21:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:21:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:21:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:21:25 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 05:21:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 05:21:25 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:22:06 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 05:22:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 05:22:06 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 05:22:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 05:22:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 05:22:10 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 05:22:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5205a1e1f7238574a7d52bb96b174549098b3440c35820756b8c8be70a79f64d`  
		Last Modified: Tue, 30 Dec 2025 09:15:38 GMT  
		Size: 157.9 MB (157942950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70dd4ae8fa1777a3c9acac4931612deec51b925832b22d342bb7453ee5e49e8f`  
		Last Modified: Tue, 30 Dec 2025 09:00:38 GMT  
		Size: 18.0 MB (17959704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca98bbde25fa1e20d9e33d327d577a20a8480df66768526930e86b5eab82d08f`  
		Last Modified: Tue, 30 Dec 2025 09:00:37 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7bf1384474575be3992eda371a5231d3756d0d09b85d6ada796cc61c0327`  
		Last Modified: Tue, 30 Dec 2025 09:00:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9a8452111f0b696a323e5b4191cb1c893da08b8799d560426e9d5e0b769d4dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f11c38fbc4e33f11e0a0400a537e61f1d662721871e428ad44a347741d90872`

```dockerfile
```

-	Layers:
	-	`sha256:00e3ac79b3f2ac316eef09a9acf606108fa0d3138647b00fed774d4c471e2ef3`  
		Last Modified: Tue, 30 Dec 2025 10:35:56 GMT  
		Size: 2.7 MB (2733723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddc5a1b7af2c6c219a3095e98abe4faa1fd54a8280fff19031a317fd153cc486`  
		Last Modified: Tue, 30 Dec 2025 10:35:57 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b330da1f1292e0ecfe2d07a9c66edee2b27a14ac322e1bbab09ec32667f9edfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195893162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4982d3d3399c57312d7f3254e6b7c7282cd90d3c562d060f52792af3bac5345`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:05:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:05:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:05:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:05:26 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:05:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:05:26 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:05:36 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:05:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:05:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:05:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:05:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:05:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:05:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b30689a6c8fb0d3773ac5b39e3291262242aa068cabd739b185d23b4c70da67`  
		Last Modified: Tue, 13 Jan 2026 03:06:22 GMT  
		Size: 147.1 MB (147069857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debe0cf03b0d8d86ce3365f87a88009f0accf20cecf209e13f211d658813af49`  
		Last Modified: Tue, 13 Jan 2026 03:06:11 GMT  
		Size: 17.4 MB (17420710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40d4f76eb9bcc31899cacfe5c606d95f82a648840c372be2b39708d54db6290`  
		Last Modified: Tue, 13 Jan 2026 03:06:09 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6da08754dd6f14914dd48f11c929cc21b5da748aaf89ab4258902db6bf013d`  
		Last Modified: Tue, 13 Jan 2026 03:06:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ee07ee4cc50082e9208c7ebb31adc35871d7ec2ac9b91d3c1fe04b20f8d3aeb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366fd196e7a06070db5f9f2abf63b9edaad00e60f5bf82bbca31feab7c83970e`

```dockerfile
```

-	Layers:
	-	`sha256:510371a003bafb1f3e79a1abae8fe374f4f033d03e5f25ad96363f9ee858f078`  
		Last Modified: Tue, 13 Jan 2026 04:39:01 GMT  
		Size: 2.7 MB (2723714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e6be765864ef49bf8cdb88027712e328861e4d5360b7ca5c50491e8b866616`  
		Last Modified: Tue, 13 Jan 2026 04:39:01 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json
