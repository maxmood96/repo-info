## `clojure:temurin-21-lein-trixie-slim`

```console
$ docker pull clojure@sha256:1b97546a2336a6cf5331ede0536758e18f791e43d76115a916668dcd5b9516fb
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

### `clojure:temurin-21-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bf4d62593e024ed908179ec94a7f5ac556971072343ec58583adb23013e68621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208913214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2a4aa260e5498fc0132f0e1555d4577cc0287f8c4f41bc3acfe768a9ad713c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:59:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:59:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:59:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:59:45 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:59:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:59:45 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:00:00 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:00:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:00:00 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:00:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:00:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:00:02 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:00:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3fb4f5de2024ae1d112b6fd391319873e072ff292bce1221237868407b660d`  
		Last Modified: Wed, 20 May 2026 00:00:26 GMT  
		Size: 158.2 MB (158166942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b94c90711d60f3fe62b2467ebae6f3616263977e83a00a4c8fbdad13d515a13`  
		Last Modified: Wed, 20 May 2026 00:00:21 GMT  
		Size: 16.4 MB (16448163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13d58e21d6ca2c4ef241307e7098b3bc3dd3d23594f8d9063acb54fa30c89a5`  
		Last Modified: Wed, 20 May 2026 00:00:19 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bbd3e86e65edb38ee9b695d05f0a253f4e7ba84b8471f96ac0d6ccea0e84d0`  
		Last Modified: Wed, 20 May 2026 00:00:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6241338ee8a12ce08ebe636c69a175a7beed3b8bc627e916d155a9257c6bb188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a17e464f8124972804d6a8b11673980e8ce6ad96df69af583d50a388fece686`

```dockerfile
```

-	Layers:
	-	`sha256:91272557da93055eb934c17f13f45c33914da068afea78ac0183d1c8b70e1c20`  
		Last Modified: Wed, 20 May 2026 00:00:19 GMT  
		Size: 2.4 MB (2367309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91a132eaacae37ff16b59b7dd2c61bfa0967936a23940a7c398e140836824f6b`  
		Last Modified: Wed, 20 May 2026 00:00:19 GMT  
		Size: 18.5 KB (18540 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0885601fa31c31af4d5691fbe1bd8eeada1c9590540ff3712ed0db1432e6a120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.5 MB (207535697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c3392f4122aec76d86c195587018fc76a0de3f47553a39d7c419e870a7e119`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:29:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:29:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:29:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:29:42 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:29:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:06:51 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:07:08 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:07:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:07:08 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:07:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:07:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:07:10 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:07:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4709e949647734fee27e681325c8b88f746cab646fd7c1860b080fd0d8ae1ede`  
		Last Modified: Tue, 19 May 2026 23:30:29 GMT  
		Size: 156.5 MB (156461323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7351cfbd759b0c2db85fc203d04a62cb08df3ce1379d65a5e0c943dece71b3b`  
		Last Modified: Wed, 20 May 2026 00:07:18 GMT  
		Size: 16.4 MB (16414265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b020a89f55d625ad2f8c96ef268da15e9cd7147b5587969975eb8b3cb9e247b`  
		Last Modified: Wed, 20 May 2026 00:07:18 GMT  
		Size: 4.5 MB (4517762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1996c3740622794992524761daa13dc2dfff145a85aad5fb17691958e8c640`  
		Last Modified: Wed, 20 May 2026 00:07:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:56c400984b20fe332af92430be95da5106cd27fcf4b5bd970092f4657c4ade66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478277546b899fb5d8e2a3cd328b7fcb07077fd69f5f38b3102939426a5c654e`

```dockerfile
```

-	Layers:
	-	`sha256:fa363bd7885a3df565a110dd00bb922b82047dd8b7a54aaa520eb383e68c9c83`  
		Last Modified: Wed, 20 May 2026 00:07:18 GMT  
		Size: 2.4 MB (2366919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:859c94cc50d2e2669975e65cc43367d3b3a0f558ebd37412485b3b1d6606f769`  
		Last Modified: Wed, 20 May 2026 00:07:18 GMT  
		Size: 17.7 KB (17707 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:28574b943b06e5cad80d35a88eef103606aaf7dc061b367003a6e4e61c8202d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212944842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc5f5e790679987c8702e305e538594ba2da651900e83fa699f10c13fa7b82c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:37:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:37:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:37:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:37:56 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 09 May 2026 02:37:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 09 May 2026 02:37:56 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:38:28 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 09 May 2026 02:38:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 May 2026 02:38:28 GMT
ENV LEIN_ROOT=1
# Sat, 09 May 2026 02:38:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 09 May 2026 02:38:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:38:32 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:38:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9429fc219825eaf2a233c26bd84cdc3eef77eb70dd8fad888800a28c7609e2e4`  
		Last Modified: Sat, 09 May 2026 02:39:07 GMT  
		Size: 158.3 MB (158343282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a97f5535a33704a2284317f217669ef9547b72e15c55ad265eed80f9b193ff4`  
		Last Modified: Sat, 09 May 2026 02:39:04 GMT  
		Size: 16.5 MB (16485319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c213aa45eb7fb8f47e57016c8e79ed3cdc0cb2b7e4a785996a07f36fccf85a3`  
		Last Modified: Sat, 09 May 2026 02:39:04 GMT  
		Size: 4.5 MB (4517727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c889bcaf8b826620210f8fd07c82995f5a6c6ba6fa75a6025f853c4963892474`  
		Last Modified: Sat, 09 May 2026 02:39:03 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4c510ce170cfb02c8ce59531e3f46d21eb091781ab609208b7f5273fce18d1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fc0282545aaf49725896a0ef7a5fe05a6ea909d305f6c0a87747969c74969f`

```dockerfile
```

-	Layers:
	-	`sha256:fe395f7b15182d58a648dd405f8c4cdbf816a210f2456fe598a44a0fc7cb5fdd`  
		Last Modified: Sat, 09 May 2026 02:39:03 GMT  
		Size: 2.4 MB (2368247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39b594a5fb82830e0abf446e22d70b1baea0f6455cede7c666f11d0a1edfe5e2`  
		Last Modified: Sat, 09 May 2026 02:39:03 GMT  
		Size: 18.6 KB (18585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:faf9aa307f70862787cca90bdfa16d572911a6189de153df66a99760947c2ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198236686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7acd25e7bd452484fd5feddf351c4790d945fc95f3518c0d022cb7713b045f40`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:45:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:45:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:45:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:45:59 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 01:45:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 01:45:59 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:46:12 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 01:46:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 01:46:12 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 01:46:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 01:46:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:46:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:46:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746052218538b3568c2d81225acd5c78df84da2f4d7599c3d3d99fdc4a9571ac`  
		Last Modified: Wed, 20 May 2026 01:46:42 GMT  
		Size: 147.4 MB (147388338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7a761e480661822e42331025606fd5990da3fafb132ff206e9d145464cb7b5`  
		Last Modified: Wed, 20 May 2026 01:46:37 GMT  
		Size: 16.5 MB (16484275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49e6b89670a6fd7784cc34630405bacc92a1a55dc104e4fa72eeda07b4dca25`  
		Last Modified: Wed, 20 May 2026 01:46:36 GMT  
		Size: 4.5 MB (4517721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9df0c40e6cb9cb5a78a26cea64dc494824df2caa25b7e04713f8c706800161b`  
		Last Modified: Wed, 20 May 2026 01:46:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c0bb6b60cd316db1d55a836a1ee41b79aaf51c9c9210213d63881c3ecbc27f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397d7fb366af8f0bcbeb659315875749bc2a1e8084b2f88fa32c3fb4fc39ade7`

```dockerfile
```

-	Layers:
	-	`sha256:350f67a721f1d48c3ede4f45fd1d3325423f971e380ee49a1fd081567a44d009`  
		Last Modified: Wed, 20 May 2026 01:46:36 GMT  
		Size: 2.4 MB (2363736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eca2cbaaa3fb8a2941ffa034d9ac27e11888b3859336e9b3fa169e2c18f2dd1f`  
		Last Modified: Wed, 20 May 2026 01:46:36 GMT  
		Size: 18.5 KB (18541 bytes)  
		MIME: application/vnd.in-toto+json
