## `clojure:temurin-26-lein-trixie-slim`

```console
$ docker pull clojure@sha256:e9fa9b3032e775551164a1edcc1f41ed3798893938b8e1225681b0ee70f80a43
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

### `clojure:temurin-26-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:46f4e41b5d6149a3b259ec1ccc6173c3162333ffad146da6c159099ffbcb95bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145270748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e981ac1ce59a8dc6adb13301bef10b82eaa962979a82fc761651392f559aecd5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:36:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:36:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:36:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:36:57 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 20:36:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 20:36:57 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:37:13 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 20:37:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 20:37:13 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 20:37:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 20:37:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:37:15 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:37:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5f40d497db616e9e8bab62f0d3c53265bfddc76ce642df21622b30556e2a40`  
		Last Modified: Fri, 15 May 2026 20:37:34 GMT  
		Size: 94.5 MB (94524372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e3bf96e9c3f054255fee3367b563ddcd5e92b1fb7445a299ad796e6e898020`  
		Last Modified: Fri, 15 May 2026 20:37:32 GMT  
		Size: 16.4 MB (16447979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf172503137bd46d77e9861b966987225293a7178e6a8a612a89f3b4eaabf4a`  
		Last Modified: Fri, 15 May 2026 20:37:32 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdec3e9ab248823742cf6b316556a373490180146d6e3ad78742cabc21a6a783`  
		Last Modified: Fri, 15 May 2026 20:37:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:17cbbe2ff7f0ab60f1e535c6745468f78627b5d6ade329e3309e023e02313d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2348840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a1ab5e49b5f60a74d63255012649682e8465ab51a8d37872b4844134045a68`

```dockerfile
```

-	Layers:
	-	`sha256:dc92048371edaa1d46db8b8926a33fdc809734a0d705fcb97d8ae84f90f1b819`  
		Last Modified: Fri, 15 May 2026 20:37:32 GMT  
		Size: 2.3 MB (2330306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:527531d37be902c0fafcff3bec1da24b7182d7a5c38940258b5c9c604ba9c48e`  
		Last Modified: Fri, 15 May 2026 20:37:32 GMT  
		Size: 18.5 KB (18534 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9280ee2a618432f7a168de2f40cf97aba3504eda7ea5f2ee1c0c613eab6ea2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144580211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4866940e5e001150e7718ece77385053ba585ac678c2e23dcf60e00e12e458ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:36:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:36:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:36:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:36:40 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 20:36:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 20:36:40 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:36:55 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 20:36:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 20:36:55 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 20:36:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 20:36:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:36:57 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:36:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0d6f29a06c87d2da8b37558e582208fee2d182d8c68e104eb4edaab6d58eba`  
		Last Modified: Fri, 15 May 2026 20:37:17 GMT  
		Size: 93.5 MB (93504423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b36e06d8c539b880f6dd264a678345f6d53f0cb2e6f055458d50b492ecc5b19`  
		Last Modified: Fri, 15 May 2026 20:37:15 GMT  
		Size: 16.4 MB (16413991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e83da7c834a5cc661c40b69affc177b5a3f07e9c966c50dd586288b0964c0f`  
		Last Modified: Fri, 15 May 2026 20:37:14 GMT  
		Size: 4.5 MB (4517726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d781f4943f8530df6d3c04948078176a2354e7cacec266d9f407418349a909d3`  
		Last Modified: Fri, 15 May 2026 20:37:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fd69efc255ad23bc69741f96d31e1aed33f42d86636d9efbd00a240b36cb5246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2348576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c13e09ea0720831794684c683d42adf11e431e48db6ff91952c115b2aeb7a8`

```dockerfile
```

-	Layers:
	-	`sha256:1046a10fb157b8f9fcb0433f0a32b09fa9bab1e5db9575f44fca6c8fb517c9ad`  
		Last Modified: Fri, 15 May 2026 20:37:14 GMT  
		Size: 2.3 MB (2329921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9ee80ca79e5d6198e0bf3bd6e8113910869a46d41dcf498cb8332cee25b592b`  
		Last Modified: Fri, 15 May 2026 20:37:14 GMT  
		Size: 18.7 KB (18655 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e0bbeef1005d6cdfe50ef7c2b62ad7142c8c34861c449ed35d98a3fba58d2ac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148503691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f6579cff2df26646d7e20246e52701ee7904495a4509292188b911196d70d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 21:48:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:48:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 21:48:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:48:47 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 21:48:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 21:48:47 GMT
WORKDIR /tmp
# Fri, 15 May 2026 21:49:24 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 21:49:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 21:49:24 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 21:49:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 21:49:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 21:49:28 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 21:49:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f8ab13e6d21adc6f6b5e2937ae339405e46ec097e90a97ff0de0b57189e749`  
		Last Modified: Fri, 15 May 2026 21:50:11 GMT  
		Size: 93.9 MB (93902067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55bf8dcd0ca0858031094124914e624100604d684fb4938d6fd0c53e31696f7`  
		Last Modified: Fri, 15 May 2026 21:50:09 GMT  
		Size: 16.5 MB (16485388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b0b6bbcb2bae1403bcbf9a8ede8470b2693553977dfca2c1a946074868b0b5`  
		Last Modified: Fri, 15 May 2026 21:50:09 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b4665ade97a3224477bf33edbbed97acdad9ede06e99635b939c13cacb642c`  
		Last Modified: Fri, 15 May 2026 21:50:08 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d13f7741ea133bda692a9333929bd0eef95510e0e08739116027c4c01250cad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6691a3e3aa497d842953add456ce9b1451e4e09b526b55cc7bd4f275ab87d654`

```dockerfile
```

-	Layers:
	-	`sha256:3da8b4c6e0320a9743e0dad3630056f7318b8e568209c3f7b87a4b0f94eef0c5`  
		Last Modified: Fri, 15 May 2026 21:50:08 GMT  
		Size: 2.3 MB (2315222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b878c4a24532daf1ac383568dedad60a941416aa01ae3bd049a391be01a01523`  
		Last Modified: Fri, 15 May 2026 21:50:08 GMT  
		Size: 18.6 KB (18578 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:6ccd4aa229b3454593900a4dce4889dedce359f04c7c7b65034f62abbab60874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141379415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e25379bf81467cfb1820c08ab7daae42e6dbd107ae0c479555c79d6288987ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 21:29:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:29:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 21:29:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:29:37 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 21:29:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 21:29:37 GMT
WORKDIR /tmp
# Fri, 15 May 2026 21:30:17 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 21:30:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 21:30:17 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 21:30:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 21:30:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 21:30:21 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 21:30:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647b934f9a56641ef83dacb057c0278ee00e478122b936708e1068495d190c55`  
		Last Modified: Fri, 15 May 2026 21:30:52 GMT  
		Size: 90.5 MB (90536963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a262aebe9839307e28e1d026005ad4d74e363c08a2f11e3c50791fe0cb801472`  
		Last Modified: Fri, 15 May 2026 21:30:51 GMT  
		Size: 16.5 MB (16483919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2070193603748820aaeb8b8f69f35df64bcf5f022f2563da406dc2ddb0cc45f`  
		Last Modified: Fri, 15 May 2026 21:30:50 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bcee3c59e821079fda595f3d257aaca4746874001ef3b65c3b981387ab10c`  
		Last Modified: Fri, 15 May 2026 21:30:50 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5cb49e3f9de50a6497eaf29bdfc98d28f51fe96f601a0b016bc887e63116adf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf42aca3bd328ccabe4035fc5e3a12ae868ce8fd6f716c1c5e6b266c7c646642`

```dockerfile
```

-	Layers:
	-	`sha256:4664a8fb3ce63b2cc2d621e3c89e225c640fae13a84f41fefa780637d1ab8bd7`  
		Last Modified: Fri, 15 May 2026 21:30:50 GMT  
		Size: 2.3 MB (2311919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7201be9223de56b2232829add4c906467ff7178ce15e4e6bf8b0a52b752f8942`  
		Last Modified: Fri, 15 May 2026 21:30:50 GMT  
		Size: 18.5 KB (18534 bytes)  
		MIME: application/vnd.in-toto+json
