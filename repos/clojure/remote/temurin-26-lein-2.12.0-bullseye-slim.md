## `clojure:temurin-26-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:ff094dec0d433fe1ba329218feac09cd63251c7dcaf6a8344083bd3d6b827a1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3f160bba60270a17801869e2565d94e77d61c0ff02a0d91ebb0bb7d33e1c8409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144570692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b887b79e2a1773a588a6120febcf9c57765ad76764ac1eceeef7242d7b8510f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Thu, 09 Apr 2026 23:36:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:36:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:36:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:36:50 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 09 Apr 2026 23:36:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 09 Apr 2026 23:36:50 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:37:03 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 09 Apr 2026 23:37:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 09 Apr 2026 23:37:03 GMT
ENV LEIN_ROOT=1
# Thu, 09 Apr 2026 23:37:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 09 Apr 2026 23:37:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:37:05 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:37:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6907d1370d29504cd7bd57e733bd9fe1155e059858a8a5ed43478c654b743b`  
		Last Modified: Thu, 09 Apr 2026 23:37:23 GMT  
		Size: 94.5 MB (94455691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fedbb4c50827b16814ef982c7a020cdca3e02ae8f249920de47f45810d8be6`  
		Last Modified: Thu, 09 Apr 2026 23:37:22 GMT  
		Size: 15.3 MB (15338808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465e555a4614290ca6ee100928aa141e7aac27ee1c3d4a354b6b259e390ae7a4`  
		Last Modified: Thu, 09 Apr 2026 23:37:21 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5aced3f258246578e141a2deb802a27380bf8ed7fda34d7955253ddfa330e0`  
		Last Modified: Thu, 09 Apr 2026 23:37:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6137a23593cac43b929713f3f35015e2e7b29fa21f6c5fef079ca4794e50466e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007ed8008c425092e37724baa200fe7c5b016e918e2c1274760e196c2fff81bb`

```dockerfile
```

-	Layers:
	-	`sha256:816e6762ed1d0601741da52c883d3a90e719e0bc9ebaf96d2cdbe8242aafcdaa`  
		Last Modified: Thu, 09 Apr 2026 23:37:21 GMT  
		Size: 3.0 MB (2993086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cc3892946658f4c8fa1df3892f717340d3929167b858920224e856a45b20cbf`  
		Last Modified: Thu, 09 Apr 2026 23:37:21 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9dd556dff0e16479fb98684f919618d59b180054dcf2f72e7b4c0ac8312c2084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141985259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb1070ba233f426706d1fb40813e18c70d22228776d12eb004caaf014930940`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Thu, 09 Apr 2026 23:36:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:36:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:36:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:36:33 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 09 Apr 2026 23:36:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 09 Apr 2026 23:36:33 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:36:45 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 09 Apr 2026 23:36:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 09 Apr 2026 23:36:45 GMT
ENV LEIN_ROOT=1
# Thu, 09 Apr 2026 23:36:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 09 Apr 2026 23:36:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:36:47 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:36:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8bfaa0d685d36f22775d52c39fe95a47588348eaf62171659bedaa54b9041e`  
		Last Modified: Thu, 09 Apr 2026 23:37:06 GMT  
		Size: 93.4 MB (93395164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a046c0cf45fec468f0b13b6d319e9bd1cf895c15db4217f7f36cce13d68bbc`  
		Last Modified: Thu, 09 Apr 2026 23:37:04 GMT  
		Size: 15.3 MB (15327230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628fd79d9742323d244b9abf099ede5701762c9c433d8d4d419980b9b8b4f11c`  
		Last Modified: Thu, 09 Apr 2026 23:37:03 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ef24978005d7b3aec3a577ccbe6d06ca8ad908e435a118f605cad252b5974e`  
		Last Modified: Thu, 09 Apr 2026 23:37:03 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:20bab74a75a3f16afbad2bffb74caeb23bdb892216eb3babec9d58519516c6c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c701efc37c37763f52a3a6611718a490f330214e07ed454f7fd620e27a5a1dae`

```dockerfile
```

-	Layers:
	-	`sha256:f6fc6cb89f6eca916a14dba88f084f6140e82d51f4cbc387e0e92043b4f10aec`  
		Last Modified: Thu, 09 Apr 2026 23:37:03 GMT  
		Size: 3.0 MB (2992692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336e817e7878d104a3aa1443f87d403c81df41c5e4ff38a88f0764fd0b872c34`  
		Last Modified: Thu, 09 Apr 2026 23:37:03 GMT  
		Size: 18.5 KB (18517 bytes)  
		MIME: application/vnd.in-toto+json
