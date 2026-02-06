## `clojure:temurin-17-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:bf378920c71b4279e0fe17b4b8df59bfb718572371cdd2e5dda6656a90a37045
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:74a4278cb4533596d6aec9e8ba38b86c7cab193c27336af1a08e6560ed97eae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195723580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7c002c5cd1367b70a974da8e3f07c2b295160980966690aef2495d70af3c41`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 22:50:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:50:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 22:50:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:50:29 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 22:50:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:03:45 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:04:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:04:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:04:32 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:04:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:04:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:04:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:04:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54a98841b33f8ca3d993ced94f26edf5b759dbee9efca70efac05975747b2c3`  
		Last Modified: Thu, 05 Feb 2026 22:51:30 GMT  
		Size: 145.6 MB (145628433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4652e8649419309682fe915e9beb4ec5f6d2a60cfb44404ac9410fcea8176361`  
		Last Modified: Thu, 05 Feb 2026 23:04:44 GMT  
		Size: 15.3 MB (15318717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46998df3631a0c69f419ef8605b6e3860359f7de2f8fc284c4c7281e900e49e9`  
		Last Modified: Thu, 05 Feb 2026 23:04:43 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799fe8b4989a2f8eaa4a1084f8632f7a8ebba352d7f16d6fb4975f5e721da67d`  
		Last Modified: Thu, 05 Feb 2026 23:04:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e4cda44f2f03954e377950e8dc52ddd4dea07065a70dbd87327f6365624d8c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3037565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed69263fa6efe4d6cd96f197754e173bfd7f6c3edae765f7296444eeaae69f0`

```dockerfile
```

-	Layers:
	-	`sha256:b9ea31248f4d902effcd397509a43b8c4197f8efc1a7e0c64e6829ca45cfc683`  
		Last Modified: Thu, 05 Feb 2026 23:04:43 GMT  
		Size: 3.0 MB (3019162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e011e3214a013343c28013be4264c6b6c3748accba22b557d97c7a0010be7b86`  
		Last Modified: Thu, 05 Feb 2026 23:04:43 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3eaad9a7251300b98b064af4de3355aee083b474154dd484f4fe3430a1e3818e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (193004623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18090d53ea74bdb8c5926abf3e14b480ec5c9baf558eb8e19d7329a497a3c8b9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:05:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:05:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:05:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:05:05 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:05:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:05:05 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:05:19 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:05:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:05:19 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:05:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:05:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:05:20 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:05:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a1569030170a2048665bfb0a42b6e258f3a7b85cabd14c56b13a0a8522ec3f`  
		Last Modified: Thu, 05 Feb 2026 23:05:41 GMT  
		Size: 144.4 MB (144436235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5038c664b54d84a011197500957dfcf5f01b60063be9c27369c06c13e1ad14c4`  
		Last Modified: Thu, 05 Feb 2026 23:05:38 GMT  
		Size: 15.3 MB (15305816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f074f9372442d484c26cd3e7aef0bfba999e928744bf4a30a82f7fbd900044`  
		Last Modified: Thu, 05 Feb 2026 23:05:38 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201d4e6c57f73cc8398cb541cf9df3fa75d0ca3a64499518a6c0c177a6537565`  
		Last Modified: Thu, 05 Feb 2026 23:05:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:40c434ecd1f550409b03672d665a46ffcaab4d0b4f755056b42c6b1bf5d4b5e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3037295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1ffaa5c031fb061c1bf78909de3176b3402f6edbdf32c5a2ce4366d44e3ee2`

```dockerfile
```

-	Layers:
	-	`sha256:5b0e0c56fb8c997f4985517d71c412e85f90c306d936787cb79216ffddb3f8f5`  
		Last Modified: Thu, 05 Feb 2026 23:05:38 GMT  
		Size: 3.0 MB (3018771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:238df86540df9d3c5df2ba031d93ecea6ff063e9bd80c6fa943725a7b45a168e`  
		Last Modified: Thu, 05 Feb 2026 23:05:37 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json
