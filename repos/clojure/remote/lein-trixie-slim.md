## `clojure:lein-trixie-slim`

```console
$ docker pull clojure@sha256:ac15225932272961ba8ad06af3f6d42ef3712c1a528fef3dd7ecc67df1d74681
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1909f97198f490d405b69ca33476e55e132169519c3352f34ac102af69f081bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142787025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b4c36b5dd1b616f450ba1f5cf8892e22dca76a6cb40d9d79210ef81202e21d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:16:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:16:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:16:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:16:46 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:16:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:16:46 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:17:03 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:17:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:17:03 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:17:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:17:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:17:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:17:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a786d304fd08ff1992af1ed85286f3c17d938d58f92533cc587bfdc20b3bd794`  
		Last Modified: Tue, 18 Nov 2025 06:17:34 GMT  
		Size: 92.0 MB (92045299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a4e0d87cc2e63313cc9f06fdc096e0ec24ae5c43a70da55bc7473b13a79433`  
		Last Modified: Tue, 18 Nov 2025 06:17:30 GMT  
		Size: 16.4 MB (16447101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8083125c32ed342b1e8c8d3b13c1920e8c6b162a3dd7a8f10a1c2758a3686a6`  
		Last Modified: Tue, 18 Nov 2025 06:17:29 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb597ad660a179dd9f19c4a929f9b3e2c4ea80e65d571d15226613422caa2d2a`  
		Last Modified: Tue, 18 Nov 2025 06:17:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:60821d8bb0e285bb09b56957741007ceb7824ab9d5ac71c0d356aed450218729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a9a2ef978a6c9407b82390199c569e90e1d372cf9b287aeb8762f869ca6008`

```dockerfile
```

-	Layers:
	-	`sha256:0b8f4873b1ad5b7a2aa69af57313225576dafec12f67f694d89f6b1dcf3788c5`  
		Last Modified: Tue, 18 Nov 2025 07:36:44 GMT  
		Size: 2.3 MB (2314754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3917291c110e96694fe801523d5dc73b5db94d070d6c505ee2e38f034bcf5a3`  
		Last Modified: Tue, 18 Nov 2025 07:36:44 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d21542fb30af653df13ddfb1f2c4f4e90a95576d3d8a6a43bfb757ad3f438f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142123129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b30b2e72221b62bba8204419471103affd8eb1c7fe0358cf9f7f2f4534e543`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:14:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:14:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:14:15 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:14:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:14:15 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:14:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:14:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:14:31 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:14:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:14:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:14:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:14:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f20866dcd073708566ec12af37589b3f1cb176987b8f515b477ec12f7a31934`  
		Last Modified: Tue, 18 Nov 2025 05:15:13 GMT  
		Size: 91.1 MB (91052500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5cf42407a5c26f09a49046f2c0a3f96db99989f96830750e7ba09e0ef750a5`  
		Last Modified: Tue, 18 Nov 2025 05:15:02 GMT  
		Size: 16.4 MB (16413846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb6e9368f6d335ba0141e1a1268affc5c99044056c008eacc6fd6aee4f18b5`  
		Last Modified: Tue, 18 Nov 2025 05:15:01 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622709db5333f8bdcb9b960f3b37e0a433d2d599428e8fe6750f6bda51426e03`  
		Last Modified: Tue, 18 Nov 2025 05:15:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7516dd082dc99934866c7f7ac78fed607ba472a388b428e59bcc25cf62eb7552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca2ce2054d0e6d9a81f78adcbaaefa514a1513571d8320269e2a2b025392983`

```dockerfile
```

-	Layers:
	-	`sha256:42a231dd18b3aa05c17a9eca5d7ed9f205f514b56fe99669a877ea323cc3d559`  
		Last Modified: Tue, 18 Nov 2025 07:36:48 GMT  
		Size: 2.3 MB (2314393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa5ae65d408ebaafa870861aeb1118849e126c791004dc03e58cb6d2d18642d`  
		Last Modified: Tue, 18 Nov 2025 07:36:49 GMT  
		Size: 19.2 KB (19179 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:fe5aa5541656b85e316a052c6c278ba204db5bab6eb750ca05c065730831d7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146214011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e0add9146c7e4feab0ecb4d2b93b808b3373d89923f3f3c00fa16f20a7351a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 07:38:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 07:38:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 07:38:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 07:38:50 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 07:38:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 07:38:51 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 07:39:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 07:39:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 07:39:18 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 07:39:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 07:39:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 07:39:22 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 07:39:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e214a9e01b759d7b08b8557e73d24cd420e1a0095fd9ed8d25175ebdcd1470`  
		Last Modified: Fri, 14 Nov 2025 07:40:17 GMT  
		Size: 91.6 MB (91610774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73041d2112f5e22071d66a770670cb410ce10c03a81d54eb3fd02de311b1d9b1`  
		Last Modified: Fri, 14 Nov 2025 07:40:09 GMT  
		Size: 16.5 MB (16486405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9479135b2efa860ce182bbc17d5909ae27f6dad8b751689949a99199dd770e8`  
		Last Modified: Fri, 14 Nov 2025 07:40:05 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8c7ab422819c96a6ba68f204c1c71a8f5749fda050c2fd62e9386b196132c2`  
		Last Modified: Fri, 14 Nov 2025 07:40:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:413c059cdc0e404198fce1b8badca7d5e88b26abf01cd30a0395d12f019c6e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6bf2bfedbd047912d7abff3ef739a26f6790e8ff0eedad5d53b15b206086de`

```dockerfile
```

-	Layers:
	-	`sha256:9e6126e25e818978d3fed88b2a7b1f958b41acfb2772e8299c44bb673403b400`  
		Last Modified: Fri, 14 Nov 2025 10:34:52 GMT  
		Size: 2.3 MB (2317050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c22db576fc9e5ca53d1b24464c62c6e36e0398966162622c3d6eaf7c9ce4d77c`  
		Last Modified: Fri, 14 Nov 2025 10:34:53 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:c9019ae3f473516e8183cc91990a5930c36984d229ae0eb7fb10c56757a66310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142563117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b18ed75006e5341400052b36287e7df9dde571259e4dbf81a66bd60b872265`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Sat, 15 Nov 2025 22:24:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 15 Nov 2025 22:24:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 15 Nov 2025 22:24:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 22:24:51 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 15 Nov 2025 22:24:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 15 Nov 2025 22:24:51 GMT
WORKDIR /tmp
# Sat, 15 Nov 2025 22:26:24 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 15 Nov 2025 22:26:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 15 Nov 2025 22:26:24 GMT
ENV LEIN_ROOT=1
# Sat, 15 Nov 2025 22:26:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 15 Nov 2025 22:26:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 15 Nov 2025 22:26:44 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 15 Nov 2025 22:26:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de331da7b5fa32193d37464667be79a9514eefa9df4d5a7f8b711124d7538b6`  
		Last Modified: Sat, 15 Nov 2025 22:30:37 GMT  
		Size: 90.8 MB (90752790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d775b8f46d7e2e95e241e64454f9e1ae7622d38b9e907634fd9ba9a33894c75`  
		Last Modified: Sat, 15 Nov 2025 22:30:38 GMT  
		Size: 19.0 MB (19016318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0628391fda317ced03a4ab9dce763017e8c59118c529f5b630f08ce887561c24`  
		Last Modified: Sat, 15 Nov 2025 22:30:29 GMT  
		Size: 4.5 MB (4517791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7314f02e8b7a15b9a1579bb58bf0334794afd7f2fa820f66ff6f29c2915fa3a3`  
		Last Modified: Sat, 15 Nov 2025 22:30:28 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2d36e178f88db65b0710c34e589daf70c3c19b40c163e80773553008365caec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2325901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38bf0ddfdf55801ca847f5fbc369a8c39d7bf6ba4c0f30c727edb2b40232dcd0`

```dockerfile
```

-	Layers:
	-	`sha256:fe7e39f4407ffb61deca1d5ded5b7615a305f54d6cd10dbb743ed8d140cb534b`  
		Last Modified: Sun, 16 Nov 2025 01:34:36 GMT  
		Size: 2.3 MB (2306811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590a1e60b79e15a4468713625bc6927268390365a9bfff1becc6ff40800ab00c`  
		Last Modified: Sun, 16 Nov 2025 01:34:36 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c685aad5fddb0a04735682cc64ba1179213169a9ae9533a15243e8be99f0fb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139046216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdad0f491a2a9f0b13f495a9b1cb201fc33face2379738adbbce5da05d4d28b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:32:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:32:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:32:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:32:01 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:32:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:32:01 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:32:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:32:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:32:20 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:32:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:32:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:32:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:32:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6e5b57d009ffc8e92434207bf8eddd2800f9112ab5f49d95410a4fdd9ca7de`  
		Last Modified: Tue, 18 Nov 2025 05:33:02 GMT  
		Size: 88.2 MB (88210704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059868bfe57be2b42674c0650828d193b9328e64392ed82608f1aca6cf0f9a0f`  
		Last Modified: Tue, 18 Nov 2025 05:32:55 GMT  
		Size: 16.5 MB (16482965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8601e52056cea1dc2ba97e9c80e1aff620e6931d1e4b37430d8beb3bd250fa`  
		Last Modified: Tue, 18 Nov 2025 05:32:54 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c694032b86b2e60bd020b213a48e04e66e589f05ff2358b29d5b49b7ca544a`  
		Last Modified: Tue, 18 Nov 2025 05:32:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:64a04390d73efb3f69d6606e9564cb1603643155f194cfb9514ab37c3a71f523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2332763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2ebd9f1f747d3c97ca1c2d7f5443632d7d74d8758a462777621a7fab9f0d77`

```dockerfile
```

-	Layers:
	-	`sha256:78cf1c842dd6b7034e8ff10f4afa2fc6c6d691b147959d81045c4b547e1e577d`  
		Last Modified: Tue, 18 Nov 2025 07:36:58 GMT  
		Size: 2.3 MB (2313729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8292d68d25f19e1f80cd0ad902642afea6500f8dbd013ac5770f3f20ed99688c`  
		Last Modified: Tue, 18 Nov 2025 07:36:58 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json
