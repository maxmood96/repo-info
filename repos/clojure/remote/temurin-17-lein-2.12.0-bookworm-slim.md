## `clojure:temurin-17-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:dad4fd7b19f69197cff52a33d1fba45f0f52e8944daa5be426366efa393762b2
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

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:474960ed0d7e4964a12c27032d4d57ecb6c60ec6217ee327275dea649dc7a98d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196417415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2671cf995740936df5b6ddee0d4feb325d1946ed4b972e2c72bf672d4bbddfae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:58:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:58:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:58:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:58:31 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:58:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:58:31 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:58:45 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 19 May 2026 23:58:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 May 2026 23:58:45 GMT
ENV LEIN_ROOT=1
# Tue, 19 May 2026 23:58:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 19 May 2026 23:58:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 19 May 2026 23:58:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 May 2026 23:58:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afe2f1ab48480be1c2c845d626639e18ad27a9ee9a4dca61bec50af4c07e3ad`  
		Last Modified: Tue, 19 May 2026 23:59:07 GMT  
		Size: 145.9 MB (145905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e171e9adcdbb13e7292a35512840a2484a0d6dd6d6bc0945da1c7b7895836835`  
		Last Modified: Tue, 19 May 2026 23:59:04 GMT  
		Size: 17.8 MB (17760234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ab59087f49484be4be7f75c67d48c4e8a9aa77cfe92c3bdf25e8538e8b402a`  
		Last Modified: Tue, 19 May 2026 23:59:04 GMT  
		Size: 4.5 MB (4517730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cf803f5f2c0845a6686e63d489e1edf4a80592bb45611411acec9a043749ce`  
		Last Modified: Tue, 19 May 2026 23:59:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e6c59d5f1f8df2a557c8c3b5f62de3ca161f0deeb7dfd6826ac4877f24217b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2749252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fab029e7451ca6d8dcd6fb85702b040164cb9f824ad276dea1b9e7fb6c4e3cc`

```dockerfile
```

-	Layers:
	-	`sha256:9dca5a77af316200c051ee87c8c1ee92d2ecbac0c9942e280890cc356a8ee5ce`  
		Last Modified: Tue, 19 May 2026 23:59:04 GMT  
		Size: 2.7 MB (2730695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aff86acb0bc7b5e90808975cbb475c0e9a443dbcb0a2703ee1c4a43b6fb854ba`  
		Last Modified: Tue, 19 May 2026 23:59:04 GMT  
		Size: 18.6 KB (18557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c02b0d93d92fa22602a3c1fd86f52a9b6f81f4b7bea8d43c050483a85530475f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (194951324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87cf3920333095e3a7bfb9597e26ed745834db1ccdb84aa26ffba0765cf5e9df`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:05:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:05:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:05:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:05:27 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:05:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:05:27 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:05:41 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:05:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:05:41 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:05:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:05:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:05:43 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:05:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934caebe9680a6a565708a8a13ef7923d19139889f031c936510703be0a68ff5`  
		Last Modified: Wed, 20 May 2026 00:06:02 GMT  
		Size: 144.7 MB (144724358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088ad466ad1bbc340dcb29123efb8720b28535385f0b0fcea07ac842b4f7107e`  
		Last Modified: Wed, 20 May 2026 00:05:59 GMT  
		Size: 17.6 MB (17593767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ee1fe5fc83f6b8a311afff3de6fa56f9e2de15bc745dca9b7d6011aa5088f0`  
		Last Modified: Wed, 20 May 2026 00:05:59 GMT  
		Size: 4.5 MB (4517728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f40036888e6ca475b3cf8d3b8e8b42ecf560621808fe8c3536fcecb96f0c4b`  
		Last Modified: Wed, 20 May 2026 00:05:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9e0974e3d2c80837257b2a8220f118fc8c4d9acc0487d6a6bf4f2bc0cc3e0807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2748988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a87766c632851bcd392fc24175ec67441b230cf46750ca681e272b4bf71d394`

```dockerfile
```

-	Layers:
	-	`sha256:5aa6623c3b471333fc34c1ea18e8725962ac4f534ee3b24aaae5593105c30328`  
		Last Modified: Wed, 20 May 2026 00:05:59 GMT  
		Size: 2.7 MB (2730310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddfecbf09d950626a874c753a10677c64909fbe1ba2bd0c6c88a64272b4fe61f`  
		Last Modified: Wed, 20 May 2026 00:05:58 GMT  
		Size: 18.7 KB (18678 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1ac68808498d4b48c015cc9e3b0f650d12b5817e27e03ebc6a2755ad45f61603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200323373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76daa01cc459e6ec11e96b80d648105a52b4226c04410a35e4d387994692c2c5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 05:54:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:54:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:54:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:54:25 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 05:54:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 05:54:25 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:54:53 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 05:54:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 05:54:53 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 05:54:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 05:54:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 05:54:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 05:54:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6633021a99f451d585b657cbca0d3fbc241ffb487dcadb3e2ad6afd10c777642`  
		Last Modified: Wed, 20 May 2026 05:55:35 GMT  
		Size: 145.8 MB (145766094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235dc93bf338b8a2fa1703b28351190a08d373b4c5230e123bff8e25b092f8d1`  
		Last Modified: Wed, 20 May 2026 05:55:32 GMT  
		Size: 18.0 MB (17963351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084a80655d3522c46078131406f30839be6fedb688a9c68f0db0c993d0506f43`  
		Last Modified: Wed, 20 May 2026 05:55:31 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a7fe2d7f58494436ad08661d2a5fa3481c7fd74b0df195dbddd606a0c8dcba`  
		Last Modified: Wed, 20 May 2026 05:55:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5078660531e646d82a4cefabf835268de594bb8cb8942f0f8e31adbcdcb919c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32bcbf9f584e2e2169163041b57e72882304e705c5437d1096c4c2182aaa659e`

```dockerfile
```

-	Layers:
	-	`sha256:a69cdefc45130805cae1827d300758450a630e48d9f4a0b62f0a530d1a4c07df`  
		Last Modified: Wed, 20 May 2026 05:55:31 GMT  
		Size: 2.7 MB (2732528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eee6b2b063a2eb23ca152faa06566a28b91fd9b1802c7b1e33beb488a307f70`  
		Last Modified: Wed, 20 May 2026 05:55:31 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:70f6b11f1c5474744acd45a9d08c4a46d32d27b9ea91477abbb1140ed644bba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184740872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639bdaf761e7a0cc9c22a80371ee57877deb380143fb92d1b2d27a5e15d8a409`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:43:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:43:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:43:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:43:34 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 01:43:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 01:43:34 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:43:47 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 01:43:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 01:43:47 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 01:43:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 01:43:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:43:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:43:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98599326617712457c00a2d8bdb39c7b97547607326c3b68b05c08a2af0c0e96`  
		Last Modified: Wed, 20 May 2026 01:44:14 GMT  
		Size: 135.9 MB (135910447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698aa721cc2bfbe558702a62a65353f417b9f77ef6729fc644e84b3a9c7fc7fd`  
		Last Modified: Wed, 20 May 2026 01:44:11 GMT  
		Size: 17.4 MB (17423644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b7b12af68085481123157f134a43ec5632ffae95bb79fd0beac0cc78a2a165`  
		Last Modified: Wed, 20 May 2026 01:44:11 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf71520b0b7012feb8f186e9c6332e686b26d1b360bf82ba6a313e51587d4e1b`  
		Last Modified: Wed, 20 May 2026 01:44:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:14efbcf6f7e85a99cd7bc37a139446fa4ea8ad58850db0145af13f299eb783f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2741066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d03f9ed645643b834e8ccde2c96a66f4f57066ad949c2e2ae3c634f0a3714b`

```dockerfile
```

-	Layers:
	-	`sha256:44fc351452ef375b9ca63cf0103ad00b34ab1be636a236138b8b2020e8fa5ffe`  
		Last Modified: Wed, 20 May 2026 01:44:11 GMT  
		Size: 2.7 MB (2722509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45e20837f2d3d1067dbc327833e7e09f7a4756a8efbcc0a9066a2f3e2bcffa05`  
		Last Modified: Wed, 20 May 2026 01:44:11 GMT  
		Size: 18.6 KB (18557 bytes)  
		MIME: application/vnd.in-toto+json
