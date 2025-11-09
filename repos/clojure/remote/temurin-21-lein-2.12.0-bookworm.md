## `clojure:temurin-21-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:66c852bbedb09959124e602495c042f89319fc51996ab5d3185f079fb3b6856c
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

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ce99157ca9e38d6190fa7ff06d7e17ceef4776475acfd6457ba66501f2ae0a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230628265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b5a86a52382136d8cf44fe5cc174512b327b24207c01918b7bd1e9c542ffb6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:43:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:43:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:43:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:43:52 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:43:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:43:52 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:44:05 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:44:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:44:05 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:44:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:44:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:44:07 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:44:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76561c7fa37879cfcf9da20827d741e2ed5b30a22dd8d4638433ffef6367a6ea`  
		Last Modified: Sun, 09 Nov 2025 02:00:30 GMT  
		Size: 157.8 MB (157825965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa2389a132b5e67977757d24bf00ca6fcc14844cd7f8d5267e8626fa128e6a3`  
		Last Modified: Sat, 08 Nov 2025 20:27:00 GMT  
		Size: 19.8 MB (19803056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3141c39c21b003b4957216535716f5ea8f9d9dfc04a000492a8697462f089393`  
		Last Modified: Sat, 08 Nov 2025 20:26:59 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f129bdb0727829e25308eab49ea96c03c53eb7e1afc7241ef8b4ce17145a978`  
		Last Modified: Sat, 08 Nov 2025 19:29:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:eaf8b9410d790e7a641ee9cbbc87307c45be6e69967a4094430c7d91acdc719a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8779fa8cc7b1bf4f68ec52d31e88c49bc449f3f8b718e87726c824063142c25c`

```dockerfile
```

-	Layers:
	-	`sha256:606b0f89069124190c91d1ebb6bfd170113f3fc332c06511e2a335b3a5aacde3`  
		Last Modified: Sat, 08 Nov 2025 22:46:54 GMT  
		Size: 4.3 MB (4283588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab1240d5c356fd63f13af5c212d99f9a984ed84681817ad31292a6085785b0b1`  
		Last Modified: Sat, 08 Nov 2025 22:46:55 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:34b50b9a9eb1694fd8eebfd6da4720c1ec096f55f82283b579806237d3b31607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228617491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd007fcb496b5265c59ca0441a0825f4d878b1038c55683527aefa942ed05bc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:43:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:43:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:43:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:43:23 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:43:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:43:23 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:43:37 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:43:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:43:37 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:43:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:43:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:43:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:43:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f826393397ef70e769ad45e540e264df808011dcd5bf0d8e6657cd5a501ccfc`  
		Last Modified: Sun, 09 Nov 2025 08:49:55 GMT  
		Size: 156.1 MB (156107661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7009bbdb4abc650cb81df6a82d0f0f13f346687a63247cb6a5d925a90a465a42`  
		Last Modified: Sat, 08 Nov 2025 18:44:14 GMT  
		Size: 19.6 MB (19632219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af71f74d7f208e933dab1f80de988a1834f5e7822e265d53af516f9e7e1818e9`  
		Last Modified: Sat, 08 Nov 2025 18:44:14 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17315664236ece6845908d3fd19c9c6e34d549591029d45834afb4ad48106266`  
		Last Modified: Sat, 08 Nov 2025 18:44:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8c1f6827eeea5403d92b8a23264499b7f6dd43eceadfd37607f1854c03f630ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cde5641a911d1185b56baa4d3f373bdc3c78a3af8b89ade1b9e69e9ec091f2`

```dockerfile
```

-	Layers:
	-	`sha256:0fa96dd4bf86d10cbfcff58fdf34004759990d7561a7f94aa5f3d6eb5ebb247a`  
		Last Modified: Sat, 08 Nov 2025 19:36:15 GMT  
		Size: 4.3 MB (4283227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446c45288e8aa62e12bff3d2d74419a64f3a6592b9b90abd6b3b1fdde19eb827`  
		Last Modified: Sat, 08 Nov 2025 19:36:16 GMT  
		Size: 19.2 KB (19163 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:b5f5f218046097374f9523601fde7ff128eb137794e14dc46fa1d95e6546532d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234810008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ad8ebaa9297ad03babda0a93b9a5675108fa64660df1466fa8d1c2bfe9ee4b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 21:30:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:30:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:30:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:30:07 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 21:30:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 21:30:07 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:30:34 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 21:30:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 21:30:34 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 21:30:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 21:30:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:30:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:30:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df5ddb30da5ca300b505c1a0ec8b4685bfad9925d2d21e6e9d69e16d2ad89d7`  
		Last Modified: Sun, 09 Nov 2025 16:12:20 GMT  
		Size: 157.9 MB (157942894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be12a0bdc57b9ebf6eed95d0aa32eb57ef2a1dc7eaa1a7be08cadaa0666a6567`  
		Last Modified: Sat, 08 Nov 2025 21:31:28 GMT  
		Size: 20.0 MB (20021649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d743e24fe9c3188a07f9099a3607d4048fb25e92dd0be101864c20cb0e53172`  
		Last Modified: Sat, 08 Nov 2025 21:31:27 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30ab5a3d6f277b3c374da5ec55577aa3bd53fd0800c3c750652b026927797dc`  
		Last Modified: Sat, 08 Nov 2025 21:31:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d4c11fa81423be2ad0a3ec6dae95e78c3e6608a390046f193eb22a1c412b605b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28602404d794b58ce75e96e12940c3ce654ae0367cc958aa67462cc73178c60`

```dockerfile
```

-	Layers:
	-	`sha256:9b89dae092cec19632f5bd17bcb8353fa96a28422eec745b1ca0f9c810956c93`  
		Last Modified: Sat, 08 Nov 2025 22:47:03 GMT  
		Size: 4.3 MB (4285459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b9e0cb88eef96b807b10c4c4b96438c47430cbf293b60e779c0e38fbc7222ab`  
		Last Modified: Sat, 08 Nov 2025 22:47:04 GMT  
		Size: 19.1 KB (19074 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:96722812f34b1249687b237424bb1c80d236bf8d6a046577752643ce84b29e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218186856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823f05c9d1c64756c85b8f55b643d5453ac710828df6a27ec834544b7defe8e4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 20:27:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 20:27:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 20:27:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 20:27:39 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 20:27:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 20:27:39 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 20:27:49 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 20:27:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 20:27:49 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 20:27:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 20:27:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 20:27:51 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 20:27:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0f1ee657e8017424c330ba8e64b9a2f627fd4b868716547a5d0262191fd498`  
		Last Modified: Sun, 09 Nov 2025 16:12:52 GMT  
		Size: 147.1 MB (147069874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca06f13d8cfc2e40be766f3126b876d18e722dc6c40e5c7238d1285efaf462d4`  
		Last Modified: Sat, 08 Nov 2025 20:28:26 GMT  
		Size: 19.5 MB (19460702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b784edbbb9db658cff0e676d2926256fb8515023cbf05753c9850d06dcb8e2cb`  
		Last Modified: Sat, 08 Nov 2025 20:28:26 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51032a75080cb365b3d66885b67d83a1da16fd38d3353e6ebc071b0ffed0311`  
		Last Modified: Sat, 08 Nov 2025 20:28:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:890c7d47869cd15507798e65eb59efd9ef5ffbcd470ad1c78dff995953a8537e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c63c59874f40bed0b2237ef4706c29d0721338716d391dbbaab5f0ecb8f54a`

```dockerfile
```

-	Layers:
	-	`sha256:47ae6997ef900226efed6f905571a1b5ba202eb04fb21187da83fc4f92411692`  
		Last Modified: Sat, 08 Nov 2025 22:47:08 GMT  
		Size: 4.3 MB (4275402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd9eabc2e3ecfa60330080c93b0e9121b2df5fada5c3d20b854da9ed3cc2d131`  
		Last Modified: Sat, 08 Nov 2025 22:47:09 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json
