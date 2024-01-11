## `clojure:temurin-17-lein-2.10.0-bullseye`

```console
$ docker pull clojure@sha256:b2cae9461bbfedd39819a155655aa34eedb1e101b1f7a4afd87cb88c9e7b7556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-2.10.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e8964c371df25a1bf545f2d8b7bcdd76f3fec07663a77f4255618eae4446dd6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218198640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38abe3707b438418b348a01f2d69f9d74a4273a08eb4024feaa1b4e1a1a90e80`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:04:51 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 05:04:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:06:54 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 11 Jan 2024 05:06:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 05:06:54 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 05:07:08 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 11 Jan 2024 05:07:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 05:07:08 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jan 2024 05:07:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 11 Jan 2024 05:07:11 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 11 Jan 2024 05:07:11 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jan 2024 05:07:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d0fbad402cd2919fb4faf35c70ab5f613bf878017c5eaf98930d965c12791f`  
		Last Modified: Thu, 11 Jan 2024 05:21:53 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b9c4f26c9c0a32107c8aeb36680f6723865478b99b2d7dc8dd5fd9cfeca495`  
		Last Modified: Thu, 11 Jan 2024 05:22:47 GMT  
		Size: 13.9 MB (13867385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5963f0eff48f4451701b034860ee9a407624383ddf37874ab0a102de0019aa`  
		Last Modified: Thu, 11 Jan 2024 05:22:46 GMT  
		Size: 4.4 MB (4399230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ba9b48c252ff811be856a8db390193875580162b1f3eae170945327581cbd7`  
		Last Modified: Thu, 11 Jan 2024 05:22:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-2.10.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:46b2fc1c5e964bf30734f45358184b1690eb86fb5981acaf7ba7b238421f6200
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215645321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06447a82ad63b4da8a2138243da7662560ef8ca63fe1a6c92d17d907a6e934e0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:17 GMT
ADD file:06ba7e39a2f8e1a7bcbb929fa9d1e6fb1f8bdcf5096dc903576af8f7014e353b in / 
# Tue, 19 Dec 2023 01:41:18 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:55:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 07:04:36 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:04:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:06:13 GMT
ENV LEIN_VERSION=2.10.0
# Tue, 19 Dec 2023 07:06:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 07:06:13 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:06:26 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 19 Dec 2023 07:06:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 07:06:26 GMT
ENV LEIN_ROOT=1
# Tue, 19 Dec 2023 07:06:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 19 Dec 2023 07:06:29 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 19 Dec 2023 07:06:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Dec 2023 07:06:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:396a672fee8bade1a7c9f228d919717447f110f39046d8b5ed21ad45ae13ab61`  
		Last Modified: Tue, 19 Dec 2023 01:44:57 GMT  
		Size: 53.7 MB (53708091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd07311e78c2924fc080a1762e027781ac7b4ae611c86133314aba5a664a33ef`  
		Last Modified: Tue, 19 Dec 2023 07:19:23 GMT  
		Size: 143.7 MB (143681714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf280fe22f2816fccdd2fea7a58800301ed7e9f6eddca4a521c24ac0ba9fdb7f`  
		Last Modified: Tue, 19 Dec 2023 07:20:07 GMT  
		Size: 13.9 MB (13855898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775aa9e66b482546017749201c7864b19b05afdd137e03fac9fb8ab65263fe6b`  
		Last Modified: Tue, 19 Dec 2023 07:20:07 GMT  
		Size: 4.4 MB (4399218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa890267023bba49264369c0d78c70c42a1bbc4f159f07a30f5f28a9bb9d9d08`  
		Last Modified: Tue, 19 Dec 2023 07:20:06 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
