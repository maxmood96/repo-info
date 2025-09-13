## `clojure:temurin-24-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:033da9be1c618f7d694c1723ca194da915523ed8d97abc7fd6e68300dc9b7132
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

### `clojure:temurin-24-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:79bd033a5b49858e94fe82308776b9c3c471f04ba27aa7bed6e1f0f4e241cb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140479829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d70393a4a4ef1f424d3be94801fe4b17d2500c9620e7b6fc648d41b16a7fdb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3796457db2fb692b506a9e335b7c0ed492356ff77fdd5f1d241778a1e11c2c21`  
		Last Modified: Sat, 13 Sep 2025 00:11:38 GMT  
		Size: 90.0 MB (89975251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edeb2a715d4efd91d63a93fffa4944ebea841ccdfe68955df23cae2769bddca`  
		Last Modified: Sat, 13 Sep 2025 00:11:29 GMT  
		Size: 17.8 MB (17758087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7dd81118db7dbde13c887d21b6642130e933ed3620696d1b82f6339bb68dbe`  
		Last Modified: Sat, 13 Sep 2025 00:11:28 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290f328b0b5c13c6fbf53b72a4e9a31b8a163615a691461359db2c4ee213b63d`  
		Last Modified: Sat, 13 Sep 2025 00:11:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dcfdbf5c22b61034ef599d88a70b64e2a99ab87dcfa1a1b06ebeab3d9ba9c076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ce126708d377d5b4ca6cdee8444d919f2e546cc6d789aed9af5cf162fb6f2a`

```dockerfile
```

-	Layers:
	-	`sha256:3db515fa787248578a3aaffb61519862df90c90b4b35e9f810444e627491fd9c`  
		Last Modified: Sat, 13 Sep 2025 00:42:14 GMT  
		Size: 2.7 MB (2679434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7fd8ccf1b8b4dd36fe5d19a5bfb8d52cad327d3ce47f2227375797acb97145`  
		Last Modified: Sat, 13 Sep 2025 00:42:15 GMT  
		Size: 18.4 KB (18437 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aacfb75636e11a2244fe3832e471511631d0e0435bea54c070213a75fca2aa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139303744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05aafde283b5b49337a15bb3a7258d360113ce2eebf370b64693f4860962bc8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20436886d36466a4f809a68b920e9c755e62b7bc3c46a61aec9630316bc92f8a`  
		Last Modified: Sat, 13 Sep 2025 00:16:46 GMT  
		Size: 89.1 MB (89092551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa31df4624fcbd9628fe695d5df519e9630f486fe3c44d5f3d8d69cfe68c1530`  
		Last Modified: Sat, 13 Sep 2025 00:16:37 GMT  
		Size: 17.6 MB (17590951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deebbd5507b88fd6f180b90621e2452081204d456716df631f77eaf9c0132500`  
		Last Modified: Sat, 13 Sep 2025 00:16:36 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f452b51ee7f2ff38afbb434fa22c92b50699637d265e52b1222602a8402206`  
		Last Modified: Sat, 13 Sep 2025 00:16:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:db61a087d4b95bbb47215dc17e95801e8cf522fbb69182275fd59fc7f76af696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2a0d68bc6118ac5df64bfa420ceaeea65d4fc17134b923936cb8c7f3f5785a`

```dockerfile
```

-	Layers:
	-	`sha256:95f0572654d5908c8faa9f417756f5563dde1190b986e99fb526f69405b8a290`  
		Last Modified: Sat, 13 Sep 2025 03:40:28 GMT  
		Size: 2.7 MB (2679046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22a4b9ac4ffb09b16bda24adb663b363bd2e6367eb2c475fc68c5f8d1a9a5d40`  
		Last Modified: Sat, 13 Sep 2025 03:40:29 GMT  
		Size: 18.6 KB (18560 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:01f0db99696f0b86b70179cdbd6d0e9bdbf570563d9a8de8678908d0ad2a9240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144464724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df7156a054ff7967b6d07cb3bcd8944e729fb3aac890c97de94ac7b876267eb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fd09d5192cc7e3cbe99d4d308da8fdfddb81b3944db144f97d3a1682452e5f`  
		Last Modified: Sat, 13 Sep 2025 03:51:41 GMT  
		Size: 89.9 MB (89918193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5401bc347b49552b72e8348b51527abb01db1e489b83ce32c2cb965f252e2e9b`  
		Last Modified: Sat, 13 Sep 2025 03:51:36 GMT  
		Size: 18.0 MB (17959639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2f5eafc7080c59c518128a5303015c46bec2e01e7295d3f165b29bd613d956`  
		Last Modified: Sat, 13 Sep 2025 03:51:36 GMT  
		Size: 4.5 MB (4517701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43572ea4ff932a3c9333397aa910f62f1e874e83497b89eef57ef22511991de`  
		Last Modified: Sat, 13 Sep 2025 03:51:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:30162265ee39aeeb725394b06dfb90c4149f90097520e7f55c28a208599861fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2701048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6cbdc0fc9aff074794321e12d098516be1f5405882c9139ec7a64cb3338ea69`

```dockerfile
```

-	Layers:
	-	`sha256:47399936e14be36e9286ffe1404e2427f82ec8047d677d9f54ccd916e6dac0ce`  
		Last Modified: Sat, 13 Sep 2025 06:39:46 GMT  
		Size: 2.7 MB (2682565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66e23218b2a29dc553a2ba206732399e5097fcd5f9e26cdba05f2de14e41b9c2`  
		Last Modified: Sat, 13 Sep 2025 06:39:47 GMT  
		Size: 18.5 KB (18483 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:43dca9257a2b915111ad102976dbb1e6ef369418e0a31c8c7c3d4a14b870443e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134048677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8a59973bdbbe3fedddc87cc424f44aa43a77a89b7072626943658b0f1c7fd6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8062d35212474884f57e135a7c513bcb3237247281dcb5972254c07f21343289`  
		Last Modified: Sat, 13 Sep 2025 03:18:48 GMT  
		Size: 85.2 MB (85226409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30072a3c1af30914859a1a385d98b9e48d0ab91e822ddb08942f6bbf495c60bd`  
		Last Modified: Sat, 13 Sep 2025 03:18:45 GMT  
		Size: 17.4 MB (17419790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8634f8d13917d452b09dcb7f313c20ec64ba85127a5f491540483c29088ed8`  
		Last Modified: Sat, 13 Sep 2025 03:18:43 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feca0651758ee91626bfcb2778a14d8ac67b5534b7ff3a15161d75b39416de78`  
		Last Modified: Sat, 13 Sep 2025 03:18:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6e1813854f0ba5bb26f8dab58b09f5a9b84f2a5e0ebde2c4d73decf8603481dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32e72dee0b4d74a287fca1475fc2b5624aaef0277977ec717eecb9eec33dbb1`

```dockerfile
```

-	Layers:
	-	`sha256:8ad07ab4d35115be83ac6b3663bd06272155b9eabf6d7e7cc30d743ae38192b3`  
		Last Modified: Sat, 13 Sep 2025 06:39:51 GMT  
		Size: 2.7 MB (2673796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6cd191c356c5c45985e3812e1e6a7cec289cb8ae2e9c9810d7a6470b235b63f`  
		Last Modified: Sat, 13 Sep 2025 06:39:52 GMT  
		Size: 18.4 KB (18438 bytes)  
		MIME: application/vnd.in-toto+json
