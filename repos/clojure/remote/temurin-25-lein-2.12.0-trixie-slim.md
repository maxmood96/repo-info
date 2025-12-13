## `clojure:temurin-25-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:1e4e5e88ee3fb18df2e5ae56a3fadadd9c73046e4f774771108ad84e21f78522
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

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0b396b1c917384d66c78bc40daf1b2162a4f90d0429782f74ae4a104323f0469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142787084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c8b46063f976692bd0368daa4cdd3162553d70b1eede3c69b38c6cc965ea3c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:56:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:56:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:56:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:56:20 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:56:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:56:20 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:56:36 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:56:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:56:36 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:56:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:56:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:56:37 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:56:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48896bd39a9492a61490b9e457ce0ce60af724794a40608e391b4c5e52d04d1`  
		Last Modified: Mon, 08 Dec 2025 23:57:13 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c730e29ccd1dbbbef0028d9615d67c329babcfefa7a0b38756f4ac5f2e8e7bc9`  
		Last Modified: Mon, 08 Dec 2025 23:57:03 GMT  
		Size: 16.4 MB (16447160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2be636d971621ea1d7078a6f6029b9813b86554337240987d29c1ced421c74`  
		Last Modified: Mon, 08 Dec 2025 23:57:02 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8f0d57244d9b0f717b231e60cec86924afaaa8d6870ab7a34628eed01c680e`  
		Last Modified: Mon, 08 Dec 2025 23:57:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:388f613d8cfb97a0e101f1c6622f93825117ddc574f9d1b980a3f8676cd8d08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c757f8046e5b688e4bc75c5a4876822cd4b648c6cc459f16b7f5778defbf4e`

```dockerfile
```

-	Layers:
	-	`sha256:8003c4e5f1b4ceba8f9cb51cbfda74ec5c7b1860b66b65337806630d784624be`  
		Last Modified: Tue, 09 Dec 2025 04:35:41 GMT  
		Size: 2.3 MB (2314754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1056580e9c592aa51da3310a98432e492973c62e802ca3d8006df3c74ec2ddf6`  
		Last Modified: Tue, 09 Dec 2025 04:35:42 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0e1a1e8b27718fb36c2d095e6edcf2cebacc8892d8282ff7fc954b42aee4d6c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142123128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785822c907394fc163994bba23421cff68f9ed8747b5de83bc9a68ee67eed1d4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:03:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:03:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:03:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:03:42 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 00:03:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 00:03:42 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:03:58 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 00:03:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 00:03:58 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 00:04:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 00:04:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:04:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:04:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b78a4bf9c76a6a9314447be88b28314f5f3da6c99844402b32067a74715001`  
		Last Modified: Tue, 09 Dec 2025 00:04:41 GMT  
		Size: 91.1 MB (91052516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfbe995ec96526e82f6b1efc24c4dfeb301dc112d70454093e2becddfafb304`  
		Last Modified: Tue, 09 Dec 2025 00:04:30 GMT  
		Size: 16.4 MB (16413807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796c36fd3d46f1fd58ac68c4576b216e2f5fc20ee3483c495449c1f6b1e96777`  
		Last Modified: Tue, 09 Dec 2025 00:04:27 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15336b786c8582203d04d80afc5d695dead03091b5ea9c3e42fe92e5071872ff`  
		Last Modified: Tue, 09 Dec 2025 00:04:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f4637ff9f864c2184ade2e34e82089b4e72674c5b151438c16f33bd443953e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba1da53d18c45441f561918c4de39b0b663e31cc53baeab78e96fa665a07fdc`

```dockerfile
```

-	Layers:
	-	`sha256:448cf8960e381d87f12a5337caca9fc71595fa9567227f24491319297930faf7`  
		Last Modified: Tue, 09 Dec 2025 04:35:46 GMT  
		Size: 2.3 MB (2314393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4114873fa461a519274dc2109c8220ebb47504d3036f7f081ec3f0a3f5b4bc94`  
		Last Modified: Tue, 09 Dec 2025 04:35:47 GMT  
		Size: 19.2 KB (19179 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2581cd14c0f9e91977ee520a4b49c6de2aca37f08a4199b7575c369ca1b60f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146211149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c659d867aacb78774193f8bf09e53831bea7987ec7aba3a936e1b196b5db4b32`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:55:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 03:55:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 03:55:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 03:55:25 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 03:55:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 03:55:26 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 03:56:04 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 03:56:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 03:56:04 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 03:56:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 03:56:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 03:56:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 03:56:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e90333d0ab795a7ae2c0a51c53552c38eb8f814a4df79b46ded26ce84b6fab`  
		Last Modified: Tue, 09 Dec 2025 03:57:08 GMT  
		Size: 91.6 MB (91610796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e011966ef3fca031e85a9597fd54d2b9c8bd27ade22d4b9696ad0830167fce5`  
		Last Modified: Tue, 09 Dec 2025 03:57:02 GMT  
		Size: 16.5 MB (16485304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0a8a5f489314ef86567a313d91b0dc8d214d14957874471513a579bfabe0ba`  
		Last Modified: Tue, 09 Dec 2025 03:57:00 GMT  
		Size: 4.5 MB (4517731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8651b0f18446654067c278ad61dd681518d2d60176a8109aa6c95f721404a39b`  
		Last Modified: Tue, 09 Dec 2025 03:57:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:451a6f240afb911928715049d593b9499e48d722a1f87551cc1cc764586f7451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2aebab891d886fbd97c1a7910b24c21e8e8950bc1539fd32f81a0399ddafac9`

```dockerfile
```

-	Layers:
	-	`sha256:62288e2d3bd850f8cd96b08c52491d3937e9c3c1a369a70b3a1109252d570005`  
		Last Modified: Tue, 09 Dec 2025 04:35:51 GMT  
		Size: 2.3 MB (2317044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a6972bc14fb7f88a197bfbc5be181e1ddcb8c4dbfd0785ce47fe2d0cc030f9b`  
		Last Modified: Tue, 09 Dec 2025 04:35:52 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:a34694d5cb76a4f49328a5702a5f6e002099952462d775f56f584993d0d30a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139942108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2580f70ddd4a191ad018bf42ebf65de10596d7c14f41def7c7e2818c15a9e80c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Sat, 13 Dec 2025 19:15:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 13 Dec 2025 19:15:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 13 Dec 2025 19:15:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 19:15:07 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 13 Dec 2025 19:15:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 13 Dec 2025 19:15:07 GMT
WORKDIR /tmp
# Sat, 13 Dec 2025 19:16:37 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 13 Dec 2025 19:16:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 13 Dec 2025 19:16:37 GMT
ENV LEIN_ROOT=1
# Sat, 13 Dec 2025 19:16:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 13 Dec 2025 19:16:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 13 Dec 2025 19:16:54 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 13 Dec 2025 19:16:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a299023170aa749b8b31ddbccaa883d75e32b7625d16dd55056362d3561393`  
		Last Modified: Sat, 13 Dec 2025 19:20:42 GMT  
		Size: 90.8 MB (90752844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977e54a0197b3134f6fdaf30aeaf49ed33c399a1ace927944b8d825f00de9ae6`  
		Last Modified: Sat, 13 Dec 2025 19:20:35 GMT  
		Size: 16.4 MB (16397892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc79ab5e016811807a77e951b8eb96a4c4611c2e34e2c6b66913e813f0b3dbb`  
		Last Modified: Sat, 13 Dec 2025 19:20:34 GMT  
		Size: 4.5 MB (4517786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638b039f49be5ee54589f087807f7f6044516012714375e82f233502dfa7768e`  
		Last Modified: Sat, 13 Dec 2025 19:20:34 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a6a6ead6a68619128380ad81c50642dd5b66ff85c696d02c5cf94e464b18128e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2325901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59f899a65558e83fde028a78ac9c47e1d143cb961bb15a730b8bab6b142d05b`

```dockerfile
```

-	Layers:
	-	`sha256:ed48de9536fc6c035cad375bfb355bde7c200b8e41e71a324ae7ac34f46191a8`  
		Last Modified: Sat, 13 Dec 2025 22:34:37 GMT  
		Size: 2.3 MB (2306811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c1bf22f74cc6b5279018a51fdf990c31b047f8e37c312fe35530bdb990d291f`  
		Last Modified: Sat, 13 Dec 2025 22:34:38 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:664c6a7d0c596ce541a801b2edf2d53f8b5e37ee9b226c229efb7e01cafcc893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139046302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7af637657ca9f9cfb0d2406f81d874f2afd3e433825f3dd1dc835954768417`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:33:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:33:39 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 01:33:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 01:33:39 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:33:54 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 01:33:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 01:33:54 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 01:33:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 01:33:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:33:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:33:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b901607e1053160f0c4a5999035c86877af07f0a5ab635c3250bef9051f1d4`  
		Last Modified: Tue, 09 Dec 2025 01:34:38 GMT  
		Size: 88.2 MB (88210741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42acfd57089deac6966b018a73cb243f9f9df8cf2f0272a590de8b3e104d37a`  
		Last Modified: Tue, 09 Dec 2025 01:34:33 GMT  
		Size: 16.5 MB (16482982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c40673e97d7aac3d731f999bc10a83a7117bc0c1b4e0f80c82191a613d6a54`  
		Last Modified: Tue, 09 Dec 2025 01:34:29 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98f8d23ed008b634baf4f2b3896b6a88601f64a30a632fd6c6d9db2bc1c1712`  
		Last Modified: Tue, 09 Dec 2025 01:34:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6252f85aa2c5c20b3e60ba2ab0cce8322403d94cf18c069d70ca43b9aa63bfa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2332762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1887277aa283ac15fcabeb22a79852ab45dd862c41e37c34f2e2d7743f41049c`

```dockerfile
```

-	Layers:
	-	`sha256:41c2a769433b6025c359a87323770910d8a02f9ed504cc6794366c9a3da325cf`  
		Last Modified: Tue, 09 Dec 2025 04:36:00 GMT  
		Size: 2.3 MB (2313729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d655f6038886374ff1f12711bfbe2b8ccf80d3703b589471bda5a7f4412a45`  
		Last Modified: Tue, 09 Dec 2025 04:36:01 GMT  
		Size: 19.0 KB (19033 bytes)  
		MIME: application/vnd.in-toto+json
