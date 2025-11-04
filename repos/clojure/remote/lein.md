## `clojure:lein`

```console
$ docker pull clojure@sha256:36c5a7669a75ed1db608928460bceed72315620e927969798592051c49a4d127
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

### `clojure:lein` - linux; amd64

```console
$ docker pull clojure@sha256:bb5060067c18829b913e1f19d7355a3a7bfe19022e8511714573838ba2318366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164838170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e1bfd52b841e4c78af8214305048dbad95a7a61681c389e5a98c5294e2afde`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:56:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:56:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:56:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:56:17 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:56:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:56:17 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:56:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:56:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:56:31 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:56:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:56:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:56:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:56:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876e96a3748f1a12d7ac77cd8fc3e28c05ef9f9e76a977f758f49008f526ebef`  
		Last Modified: Tue, 04 Nov 2025 00:57:10 GMT  
		Size: 92.0 MB (92036048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9455f4e65f2496b898151c8b795801ac8bb6874b405476a9c1e66cee8297ee`  
		Last Modified: Tue, 04 Nov 2025 00:57:04 GMT  
		Size: 19.8 MB (19802896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b464f53c490d51aec0e58271e8456aaa3e4418c9415c72539d5e7a82ae63ee`  
		Last Modified: Tue, 04 Nov 2025 00:56:58 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304ebe47ad95bebdecbcb47abe6c5ede58b873901c11b4bf6b4b635786376504`  
		Last Modified: Tue, 04 Nov 2025 00:56:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein` - unknown; unknown

```console
$ docker pull clojure@sha256:3bc2b3a698f65b37d80b36ba0aca0d805bafc96c2efe4514ce9b683156b6d9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10f00fc6c0f54e92434c75a1b181dbca558573338802994b0b6454110684ef0`

```dockerfile
```

-	Layers:
	-	`sha256:53ba6ec22da440d4cbcc1964ca1bae4c223febb90c4c283b007c7f84ac832fdf`  
		Last Modified: Tue, 04 Nov 2025 10:34:43 GMT  
		Size: 4.2 MB (4232382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da14e2eb0c1858460ebfc9c82b4f7b1dd278f87bc5e9504eb50313bdae51aef1`  
		Last Modified: Tue, 04 Nov 2025 10:34:44 GMT  
		Size: 20.3 KB (20258 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:40de6eb292412f57946263e77e1e8aab3b559e37c480afff3b5faa16b6741d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163555085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc96d6c8fe326dae44dee69748a42b87def853c8cf80b7a51e5f3a15cf128eb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:56:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:56:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:56:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:56:59 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:56:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:56:59 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:57:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:57:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:57:13 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:57:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:57:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:57:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:57:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ed717727c64f810de0c25d6cba39789f9a16cae1690aff5e33148ea9eeef1b`  
		Last Modified: Tue, 04 Nov 2025 00:57:51 GMT  
		Size: 91.0 MB (91045237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731fe02463948f604ae9344802df4a3354dbd13d1c306847919ee41991d8f202`  
		Last Modified: Tue, 04 Nov 2025 00:57:45 GMT  
		Size: 19.6 MB (19632218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b5802139f1906159b2428b15f81e7f9bc7d4b8112cac420889c24b465f5fd8`  
		Last Modified: Tue, 04 Nov 2025 00:57:44 GMT  
		Size: 4.5 MB (4517725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919ba0bbdce2e988cc3cd186b14bd946908ee5053a2c236aae5aba67ebb34cc2`  
		Last Modified: Tue, 04 Nov 2025 00:57:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein` - unknown; unknown

```console
$ docker pull clojure@sha256:29c094f206249b1ad43d439bc17e62ad9dc774c5926ea4b3fb564cfb9a86b0c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e95224ad484200b5ebd8ce58b902a5e740a56fb9d95bc4638a3dff849970376`

```dockerfile
```

-	Layers:
	-	`sha256:0efb9c30b66e8042e88970cc74cad4588f8d307cc5604732aff0bf9844d53c3a`  
		Last Modified: Tue, 04 Nov 2025 10:34:49 GMT  
		Size: 4.2 MB (4232066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:385b02052256a13f1c9124e532e2e6e3c27d0df9d0e064998f5ed225571a646a`  
		Last Modified: Tue, 04 Nov 2025 10:34:49 GMT  
		Size: 20.4 KB (20450 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein` - linux; ppc64le

```console
$ docker pull clojure@sha256:5bc05d55b8421e21f0ade4219927030fd8ecbae778df0ec6a89d476b28c4e444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168468824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72e099838d4cb76dc634265a041518cab7f610e8672579a6de195a1759107fe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:57:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:57:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:57:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:57:05 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:57:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:57:06 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:57:38 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:57:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:57:38 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:57:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:57:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:57:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:57:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697fd59e7c3bbc197eda379a24912ae560eb9e07af558ef7f46c037d6dbf5da3`  
		Last Modified: Tue, 04 Nov 2025 00:58:43 GMT  
		Size: 91.6 MB (91601697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb44fbb0a692ca1c605ebf796a038a602f14dc4157e7bfce32f74812b4b98e90`  
		Last Modified: Tue, 04 Nov 2025 00:58:35 GMT  
		Size: 20.0 MB (20021708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48373f5d15d57d462c1a3df1d72fef37b255e79a80e3bcf4ee0328ff5b62f5cd`  
		Last Modified: Tue, 04 Nov 2025 00:58:33 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06303b42a5b01a70706f305e91b121dd561a8307c86ce4c3b18963dd904153d9`  
		Last Modified: Tue, 04 Nov 2025 00:58:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein` - unknown; unknown

```console
$ docker pull clojure@sha256:88b8f48ff8eaae022ad058df29019bbb27be59597ce03cbbaa9d69c17d28a05b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4255914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d607ee8fe7df6c3d6a32f7ae877f203dc7cb5a93c31f5a302f5e4aac7f8d9c`

```dockerfile
```

-	Layers:
	-	`sha256:6a62c2fb15927a53993c26b5fa8736f7128082f3f22cf75eed2b84da4b2a6d08`  
		Last Modified: Tue, 04 Nov 2025 10:34:53 GMT  
		Size: 4.2 MB (4235575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63c69cb39034230863328b5898558e7e575c7e71dcac08b27c098ddcea7858eb`  
		Last Modified: Tue, 04 Nov 2025 10:34:54 GMT  
		Size: 20.3 KB (20339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein` - linux; s390x

```console
$ docker pull clojure@sha256:a96186d113fd0d75d35913b30f0294a817c23a73854b9cff8733d66e3fe351fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159323355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a79ec1281c65a4dedfdd43eebe9a176b705aa395281affa13d7fd4123fd0091`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 06:16:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 06:16:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 06:16:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 06:16:46 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 06:16:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 06:16:46 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 06:16:58 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 06:16:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 06:16:58 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 06:17:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 06:33:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 06:33:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 06:33:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44c022f304dd76bdc7608befad5bc0f9a88754ecb1970943a535e7f9c6a8b41`  
		Last Modified: Tue, 04 Nov 2025 06:18:05 GMT  
		Size: 88.2 MB (88206432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4797b699d0becca5ee1201eb2c1a06b6472748208b2348a5cc34af731bf2ae5`  
		Last Modified: Tue, 04 Nov 2025 06:17:59 GMT  
		Size: 19.5 MB (19460647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b04185c3db4a984d05b99a92d23a73c5e1e780e57aaacebc16c52fdc474f41`  
		Last Modified: Tue, 04 Nov 2025 06:17:58 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af6a093f732668961ab4e15d4c946d5b3c0a225e96b3d85c0e742cc05d207ab`  
		Last Modified: Tue, 04 Nov 2025 06:34:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein` - unknown; unknown

```console
$ docker pull clojure@sha256:168bd016ff685d484ca0837b032f88333d8b5bc1bbaed73c0bfcdd3ef2f3f26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4031ffa269e8dec54b7f78f4a8be6b3f8a98f8fd1f42386b746972099c7d1c2e`

```dockerfile
```

-	Layers:
	-	`sha256:4a8910c75ece27b32d22bb1db926aab517e9294b8cd063008d40f4f9feebfafe`  
		Last Modified: Tue, 04 Nov 2025 10:34:58 GMT  
		Size: 4.2 MB (4226744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8780368ae7dd81153e4c73ca3a98d8d4ed49970d6b2de5b866804a405c7eeecb`  
		Last Modified: Tue, 04 Nov 2025 10:34:59 GMT  
		Size: 19.5 KB (19459 bytes)  
		MIME: application/vnd.in-toto+json
