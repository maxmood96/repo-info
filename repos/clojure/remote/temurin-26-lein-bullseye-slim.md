## `clojure:temurin-26-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:c978b77ccd0069536ef08ac67b692dcef91c6c625a4109b81dc0513d7433187b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:874dacc0933d8c48d7f71850ea0e025ce5998fb38aa93be6b291dac381a13a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144639302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd3492a41f85b1e0c98a42c1d44bafe623b879d765cb544531f3f43d2b44c89`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:36:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:36:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:36:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:36:26 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 20:36:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 20:36:26 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:36:37 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 20:36:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 20:36:37 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 20:36:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 20:36:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:36:39 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:36:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc625ab0122b565511ec9df67eb35a283228c6302fdb5fe92c8bc65aad7fa3d`  
		Last Modified: Fri, 15 May 2026 20:36:56 GMT  
		Size: 94.5 MB (94524372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e759e4d4c14a7340178c15be1618dce832192de02bf8fa7e356b8dd27fcb0342`  
		Last Modified: Fri, 15 May 2026 20:36:54 GMT  
		Size: 15.3 MB (15338792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4df64bec8b8b6c4d444ce2a77f977768acecd2e0e1533ab54ba69b0f55931af`  
		Last Modified: Fri, 15 May 2026 20:36:54 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba4765fc71528247202a0ba2ea296bcf022306fc27b219fd10a84eb10aa284a`  
		Last Modified: Fri, 15 May 2026 20:36:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3d9d20b52be75ce41923ca9d38c992cac295b84ef1d69683c3f53ff6b5f70cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3819296ffb05dd4dd96e3b0ef9fafc983b78f11fb69c6f9802d3ec57d3413c6c`

```dockerfile
```

-	Layers:
	-	`sha256:deba0b938a3570b3b63922a1b9183af9e1a2add39e2c39ede46b5a585eab0213`  
		Last Modified: Fri, 15 May 2026 20:36:54 GMT  
		Size: 3.0 MB (2993100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f7314424714ca30115d25c6bae5082255be7ea09d7e04daa3f2836cf5e486c4`  
		Last Modified: Fri, 15 May 2026 20:36:53 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2a2deb2221bd6786d78aeac59578de874fec9ac21fdfe70cfa2ca65af0767e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142092394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039e1db68cbf581f4d179db07a1a88c3cc9684986053cb712ffb5c74b58de4c1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:36:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:36:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:36:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:36:17 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 20:36:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 20:36:17 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:36:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 20:36:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 20:36:31 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 20:36:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 20:36:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:36:32 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:36:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37787db71b9cf81d1713c7469a8cf735ae87be523cdbd02c273fc22bfccdf1d6`  
		Last Modified: Fri, 15 May 2026 20:36:51 GMT  
		Size: 93.5 MB (93504415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadc9724875d0a6f8512bb1eae589ae4f130a9cbb447294a0f9834f5f7ef856b`  
		Last Modified: Fri, 15 May 2026 20:36:49 GMT  
		Size: 15.3 MB (15327267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d77fcdae7fb021b76955ebefee089628bde0d909e5f81d657fa6ef785fcb3fb`  
		Last Modified: Fri, 15 May 2026 20:36:49 GMT  
		Size: 4.5 MB (4517691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b33dcb4408619e0484f27ea44e56093001cdc6052d9f53353fe14dd4e15467`  
		Last Modified: Fri, 15 May 2026 20:36:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:32062061f3b57402227d0bfb18b4cc06662b3d542d0d903b63cdd7f853a7b834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0029ac73738631cc9e6b1adda70a67a840454f45fccb474a7b07a5dcc5bf78`

```dockerfile
```

-	Layers:
	-	`sha256:cd942025cb8820adf9a6dc0733d52b33df097519dae4c61c4189e7fc7f3895cb`  
		Last Modified: Fri, 15 May 2026 20:36:49 GMT  
		Size: 3.0 MB (2992706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02960a435f1188230260f5039c4cde5599e597f5b0d8c0b35e5a860b0c8dc028`  
		Last Modified: Fri, 15 May 2026 20:36:49 GMT  
		Size: 18.7 KB (18671 bytes)  
		MIME: application/vnd.in-toto+json
