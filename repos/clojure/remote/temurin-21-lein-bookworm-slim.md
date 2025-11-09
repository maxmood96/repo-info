## `clojure:temurin-21-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:38315e141200e91cf9063048eed6a67f2fafa32846070142dd66247aebdef3da
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
$ docker pull clojure@sha256:360b69e0020d278e3fceb15f4fb4a5c7651d3aa3bcd84d4a23f2ff0883a276a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208330790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584371b6e354c80d1d916da7d2529d3c0f1b653daa252f3468215c0e85e671c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:43:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:43:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:43:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:43:51 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:43:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:43:51 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:44:04 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:44:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:44:04 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:44:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:44:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:44:06 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:44:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcc818df5a30a35f93ce6cde998cdc1a5b35ed1d95e6614dad1cbd36afbd0f2`  
		Last Modified: Sun, 09 Nov 2025 04:12:44 GMT  
		Size: 157.8 MB (157825965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c63013139bed00c4c882538a13d1c1e3ee0b0821a35144f59b0afc8800c522`  
		Last Modified: Sat, 08 Nov 2025 20:39:53 GMT  
		Size: 17.8 MB (17758075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec62e43106b9e43dc904ec3d92365106cc382f634f1894271fc8d7a0d9e60dd9`  
		Last Modified: Sat, 08 Nov 2025 20:39:53 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36ee7f4cd11ea13faf3fcf92c4a0d97d7d33de8585ceb8e4b1b5c950e546028`  
		Last Modified: Sat, 08 Nov 2025 19:29:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2484633367eee80699c6e14724bdda44b9fbfa3e562e337059fa487272ebe743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a34a8de963777ca27bbd65c9ea91edadec1a5447d96485ab51e3e3fadb6cbab`

```dockerfile
```

-	Layers:
	-	`sha256:b43cb3fd26a0fdf6247f9684c5089c99428ba48e9144c6e7c0ef1349283e8812`  
		Last Modified: Sat, 08 Nov 2025 22:47:24 GMT  
		Size: 2.7 MB (2731890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd73b3aa912244fcefc2e27c3b85391107487c0336540d4364b44bad43edb150`  
		Last Modified: Sat, 08 Nov 2025 22:47:25 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:28db36fe6c196a9521a8547a1767010fd6e2a95ce549f1e1c7bd6e831d048059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206319341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04c9647d351250a7091697c31d1af333be072d03765a339b8bbeeda4b137217`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:43:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:43:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:43:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:43:24 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:43:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:43:24 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:43:38 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:43:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:43:38 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:43:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:43:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:43:40 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:43:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8e8fb110f609ad31f3685c2eda665aa5903302f087df8bb0f19ef9c24f8c77`  
		Last Modified: Sat, 08 Nov 2025 18:44:02 GMT  
		Size: 156.1 MB (156107661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5b1eb82dcfa1e28267893faaab0aa0681546c4b3294aa1b8ec5f2de7e119f8`  
		Last Modified: Sat, 08 Nov 2025 18:44:42 GMT  
		Size: 17.6 MB (17591150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb2c6b0e4a23c1b5fd2f7a0e1cae598abafbdb41b88821abdc2da974d35b6cc`  
		Last Modified: Sat, 08 Nov 2025 18:44:41 GMT  
		Size: 4.5 MB (4517726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bfe76dcb159637fcdb124e27979f5b621f68016ba0d8ed6b21902d399bfccc`  
		Last Modified: Sat, 08 Nov 2025 18:44:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a1a893119c36abc68469255228905349b58536418f0c91d542916b7ff7d64beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da71926e496bf787173ae406a65de2e91b6623704cf7e3e76a9ee896d4e3240f`

```dockerfile
```

-	Layers:
	-	`sha256:2eb35912a38a4ed9a8ee1e47adcd30721b04a136c8696f78676bf2fd6f9aa098`  
		Last Modified: Sat, 08 Nov 2025 22:47:29 GMT  
		Size: 2.7 MB (2731505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd75275a3d2ae15dd342d2edd314651b9a5325b30990423ceb38babc121220a2`  
		Last Modified: Sat, 08 Nov 2025 22:47:30 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:9dc249340d86220e0b43ce4e0bf6115be297353750fd319a501edf0b621e3928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212489616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1d8bb1ea627da3a20386d09f270777767c3804d813e6e9267d5efadf4e3a30`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 21:31:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:31:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:31:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:31:35 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 21:31:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 21:31:36 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:32:05 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 21:32:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 21:32:05 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 21:32:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 21:32:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:32:09 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:32:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944218b16390f9d8d7ad4ec3d5e2b435f5ce7651679065a781dd9f5140c7a7e0`  
		Last Modified: Sat, 08 Nov 2025 21:32:50 GMT  
		Size: 157.9 MB (157942933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1ee7d03245aa51775ab2d7cf0cfddf9c1c93ae2ca2f010fcc7215a2a6a3a8f`  
		Last Modified: Sat, 08 Nov 2025 21:32:56 GMT  
		Size: 18.0 MB (17959626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d2c836dbbbac2dbdde7fea1a4d264db1ec9b3feae3e2303c9ccb5b89882ea8`  
		Last Modified: Sat, 08 Nov 2025 21:32:56 GMT  
		Size: 4.5 MB (4517722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f616e516d67b47e1c78538b92eb3cff38f2aec34f3c65f37d5f64eb7599b3c`  
		Last Modified: Sat, 08 Nov 2025 21:32:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0dc8f94151c515a1f4086a2ee7b073e41d6091267de4694dccf4e7630a497719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c5c2b4321be03d3a4af35f830c27b5488944ba49865900ac50fa886875e731`

```dockerfile
```

-	Layers:
	-	`sha256:bb3406938c48714e562388769d6fefd56d1fe9e2197865e6bdf540388436dd80`  
		Last Modified: Sat, 08 Nov 2025 22:47:33 GMT  
		Size: 2.7 MB (2733723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b9af282e2f92151d2cf52340896192362af819bf662ebc21ec96f8578cbbf0`  
		Last Modified: Sat, 08 Nov 2025 22:47:34 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:efc0addd68faed2956a7cded53128c6c2100ea5da324b4b121fe8e24b0051b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195892365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78635fd8b6c867ed08c653f190310df922a82122cef4f9f64e82df928bcf9e37`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 20:28:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 20:28:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 20:28:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 20:28:38 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 20:28:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 20:28:38 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 20:28:48 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 20:28:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 20:28:48 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 20:28:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 20:28:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 20:28:50 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 20:28:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179ec4598348efb229bf449e5b14947188b3aa2ce7fd6f3f7718376a0bd1679e`  
		Last Modified: Sat, 08 Nov 2025 20:29:16 GMT  
		Size: 147.1 MB (147069879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5686c0844c8e7297df2a9485ca44f6c0b0fa0db5c2b56ba79315ff9f3b7046b2`  
		Last Modified: Sat, 08 Nov 2025 20:29:23 GMT  
		Size: 17.4 MB (17419761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd0bf786cafd252795a34a3b5d288f077cc56cf23125d1c23b2f31774979536`  
		Last Modified: Sat, 08 Nov 2025 20:29:22 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af366f5653a9c8c94d20b3983a261eba3cb1b33a172d51bd07c255aa035f569`  
		Last Modified: Sat, 08 Nov 2025 20:29:21 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4f0f977c33167b2626cec4f7cfc79eae1fd8123a51aed6d68134ec7497a79b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:203304c1cb46f7bde8d194b8f31ca0e1c04d08d6b223c39d70ef03334d73b7da`

```dockerfile
```

-	Layers:
	-	`sha256:81c49b2a80614147c3e65698998bfc2c45979a465cc74c1beed8ba3f64bacc15`  
		Last Modified: Sat, 08 Nov 2025 22:47:37 GMT  
		Size: 2.7 MB (2723704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7b15827caf4be60652c1ce84d7ca1c866c61cb4df5bd547851a3ac513a001bf`  
		Last Modified: Sat, 08 Nov 2025 22:47:38 GMT  
		Size: 18.4 KB (18402 bytes)  
		MIME: application/vnd.in-toto+json
