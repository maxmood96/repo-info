## `clojure:temurin-26-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:26e6855f0e20f4674afee2faa58729b1bec779e77bd0726ee0527a15ce2372b1
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

### `clojure:temurin-26-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:be49dd2cfedd76f6174279b6001d151c2af3fc732ca5f7562c49b4c351288bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166861624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b112d03ce9272e1c187135aed291bc7fce1e4152e15326f9cabca54489fa33d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:20:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:13 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:20:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:20:13 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:20:29 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:20:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:20:29 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:20:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:20:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:20:30 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:20:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3120263d4a6835852e228280c8c241a2991954cc7e8e3b834fde5db3de71f0c`  
		Last Modified: Fri, 08 May 2026 20:20:50 GMT  
		Size: 94.5 MB (94455690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc115197fcf97976e6131f70f523b1fcc9a19473a1c23efd65df33efc0123289`  
		Last Modified: Fri, 08 May 2026 20:20:49 GMT  
		Size: 18.6 MB (18585475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa73c2a36708e75d2e9c4273010fea4a0fa71068155f472ea65c46ca6129083e`  
		Last Modified: Fri, 08 May 2026 20:20:48 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daabb6bcc319fac66733fa776875f141ad3aa5c60c03e68156adaa3c188d3e08`  
		Last Modified: Fri, 08 May 2026 20:20:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bef4f49a4160e8cfca9c338b8eae703941f240da9e8db4d87e98c5261e8aa7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1bc1eff409adcce387fa343ccbb05e827d50b60d69c20879976b9340be7886b`

```dockerfile
```

-	Layers:
	-	`sha256:ba231bbc788fe2bc61f8b0c0ca3fb976c5f7061f2cb1ec201a0173610e6df411`  
		Last Modified: Fri, 08 May 2026 20:20:47 GMT  
		Size: 3.8 MB (3781031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1efb0713d0d7bae85339c10bcdca2c611268442a14edb95cd30746c5ebe5568a`  
		Last Modified: Fri, 08 May 2026 20:20:47 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3a14f588d8e1e3594a87a401104ae08df8909dd01678b0ca5b923998da4b4910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.1 MB (166128243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ee89d5b86a18db5d6b2a05cf1c8aa4c9ddebbe56600ce7ca28b92e8b1d14af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:24:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:24:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:24:43 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:24:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:24:43 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:24:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:24:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:24:59 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:25:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:25:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:25:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:25:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89b2590c4ba7b5a7abf31bdce5c9d78d74445da1a7c5431c7b93c497c48cbba`  
		Last Modified: Fri, 08 May 2026 20:25:21 GMT  
		Size: 93.4 MB (93395166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00432d3c5a403784bf0d4fad986c69632fc9828a3bd5f6cc144c2da55c139fc`  
		Last Modified: Fri, 08 May 2026 20:25:19 GMT  
		Size: 18.5 MB (18545455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889b35d8410e3306d555bdf7161184fa650adf464ab1e6756c7453fd26e3d7d5`  
		Last Modified: Fri, 08 May 2026 20:25:18 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e704cdc03739360075441765207e6b9b3f98604ad46ad9795c263bdfc272ba6`  
		Last Modified: Fri, 08 May 2026 20:25:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:12ae4d5f953882546d3368301698a392a503522956d9c7e008b81a5532776bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dda5ebc58eaf7e13433076257889417a25d8f1310fde227046394046e2f05be`

```dockerfile
```

-	Layers:
	-	`sha256:fe115974f97a1102d74876000fcfbc37ca4945a9c7bc7835053d8e0f4ffd63e6`  
		Last Modified: Fri, 08 May 2026 20:25:18 GMT  
		Size: 3.8 MB (3781905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1b9fade7f1c84e5f2be810586c8ec19eca471dd2f53e28c7a32d1c26e1a3222`  
		Last Modified: Fri, 08 May 2026 20:25:18 GMT  
		Size: 18.5 KB (18466 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:4e1673baf7df42b4b1f4974600eef5e232c8cd1622b6f94cb189edce5f445bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170063775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df781c1ddbeff4dfa6fe1740609336a3fa16d95f564773302f2a513ab931957b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:48:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:48:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:48:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:48:10 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 09 May 2026 02:48:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 09 May 2026 02:48:10 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:48:41 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 09 May 2026 02:48:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 May 2026 02:48:41 GMT
ENV LEIN_ROOT=1
# Sat, 09 May 2026 02:48:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 09 May 2026 02:48:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:48:45 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:48:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f380ed992dc2e5079fc5af8b7e42121e0c356119cf7446f3b8707b481cc61b56`  
		Last Modified: Sat, 09 May 2026 02:49:19 GMT  
		Size: 93.8 MB (93781452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04fe27bff23f80e985fd61201ddf67b9492bd502dc4efc98bf5b2dd4af52ca8`  
		Last Modified: Sat, 09 May 2026 02:49:17 GMT  
		Size: 18.6 MB (18641015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c377c9d392baa6b6de3d049bbb6db50d04b98788ad261d3b869340cdc7b7610`  
		Last Modified: Sat, 09 May 2026 02:49:16 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf711dd9a4fbc8406d1e5b846575c679e59c20b5c3336fbe45de1c7fc0721f0`  
		Last Modified: Sat, 09 May 2026 02:49:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c77a298139aac48ae52dc9785b6aac4d079fc6cafb61a67b317a14ed54100d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be35de509c2fa64a8c2d72632a7eb8e4eae04c82808b5ffaa6560be598c6cbf`

```dockerfile
```

-	Layers:
	-	`sha256:8150248c79dd8fa89c18da49af71d7e5592b731d4e3014ba4a38e3f185b77d03`  
		Last Modified: Sat, 09 May 2026 02:49:16 GMT  
		Size: 3.8 MB (3765967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019e1c693903da267986eace0965bcec5c8474e58cb5bdb09faa199181b9b2ee`  
		Last Modified: Sat, 09 May 2026 02:49:16 GMT  
		Size: 18.4 KB (18389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:9ec692e65926566f42a1ca52777d66e9024ad65c784b46f8bbb5dee9f212b191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.9 MB (163862770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794d7f3694e38cf1f3a94837adeb176d91bfe74c2bb32fece6fc43ff7b9727aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 19:04:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Apr 2026 19:04:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 24 Apr 2026 19:04:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 19:04:05 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 24 Apr 2026 19:04:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 24 Apr 2026 19:04:05 GMT
WORKDIR /tmp
# Fri, 24 Apr 2026 19:05:42 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 24 Apr 2026 19:05:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 24 Apr 2026 19:05:42 GMT
ENV LEIN_ROOT=1
# Fri, 24 Apr 2026 19:05:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 24 Apr 2026 19:05:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 24 Apr 2026 19:05:58 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 24 Apr 2026 19:05:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d33f3b0d1516a154dea10fb422a41e3746a0c108f2eea69181e9875275fdbe7`  
		Last Modified: Fri, 24 Apr 2026 19:09:49 GMT  
		Size: 93.0 MB (93008124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57ce22578959d56f7563c54160bac99ac1362c11c900af4ececc0eee8543ae0`  
		Last Modified: Fri, 24 Apr 2026 19:09:38 GMT  
		Size: 18.5 MB (18538214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7932c75ef6d407359f735470586fef9fcb662ca3132e9f632fa1b09bfd767ce8`  
		Last Modified: Fri, 24 Apr 2026 19:09:34 GMT  
		Size: 4.5 MB (4517786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868715dbefcbeb6015a6e678f671e860547e83a4835e68043adb6d6f421679ee`  
		Last Modified: Fri, 24 Apr 2026 19:09:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0eedfbc236bf1be3df4b18ddb83e0497b76c6a810e13a02cbb89b0b64ca041db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3772532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55913f4e77ee7ab7b85d540c71d00b5eefbb477f53d83f1e787a4587e09a3287`

```dockerfile
```

-	Layers:
	-	`sha256:ccae298fb7c387b1f1571f9f8ce99bba7e26ecfd6f9efe7e4056023dcaf30f4a`  
		Last Modified: Fri, 24 Apr 2026 19:09:33 GMT  
		Size: 3.8 MB (3754143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1544ad07fae453b04a2916e8a46ac22e3c489d07521016687790fbc952a6ee4`  
		Last Modified: Fri, 24 Apr 2026 19:09:31 GMT  
		Size: 18.4 KB (18389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:7c76a6ff888d867bc1aaafb45ed56f35c0728f8b3235e22fdb78066a42179faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163064958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59de2d9ff5d19cab84c28b6200c828db7d7d8b60d028ee891200292c53c234b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:21:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:21:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:21:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:21:25 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:21:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:21:25 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:21:37 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:21:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:21:37 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:21:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:21:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:21:39 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:21:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea63852b62fa38d78ab507e59ec519d91cb7d1e9a5a2d2372b05f64d7765244`  
		Last Modified: Fri, 08 May 2026 22:22:06 GMT  
		Size: 90.5 MB (90547732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c2679c75d802dd9647b3e18339cf5820962cd5886e3d51386d4b146e3326ba`  
		Last Modified: Fri, 08 May 2026 22:22:04 GMT  
		Size: 18.6 MB (18626741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b31980076f6f1206c71a99a0f9fb72196dae454da17e513c0ebc0188e2b0d41`  
		Last Modified: Fri, 08 May 2026 22:22:04 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84c8ed5a956550d0d4eb64d027c87824870900fa30bdfabce403f19c25d7966`  
		Last Modified: Fri, 08 May 2026 22:22:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:05f236d02560834ea77208ec0703bc12ab034d0a3f950261843b26b10f1777ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3780988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b1a8a8c6f07abfa802047f740317fea672c29f35cfe618bae86cfef6f075a9`

```dockerfile
```

-	Layers:
	-	`sha256:1f32d62b4ff69faab7c41f592dd1208f3ead7f02a71fcdb10080ce6a317e9091`  
		Last Modified: Fri, 08 May 2026 22:22:04 GMT  
		Size: 3.8 MB (3762644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91dabeaa74a02474a1c2fa852ca4c12514a16ef66cd3dabd5deb59c671398ddf`  
		Last Modified: Fri, 08 May 2026 22:22:04 GMT  
		Size: 18.3 KB (18344 bytes)  
		MIME: application/vnd.in-toto+json
