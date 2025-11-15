## `clojure:temurin-21-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:1c73193be005c96f9916a5f3289676dcb07cd9f2ad3734eb7bef41980afe83c2
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

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:ca4e43b5ed56c4353db1165b0bfb7adc95e1b30282c9b9df18493f382c46f7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230208887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff1411777e4ccb85304c3d1959067b3b4ea03ebcc5685db4a91d18313782597`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:54:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:54:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:54:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:54:09 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:54:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:54:09 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:54:25 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:54:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:54:25 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:54:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:54:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:54:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:54:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c6668e2a7faed80dadeb6c27c929b8a0b40fa70e6de6ca65b3c3af83c20fbe`  
		Last Modified: Fri, 14 Nov 2025 08:25:00 GMT  
		Size: 157.8 MB (157825974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ceae9030f5e80628f19062c8b1ccdd3d6e2edb365fe2ea91b931267b8413dc`  
		Last Modified: Fri, 14 Nov 2025 00:54:55 GMT  
		Size: 18.6 MB (18579148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56f351c059058232335cfa31f01fd36ee55728aae87fa8542ebf3297d985078`  
		Last Modified: Fri, 14 Nov 2025 00:54:54 GMT  
		Size: 4.5 MB (4517707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c275f0027fd22236f2f8c04780d8454d91a29aa667e691c5bb926cf935e59d`  
		Last Modified: Fri, 14 Nov 2025 00:54:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a10b20898a03a42d7cdef85fdb128023e65651de1a1338d63fb50f56e1b5bba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7aab003a1a8bc15dcaeedbb1398624656533a311cc99d853b824b31902f91c`

```dockerfile
```

-	Layers:
	-	`sha256:539ab1f74e8779e6a2366e3f7404a3fc915300e2af73f0b003b68f3cccfe1ae9`  
		Last Modified: Fri, 14 Nov 2025 04:39:54 GMT  
		Size: 3.8 MB (3816488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4060c6605187aed3bc998a810a81611ed506fb0a2608b3b5e2788f632f2e3a58`  
		Last Modified: Fri, 14 Nov 2025 04:39:55 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4c0b852a7e52c01a28245e90cc57b1ab149e80e8b5914c272bba0f07c555beda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228816217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0005363d2d052b3dac87b6b970c36eed838a544043ba1c12efd8a7a25dbb528a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:56:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:56:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:56:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:56:24 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:56:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:56:24 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:56:41 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:56:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:56:41 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:56:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:56:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:56:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:56:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99d9902a23159639f8b4864362118801239e278d34a6317bf32a8dcf9e864db`  
		Last Modified: Fri, 14 Nov 2025 00:57:05 GMT  
		Size: 156.1 MB (156107636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d34cbec8f064ecd4a4b57ad68490f97846f91bd51e996b365172f5f24493196`  
		Last Modified: Fri, 14 Nov 2025 00:57:15 GMT  
		Size: 18.5 MB (18539973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead48697dd70e78deb1a1eb4a9db4728e228ca92c403e48eae45902a9b8fe6d6`  
		Last Modified: Fri, 14 Nov 2025 00:57:13 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340ed8ad03c996885847012661afee28b9691399b88f6394afa54a77238450ef`  
		Last Modified: Fri, 14 Nov 2025 00:57:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b785033ab90ecb0ca039b2ecef805d9e8f09c031defbcb9730da194dc34d07df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cd9432f2fccb6eb74134d58d94349291162b977838db7ac245c7535dfdf973`

```dockerfile
```

-	Layers:
	-	`sha256:6f98521c02bd76d6fc2e6f8549e8a335d9246f990a8fdf26910880f43661c668`  
		Last Modified: Fri, 14 Nov 2025 01:44:16 GMT  
		Size: 3.8 MB (3817365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:448f8ea900cf03ec3f3eaff7b23a5acd997a54a33507d0a5de8f528f17e5b295`  
		Last Modified: Fri, 14 Nov 2025 01:44:17 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:6c4999764d66ddb2e0eda729573281ef97e360ddf1ebb5d944030c5c68a10fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234207797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16ce614af4a32ea206bf861d682dd84a14299bde574f48c3a587a9ab7779b18`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 07:22:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 07:22:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 07:22:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 07:22:47 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 07:22:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 07:22:48 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 07:23:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 07:23:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 07:23:14 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 07:23:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 07:23:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 07:23:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 07:23:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1846f067e1ffa573181ab2b7636dd7c09e6a6163953bc6affa72a6b0b1d4e9`  
		Last Modified: Fri, 14 Nov 2025 23:29:28 GMT  
		Size: 157.9 MB (157942937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aaf8de2904ecbcb55152c78bbdc0b68ecf8e3a7138418e3f630c1ef845db4a5`  
		Last Modified: Fri, 14 Nov 2025 07:24:10 GMT  
		Size: 18.6 MB (18636543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87050359b586c0cea2ecbcc8f27f151676c814d7b0d62470542d2167b69d78b6`  
		Last Modified: Fri, 14 Nov 2025 07:24:07 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1972d7184de975cf41517dca11b91bc24ce735e942a6bbbc59dd6942dc425d2`  
		Last Modified: Fri, 14 Nov 2025 07:24:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b64f44eba654c6c483fcf1799b9a7d940ccf0ee2e027b1e843a7f65ce3ae5995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32b43f39ab313c0cc756a73ef0520c88eaea271dee007d8ef7c7c6ceece5395`

```dockerfile
```

-	Layers:
	-	`sha256:d832a29a32afed18715974aae9e0fe5bb59015223ab646b99e61b0d9c0dde248`  
		Last Modified: Fri, 14 Nov 2025 10:38:24 GMT  
		Size: 3.8 MB (3817486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d1605ee382eef37bd3c9296fb08f9e0ef9c69359945a79bad09974481717508`  
		Last Modified: Fri, 14 Nov 2025 10:38:25 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:21a06ae18f0f060c5885e9b5d7069405c00eca1b9de36466d6c7f8e4f8d6eb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228014509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c397ac31d873d4c9994278d9f4f15fced9a16461ad615b0254e79be6c0db750b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Mon, 10 Nov 2025 03:52:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 03:52:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 10 Nov 2025 03:52:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 03:52:50 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 10 Nov 2025 03:52:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 10 Nov 2025 03:52:51 GMT
WORKDIR /tmp
# Mon, 10 Nov 2025 03:54:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 10 Nov 2025 03:54:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 10 Nov 2025 03:54:20 GMT
ENV LEIN_ROOT=1
# Mon, 10 Nov 2025 03:54:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 10 Nov 2025 03:54:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 10 Nov 2025 03:54:36 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 10 Nov 2025 03:54:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5be84f75f5cfb38b82da427fff2f97f31bf8aabe180cf4ebe04e740d623ca5d`  
		Last Modified: Mon, 10 Nov 2025 23:12:45 GMT  
		Size: 157.2 MB (157194308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9503e9340441b61ea248c61e24e7625c18a03bd9b923ffb5e3470d5703d74949`  
		Last Modified: Mon, 10 Nov 2025 03:59:13 GMT  
		Size: 18.5 MB (18531066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64bdeacfe28ff26a8a06cd955da4fd14a540bb9568b40f2ff9f77d2e16c844b2`  
		Last Modified: Mon, 10 Nov 2025 03:59:12 GMT  
		Size: 4.5 MB (4517780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b1a820a21754f8741c180f644bd89ef6eacda57677eb776842ffe5365c289f`  
		Last Modified: Mon, 10 Nov 2025 03:59:12 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:442e16ce0ed859c011b133686d3e03122f9596edd0a92d8964f41747b8277b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3825359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2550dfbe9a77cc0f0754076ece5b379976a5b3722af49c66612ccede001f0b`

```dockerfile
```

-	Layers:
	-	`sha256:6629bc54760670775e5c774a2a2317d0c7fcccd4c6b4df80a353b468f121909e`  
		Last Modified: Mon, 10 Nov 2025 04:36:53 GMT  
		Size: 3.8 MB (3806963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac897c45553fd2a735f9987098f88b867a5f497e7a965028659ea20c70e28db7`  
		Last Modified: Mon, 10 Nov 2025 04:36:54 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:a6c11e487b145d9dbd86f2a949f6cb7ff50fdc5f8feb6193aed2fe529b81d299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219560503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724b7daa6fa753ea73b9b5784c7d2b1b7dee901f90897c6aeb67eef1a8d325a7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 01:00:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:00:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 01:00:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:00:06 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 01:00:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 01:00:06 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 01:00:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 01:00:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 01:00:18 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 01:00:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 01:00:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 01:00:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 01:00:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f61465f3fdbb3923a28f1755c9191bead554b0aaa1919ab4d89fc9130dde133`  
		Last Modified: Fri, 14 Nov 2025 01:00:45 GMT  
		Size: 147.1 MB (147069832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a7da034680f5dc74e59c7b3dd46888cee89cfd08a46128239533a91acb26a6`  
		Last Modified: Fri, 14 Nov 2025 01:00:53 GMT  
		Size: 18.6 MB (18620199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bed18be6d0b472fbaa66382689306f6b90cc982668bc0e987ed0e8aea517637`  
		Last Modified: Fri, 14 Nov 2025 01:00:52 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac0848fc5e4c4f356efe78be249730b48e7e3125ae89c328210c96db506c47a`  
		Last Modified: Fri, 14 Nov 2025 01:00:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fd5519c441e1ac19cef9ef245e81b8435e61a6d32b6b351e30e894397605437d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541330805d431334ded56067a5e358db9ac94ce107fc4440770685a64b96c942`

```dockerfile
```

-	Layers:
	-	`sha256:67dae3b1daee35b77c3f2d81217909b534817fce5a3d3fe54fc6c7891181d527`  
		Last Modified: Fri, 14 Nov 2025 01:44:31 GMT  
		Size: 3.8 MB (3812915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:411e89251922147cf7af584582f3c1ba55dbd7ded809199977b015ce178dbed4`  
		Last Modified: Fri, 14 Nov 2025 01:44:31 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
