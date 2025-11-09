## `clojure:temurin-21-lein-trixie`

```console
$ docker pull clojure@sha256:c2d7f158f3ca59fa056d7763df1a733afe7df33edd9ca3e75cd6846a6e532cc4
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
$ docker pull clojure@sha256:c5f2674538c8f7ea2507e46a74136a89440f17d1f581a526e8b1c55a17d3ee3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230208962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab89bcc4720ff82a3b00e65149e400759064b97fafaf09b5e1959070178a4486`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:44:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:44:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:44:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:44:14 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:44:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:44:14 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:44:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:44:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:44:31 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:44:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:44:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:44:32 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:44:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac9cb653666e62b9a8e2d330b8d23c7e889b2f8cc3ce5a4f4cc71a773bae196`  
		Last Modified: Sun, 09 Nov 2025 04:24:26 GMT  
		Size: 157.8 MB (157825975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fa5b5c1836023cc56f488d3be5e80ed254dbf0925a3a5b51969edf6698762f`  
		Last Modified: Sat, 08 Nov 2025 18:45:50 GMT  
		Size: 18.6 MB (18579233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7c5f5277e128321a0c8d5b5efc64188b05a75f743c766aa80de33c13eac5d0`  
		Last Modified: Sat, 08 Nov 2025 18:45:49 GMT  
		Size: 4.5 MB (4517696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a0538f8d91076f7b7d7c9a864da7f1d6df90b1b52e2d014cab98418a9e5cd9`  
		Last Modified: Sat, 08 Nov 2025 18:45:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:087e5f6a8b93500c1ced0fc04b907a570cf9a7e3516f2f901dfde84f4fbeed2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e8f1c557f56145f5a2787900cfa7f812aaa90a045780cf92ae09f12d8b674f`

```dockerfile
```

-	Layers:
	-	`sha256:f6bc2066861cc89d59f5cf50ea42040929b97b15071702f1d99680433c76a6c2`  
		Last Modified: Sat, 08 Nov 2025 22:48:25 GMT  
		Size: 3.8 MB (3816488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2a4bd140760d0ac30ec1c94c6b34049818e949fcd5c912eb315861eac11037f`  
		Last Modified: Sat, 08 Nov 2025 22:48:25 GMT  
		Size: 18.4 KB (18351 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5b0fc906ecc0fb2ae14f68d6e539610071702e381728de7bc39c61c09a627162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228816196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e1c085e582aba5518769ade0b459a00c0788e0db27bd2a4fb7ea14e34adce00`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:43:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:43:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:43:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:43:51 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:43:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:43:51 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:44:07 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:44:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:44:07 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:44:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:44:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:44:09 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:44:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa385300336294ffc40596786ff1db9e50133ac24331d3eca18da1101fc7585`  
		Last Modified: Sat, 08 Nov 2025 18:44:32 GMT  
		Size: 156.1 MB (156107663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d917d7d2cd10090bb354ea8636ced64123e575011fde876d6de2e9128bd72265`  
		Last Modified: Sat, 08 Nov 2025 18:44:56 GMT  
		Size: 18.5 MB (18539930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e13daae73784a3d4c0ab011e0cd2a25d671a558d43d9518240c84577c5f6029`  
		Last Modified: Sat, 08 Nov 2025 18:44:56 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6739cd699314b7dbf16492e06b5176459fefa8e5abc2223e5d26605758aff`  
		Last Modified: Sat, 08 Nov 2025 18:44:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7f901d0289f6e6abe399dca2f577e088dae2e3e90ca5e6287b30676a0174f971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae85d2ecaf137566b5c0399cb1cbe6380bfcd1423c5a77f5ebbaab181c1a6acb`

```dockerfile
```

-	Layers:
	-	`sha256:e9bff37cfdd943df62e3e47f3f1426156e362d9f886693ffe4efeece2119c0b6`  
		Last Modified: Sat, 08 Nov 2025 22:48:29 GMT  
		Size: 3.8 MB (3817365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:931deef77581b78cbeab4a14b22a777af1e22b3e8392ce45d226a275cf163db3`  
		Last Modified: Sat, 08 Nov 2025 22:48:30 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:a4e97486f451ced0da2e53e061f184680d919014106231e63aea84abf8ac6cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234207831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f48149ac10a577e9646b0e4c7aa3923cf8cfd1cce7478c8da45d4f87fedb641`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 21:34:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:34:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:34:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:34:48 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 21:34:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 21:34:48 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:35:26 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 21:35:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 21:35:26 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 21:35:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 21:35:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:35:30 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:35:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f62b25a3d3796aee9675283f38cc81cb5638600359ad12a143ed501f80cadd`  
		Last Modified: Sat, 08 Nov 2025 21:36:11 GMT  
		Size: 157.9 MB (157942894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c70e739604527b84361fa8a0e1a06e596ca53987695e976249a82ac9784e09`  
		Last Modified: Sat, 08 Nov 2025 21:36:19 GMT  
		Size: 18.6 MB (18636625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bc985e70d064ffda4d5250177a227fa9841881630fd381d12afe273ebe9d48`  
		Last Modified: Sat, 08 Nov 2025 21:36:17 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ce8fd33a9c13a394254d1189fd59901457a3ca0ae85bbe402826087b1bc72f`  
		Last Modified: Sat, 08 Nov 2025 21:36:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6a5c0d877c44eea3505aecdff038a7a319c74237e04f4b4151b5bcaecd3e5192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63abf4e3e307c18dd2d535d922a434e722412647434ce114e73c151f1101a7f`

```dockerfile
```

-	Layers:
	-	`sha256:c95fd70617d09e9b2a16f46b9e3dc07f40e116c2fbd666e1060cc66a27822dca`  
		Last Modified: Sat, 08 Nov 2025 22:48:33 GMT  
		Size: 3.8 MB (3817486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f233caf92f33580e2e3a2a32252be2d2b388deedb6fb98320b304d276782f39b`  
		Last Modified: Sat, 08 Nov 2025 22:48:34 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:6dfd3d71224469fac5537c01695cdef530decb8c3bdf710e96ca212656b9bec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224413751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d55027c00dd85a88db90b4fe4eb86b7875275fd89f89d66bd266197bd63daf1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Fri, 07 Nov 2025 06:33:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 07 Nov 2025 06:33:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 07 Nov 2025 06:33:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Nov 2025 06:33:03 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 07 Nov 2025 06:33:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 07 Nov 2025 06:33:03 GMT
WORKDIR /tmp
# Fri, 07 Nov 2025 06:34:33 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 07 Nov 2025 06:34:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 07 Nov 2025 06:34:33 GMT
ENV LEIN_ROOT=1
# Fri, 07 Nov 2025 06:34:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 07 Nov 2025 06:34:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 07 Nov 2025 06:34:49 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 07 Nov 2025 06:34:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f02f73111e105921cc185c6c33251c2d50b1703e0a326d71d528fa31b308a9`  
		Last Modified: Fri, 07 Nov 2025 22:59:25 GMT  
		Size: 153.6 MB (153593539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eab8a0694c2a94b63bac43f71ae459023e117cfbd1b9c9dacc941b7a979c97`  
		Last Modified: Fri, 07 Nov 2025 06:39:18 GMT  
		Size: 18.5 MB (18531067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da927d70cedfee184c09d7bdd375b179d2defed535252f705d6ba2a7a7feb45e`  
		Last Modified: Fri, 07 Nov 2025 06:39:17 GMT  
		Size: 4.5 MB (4517792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dcd1f91d730fb4e534fe2a702fd1eaa806a168aae85b1ba229dcef83fe9a00`  
		Last Modified: Fri, 07 Nov 2025 06:39:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a4971809ed5ac115a4ab3b9af50bbf3b05f0b0e4c600cb274396939966ccc176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3825357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5604861d50b69ef768869cb0d601e771ef6ab35c88d92e3a3f92876e6cc8b901`

```dockerfile
```

-	Layers:
	-	`sha256:b92bb63b33d6bc04d613bcb4b2d15a74520889a84a09e6ddf7ca3b605cfbcbad`  
		Last Modified: Fri, 07 Nov 2025 10:36:50 GMT  
		Size: 3.8 MB (3806961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0f3b089a9cfa0b5110fc2106774113e422c1845f008bf73f616238823530e6a`  
		Last Modified: Fri, 07 Nov 2025 10:36:51 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:598913638908cd157ce58a346e6b5aaf12d4fc9b46b0dafee46d6426f6a76c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219560623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744c15ad72cfec3e1192a962323e695935b62050dc0db27db63ea543039ad2e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 20:30:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 20:30:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 20:30:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 20:30:17 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 20:30:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 20:30:17 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 20:30:30 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 20:30:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 20:30:30 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 20:30:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 20:30:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 20:30:32 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 20:30:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03b440ad1ae9ec56d21ad6945930007c4f3b5f2f34fef5c2ff1ff4580753129`  
		Last Modified: Sat, 08 Nov 2025 20:30:59 GMT  
		Size: 147.1 MB (147069867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f676521ccf1cf343109cc41639bb690b2ca3ec5fd2e6bc703d2f52596f2bb4`  
		Last Modified: Sat, 08 Nov 2025 20:31:06 GMT  
		Size: 18.6 MB (18620289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11dc59c72b6987f039bd8724190a8d18e84897e22c3b68669c366f3cec0521ca`  
		Last Modified: Sat, 08 Nov 2025 20:31:04 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43e498c5624f22d19c46990eb5b9c88aab183d0ad750901aa4157f7aeffc84f`  
		Last Modified: Sat, 08 Nov 2025 20:31:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:96942c85bc953daf5021d518ea58bcd96f9833226d69d3a0845a9e20a27b4bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3155ce54a743a8097f7550db00ce4b21b8feecff15b2e9a426d60c5d208ccf`

```dockerfile
```

-	Layers:
	-	`sha256:aaf8f4926e835a52f051aca45312ed20f7bf18e30bcb2f2bffa12b92b0eb0859`  
		Last Modified: Sat, 08 Nov 2025 22:48:41 GMT  
		Size: 3.8 MB (3812915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad03a32bc10f4476756b09e9b05f5f35b292728ac5a0f0b21385a3f747903f84`  
		Last Modified: Sat, 08 Nov 2025 22:48:42 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
