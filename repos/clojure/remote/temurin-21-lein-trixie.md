## `clojure:temurin-21-lein-trixie`

```console
$ docker pull clojure@sha256:61edb0ebdbb2e7fa5dc1a78c8b52d9d4f122c783b40f7d40f73198beb44c9761
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

### `clojure:temurin-21-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:5095b36ba9c035d39c4db640ca87e8d7da43c797fc91675ac5ae762bf8c0a02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230213351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676d8610fa4588048342fd9a0b0f7b0d712137b83307c07579d5fc9d2baf95df`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:54:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:54:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:54:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:54:52 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:54:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:54:52 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:55:10 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:55:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:55:10 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:55:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:55:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:55:12 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:55:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d82917b492c8ce04e0f65565a2842cfb9d1f3f3f114e0b66589d71154851af`  
		Last Modified: Mon, 08 Dec 2025 23:55:55 GMT  
		Size: 157.8 MB (157826042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae86337c47062a193b9c05cf1baac029613b372afc37d5889cdcd0dc0cf92d94`  
		Last Modified: Mon, 08 Dec 2025 23:55:42 GMT  
		Size: 18.6 MB (18579637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870049b8a978b4d030fd7830dab77bc68a375c98851577f2fa01f04d730a7e9c`  
		Last Modified: Mon, 08 Dec 2025 23:55:41 GMT  
		Size: 4.5 MB (4517723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546490e3f8f4ab99e926f448bf6f8949e840a7a6518a6af1c0524e599c8e1a9f`  
		Last Modified: Mon, 08 Dec 2025 23:55:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cce834c643802fbe5242c50d9df1e40d1d568c4ce5e07db147aebfb075b36815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:237e647da1943a4c7a886db991b394b6a52f5d774e9965c6dbb7b292001ac8e7`

```dockerfile
```

-	Layers:
	-	`sha256:1c63b0a7ac2f7436bbb1d76d62905249ebec4759f17357a1a27d76e3fae283e1`  
		Last Modified: Tue, 09 Dec 2025 04:43:38 GMT  
		Size: 3.8 MB (3816482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40f234a05c9bc36ae1f2d569796232f64ad602eb3081147bcaddd479f7620260`  
		Last Modified: Tue, 09 Dec 2025 04:43:39 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5539438bf3bbb6b16fe9e3f2219149e73382b92e4c44ee394faae239e3947613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228816673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a12aa1899ec657a3b0fc8d6d795689c662796f2a0e44e2975e7f4a196fdfab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:02:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:02:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:02:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:02:01 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 00:02:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 00:02:01 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:02:17 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 00:02:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 00:02:17 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 00:02:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 00:02:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:02:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:02:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbe7fcb0634a746fddf85708120e696443c2f65d421cdd7b6e032eaed5147e8`  
		Last Modified: Tue, 09 Dec 2025 00:02:58 GMT  
		Size: 156.1 MB (156107650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26e354de6abcadc754fd5f600a3e0b861be3e85605810dce96928d14eba5a92`  
		Last Modified: Tue, 09 Dec 2025 00:02:48 GMT  
		Size: 18.5 MB (18540630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a139580c6ddc2465143bc9378eca52a8915dd5f0a354fbc3667a67645df7ca7a`  
		Last Modified: Tue, 09 Dec 2025 00:02:50 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054c9fff6e7faada7fc2ea8465e9fced93195e677ad6d30515f2b03bb19e0677`  
		Last Modified: Tue, 09 Dec 2025 00:02:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b38259af886a90bce70a036edc7b17ad27c96eba947f212510b9a333bde8f956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00fee8a17fde94444f0c672d7a04f1a84acfb76058ced2db5fc78de6fe1efff`

```dockerfile
```

-	Layers:
	-	`sha256:96825cdfd3f05ae5df3537144b0e859c544516d6312db993b29d5f29c45c76fb`  
		Last Modified: Tue, 09 Dec 2025 04:43:43 GMT  
		Size: 3.8 MB (3817359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece6bde546603df1a40d6edc0f439ec993806f353c27e7fbb35da7ac0eff5d43`  
		Last Modified: Tue, 09 Dec 2025 04:43:44 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:df41c8e743fc3c753b672e12040d8d0e2c1e8c2f784b134d2ff3b1acc738509e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234206722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fba662605d25df9b79af87a8e9588be818193239f7af8b0ed2e802d034fe5a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:29:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:29:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:29:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:29:48 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:29:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:29:49 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:30:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:30:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:30:31 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:30:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:30:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:30:35 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:30:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6a2ef35163b9d4f6648137cf0019838288c6072622a6112548fb68bfe52e18`  
		Last Modified: Mon, 08 Dec 2025 23:35:07 GMT  
		Size: 157.9 MB (157942951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0c3d972a1c1e5958d2cd2704a17d6fad73e5caa8ac3270f16a8c00982583f7`  
		Last Modified: Mon, 08 Dec 2025 23:31:40 GMT  
		Size: 18.6 MB (18637114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169f0a063d991ca954bca204e4d9be719a1859285e3691fff7e6af041c03ea3c`  
		Last Modified: Mon, 08 Dec 2025 23:31:33 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca79c1c7fd24e9335b94385e0dada9851d08ad99ae0f00636915983d6f2d1fc`  
		Last Modified: Mon, 08 Dec 2025 23:31:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e9974e0d9913ed8377a8dfac967f61fc1f878fd7b6c4b631075d33619ddfadc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587f66e2f0af835f3da40f476ccd4623da0cc9bdf2c137559c415e4bcf55431e`

```dockerfile
```

-	Layers:
	-	`sha256:23b25a5db43a4cbcca832edbc0d4021957ae5e375e329920909a06004c25034d`  
		Last Modified: Tue, 09 Dec 2025 01:37:55 GMT  
		Size: 3.8 MB (3817480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c27bbbbbd0a0f0a1d4c80f01b2b3ee68c6a081c0c5df8fced39aaefc7a617fd`  
		Last Modified: Tue, 09 Dec 2025 01:37:56 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:20c7a52dced001efd07fa9e8317b86b6b309189595148fc08cebe5982360799a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228015345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2d987f6ade5f7531a267bb9cc48dfecd8ee67b9df081e13c3a556093b1cc8a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 18:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Nov 2025 18:20:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 20 Nov 2025 18:20:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 18:20:05 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 20 Nov 2025 18:20:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 20 Nov 2025 18:20:05 GMT
WORKDIR /tmp
# Thu, 20 Nov 2025 18:21:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 20 Nov 2025 18:21:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 20 Nov 2025 18:21:35 GMT
ENV LEIN_ROOT=1
# Thu, 20 Nov 2025 18:21:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 20 Nov 2025 18:21:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 20 Nov 2025 18:21:53 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 20 Nov 2025 18:21:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ed0507b92b5f6d1bbf086936336ca6e85b2d0afbbaab333064cc752190ce52b9`  
		Last Modified: Tue, 18 Nov 2025 01:45:17 GMT  
		Size: 47.8 MB (47771195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9510e39712dd763e37991974565f84df07e5754bd9efcade332f8c04005a4403`  
		Last Modified: Thu, 20 Nov 2025 18:38:42 GMT  
		Size: 157.2 MB (157194242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d0a709acf0eec1c81094f998941014bb85d03170fbfb75b344efa637d0d305`  
		Last Modified: Thu, 20 Nov 2025 18:26:30 GMT  
		Size: 18.5 MB (18531674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76e86e50a152e7d34183126862a68322bb1bd028eab66e860cbd96b32157cf8`  
		Last Modified: Thu, 20 Nov 2025 18:26:25 GMT  
		Size: 4.5 MB (4517804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf5a4e09fb6c1a091b378ecc96596ed99dff403c2caa2156ae2d5653860d426`  
		Last Modified: Thu, 20 Nov 2025 18:26:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:eb96909fcc5cb8c62fdb0acd9d392a8923542e0364fd0a61fff4b3d228165c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3825353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb77dd9681ed9a856c3a92834675d877161d3f166fbf41d1ae257665c4414186`

```dockerfile
```

-	Layers:
	-	`sha256:2b521cf03ff3bc6f24e6a0328f435f54bc4d03cec387bb4c7cbea2a0e59abf16`  
		Last Modified: Thu, 20 Nov 2025 19:36:50 GMT  
		Size: 3.8 MB (3806957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d98b7dc0d7c9d3f4aea2347e4293503afc7258d5b35e1197412152164549541`  
		Last Modified: Thu, 20 Nov 2025 19:36:51 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:2db41c475db1c1559d6e29c49fa5b596dd0494634d2282bf385a4e44adaa3ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219554531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508274dd9a118e6d2554def5aaf4c625c7a895e43d4189064b0486fb958eebc0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:31:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:31:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:31:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:31:13 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 01:31:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 01:31:13 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:31:27 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 01:31:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 01:31:27 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 01:31:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 01:31:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:31:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:31:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ad8af80bd1fca505a458dadc68d16da2d131f0ace69cc71fe587e4b3a2a78d`  
		Last Modified: Tue, 09 Dec 2025 01:31:58 GMT  
		Size: 147.1 MB (147069847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757bfe0ba7933814c8ed5d3743e7ad13247a58b4ab34357cec3963165a09e7c2`  
		Last Modified: Tue, 09 Dec 2025 01:32:05 GMT  
		Size: 18.6 MB (18620654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4986d47826dda3c3468a6be08162d2d597dccaf02533a61446aac64bcacf3f20`  
		Last Modified: Tue, 09 Dec 2025 01:32:04 GMT  
		Size: 4.5 MB (4517696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264ea6c94208f4699e90619db2bc4ab5376dfae83e042a86408ddcc690294216`  
		Last Modified: Tue, 09 Dec 2025 01:32:04 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3d29ea9a23a54fce0c4bd4806468d866d22d5b40ac589407e55cb7604f3950f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f6aee6f93ac448cd35dbed6ee90387548852b9c6f2a1ce325b80c8d0ed98ee`

```dockerfile
```

-	Layers:
	-	`sha256:6ccad098278b386d6e39f7eaf9c32040f495e7a027e7dad6a3f174a3b708979e`  
		Last Modified: Tue, 09 Dec 2025 04:43:54 GMT  
		Size: 3.8 MB (3812909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a38ae858177688cec332375ff310201092ed7bea818a352440dd165e63b74218`  
		Last Modified: Tue, 09 Dec 2025 04:43:55 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
