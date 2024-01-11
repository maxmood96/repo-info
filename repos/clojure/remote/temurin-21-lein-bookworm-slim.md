## `clojure:temurin-21-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:2e1947f975708631cfdf1a237fb7297fc585443fd652c2cb974e8e213b654b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6c5c8a84da89fa316fae65f73bdbd0783fb64f451f7cbdd30dd724b3464be6dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207154373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95ccbe87ae2cd7c0d1ed735dd915f031afb68d13a1665462108348a609b3338`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:52:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:09:23 GMT
COPY dir:e6025cb107ac582823e7222bca84438ae7fa7384431777ac5a68b80c2a5b3d9d in /opt/java/openjdk 
# Thu, 11 Jan 2024 05:09:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:09:24 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 11 Jan 2024 05:09:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 05:09:25 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 05:09:40 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 11 Jan 2024 05:09:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 05:09:40 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jan 2024 05:09:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 11 Jan 2024 05:09:43 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 11 Jan 2024 05:09:43 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jan 2024 05:09:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda2efbb0e8cf954865d770965b7b55222d1df05b042532985f486eb2237acc1`  
		Last Modified: Thu, 11 Jan 2024 05:24:58 GMT  
		Size: 158.6 MB (158630562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80325217e799e757b665fb4340a66b91f0d800f19dcee82e27ba2ca7722f1360`  
		Last Modified: Thu, 11 Jan 2024 05:24:47 GMT  
		Size: 15.0 MB (14998267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c5947afdc53490d6da5fbfaf47b52ba7caa8b340a07ebaeb9d94d8432897ae`  
		Last Modified: Thu, 11 Jan 2024 05:24:46 GMT  
		Size: 4.4 MB (4399224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a965d7cb2c025c7153eeb419cf631286f35bf4b946400fd5455ae1c6a9c120`  
		Last Modified: Thu, 11 Jan 2024 05:24:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9b292f07561bb97936b2546097d8853a453e91765b2ec107dd13f60e30c7885a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205249127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48a8419213f7f6a07b002b38c2e510474fe45f06db65900101d2187c9c38e18`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:54:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 07:08:17 GMT
COPY dir:6c09b6d38e0ce748c3ef1f9f172525f08b1f5fa7d2d583b56755ceb9d38b6e61 in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:08:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:08:21 GMT
ENV LEIN_VERSION=2.10.0
# Tue, 19 Dec 2023 07:08:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 07:08:21 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:08:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 19 Dec 2023 07:08:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 07:08:34 GMT
ENV LEIN_ROOT=1
# Tue, 19 Dec 2023 07:08:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 19 Dec 2023 07:08:37 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 19 Dec 2023 07:08:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Dec 2023 07:08:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb9d49b297d41f5d373175747ce170977d50cd772ea457aae74b2bd33c0cdb0`  
		Last Modified: Tue, 19 Dec 2023 07:22:11 GMT  
		Size: 156.9 MB (156872112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442ce26a7c22f013f903823c81d3ac6e71e0ff035eac2bac1284c0936f1f65f8`  
		Last Modified: Tue, 19 Dec 2023 07:22:02 GMT  
		Size: 14.8 MB (14820136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e558dc72b9b8629afa13802e92d0edf5b5f267cc54a14bc9909f3b8965686a`  
		Last Modified: Tue, 19 Dec 2023 07:22:01 GMT  
		Size: 4.4 MB (4399209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777178a9eee7a862e28ead1f185bb18c651a8ddb40aa6c0d681db46a03b98dc2`  
		Last Modified: Tue, 19 Dec 2023 07:22:00 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
