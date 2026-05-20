## `clojure:temurin-26-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:89da8fa393ae504beed4cf2d5d374e09b40c672eb51ba71e1eb2497151fa53ba
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

### `clojure:temurin-26-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cccabaf613bfacb6353b3ee478519b86deb255e1801b2bb4cd2d41bc7f9bf1f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (145036296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67bd0fd4a06adfa6ba9313186356f770c2f5f34d44135322877e96faa327d9c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:02:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:02:00 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:02:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:02:00 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:02:13 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:02:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:02:13 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:02:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:02:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:02:15 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:02:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4542ff26284f1989b913d947ae2efcaacdda7679d9316ced316ab49cb4926d6f`  
		Last Modified: Wed, 20 May 2026 00:02:34 GMT  
		Size: 94.5 MB (94524332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b267328e39095374e35b2adac8810d4695a3c7c5051d94f567e90a9d577c19c8`  
		Last Modified: Wed, 20 May 2026 00:02:32 GMT  
		Size: 17.8 MB (17760280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0b170db0c539a52f5998a692e9318293b486fe9d73f5f08d367d7ad36a6236`  
		Last Modified: Wed, 20 May 2026 00:02:31 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5191aa7c2428d8e63f85d5a2956e445040b92fb02b098734a644221130a6de53`  
		Last Modified: Wed, 20 May 2026 00:02:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cae055a994db9787e4ca498e34f08cf8c511fd2aa249664e8e514219f97d4db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2714136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3624ab7b2a20d4a402e6c98fa187c452ff35312af723344895c695bdbb5469`

```dockerfile
```

-	Layers:
	-	`sha256:687fde6f816fcb7ff10ab11a85de114ce528cc133bfddaee417e5624f891f6b0`  
		Last Modified: Wed, 20 May 2026 00:02:31 GMT  
		Size: 2.7 MB (2695586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5903021f0b64ddc3047ee461816ed0dabd7ef55dd30383fe0d26ab0a1602b0a5`  
		Last Modified: Wed, 20 May 2026 00:02:31 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:43facea36ac47fb7bb069d8aaf6512a0151435d98e90b22d78ad73ce1210f0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143731368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc44518c3c89aa6724288c07790995a4da8f7b9f5a70e77591177971512c6e5c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:08:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:08:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:08:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:08:43 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:08:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:08:43 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:08:57 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:08:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:08:57 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:08:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:08:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:08:59 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:08:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d5e2199769bc7c8aaafdcef7768cb51841c656f185577782a7eeeae44bb87f`  
		Last Modified: Wed, 20 May 2026 00:09:18 GMT  
		Size: 93.5 MB (93504373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b9a8263d06f144526c63f5e1c370db6a6522791fdf406f79a4a7ae7db01629`  
		Last Modified: Wed, 20 May 2026 00:09:16 GMT  
		Size: 17.6 MB (17593804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad8cc4be3d1f79ccb838a266f4fc20342ba30a25713cc773f085b56ae16bab2`  
		Last Modified: Wed, 20 May 2026 00:09:15 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22928c5af464df0bf749f94ca2fc3b8b85de0e822e25235a07b174723ddad29`  
		Last Modified: Wed, 20 May 2026 00:09:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:83db69bcd3631aeda8da4c622155ffa131a7b89debc0df5a6f5c85670ac05595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2713869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21194b976ffd9958b83151676b8d64cc6e200128c890e0c698553113dd4c24f5`

```dockerfile
```

-	Layers:
	-	`sha256:ffe7eb3dcde88a4d6484a387c99453a44064c9cfd9ce3f1988a68d029cc871d0`  
		Last Modified: Wed, 20 May 2026 00:09:15 GMT  
		Size: 2.7 MB (2695198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a50e4ba36f3f50e53c8016abc79d33f4016668ea6d1bedac4b7b0ef6883d4b`  
		Last Modified: Wed, 20 May 2026 00:09:15 GMT  
		Size: 18.7 KB (18671 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f80ddb332c5264f3a5575e6a6b4d083f710af362e8669ac3b9590d91f0a03a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148459288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9b372c2d7bf4769ae7621a5b115c15b7311118d3d0b54381eb9bc2a0fe8d5c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 06:10:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 06:10:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 06:10:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:10:57 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 06:10:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 06:10:57 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:11:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 06:11:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 06:11:27 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 06:11:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 06:11:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:11:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:11:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97e0d4e70f345e6ec3f734a63e6f3053a7af5fb9379e888c145034be666b5f4`  
		Last Modified: Wed, 20 May 2026 06:12:06 GMT  
		Size: 93.9 MB (93902017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a53ed590e15078931a0125affd1730cc7b999b1dda4a403220bca4a7ec1b8b3`  
		Last Modified: Wed, 20 May 2026 06:12:04 GMT  
		Size: 18.0 MB (17963384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1e00d89e4828b2a36c3a8e88ab2b475b68ff609fbff355c3d0169dbda5b68e`  
		Last Modified: Wed, 20 May 2026 06:12:03 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9111e25c230de13bed95d6b43a49acdd234797824124ca5d0b51ae40a0d25e14`  
		Last Modified: Wed, 20 May 2026 06:12:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4ac044d3bcc1afed5bd56d0f69ed3ec0f724513968854d7fa7bdbf3a231ba6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9d91db6d3db63e8627630be8e71e8456a656c8cb74ff74a52c6c64acf903a7`

```dockerfile
```

-	Layers:
	-	`sha256:bdfd000f62c33b477cd51c0b3612305f39e354bce719cda338a377d573c3e9ba`  
		Last Modified: Wed, 20 May 2026 06:12:03 GMT  
		Size: 2.7 MB (2681355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a1caf27546948bfb60616f8683098e7ae0dc41e3ab358cc8f8f3e2573b26b7`  
		Last Modified: Wed, 20 May 2026 06:12:03 GMT  
		Size: 18.6 KB (18594 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:03640a2fdc0f3761b1a14f56d636d722abcafccd292e48c14e74e1f62b7bd02a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139367466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f3bd6e8015d81170443272feed1951d7301a6d5c6bebfe5e2741be630798f6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:49:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:49:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:49:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:49:15 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 01:49:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 01:49:15 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:49:26 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 01:49:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 01:49:26 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 01:49:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 01:49:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:49:28 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:49:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c29118544f59e703ad98367e9fb39137130383fc3cb03728d1b9b2d61a0ba20`  
		Last Modified: Wed, 20 May 2026 01:49:53 GMT  
		Size: 90.5 MB (90536968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae882ad36a4a4aa4e94541f67636294a5c5174ce03abf7ac26e3f02018129a55`  
		Last Modified: Wed, 20 May 2026 01:49:51 GMT  
		Size: 17.4 MB (17423723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a318ab7899c5d8970e44b1d95ffee96b595d9dca61e6fc80283f1c45d81345`  
		Last Modified: Wed, 20 May 2026 01:49:51 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d97e16aeb316ec8722a8a6a8e5b79a451a1907761a2e9f8c755a686c9d744bb`  
		Last Modified: Wed, 20 May 2026 01:49:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9e1436718ac11dd8a98cfe7de06e4a3f2fb0a360ed9b084f9204313a4f7b8f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afc0c1520486e6f3cd7fc6ca7315d02b9809e8eb85a0376f12f4f502091d466`

```dockerfile
```

-	Layers:
	-	`sha256:ce34dd428f060091ce319b549bab30393903959d815ca8819a1384ba54275015`  
		Last Modified: Wed, 20 May 2026 01:49:51 GMT  
		Size: 2.7 MB (2672586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fef5f86d611fe80e3fec63bf3bb84d147d444382dd4a093468c35e8071551892`  
		Last Modified: Wed, 20 May 2026 01:49:51 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json
