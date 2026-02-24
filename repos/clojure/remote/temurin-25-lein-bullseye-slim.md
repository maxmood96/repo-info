## `clojure:temurin-25-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:415a21054a1175d8c227f0508f6ceb7abd2f4ac9759e3f368fe4f0d3f270bcfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1d4a6c81148fed5889d3df5881864676d5c0b04835dfbcab51d17101e6d0b0e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142371616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4eed014cf27d76f38128f9b5297f4a70941631e10f2dff192ba9ea3a23a8077`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:56:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:56:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:56:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:56:43 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:56:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:56:43 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:56:56 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:56:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:56:56 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:56:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:56:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:56:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:56:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d66a0c31209f75bf950c77c1bf4891076608710921a99c0088073231fb3d1c`  
		Last Modified: Tue, 24 Feb 2026 19:57:19 GMT  
		Size: 92.3 MB (92256282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df71a8daf2bff32c6fe9fe078430b8f2d0711e4a8cb8bf8fda8ea04bd83ef1b`  
		Last Modified: Tue, 24 Feb 2026 19:57:12 GMT  
		Size: 15.3 MB (15338790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d777e92947392c57cba6bc8110b3af59c7049538e91b76504ce52bc2402a4a5e`  
		Last Modified: Tue, 24 Feb 2026 19:57:12 GMT  
		Size: 4.5 MB (4517736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecd170a5ebb69eaee07e5183568c980155a3ea6e12504d103047d9c56119be8`  
		Last Modified: Tue, 24 Feb 2026 19:57:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6ff4de8c4f2274518c5fc68a80ec47c779d7de47f0a84d49ec05f65ca0c50e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3016324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f445f70d8a701e492c5959523ca7482344a6d4496040a8661d3331e110b50bc`

```dockerfile
```

-	Layers:
	-	`sha256:054295c433667d3210c1b0354371b455d6e3db99b041761ce4978654cd41b9be`  
		Last Modified: Tue, 24 Feb 2026 19:57:12 GMT  
		Size: 3.0 MB (2997266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a23b1e404de9a953bf89dcf91bf58a4cd3a609ebf5b79a3c29c5ec6ee71a8357`  
		Last Modified: Tue, 24 Feb 2026 19:57:11 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8e2d19d3170e5e3f8be9d8d56a5a76f8dd33a29a9faf89e11fc95843809523c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139878097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6729b5aa890db49eadcd37f73840b388bc8cfbffae3a287f707ad8f362948a59`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:07:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:07:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:07:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:07:31 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:07:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:07:31 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:07:44 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:07:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:07:44 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:07:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:07:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf7db0639b9604757615e38919ccec56b3ea72873f074df0bef51269a953f2e`  
		Last Modified: Tue, 24 Feb 2026 20:08:04 GMT  
		Size: 91.3 MB (91288270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ffda554da6e3fb8c5f046cdf622f78417cd23b0325e03f5f1a2fdf0fcd29b6`  
		Last Modified: Tue, 24 Feb 2026 20:08:03 GMT  
		Size: 15.3 MB (15327189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3e155630a62d000262351734859ed533624d0e2c777f1159f067752c7e71cf`  
		Last Modified: Tue, 24 Feb 2026 20:08:01 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f757ea383e47edf2f5c0a7a12626c60df72add6fb3ad74a379a13bf60387ab2a`  
		Last Modified: Tue, 24 Feb 2026 20:08:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4ef6581b25ca41651e3a29481bff5648e912550a6327ae8ee610fc7071e3852a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3016099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d30473f341210f3848c7b764df2f65709c3bfd79a82223659aad34f9b81b2d1`

```dockerfile
```

-	Layers:
	-	`sha256:02683f3cb42e8910bfe9b8100ff3dd4640323658b007318d15b9778db258b81e`  
		Last Modified: Tue, 24 Feb 2026 20:08:02 GMT  
		Size: 3.0 MB (2996896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33f2ee7c793a22a864e8d7181f72ee969912dc678515b4ae451771b003969401`  
		Last Modified: Tue, 24 Feb 2026 20:08:02 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json
