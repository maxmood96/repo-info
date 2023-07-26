## `clojure:temurin-17-lein-2.10.0-bullseye-slim`

```console
$ docker pull clojure@sha256:a5861c7485270918301fe90387da2975d72e9258262e36b42cd150ba92e7dd62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-2.10.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ec4080340c2e64b0f5bec81dd79f818b3e13586557679ac89f9786e13ab3e741
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240973770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c4cd898640f048cdc9610eb2b566dc0cca335f57cc126fe6e3a7d17aee4750`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:00:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 11:24:32 GMT
COPY dir:4f02f3c240ecc691ff41263b0454f619d51a2ba11a57fe51c0e31e7ff62a9194 in /opt/java/openjdk 
# Wed, 05 Jul 2023 11:24:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 11:26:13 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 05 Jul 2023 11:26:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 05 Jul 2023 11:26:14 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 11:26:28 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 05 Jul 2023 11:26:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Jul 2023 11:26:28 GMT
ENV LEIN_ROOT=1
# Wed, 05 Jul 2023 11:26:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 05 Jul 2023 11:26:30 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 05 Jul 2023 11:26:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Jul 2023 11:26:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fafbbd507c7f35e198981926b1a326f224d7e89d5a693df01bea8a92ba4e7d1b`  
		Last Modified: Wed, 05 Jul 2023 11:36:02 GMT  
		Size: 192.6 MB (192580435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82a929f93a5d57736d0236be09c8042e8d3a894084de5509323f764fb3ab4c5`  
		Last Modified: Wed, 05 Jul 2023 11:37:03 GMT  
		Size: 12.6 MB (12576295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56958dd82066a9c4b54feef171d893e124557a16242cbf4a0c1473b05d380b7f`  
		Last Modified: Wed, 05 Jul 2023 11:37:03 GMT  
		Size: 4.4 MB (4399253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9efbd5b6b160df7bc73773f1c96a23b41b5b4b00e71bb813db19c2036df940a`  
		Last Modified: Wed, 05 Jul 2023 11:37:02 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-2.10.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a66cdcacf520096778abaf416fdb1d5c3c0130fd2b99fc9fc96c7b79269060c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.6 MB (190564307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb02df178893c914c8d4e8d81aa5907ac9b2cce95d94b1b4a48e0ae797cd775`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Jul 2023 22:58:45 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Tue, 25 Jul 2023 22:58:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:00:35 GMT
ENV LEIN_VERSION=2.10.0
# Tue, 25 Jul 2023 23:00:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 25 Jul 2023 23:00:36 GMT
WORKDIR /tmp
# Tue, 25 Jul 2023 23:00:48 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 25 Jul 2023 23:00:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 25 Jul 2023 23:00:48 GMT
ENV LEIN_ROOT=1
# Tue, 25 Jul 2023 23:00:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 25 Jul 2023 23:00:51 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 25 Jul 2023 23:00:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 25 Jul 2023 23:00:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c798e6c54e318dbfe8b5b1325d38da64ea5e5a387b26c620cc1f0c2820d0f70a`  
		Last Modified: Tue, 25 Jul 2023 23:05:13 GMT  
		Size: 143.5 MB (143538051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b6c4592d6de56d94d919730fc3eb261d2848ab6ef716674f00351d45d157c7`  
		Last Modified: Tue, 25 Jul 2023 23:06:13 GMT  
		Size: 12.6 MB (12563699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f628cbad19a5faa970cb09abc3e3d30e206fc781df2475ffde8302a4caeab7`  
		Last Modified: Tue, 25 Jul 2023 23:06:12 GMT  
		Size: 4.4 MB (4399201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fed468a3b8b3a3ca846edcf56f941fffe109b9b4e7f30bfa7d908754e3fc82f`  
		Last Modified: Tue, 25 Jul 2023 23:06:12 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
