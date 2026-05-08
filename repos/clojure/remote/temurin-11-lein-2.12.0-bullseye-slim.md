## `clojure:temurin-11-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:f109be886f334534d971900f9a7b0ad8086afb26f6de5d2c6634be4216c5f523
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a8961d1759dfaaa33c3a9c093c718bac4caa566af4561b165ec3f4942836756e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196000691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab98e1504f95abc58dd33826fe273eb9e38673b1db3f958335da3a99a8b33043`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:06:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:06:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:06:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:06:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:06:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:06:18 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:06:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:06:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:06:32 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:06:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:06:33 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a6ae4dc4731fc00c215b9baa7c42405100db9aa74941c672de144cbbeb4a7f`  
		Last Modified: Fri, 08 May 2026 00:06:53 GMT  
		Size: 145.9 MB (145886193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ecbacc6392f05f5f320a50e99afb43ef8148ad7af4cd19664b7ca8757a1688`  
		Last Modified: Fri, 08 May 2026 00:06:50 GMT  
		Size: 15.3 MB (15338829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e07cce2aaabc41c95b604f96ef562c6b10e2d380362491299ff1341d647ae3`  
		Last Modified: Fri, 08 May 2026 00:06:48 GMT  
		Size: 4.5 MB (4517703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:14851d1921c1587b188c721b3ec84709c343be643a729918052d098aeb56a87c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43db445793a754a33e68102a8ebd0d034b359064094f20abb1f3c205c476592e`

```dockerfile
```

-	Layers:
	-	`sha256:bedc5bba46691b72cfd7a654fc201dbb4eba06583b422d1c689875267e98bf1d`  
		Last Modified: Fri, 08 May 2026 00:06:50 GMT  
		Size: 3.0 MB (3047725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74aceb60113261a369f2506ce110d51e19cb115f0dea68294523a054e74b5fc4`  
		Last Modified: Fri, 08 May 2026 00:06:49 GMT  
		Size: 16.6 KB (16565 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ab2fb7020352ac9f6e8183b7cd51ffbc67b5421a9cbb87aa537c127103a42da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191169684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d02c29613ef7397b17906d20208fa69976d46b8bbe51d771c18bd4c1491b9c5`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:05:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:05:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:05:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:05:24 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:05:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:07:52 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:08:06 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:08:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:08:06 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:08:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:08:07 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34b072670b8fce1894153d324600f78931e1238be7df1ea72a6a0512570fb79`  
		Last Modified: Fri, 08 May 2026 00:06:14 GMT  
		Size: 142.6 MB (142582245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d155a1ea3b8112d3acb2776b0688e9fa3085b8036c46da8bca1d6642ce26e81`  
		Last Modified: Fri, 08 May 2026 00:08:16 GMT  
		Size: 15.3 MB (15327180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24ef4526cc61ab19485d75a4b3525b7c9aef6f9fbaeffefff5fe8c2f00adc9b`  
		Last Modified: Fri, 08 May 2026 00:08:16 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:51b62296598b7e8ad3ba319f7ea5154e43867a8191a723dc542115ca348018a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da449f90373a0468bf4b158fe326fee50208267a2293cab8b510eb0c1f7019c4`

```dockerfile
```

-	Layers:
	-	`sha256:a3fc0be608d274ba600733cf3cf8579a227781a6c81674bf4effd693b8ec7530`  
		Last Modified: Fri, 08 May 2026 00:08:15 GMT  
		Size: 3.0 MB (3047952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91fddbbc7541e5be53b0e17d9c647bbb51cc9e99b66691fad3209f59e57add6e`  
		Last Modified: Fri, 08 May 2026 00:08:15 GMT  
		Size: 16.7 KB (16687 bytes)  
		MIME: application/vnd.in-toto+json
