## `clojure:temurin-11-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:13034f3e775e5344ac3f4a8b4fe6fcf63e44ff0ed3e098f8b7d5cd463c6aeb79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ddcfbb0111242f38d6f92d729476c99d59ff5455813e28da4035f4dc2308dd58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195921397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11ecf67aad77bdf2590267803c8745c6eed6670da42c42ec4dabf598d99aebf`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:02:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:02:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:02:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:02:20 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:02:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:02:20 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:02:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:02:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:02:34 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:02:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:02:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5005f1c10bfe40891fcf1dc7c312dae85700e0aeb9520d6b13563f7423653b40`  
		Last Modified: Wed, 15 Apr 2026 22:02:56 GMT  
		Size: 145.8 MB (145806832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8cc091317a785f55665e983b51279f2ab36ee784aca0c0ac0adc42a4feca34d`  
		Last Modified: Wed, 15 Apr 2026 22:02:54 GMT  
		Size: 15.3 MB (15338800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d52535042b491d71aff0da674276ce3e22268cd812dcf50da2cc7ba29d985a1`  
		Last Modified: Wed, 15 Apr 2026 22:02:53 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:550b450f321174901cfd5e01c98e651f07749fca5487e416f3f0a4d55bae6629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0247127ae2cafcb91e5aef661597503a96cb3928b1000553c692db2aa90bc76`

```dockerfile
```

-	Layers:
	-	`sha256:a090c19bd989f6a3bcf5e0a3a195686c3ade3a7b8c0b1ea57d9e22d78ad2033c`  
		Last Modified: Wed, 15 Apr 2026 22:02:53 GMT  
		Size: 3.0 MB (3047723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ad9ae85fcfd0ee1be29bac4b1550ba82cf7a738c651854e33f6ecc8a8f30719`  
		Last Modified: Wed, 15 Apr 2026 22:02:53 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6dfdc8c3894979275037afb449eb03f02fa8479397cc9748e50e315824d43fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191088274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9f7b7d3dfd00002270ef3ee269c5f4f9a8ba93779e43059299dc331bf8239e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:46:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 01:46:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 01:46:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:46:23 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 01:46:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:20:21 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:35 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:20:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:20:35 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:20:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:20:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bdb167dbf05cdc0c6dd7533e6dce5bd56d2d2c8ca8ca08e2fe3f0abd103f26`  
		Last Modified: Wed, 22 Apr 2026 01:47:08 GMT  
		Size: 142.5 MB (142500803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e733d3acfa643b640c3b25d051f4f2630723130cf6197b7ee86060503437fc`  
		Last Modified: Wed, 22 Apr 2026 02:20:46 GMT  
		Size: 15.3 MB (15327221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fdfa16d65ffe44747ae38f8efd834455023b594d661b66a16fd909febec51c`  
		Last Modified: Wed, 22 Apr 2026 02:20:45 GMT  
		Size: 4.5 MB (4517706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:510580b396df3ae897112dfae28e11078be085575eb5527b04e81cafefe23ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3063681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15cfe979b41211234056668bc4b649fcac75d5cfb0ac3cf577fc134df5196c10`

```dockerfile
```

-	Layers:
	-	`sha256:8583983bb36b0756882d586c44a591d949e7bf0a66f0f6333959d73d9b0b7126`  
		Last Modified: Wed, 22 Apr 2026 02:20:45 GMT  
		Size: 3.0 MB (3047950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:819290d8ebaff740a627bcdd99cac6f3cfa1ab96bbf2665cf584599c3e495c8b`  
		Last Modified: Wed, 22 Apr 2026 02:20:45 GMT  
		Size: 15.7 KB (15731 bytes)  
		MIME: application/vnd.in-toto+json
