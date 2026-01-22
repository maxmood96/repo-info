## `clojure:temurin-17-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:e5f982c6d1bda03401860ed31e48b33a8736aef37611e23622b8adb84362d62b
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

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:6fb1f6a647f0016682f42b8e274122771dcf0d8089aac8e653baf8681e7fb561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217231544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8703581a4ad9a7d376b3f88c8b840af086e7d6cd72b2e7f2db6bccaf7309c4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 01:53:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:53:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:53:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:53:45 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:53:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:53:45 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:54:01 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:54:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:54:01 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:54:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:54:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:54:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:54:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d2d2fd7a85b4685f5029a03db05765ee2453f4f27331c98f1c01b266406b2b`  
		Last Modified: Fri, 16 Jan 2026 01:54:24 GMT  
		Size: 144.8 MB (144848042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea5fd9abd659e5e21cb0bfe6614c435320d5f65d3bddb932ff75f6c881875eb`  
		Last Modified: Fri, 16 Jan 2026 01:54:21 GMT  
		Size: 18.6 MB (18579694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6470df8ebff0a338caf966d512dc8cf800f1ef36942c201d4277d429d9875e16`  
		Last Modified: Fri, 16 Jan 2026 01:54:20 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8683cbe8831ee68f181e6f7cc35dc79e32fc8b263d9e3ae77da04daff2457d`  
		Last Modified: Fri, 16 Jan 2026 01:54:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:afd6f38001a312728d004109772dce776b41efc04a98761210efb4b1d778a6c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b2bdca3fec3598e3468700783c0c0331e5f00fb6398b2da4ddd8945a1fba04`

```dockerfile
```

-	Layers:
	-	`sha256:849c0aff3600c3f6992d5e281896e54ce6d5368ccfae5c4398c313a2117f9adb`  
		Last Modified: Fri, 16 Jan 2026 01:54:20 GMT  
		Size: 3.8 MB (3814239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db3cf5fa9f8d56cb91c84eaf9d5f92ebd1d2d2796e7da7e75faef28fb0d08b2c`  
		Last Modified: Fri, 16 Jan 2026 01:54:20 GMT  
		Size: 18.4 KB (18351 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d5ccb6c6a61de4421a1138944a1f20eb601885ba04525a417d774cc7006150b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216386924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46884cb30e506f1e68c0f7c5cda244228d29cc7a73423b930a5139a95a2ea055`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 01:57:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:57:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:57:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:57:35 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:57:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:57:35 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:57:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:57:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:57:52 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:57:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:57:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:57:53 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:57:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35f3b1dfb886999b55bcff2ab17c16413671bb399727a87732df4f5ac0f6f92`  
		Last Modified: Fri, 16 Jan 2026 01:58:37 GMT  
		Size: 143.7 MB (143679919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69934a4e01fef46c8120ac229013d152095782aea1548f861bd4c318b0d382c4`  
		Last Modified: Fri, 16 Jan 2026 01:58:12 GMT  
		Size: 18.5 MB (18540787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c440400917cbec5088b0b2fbf2d26b17a5ce024afb93afe9f5160edfad066821`  
		Last Modified: Fri, 16 Jan 2026 01:58:11 GMT  
		Size: 4.5 MB (4517706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36da625707e9243d5d5a6fb55fd69e17cd2ccb5734c16ab0b428e20a0e3940e6`  
		Last Modified: Fri, 16 Jan 2026 01:58:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:90595dfd6f07a9183fb004e3ffbe320cee021d5fe85c5198d96ffdfe002e0083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d9bbc17c4a26f919d1c13444b8d5b801a9735701aad02a5b7d6a1d4b00d641`

```dockerfile
```

-	Layers:
	-	`sha256:e6738a7a3e0559ffa8c8df2fd4b367432a5721e0fc06b19a8b20b7230cc944de`  
		Last Modified: Fri, 16 Jan 2026 01:58:11 GMT  
		Size: 3.8 MB (3815116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdadae75e927a4fc59ef17dc95850cec4e829cf194d505d50414c641261438b5`  
		Last Modified: Fri, 16 Jan 2026 01:58:11 GMT  
		Size: 18.5 KB (18472 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:e43fd6c54a637ac58ff600273f307f2ed4087ff913925f7e8ffc4bf9d745d81b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220787159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750d5101f0efd94c685c822bfe4d7a2096c6f7c214b905734f7edbbad1c816b3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:16:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:16:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:16:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:16:27 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 03:16:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 03:16:28 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:17:29 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 03:17:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 03:17:29 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 03:17:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:17:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:17:34 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:17:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6bf15ee3631779c5e8a10fa679c64130a5b54ad0969e061ffe1b160beac0d5`  
		Last Modified: Fri, 16 Jan 2026 03:18:34 GMT  
		Size: 144.5 MB (144524715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a62236b2638faa68d0b09541095c7181e2e374730d1e86f8437787fe943dae`  
		Last Modified: Fri, 16 Jan 2026 03:18:39 GMT  
		Size: 18.6 MB (18637296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c09c3f0f5238a782df1b6b3b918720a39f5edc42b03b2e1fb92db3b4cecb60`  
		Last Modified: Fri, 16 Jan 2026 03:18:38 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15084bfb054805a9bbbd4ac313e5a8e9f108c81d760723d541f73def9b8ae534`  
		Last Modified: Fri, 16 Jan 2026 03:18:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f65fc9cf6db96ece203b16d939e4194d783e9a1ebd31d297137eeb3d86842ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2419584bd539e548368ad66a8343e3aa2ba07382a7b937137715b6a053497619`

```dockerfile
```

-	Layers:
	-	`sha256:dde42d0fd992a9ea5fbecba326be9cb4976168e9ce7e213885b2053288256cc0`  
		Last Modified: Fri, 16 Jan 2026 03:18:38 GMT  
		Size: 3.8 MB (3815239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb3852fe56df27bf2aaada7ddaf19021ccab492fc87ca4f38f62eb217ee50c0`  
		Last Modified: Fri, 16 Jan 2026 03:18:38 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:72cbf67bae251faee1c9f121f51ca8df093a61fec9abf5ba8a57170dc6be3617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 MB (212710365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0220ad6b7898aaf5ba676aa3e8bc26633a0060c004ede976896d33eff1313c44`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 03:13:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jan 2026 03:13:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Jan 2026 03:13:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 03:13:16 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 22 Jan 2026 03:13:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 22 Jan 2026 03:13:17 GMT
WORKDIR /tmp
# Thu, 22 Jan 2026 03:14:48 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 22 Jan 2026 03:14:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 22 Jan 2026 03:14:48 GMT
ENV LEIN_ROOT=1
# Thu, 22 Jan 2026 03:15:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 22 Jan 2026 03:15:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 22 Jan 2026 03:15:03 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 22 Jan 2026 03:15:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:559020494fc8527e77b291bee49cdac1db6bca66f8926cda195e0e4ebe7d2d3d`  
		Last Modified: Tue, 13 Jan 2026 01:06:23 GMT  
		Size: 47.8 MB (47770843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f2dc6ee466bc891aa5bacbe66750c17f24c66ed70eb75e898c457e89e0b77a`  
		Last Modified: Thu, 22 Jan 2026 03:19:08 GMT  
		Size: 141.9 MB (141889561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fccd29ea1f73e6ede424ecf91bb3ae4554cbe65b75d56b38311e6510bfd2bb`  
		Last Modified: Thu, 22 Jan 2026 03:18:49 GMT  
		Size: 18.5 MB (18531741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe3031736ba6eacecb2a4e5113011503ac3304187aa0f151935aece4f5c3a12`  
		Last Modified: Thu, 22 Jan 2026 03:18:46 GMT  
		Size: 4.5 MB (4517790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6630b0606e0c8c49a5c8aaa952282c8887f26e514e26440f324f1aacd0b56a`  
		Last Modified: Thu, 22 Jan 2026 03:18:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:17035536c89e4d7c5bd5f9419c9bfce05d106f1a8e83949f62483e6afbe2e892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3821192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715d5750ab32d404da207ac99188407ffbb5d1713b98dc7cdec1196c73fde232`

```dockerfile
```

-	Layers:
	-	`sha256:931aa201b913e7e414bc52ee52bd454380a80cd72ce8d909e54bb5dfe1cdd9db`  
		Last Modified: Thu, 22 Jan 2026 03:18:45 GMT  
		Size: 3.8 MB (3802797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6868c2f4cc7a73de460a19a247a55f019553e395d15829d27b09739833ddab2e`  
		Last Modified: Thu, 22 Jan 2026 03:18:43 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:f503b1ef3fee9e325a922a7787accacb969a30122229d496cfa21fc6b8272871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.3 MB (207347317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8ac1662a5cdab876a92224468129ff5bd98f3c3d0f23ee14ca04186cdbfb8d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:14:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:14:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:14:51 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:14:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:14:51 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:15:04 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 15 Jan 2026 23:15:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Jan 2026 23:15:04 GMT
ENV LEIN_ROOT=1
# Thu, 15 Jan 2026 23:15:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 15 Jan 2026 23:15:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:15:05 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:15:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:46 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08054f6039e2280b26ac40e203037cfb04df46b507fd01341e85a498b8db938`  
		Last Modified: Thu, 15 Jan 2026 23:15:54 GMT  
		Size: 134.9 MB (134859759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b60ea8df64b8cca44bbc0df45cef91eeb194e16807f2dead8f4a8c786be624`  
		Last Modified: Thu, 15 Jan 2026 23:15:39 GMT  
		Size: 18.6 MB (18620708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2a3c2c900957396a0f8611f8f51e98d087108b0a336b5ebc6aa3d29111e0a8`  
		Last Modified: Thu, 15 Jan 2026 23:15:27 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658c9dddd28e667a64d237c79f2f717cd5109b651188ec24a33983db49c19bba`  
		Last Modified: Thu, 15 Jan 2026 23:15:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a987fd21f0cb5276fe7693e24af3a5cad1716fc7962217776f2afcf337826785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3829018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc0a7012989b56502b0555a40cd661e7c4a00bddc66ffa27f966f0323ca20256`

```dockerfile
```

-	Layers:
	-	`sha256:a7407f19a3435b456b68c57bb6eb11b97daf882f2ed168e9eefeee1035babee3`  
		Last Modified: Thu, 15 Jan 2026 23:15:27 GMT  
		Size: 3.8 MB (3810666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75e7387442387b1721d48988a09176685afd3379f1200f17a83503c282b32df4`  
		Last Modified: Thu, 15 Jan 2026 23:15:27 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
