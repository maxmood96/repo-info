## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:c00c3d60b3713965158270a266872bfe971fd46cf257af06d5653b58428a8c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:49bda43ad0b8c6ba3a931c1f9c5eab8ab3ece3abb667a9e9f982ad21eeebde62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 MB (221150061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356464a2d8fd9b2bb9f3b89260f489c3a4656abbd89569cc364dc1b9dcb86fa8`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 15:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2957c5df2be828d59b29d1f356fc101fefcc3925a93e74c4f2e122d362954fe`  
		Last Modified: Wed, 29 May 2024 19:57:00 GMT  
		Size: 145.5 MB (145504897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225d4aa07cf0d60ca4dcdbfbacf9007a2090e262d3222bf7c30403fa62038e1b`  
		Last Modified: Wed, 29 May 2024 19:56:58 GMT  
		Size: 16.1 MB (16147657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c4e6b16450cc6516752097ff6c9d3494030df53216b23a38a34cc3810cdc56`  
		Last Modified: Wed, 29 May 2024 19:56:58 GMT  
		Size: 4.4 MB (4398076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:56198be04a60a0107d178202127d29b34d03df75dcc384d8137956ffdab0a451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e0ea7b750576e4945b80e61be8c00b12ee1a1e5b714c059c0abb3f110dcb85`

```dockerfile
```

-	Layers:
	-	`sha256:02c23f78caed7d12b42c31d589b6832c11c6a4bf32f6021bfd2195882d6e8b11`  
		Last Modified: Wed, 29 May 2024 19:56:58 GMT  
		Size: 4.2 MB (4151310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4bd4d030d6ab9faa288fe3a61a8e952ddc34f6b12c65a8533b448004fff3d70`  
		Last Modified: Wed, 29 May 2024 19:56:57 GMT  
		Size: 16.0 KB (15988 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4377fc2db11c355a07fbbd14fe4af18f220740f24a716418e9bbff088ad3c14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 MB (216577673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d3f9cda0bcfa22f24063107b56d306e59d757b2d949776c04686240bbfc4c6`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:47 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 14 May 2024 00:39:48 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 15:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5180cdf83b9e6d688ff5d031db6a4009dc64691aa8d105945b1d8621f3656844`  
		Last Modified: Wed, 29 May 2024 20:37:28 GMT  
		Size: 142.3 MB (142304134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d22403a88286e5b6d2720769de517d2033d94f9f75c44c86a0192581749e4e`  
		Last Modified: Wed, 29 May 2024 20:37:25 GMT  
		Size: 16.1 MB (16136444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd639bdb551be85b457cf326862f025ecbd8c74861a02434d9409f05419eb22f`  
		Last Modified: Wed, 29 May 2024 20:37:26 GMT  
		Size: 4.4 MB (4398073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f9b41ad47df59a5a5054e614e79d773bcca6b6298782d47bfd1a54c68c798268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dace7f402d0b6fb4a94ce1ac3db9ec392007f55ede1c2ecbf81d04822cbd7134`

```dockerfile
```

-	Layers:
	-	`sha256:d838a942a7d78224f95d5ad0762b934cb5a25d6815ad4153bd244a118ed3573e`  
		Last Modified: Wed, 29 May 2024 20:37:25 GMT  
		Size: 4.2 MB (4150900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee4d679a585cd8e0f3cb56f73ad29cf29a5a573581a3c56a68261627947c6aa`  
		Last Modified: Wed, 29 May 2024 20:37:24 GMT  
		Size: 16.5 KB (16512 bytes)  
		MIME: application/vnd.in-toto+json
