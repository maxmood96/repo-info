## `clojure:temurin-25-lein-bookworm`

```console
$ docker pull clojure@sha256:095ada74543509b1c1cb033a95993e82cd0acc7ebb3903137d79c3e89451f497
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

### `clojure:temurin-25-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:30a98c595902692a084a39bfd83e8a81753143921c2f7211d439133685e3e414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165388022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e5f6f936d15949b346dc107035b8ad6b639e68f7f518487a9075c84cb65d0d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Thu, 30 Apr 2026 23:53:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:53:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:53:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:53:00 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:53:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:53:00 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:53:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:53:14 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:53:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 30 Apr 2026 23:53:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:15 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a83e027a563374d7ff9c4765e6372a552451fc66cb16c1c2ce2b343cd790d17`  
		Last Modified: Thu, 30 Apr 2026 23:53:34 GMT  
		Size: 92.6 MB (92574598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f7e65ba4e6af0ea04dc452a488cac9841cc136753e77f0754b2411f1785a38`  
		Last Modified: Thu, 30 Apr 2026 23:53:32 GMT  
		Size: 19.8 MB (19806610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc724d746c6313f1786ac96da38ddbe60e1ebe772a10d565ca6d49fce107758b`  
		Last Modified: Thu, 30 Apr 2026 23:53:32 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ff11bd8c48c516ae99a187b442b6714c5423c0d3f3f52c42ceb5728fdc2a2c`  
		Last Modified: Thu, 30 Apr 2026 23:53:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:acb428e68e55abe7563a2702352abd8b13a546a94218e66b2da267c697151be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a922209a5a60a7647c0e207cf0ab508c59d90b6626824396358127f30db0a87`

```dockerfile
```

-	Layers:
	-	`sha256:ec5bb169b373ff42232f501507575c6adb57b2cced926080335025986b0aa41e`  
		Last Modified: Thu, 30 Apr 2026 23:53:31 GMT  
		Size: 4.3 MB (4251650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceb45ecdd80b2286a7b9e66cd9a24243349b8e56eb90dee4ef5bada4544d6ca7`  
		Last Modified: Thu, 30 Apr 2026 23:53:31 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c9b2343f251b0b46d1be8c97bdcd925b38dc1086b487afde61703786a0400a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164070522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee87fe1109d49d09dc6db5de71eb81bb9ad9d4df1fee063cd800cdb2cf9c138`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Thu, 30 Apr 2026 23:52:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:52:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:52:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:52:32 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:52:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:52:32 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:52:46 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:52:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:52:46 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:52:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 30 Apr 2026 23:52:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:52:48 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:52:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938a700ef1fc1c4f4faab146badc0d53da775e9e880076a8808dfc553b686b61`  
		Last Modified: Thu, 30 Apr 2026 23:53:08 GMT  
		Size: 91.5 MB (91542288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3317c50fd86f78bf5179b56b60b55b7cab5ddecc4caa32013dabb8bee2361b8`  
		Last Modified: Thu, 30 Apr 2026 23:53:06 GMT  
		Size: 19.6 MB (19636978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8531bd2f00ff7aa7cc581adf00cf31d29a6d137e258dce53169e7d61886132c1`  
		Last Modified: Thu, 30 Apr 2026 23:53:05 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4061c22b8528af36b58230c4c663dc170457c264cc534d38f044c76c1871fc`  
		Last Modified: Thu, 30 Apr 2026 23:53:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d021fdc32df0e08d976ee84376c7711eea90c1ac3862e43acc7fa2c11d9af7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43ac6ea9cef2bd18c2d3b85ac6125eb3c2fefac464b1c21aa9186a80fb6f425`

```dockerfile
```

-	Layers:
	-	`sha256:440ee07857fd37bf28e5bc82bc1d0a3deeb737fae1fa27185b360887eed61cdf`  
		Last Modified: Thu, 30 Apr 2026 23:53:06 GMT  
		Size: 4.3 MB (4251334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5490eb3d71d3f6190faa8e8fba1fe55623593bfdebb0eb9e0402c3b8498d5c60`  
		Last Modified: Thu, 30 Apr 2026 23:53:05 GMT  
		Size: 20.5 KB (20451 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:5a6db6c377e1074d830134bc23efa7777a39ab7886e71c495f2e4357154e013f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168799430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396344cef40e5239cdcc1e5acb3e5bd727847e8fadf3763cd2bef162a6412679`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 01 May 2026 00:07:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 May 2026 00:07:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 01 May 2026 00:07:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:07:11 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 01 May 2026 00:07:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 01 May 2026 00:07:11 GMT
WORKDIR /tmp
# Fri, 01 May 2026 00:07:45 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 01 May 2026 00:07:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 01 May 2026 00:07:45 GMT
ENV LEIN_ROOT=1
# Fri, 01 May 2026 00:07:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 01 May 2026 00:07:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 01 May 2026 00:07:49 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 01 May 2026 00:07:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01487bcba0d0c1649162f2116f011092d3effd12c3f381faa370fdd01952d8b6`  
		Last Modified: Fri, 01 May 2026 00:08:34 GMT  
		Size: 91.9 MB (91914030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5861fa1b14a7aebd53e77b55b7470ca4d71c7bc6806cd6a1f6b804c9bf9fb9`  
		Last Modified: Fri, 01 May 2026 00:08:32 GMT  
		Size: 20.0 MB (20030495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6131a869cce9f026526a23905f8b4d17749c6b20f162420b9f0904dcf4251db`  
		Last Modified: Fri, 01 May 2026 00:08:31 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dd7a080ae73edb65cf28a6202dcb43373dfab28ca10eaf85ab0b00f50e4723`  
		Last Modified: Fri, 01 May 2026 00:08:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:db2f7ee5e5888c21e96c91cc55010f156acf3d794ff8a62b02da25ebc0be6e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4257198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd30a861ee53aaf647395cf583c8346d8592ea4d66186cf33ae6f36e9ba8ae1`

```dockerfile
```

-	Layers:
	-	`sha256:5d51a1522b0ecc4086156bc4017b6732d3900b100db94062c658f234d58320f5`  
		Last Modified: Fri, 01 May 2026 00:08:31 GMT  
		Size: 4.2 MB (4236859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c51f5fa29356ba8204efd5f0c39d41a78f8d4693a228b7087d1488a329a437e`  
		Last Modified: Fri, 01 May 2026 00:08:31 GMT  
		Size: 20.3 KB (20339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:d7348e80f4468f3b9b44758e83373b0d753a13bb6cf1f5396a4315f73d3120a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159553161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57bcd30908320e6c2a4dd07fa7246a2fbe35619cfb5a826e0c51045693c874f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Thu, 30 Apr 2026 23:49:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:49:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:49:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:49:45 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:49:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:49:45 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:50:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:50:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:50:03 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:50:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 30 Apr 2026 23:50:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:50:05 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:50:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f546523e17144e6adf96648f2aab96177c22f8992d4957c2ac55d515ef040136`  
		Last Modified: Thu, 30 Apr 2026 23:50:34 GMT  
		Size: 88.4 MB (88420323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d3e5ef4db21ba91e38e66753f81b031cfc833ab9a643bcaec15bff86d8a702`  
		Last Modified: Thu, 30 Apr 2026 23:50:32 GMT  
		Size: 19.5 MB (19466693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93247ed19dae32474786717333324e6d2f1110fedaf834fc803291b99f086508`  
		Last Modified: Thu, 30 Apr 2026 23:50:32 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836ba836443fe4c82176244d3ad0764503f10823c34b592581135e5ae45975fa`  
		Last Modified: Thu, 30 Apr 2026 23:50:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d87a9235cdd3aa55617230d1a525bd23a29f510ad3cb2e74ae0c88742291dce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbba0006245804f1c1bf3d84c42f6eab609fac634da1a90cf71c267143d41011`

```dockerfile
```

-	Layers:
	-	`sha256:e28d8b32a2e01a894835b56eb7e22cd336b8aa32d951861baeefd0dfa3b50700`  
		Last Modified: Thu, 30 Apr 2026 23:50:32 GMT  
		Size: 4.2 MB (4228026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14c6996aa4149718f8623653e0c647f6c5b4cd397fb23e6c4d161a52115e3439`  
		Last Modified: Thu, 30 Apr 2026 23:50:32 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json
