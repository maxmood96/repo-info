## `clojure:temurin-17-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:c871991b9597dc9aa7d27884b0c7b70ff1719d91889699aa232cf67ec707b4da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c25bfeeafc2da7f0c2243fbb6c4d073d823b4e19998dd18554ddbb7f2cc7b2ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195743222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a80a801587a7cc9493bd11ab5a0f4953373e3758484a608b4fc7f6f58db2030`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 02:41:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:41:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:41:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:41:10 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 02:41:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 02:58:04 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:58:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 02:58:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 02:58:18 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 02:58:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 02:58:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:58:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:58:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec577430fa14586a2a8e706c9cacf118b21ccf274c641833d49f70595b30c41d`  
		Last Modified: Tue, 17 Mar 2026 02:42:09 GMT  
		Size: 145.6 MB (145628435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71852c8580baf1bd858cfee8afcc05b40a9a97e87eecb1eaec5897c71b89a16f`  
		Last Modified: Tue, 17 Mar 2026 02:58:34 GMT  
		Size: 15.3 MB (15338830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da311e9d46172fa8aa36a7962226e08cc9890b4377f7fcb70a3db9d71478b3f0`  
		Last Modified: Tue, 17 Mar 2026 02:58:33 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ae53e5fb8427c5ea7b29ed75b2f279fe35711a8ac9f7aa53f987f33c9f3ce6`  
		Last Modified: Tue, 17 Mar 2026 02:58:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b08c648b05635368d88636f692ec8976c58a8e402eb9596013fda26eefb9f999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3045985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7ef5e31c5ad429479fdb9533c7a4795312c5b0601d11de301deaa7063e7d6f`

```dockerfile
```

-	Layers:
	-	`sha256:d34b0eeba031f17fef18377459df6a35cc291b8bf4bd9145df8489ec4ffd1fac`  
		Last Modified: Tue, 17 Mar 2026 02:58:33 GMT  
		Size: 3.0 MB (3027582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daf0b026fac38e3b1038bc85696f79c96acff54070503d0d9e354cb59ddc9d03`  
		Last Modified: Tue, 17 Mar 2026 02:58:33 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:06c0540e895ec12797457a44d86a9ab4a885b387ac24937718889bf8561a6426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (193026140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78569b1ae0e55d3840f2abd541ccd2f9f099e3a0d4134e4fe4ce1b7ed7be6fa5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:02:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:02:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:02:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:02:44 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:02:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:02:44 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:02:59 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:02:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:02:59 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:03:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:03:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:03:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:03:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8427a02fddad016371ae1795fde2a5efc8c2bec67b92490e5b8f0e49491123af`  
		Last Modified: Tue, 17 Mar 2026 03:03:22 GMT  
		Size: 144.4 MB (144436219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e445f92e66553071ed8134dae8effcc09b20e84f2fdb22f01a3b2ea32def558a`  
		Last Modified: Tue, 17 Mar 2026 03:03:19 GMT  
		Size: 15.3 MB (15327206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3382edee14fdfa042aeaf6e2fcd2c5947e84b826e26f03f4579a5f9f39f6e251`  
		Last Modified: Tue, 17 Mar 2026 03:03:18 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0111dcaa3008ee8216d28d6883812494fa340f3e773617c49ddd34339f01a5a1`  
		Last Modified: Tue, 17 Mar 2026 03:03:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7120424e85feb25c02afef28e6e73350d1fe1f49d40e0c50c1b161018f88f99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3045715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a602cb7e7bd7d741e2122bc671e31c8b27cafa379a28f47bd208e11724dc87b`

```dockerfile
```

-	Layers:
	-	`sha256:ec3623142f29be217ccf9e4359a4525dc1db1007572c1a4a124c56c3637b2aae`  
		Last Modified: Tue, 17 Mar 2026 03:03:18 GMT  
		Size: 3.0 MB (3027191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d208e1d88b101489fbebb78e97ea1b7ad86673938a195e5a377469a159c9581b`  
		Last Modified: Tue, 17 Mar 2026 03:03:18 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json
