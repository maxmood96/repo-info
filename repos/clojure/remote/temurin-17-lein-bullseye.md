## `clojure:temurin-17-lein-bullseye`

```console
$ docker pull clojure@sha256:f41c71272d2f0f1db49fd979512c1adc01578f7aba062c302f69c3b75fad1ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:eb63d921d3d4020c239e4f38fe80e754655c532aafd6ebc5b7844530f97cd601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218198701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc51cb8c94f7ded00587eed1a151ad849310fad192f14c2dd15516c5dea3c641`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 10:02:53 GMT
COPY dir:e13dbcd57950f4d4d23f4aba8428b6fbbf838d8f4801d32a25e344d37d33c37e in /opt/java/openjdk 
# Sat, 02 Dec 2023 10:02:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 10:05:39 GMT
ENV LEIN_VERSION=2.10.0
# Sat, 02 Dec 2023 10:05:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 02 Dec 2023 10:05:39 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 10:05:54 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Sat, 02 Dec 2023 10:05:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Dec 2023 10:05:54 GMT
ENV LEIN_ROOT=1
# Sat, 02 Dec 2023 10:05:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Sat, 02 Dec 2023 10:05:56 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Sat, 02 Dec 2023 10:05:57 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 02 Dec 2023 10:05:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a35d66848e01a74b7790ea370bb493db47c5518cd5c088ad8d2bf98e4e7b617`  
		Last Modified: Sat, 02 Dec 2023 10:18:57 GMT  
		Size: 144.9 MB (144873962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2fc88d07035b1e4af2088be9ba25b50b7b417e4ba075e1c64a5b6eac1bf231`  
		Last Modified: Sat, 02 Dec 2023 10:20:10 GMT  
		Size: 13.9 MB (13867196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e785f6b02c350ebf2e3e72f06a9a24e5eead13669338bbe0c3d2e8e5109cd53`  
		Last Modified: Sat, 02 Dec 2023 10:20:10 GMT  
		Size: 4.4 MB (4399238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15318d48715018b74242dc10ae7cb34d2112f8ac1443ad8e7f142ec69f2ac34d`  
		Last Modified: Sat, 02 Dec 2023 10:20:09 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1797ae6dbbcb55c305dba0815d56ece6e587af966ceeceefc37a45ffdfafce27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215645285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6676f4d36f3419562addd489ef2bf3ff44833ce54e723f0ec6e95cad47487c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 08:53:59 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Sat, 02 Dec 2023 08:54:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 08:56:35 GMT
ENV LEIN_VERSION=2.10.0
# Sat, 02 Dec 2023 08:56:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 02 Dec 2023 08:56:35 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 08:56:48 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Sat, 02 Dec 2023 08:56:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Dec 2023 08:56:49 GMT
ENV LEIN_ROOT=1
# Sat, 02 Dec 2023 08:56:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Sat, 02 Dec 2023 08:56:51 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Sat, 02 Dec 2023 08:56:51 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 02 Dec 2023 08:56:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188efff16de26f2786cfb1a16453748b1bec33191f4cc6735aa049a5a316877e`  
		Last Modified: Sat, 02 Dec 2023 09:08:30 GMT  
		Size: 143.7 MB (143681758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c257e978e31599a40e6fe0a7b157c4b17e192a3c85e82eacab5ec8d2dd9ff1d2`  
		Last Modified: Sat, 02 Dec 2023 09:09:44 GMT  
		Size: 13.9 MB (13856062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511d65253634d4b38df0aea2ce18e082d6d5457cb3926a78f638cf717d6d5902`  
		Last Modified: Sat, 02 Dec 2023 09:09:43 GMT  
		Size: 4.4 MB (4399193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b36839544f1a17d37c2c783c0d00d44f2c57dbb5698d47699d86e614a20e8e1`  
		Last Modified: Sat, 02 Dec 2023 09:09:43 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
