## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:f9ab4083e7e6c33b80a076f62f92abbb2d73ea91b1e7be317454003d817ca5a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7a6914a0ace1461111908f1dbc6ca5437c6d7254e998c5e465fa6f3fff0b120b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220716667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ccaa1dc739f4c75b96b9916eaecaa3014222d0e8038e7932fd07cafbb967a9`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 02:56:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:56:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:56:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:56:53 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 02:56:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 02:56:53 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:57:08 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 02:57:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 02:57:08 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 02:57:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 02:57:09 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:e759575b5b0029fea51256b7ad3afa90c8ff1a6a9457787359c2b05b4a964edd`  
		Last Modified: Mon, 16 Mar 2026 21:52:53 GMT  
		Size: 53.8 MB (53762481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6e88f8e7675fb8b622b2ebd5d03a51a56055d22cf51099247b14571e0040e2`  
		Last Modified: Tue, 17 Mar 2026 02:57:30 GMT  
		Size: 145.8 MB (145806979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243b80f305d4e849340c9872ac59941d3f2dd190a965906b3407573a48791957`  
		Last Modified: Tue, 17 Mar 2026 02:57:28 GMT  
		Size: 16.6 MB (16629471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb4837b2e9c16e4646c321eb8b2288cb1a3490a86b0ae3841434719d98b9343`  
		Last Modified: Tue, 17 Mar 2026 02:57:27 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ee766a6cf2bba4ffc941bba6f3cad77b8427cf6220ce45a55f4b846739726107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d3760695ddd7d3b4d6fa88bdb01a5d13cbe4eacf9d799da0599c5ad00c98e3`

```dockerfile
```

-	Layers:
	-	`sha256:273456af4ed41a4d1116e3ae2f08604a0a68d3741864e0f13d4975fc7843b592`  
		Last Modified: Tue, 17 Mar 2026 02:57:27 GMT  
		Size: 4.5 MB (4506003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8e58c7ad0f61f477cc5d989d54ea8e88a0b72c7aff69fdb49182e987f450d3a`  
		Last Modified: Tue, 17 Mar 2026 02:57:27 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3aaf13701c2a93271094c4a7972daa11cd4f56b8182cb47a85d73dc67557f3ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215881523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8a48e51abe17d33d413727fb38e7125359ddb84896d190d8658ff80e5a53f7`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:01:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:01:09 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:01:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:01:09 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:01:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:01:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:01:24 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:01:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:01:26 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:da8e260297fdb91b3f012b26dd982feb43d0bf977ff8adeb7a850ef9c5829770`  
		Last Modified: Mon, 16 Mar 2026 21:52:51 GMT  
		Size: 52.2 MB (52247254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20829c531ccf7961d65e4bf67f36a1cfa3ab4373abe8106c497c2da606ed900`  
		Last Modified: Tue, 17 Mar 2026 03:01:51 GMT  
		Size: 142.5 MB (142500035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dce4d83c91df7ad66a85140c4144801ec2f17978a191be8134b4b52d1b157c`  
		Last Modified: Tue, 17 Mar 2026 03:01:48 GMT  
		Size: 16.6 MB (16616459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5876b88306675d374ee6e750f310c8e24ccbe490bfd717abf77b6a0cb9cacd`  
		Last Modified: Tue, 17 Mar 2026 03:01:48 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:be3a4994425332ad662eb707612ae39b601b6c125c5015220b0da44006577378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec85a2b97fc197d1f465c83f60b1b9abbd5198d5106c1e5ce8b80a646d0b3e26`

```dockerfile
```

-	Layers:
	-	`sha256:06ac6d2b23647a1df6b31f20017e5f58f566c6070f064637132c2a4b6c56cb57`  
		Last Modified: Tue, 17 Mar 2026 03:01:48 GMT  
		Size: 4.5 MB (4505595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6348836f77572957c20e2e2d48dcba55cdf0bcd95ee54b4b83c355075643ec8b`  
		Last Modified: Tue, 17 Mar 2026 03:01:48 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json
