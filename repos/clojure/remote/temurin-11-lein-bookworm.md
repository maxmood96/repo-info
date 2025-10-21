## `clojure:temurin-11-lein-bookworm`

```console
$ docker pull clojure@sha256:1e354e8a74173d4fe52f0487d6fee9abd81509020ce186d2e37173c2d88ecae0
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

### `clojure:temurin-11-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:dc837c0ce9a147e8fab3a8273fb761ec1ae88e2615867d0de2029ae03a5b2401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.5 MB (218459617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cccbaf31e411f6757fb1de2c49f76ba40161ec87a963a6b689590513d37d8f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcd32d949eb218997db8753d4d869a5022cc6d0929a9079b7b93cc4231390fc`  
		Last Modified: Tue, 21 Oct 2025 03:54:47 GMT  
		Size: 145.7 MB (145658349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bf433f9c13be60e42b8bd6e9fa3711087b30bdbbdac8868ffaae7ed594430d`  
		Last Modified: Tue, 21 Oct 2025 02:20:17 GMT  
		Size: 19.8 MB (19802920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29cd59397587a7ad326d456d6c0e060ef60497982b3ab973d57dd2d3620adc6`  
		Last Modified: Tue, 21 Oct 2025 02:20:16 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d46f354b722a560a396c958cc3e2011a9791d6a0c7b74ab7cf328156de854c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4316400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82768e1cdb1a52d79769b1f51c5d9ace32cfd7f0cd43e82f65030a2ca68cd335`

```dockerfile
```

-	Layers:
	-	`sha256:b0e467f6d32d7cd65dea8b70ce3aa23604c935954c1554f7165a9f633d7bd2ac`  
		Last Modified: Tue, 21 Oct 2025 09:36:19 GMT  
		Size: 4.3 MB (4299975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8113c0dca0c986885c17b1e8fe890bd18f468954ef49bcae9ef890c73ac56926`  
		Last Modified: Tue, 21 Oct 2025 09:36:19 GMT  
		Size: 16.4 KB (16425 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:43df75c254faff67a0f87eaf369fae599c5e45ec3bba53a719135549b2788992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (214969503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9812fab2e590f94fd705a1d355927364793055f5e3f626e2abe219d71761456`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf4ff441e1e139d3d55c506bbfe01297495240642a95ec9334409a63cdf6be0`  
		Last Modified: Tue, 21 Oct 2025 02:25:45 GMT  
		Size: 142.5 MB (142460648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca7f7e2726f5e0950fa30f794590a1ca164f5009ea15eca0961adab6463378d`  
		Last Modified: Tue, 21 Oct 2025 02:25:52 GMT  
		Size: 19.6 MB (19632114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a972e36f9dd01912d22ef46c3b3570eeef3adca5f2734db67f8f65809a1ea22`  
		Last Modified: Tue, 21 Oct 2025 02:25:51 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:995d8fcc1e1e594171673b1bb1d8698337d9892cb964639f942552285ca47d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4316754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c60af80d837c7fb310cdcbb5337afce489993ac73890762f00cfdab810ce678`

```dockerfile
```

-	Layers:
	-	`sha256:938add38b091f2718c745a3a1271117ca6c8f6385554031f8ff2f1fbeb139efb`  
		Last Modified: Tue, 21 Oct 2025 09:36:24 GMT  
		Size: 4.3 MB (4300208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fd64b73f57cb32e8254de15d5925b3859fd6928cb3a27f6151f4e690a29a0c8`  
		Last Modified: Tue, 21 Oct 2025 09:36:25 GMT  
		Size: 16.5 KB (16546 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:eea96dbdaeccee056d63336c67ca4e99545361f6a8d5c2aba2f6bedb18ff3742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209719427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170fb17ede6df727f8acd411b753a603230522334f0a41f4a688ecde5241a5e5`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9775786e5c038055f9d7cc602cd56de1156477d7f85bdc656ed523ac899b868`  
		Last Modified: Mon, 20 Oct 2025 15:04:43 GMT  
		Size: 132.9 MB (132853219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570e43352670dfb604cb8d384c4a8bb9f81c56193e056cac08d915f46c6a63d1`  
		Last Modified: Fri, 10 Oct 2025 04:57:33 GMT  
		Size: 20.0 MB (20021664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73547716d76dcac192ee2683c44c9c27c6d89513cce7abe2c0269113a262f63a`  
		Last Modified: Fri, 10 Oct 2025 04:57:33 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7598336b4fa826e4f8f15442f46749fbad5aefa1a52b3f03c797fd3e8683887e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4317688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4204a73468eca292d9a7d3931156104f19b6c647d31ac37bab83086b0a03d6`

```dockerfile
```

-	Layers:
	-	`sha256:362d63b5e4456264372a516a7a237efa0834ff7566138b9ee005bb09afb3f91a`  
		Last Modified: Fri, 10 Oct 2025 06:37:10 GMT  
		Size: 4.3 MB (4301219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc2cd980279acfd88f4dace642528667d77ae1370b7545b54ad146c8788fae7e`  
		Last Modified: Fri, 10 Oct 2025 06:37:11 GMT  
		Size: 16.5 KB (16469 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:27657d335f0683bc545fb3e64118cfdd4585d45df303aee170a8598c83a2e643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196738081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593bafd37dcc1e59e147037110b800db02a5735a1bd5222ce368236f4948a5b2`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:87d1bec83b35277b636c6e05b9418301b2f025752d7539cecae442f0b94d8fbe`  
		Last Modified: Mon, 29 Sep 2025 23:33:26 GMT  
		Size: 47.1 MB (47137446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ec68282f946501e8651907346ed42431fdda18b82c1c7e69c431aeba35370d`  
		Last Modified: Thu, 09 Oct 2025 22:51:30 GMT  
		Size: 125.6 MB (125622159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1586a1c222f078b3469fd5a9c5fd96dae846d0b9b850923b7ae791e3bba9bec`  
		Last Modified: Thu, 09 Oct 2025 22:51:19 GMT  
		Size: 19.5 MB (19460698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b200e238db0e17acb6ead96cd3adbd99f659b117f5f8604ab20520051c94f4`  
		Last Modified: Thu, 09 Oct 2025 22:51:18 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3b8f04a561861bea10702bf6f387d34d059b0c6d0c9c33c32b9ae34b568c3b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4308218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0b1b016af33913da51c3c7c3019b22614567d750b7c88c77a3259b8dd38fb1`

```dockerfile
```

-	Layers:
	-	`sha256:ca29ad7dcb5b2d211fd3a55d8c09890172a851f32a1c55af2eca115664a1a1bd`  
		Last Modified: Fri, 10 Oct 2025 00:35:50 GMT  
		Size: 4.3 MB (4291793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c21a2ff4af219d02b92e865f8b1371799498b0bb837e61250bfcbff00a615c27`  
		Last Modified: Fri, 10 Oct 2025 00:35:53 GMT  
		Size: 16.4 KB (16425 bytes)  
		MIME: application/vnd.in-toto+json
