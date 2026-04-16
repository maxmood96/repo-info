## `clojure:temurin-17-lein-trixie`

```console
$ docker pull clojure@sha256:c75aa3de3f08fa7d87fc8c7ddae185cdb3a22710390e6b5c24dcbaba318da5cd
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

### `clojure:temurin-17-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:448a661fc75a9058153ec40d71b07c76b6f20aa0112fd8dd3082d613a89528d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 MB (221533899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f4195b58d5b3c0ff7e062305883bc04d6291dc16a148d6289378c221016c89`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:03:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:03:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:03:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:03:59 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:03:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:03:59 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:04:17 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:04:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:04:17 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:04:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:04:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:04:18 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:04:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743be0e1a74c449b8e6dd7c5721bd5585aaee7bc4aa161f78729828ce86c2217`  
		Last Modified: Wed, 15 Apr 2026 22:04:39 GMT  
		Size: 145.6 MB (145628750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af2d833bfcc8028b4f9de152d22c02efb1e03c51cc5687ee700d95668775700`  
		Last Modified: Wed, 15 Apr 2026 22:04:36 GMT  
		Size: 22.1 MB (22089174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3b0d7d3ccc29d79e9d617eb2273053e4ce4b5358a4fb6862c186d44bf68ad8`  
		Last Modified: Wed, 15 Apr 2026 22:04:35 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66075fdde16b053878dc006d741b160dac07df80831243f582bcf981e6c26787`  
		Last Modified: Wed, 15 Apr 2026 22:04:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:538bb0d155f0292bf4502a743dc491f460a27de3ffb9b6b87f81195711bf35ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c8706f63eb5ae99866513b16c22e867a5904123d2a98d411441c103aaafd54`

```dockerfile
```

-	Layers:
	-	`sha256:ad8ed701bc9754e587f7ccc2ae657f69077d1a81add2017e601caf2a6ffc1124`  
		Last Modified: Wed, 15 Apr 2026 22:04:35 GMT  
		Size: 3.8 MB (3815527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d524d0c35c94c4a22107b6a97f89536a6de61bd51a83c959f63f8afaa03bbe`  
		Last Modified: Wed, 15 Apr 2026 22:04:35 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e8e6d134babc55eb1db645b93caf87cefd150f1e90879e5db12e6289e5866c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (221043775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730bcf06b732791a4b68684d187906b0fbcc4563dcb4af119280ca9d3562d71d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:15:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:15:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:15:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:15:13 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:15:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:15:13 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:15:29 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:15:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:15:29 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:15:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:15:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:15:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:15:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f171767ce352c62b092ce054a03e16569b4858065b614a06971c3cdc2f5f62`  
		Last Modified: Wed, 15 Apr 2026 22:15:53 GMT  
		Size: 144.4 MB (144436187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b990dc2adfee01a4f0f5c9c03dc5a26dc044f000f3145ebd8ea5f9a4e62c0b78`  
		Last Modified: Wed, 15 Apr 2026 22:15:50 GMT  
		Size: 22.4 MB (22424173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28dd73be1f32f6a6e1df78d540447d2a2a9f99d6c3965ca2e656cd9def620fc5`  
		Last Modified: Wed, 15 Apr 2026 22:15:49 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f179ea83bd6b05c4a5fd3e167f1591fd5f0c256e8efadff2f86caa4eee7a10`  
		Last Modified: Wed, 15 Apr 2026 22:15:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7ac997429e9d2fc4a6a8690877d6a7ec7711a873e971da09dd02558c6eea1e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e88bcf215899d787d157295547f900f38d993af2d2573380e1e439e3123b3020`

```dockerfile
```

-	Layers:
	-	`sha256:c2128e49fc2a36040aa6972d59df520c1da0a4c79a99783bfd982504ea95fbb9`  
		Last Modified: Wed, 15 Apr 2026 22:15:49 GMT  
		Size: 3.8 MB (3816404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a6fbcfd4e8cbd0131dc2d5dd334bbd9c8eeacfe56ea8e8147e7a42243db6d74`  
		Last Modified: Wed, 15 Apr 2026 22:15:48 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:ccc14ff74d9afccaf83e6f14a8e6876ca3d41ea2382ba202c6826c7ee6031ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221715945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7648da312cca19d6ac79a48cf42b0794d62b7ace2b495ede5a88d5608c32c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:39:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:39:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:39:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:39:23 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:39:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:39:23 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:40:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:40:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:40:11 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:40:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:40:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:40:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:40:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a76b0a411921a776a6aa7e333480c75bdb58776d62cc75ddfeb7b455ebd920`  
		Last Modified: Tue, 07 Apr 2026 14:40:55 GMT  
		Size: 145.4 MB (145438242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920804915361aee82670d42c8d060c0c5e282ec5246e5ac26b7d69cb061e0f88`  
		Last Modified: Tue, 07 Apr 2026 14:40:52 GMT  
		Size: 18.6 MB (18640870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6480fd14f320443333ad31ced3605efb4e439d50d7a90e1d8c8d297d8090a5`  
		Last Modified: Tue, 07 Apr 2026 14:40:51 GMT  
		Size: 4.5 MB (4517734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd5fd8399bbb192420cebc48a68f4b37a227a90a1eaf53d9a983d612972b714`  
		Last Modified: Tue, 07 Apr 2026 14:40:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:29fdb6898ef4419eaf3e1f4e3a766c3aa76a0fd41f791fd21dd840a37730250d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c84d8246e2e3a0c7cada59e501137d41466be383cea69b03ecc62f2898bb49`

```dockerfile
```

-	Layers:
	-	`sha256:567cbdeef664cafba694f655c6614ca7a3a234d55f897f37078690cb748ab9a0`  
		Last Modified: Tue, 07 Apr 2026 14:40:51 GMT  
		Size: 3.8 MB (3816527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42e3cf6a571b47100ebe5b20402c905fbd89d87a212c0786538160062e934b7d`  
		Last Modified: Tue, 07 Apr 2026 14:40:51 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:1168dca0dc93092f1a5f260f3d26afcd9a1f5964cc3fa17d0a8bc69157f2c957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 MB (216670027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356758198ac1bce83cd0993797093bf9e674a9b6c424704040d3a5cd00b0464b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 21:15:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 21:15:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 21:15:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 21:15:29 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 11 Apr 2026 21:15:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 11 Apr 2026 21:15:29 GMT
WORKDIR /tmp
# Sat, 11 Apr 2026 21:17:07 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 11 Apr 2026 21:17:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 11 Apr 2026 21:17:07 GMT
ENV LEIN_ROOT=1
# Sat, 11 Apr 2026 21:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 11 Apr 2026 21:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 11 Apr 2026 21:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 11 Apr 2026 21:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de3586f52f160113005887920f505e18e0518029e2ec38342484f9914d399e5`  
		Last Modified: Sat, 11 Apr 2026 21:21:35 GMT  
		Size: 142.7 MB (142663032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f4f25a671f6d0c898606701e09e19bd3e372590170e2cc7bf90fa44ced5686`  
		Last Modified: Sat, 11 Apr 2026 21:21:18 GMT  
		Size: 21.7 MB (21696144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b48b8b2e1e86c905a0a8c5c9a0e1ff2c1f41320bd58449267c0e636cdf9f51`  
		Last Modified: Sat, 11 Apr 2026 21:21:13 GMT  
		Size: 4.5 MB (4517795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb36a837ab5edd5fc81e96b50dd3b097bc05c1fe66b2d55d6604ee495f454d9`  
		Last Modified: Sat, 11 Apr 2026 21:21:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8aa15b13e5825dae98e6464c4ae137e0f437399f820b56e40ea50b7156250938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3822481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88559f76048bdb468afc8108a74a5eb828f9bd732fda4c6e1bad272d9f9b8d83`

```dockerfile
```

-	Layers:
	-	`sha256:a3ba12392c12949bd18fd51ff060b91e4f074ba3349c36c3a3fbf382b2906cf9`  
		Last Modified: Sat, 11 Apr 2026 21:21:12 GMT  
		Size: 3.8 MB (3804085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da7f1640762f353bef90ec21eac84b8ca7574020c797098eb426d4a45c2a61ba`  
		Last Modified: Sat, 11 Apr 2026 21:21:10 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:665e28c0dea7b005ddb26b964ad63dc350d5724231eeff133ee9f0f098dbda75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.3 MB (211292490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4b4d6930dd9627b15f420e5d0343923029ce01519070d2eace8f25d219b615`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:38:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:38:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:38:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:38:54 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 00:38:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 00:38:54 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:39:07 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:39:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:39:07 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:39:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:39:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:39:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:39:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1b243ec701908744684ff8f876b0df943a470da89fd2f043fd1136488a15d0`  
		Last Modified: Thu, 16 Apr 2026 00:39:35 GMT  
		Size: 135.6 MB (135627010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9450204438715301b31a7d01b8370fe6b3c567c356f6682299094af88becc1`  
		Last Modified: Thu, 16 Apr 2026 00:39:32 GMT  
		Size: 21.8 MB (21782242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b4fcb2b2e7ac8b69d6d39ca285805e963f9bc54ca82b3c7c37d5e12c901451`  
		Last Modified: Thu, 16 Apr 2026 00:39:32 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab105f4f406d0223abb588c31552e097dd71765c2c768042616c3a8ce0b7476c`  
		Last Modified: Thu, 16 Apr 2026 00:39:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ce530987e01a01aafed1daeb411f9af8990cd914235237e09e039659837ed29b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3830306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b550fd099ba1f028edb3526c57657c88ea973a0f3752d676e3176cb3f5f758d3`

```dockerfile
```

-	Layers:
	-	`sha256:efe778013fc3f6311540e563065f5a93fbd59a929cb9d6b7774319ce62cef2f0`  
		Last Modified: Thu, 16 Apr 2026 00:39:32 GMT  
		Size: 3.8 MB (3811954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f3c025aca94f78ab4c649ee491e1454c0f14dee5db9bb263f9a54706c425036`  
		Last Modified: Thu, 16 Apr 2026 00:39:32 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
