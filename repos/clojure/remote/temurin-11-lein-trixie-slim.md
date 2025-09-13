## `clojure:temurin-11-lein-trixie-slim`

```console
$ docker pull clojure@sha256:cfcc98987b5b00de3cbfe63d9eff69d8aed54683c27a21a930afbabcdec7d9b5
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

### `clojure:temurin-11-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0989f9a711180feb5ca17098ab1970f5a71bb8ea36114517b3fc3f6dca709c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196396808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1683f686ba0dd357de582f8552ad23eaf50eecd78c94933f8bcbf45d145b05`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea05a3c1480bb4b35609d697c8f3bc5af4d5971f21d62644208208e3b398c94b`  
		Last Modified: Sat, 13 Sep 2025 00:03:40 GMT  
		Size: 145.7 MB (145658209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9765d2f17ab00474df586adc7e0ac86cb4e63d3c6cd3197d2285d54fc37e5211`  
		Last Modified: Sat, 13 Sep 2025 00:03:53 GMT  
		Size: 16.4 MB (16447357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27de811f00b02e7b5adbccaf8b8763c5cb9fafd9ff5f7188da9f5fd508023b26`  
		Last Modified: Sat, 13 Sep 2025 00:03:52 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:415be8d1433f3ded47d742db50a7b7cc6115e3c2c71b2b255fc38e73917898d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc03e2a9ca38edc7d74ca00fc521bd0273e0357b5ba2b2a971954eea71035fca`

```dockerfile
```

-	Layers:
	-	`sha256:f2573f7318571f4f46d973b374001a8e595932ab7d9b0a2965d5e1c0c99e8145`  
		Last Modified: Sat, 13 Sep 2025 00:37:21 GMT  
		Size: 2.4 MB (2383529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53eba77b7a230b92f3e4bddfb90132087fa0e64e7ca3a2dbaec16b99e7e4da0c`  
		Last Modified: Sat, 13 Sep 2025 00:37:23 GMT  
		Size: 16.4 KB (16437 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c8d7d1b2f98bba71dcdf1a524bf88268c3312a24c47e1098c28e60139fe19179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193527044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f09ed0cea7211255f8ec17a897ad4eb5ff1ded5b4fc5f80ec84b321b1c26546`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1c96fc2869f728ff01db18a998c30d49e0f98be944a4d3ee24d36356ded691`  
		Last Modified: Sat, 13 Sep 2025 00:15:11 GMT  
		Size: 142.5 MB (142459088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23530b683fb85879a1e0e4f02a19faa2162425ce26a3b5ecc4d2dfd68ffb0011`  
		Last Modified: Sat, 13 Sep 2025 00:15:29 GMT  
		Size: 16.4 MB (16413548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33bca0d6e2191ef555c19846f1fe7e9f87184f2b3c90dd166e6762ad065d363`  
		Last Modified: Sat, 13 Sep 2025 00:15:31 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bc75650fd00b9776bbcb44e2cc87853e71c5380deb3f0f602aa4247799cbc4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63de01b16bdec7cce0c79abff784576f3aba2705975bc2a6e76aeca007c07e9c`

```dockerfile
```

-	Layers:
	-	`sha256:73b073878518a7cbb4981ee6b7f467ef625251008745ef60149ea88a6f3de3bc`  
		Last Modified: Sat, 13 Sep 2025 03:36:25 GMT  
		Size: 2.4 MB (2383765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4361998c96c9645f3be51e0d9c73c76f91e6c3fd71400a2e548da23095c1c3d`  
		Last Modified: Sat, 13 Sep 2025 03:36:26 GMT  
		Size: 16.6 KB (16558 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e2aed1944584dbfef8af98da4edb4673437e30cff314148888b2dbce1dd039b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187451669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8969f77333ac78fc42fede28280b56e87873cca0b14a957c0ad7ececc05979`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80711450d1906fa3e5546b88cd727ed8be3bab693a2059b81aa05b285f401985`  
		Last Modified: Sat, 13 Sep 2025 00:02:37 GMT  
		Size: 132.9 MB (132853109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6517e35b281cc1f4072a0608940c7a4a55557893238fce20f0253cb26beebbb`  
		Last Modified: Sat, 13 Sep 2025 03:32:33 GMT  
		Size: 16.5 MB (16486449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dced6dfa88388af7de0fbc111542c02f36404a07974cd7476a26563183d6b552`  
		Last Modified: Sat, 13 Sep 2025 03:32:32 GMT  
		Size: 4.5 MB (4517728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:47fb8896852dcfdc14b12d5bbd0c68f7982a38c04a2be1bc3f5595a162a185d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696039478904ac73fb6c0cd4fc068f9489c9dcb99469c4a6cff2c13e23e821f5`

```dockerfile
```

-	Layers:
	-	`sha256:82a9fa65dba88410fa3ef251e0298d6a17b23e2397ce33bb6a14c2ae9063c645`  
		Last Modified: Sat, 13 Sep 2025 06:36:08 GMT  
		Size: 2.4 MB (2383894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99b20d24e7298388fe4c0fb06c92270dd620307c395b6afb101dda38bc470095`  
		Last Modified: Sat, 13 Sep 2025 06:36:09 GMT  
		Size: 16.5 KB (16480 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ddf8c8953f36d8db6cd9b93db861719af4f49a2948618a2b784861824c7f8ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176456664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48325649d63de77d6eea6abcbdf7afa90241be08f814be88aa59514e984bbf2`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fd3e533b839e7552e336d42f71226b5f34233f0755c691627ee57821194260`  
		Last Modified: Fri, 12 Sep 2025 23:47:55 GMT  
		Size: 125.6 MB (125622199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4a149249221936090436a3a707507df4dee6d6a3499e93029a7d867f83dc67`  
		Last Modified: Sat, 13 Sep 2025 03:06:55 GMT  
		Size: 16.5 MB (16483786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d373e0fa60d220aee0ad0491a8e97729dbcec88094f4c23d9a6bce091a3c01`  
		Last Modified: Sat, 13 Sep 2025 03:06:54 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:946cbc3446faea84945c355c647c8031814c041fc70fd66525ce4a00a31d784f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2396397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4603d71420849e3e5c866ea9e5c2cd23167118d1a46c6572d7bf9bcc4b46ce1b`

```dockerfile
```

-	Layers:
	-	`sha256:dba75695edfccc5c3acf37e3c137a225d0d7c0140d859cbc33ebfca0def407a5`  
		Last Modified: Sat, 13 Sep 2025 03:36:30 GMT  
		Size: 2.4 MB (2379960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b91b7bb8c1652f547027ea84381a204463dee7fc28c870355581f0d13fce64d0`  
		Last Modified: Sat, 13 Sep 2025 03:36:31 GMT  
		Size: 16.4 KB (16437 bytes)  
		MIME: application/vnd.in-toto+json
