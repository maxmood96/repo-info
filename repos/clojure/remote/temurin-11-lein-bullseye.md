## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:8af6160afd5bd460b16ffd44d70aeed779659ef82b462cbf73578e0076487e88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b2b5db4f78a30cd2372d511f70804bdd82430cd364576ad66ca3f9c649906d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220109788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba867130a05948ff6a3aaa2007c7f6b4a27a48342b4f6539e6323696cd06b222`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 01:46:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:46:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:46:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:46:40 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:46:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:46:40 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:46:54 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:46:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:46:54 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:46:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:46:56 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:36 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b2218bac8400c21fdf33da7456b39d1086c049607c721a658052da68c66d21`  
		Last Modified: Fri, 16 Jan 2026 01:47:16 GMT  
		Size: 145.0 MB (144966605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56165bf66e365d9cf329a8340a96a087a88acdd896800e0443510048a320d8b4`  
		Last Modified: Fri, 16 Jan 2026 01:47:24 GMT  
		Size: 16.9 MB (16868967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb831c33a7673e49ae7ecfc035a38758ac5d4479501298aac9325c9b461bf0`  
		Last Modified: Fri, 16 Jan 2026 01:47:25 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cfca50bde13ba2b1f193a943e9d856fae0f85776d9d26c03622c2d7726dac524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4512711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:763c4126bb3a9d25158811235041a88b389b1ac2145bdc40135a14c65d9a00eb`

```dockerfile
```

-	Layers:
	-	`sha256:a4631ff150e3348e560e68d35b8ff2f9de1525f146532822ca731cd554dad64c`  
		Last Modified: Fri, 16 Jan 2026 04:37:57 GMT  
		Size: 4.5 MB (4496329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:360d26329657c95f69960c09bdc4261ee0aab3ba213f8bb2f17d0930cd3b79d5`  
		Last Modified: Fri, 16 Jan 2026 04:37:58 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bee59a3a5981393d8c05d62f3faef5d9b7d4db879acac23b9e7e49c7097c160d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215362691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c3932373d295e29e53598a63cc0267af50e3933a86ac21e82f7c28bd413169`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 01:50:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:50:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:50:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:50:10 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:50:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:50:11 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:50:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:50:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:50:24 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:50:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:50:26 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:52 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6411d8f9d23bfabae4f0f34639c3f429909054478e6998c41a1ca5ce1e29ca`  
		Last Modified: Fri, 16 Jan 2026 01:51:11 GMT  
		Size: 141.7 MB (141729881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0467509ee9b605cdd4da8f356132cef1fab03500740796bd8ac03d2071ebdff4`  
		Last Modified: Fri, 16 Jan 2026 01:50:43 GMT  
		Size: 16.9 MB (16857258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba83f0c5bcb31e713b4ae6c9012144b9be2c6919db590f9761e1b30bacf6981f`  
		Last Modified: Fri, 16 Jan 2026 01:50:42 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:666c5d7355eed67d9324c59dcb67aa67138b7812c2bdbd631fd4227e8a139d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4512423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d3ef3738b964e7b2bb7e1f8e16d6cf48842f16a8fe29a83275c11244c40adee`

```dockerfile
```

-	Layers:
	-	`sha256:f6e7df60921a464e08988a2f372308f889387a65245658b00bd9a894afe1b7f0`  
		Last Modified: Fri, 16 Jan 2026 04:38:02 GMT  
		Size: 4.5 MB (4495921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db5b677aa4dd76a290743c0eccaf845c8bdffd4ba462be56a6a86917ddd49f10`  
		Last Modified: Fri, 16 Jan 2026 01:50:42 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json
