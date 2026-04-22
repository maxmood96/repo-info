## `clojure:temurin-17-lein-trixie`

```console
$ docker pull clojure@sha256:8e40b0a2629bdc1e3308ba1b4672543b578eb9b5d5f546922ac9ef627b1fa3d0
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
$ docker pull clojure@sha256:b665fddc60b19044886b96c6f1a7084df02ea0dd4e2e2bfc5fef415dce1e71fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217169131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31acf32329949c90d4da4a3515f408098edd88f463d15870a26f59a18032400c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:21:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:39 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:21:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:21:39 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:55 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:21:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:21:55 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:21:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:21:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:21:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:21:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94920e62edd7a1a6af23879f8268baf50c96844c82bb41f7d5a401175e6683fd`  
		Last Modified: Wed, 22 Apr 2026 02:22:18 GMT  
		Size: 144.4 MB (144436243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccaa471ad7d71214caa2db25a6e19529c3a9f47fe33098c16f0da0a8bedcb9f`  
		Last Modified: Wed, 22 Apr 2026 02:22:15 GMT  
		Size: 18.5 MB (18545480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cbbf34ee1049d4856d863ebf8b1aa4a7345edc5476f42d9ec16c7b4e571c37`  
		Last Modified: Wed, 22 Apr 2026 02:22:15 GMT  
		Size: 4.5 MB (4517734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b06530e3f6ac3afd8138486db1120c10745c96254983c12709d0515a06752d4`  
		Last Modified: Wed, 22 Apr 2026 02:22:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:aa2b60e18d050dd378e82c5f98a8e55e360ba3a108f8f824d272c2f54f5a6c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82830c04cdada29815b43171f255c4037796bc99ee618a073a764b4876f4a6be`

```dockerfile
```

-	Layers:
	-	`sha256:9f4a275e6c8ec038adb39ea7c1feb94baab950e6740ecfec2f735c2930576b13`  
		Last Modified: Wed, 22 Apr 2026 02:22:15 GMT  
		Size: 3.8 MB (3816404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b24a745a0166147395104123adb5127854f5916416d0775a13cd335ec4158131`  
		Last Modified: Wed, 22 Apr 2026 02:22:15 GMT  
		Size: 18.5 KB (18472 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:eb1f1c51550a83030b59e81cf6b7573a8b78203d019b9f2419d8213cd478420e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.5 MB (225466705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e710b7a680c2cf45ee3811ed1b3fa30fe9565e17035e4d790c0038873db0d024`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 02:51:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:51:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:51:45 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 02:51:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 02:51:46 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:52:30 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 02:52:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 02:52:30 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 02:52:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 02:52:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 02:52:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 02:52:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d63fa71f8a08634b0312e1df11dd8fc3363471d8c3e45af52999c7c3ba56e4`  
		Last Modified: Thu, 16 Apr 2026 02:53:12 GMT  
		Size: 145.4 MB (145438287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3b59df9b7048fcc48f0a932a22aec9fb91a983747c47f2d7a37bd61930259d`  
		Last Modified: Thu, 16 Apr 2026 02:53:09 GMT  
		Size: 22.4 MB (22391595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e316d39efc4302855ca5f61ef99aa23eca9f6fbc938038befbc90d8f747c8b`  
		Last Modified: Thu, 16 Apr 2026 02:53:09 GMT  
		Size: 4.5 MB (4517723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ce2ba5a8dec23011014f7eacf3a4ed752a8ce106dd7eed3e5db4ebb2c08b5`  
		Last Modified: Thu, 16 Apr 2026 02:53:08 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:77bf7ae6c67e5383682f1798837df2acf5344e9a0c1abcff45b7804f012652b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63b2dc82195dfa39a4af0dc84b50aa48fef739a997d4e5c5f684bfe73a77937`

```dockerfile
```

-	Layers:
	-	`sha256:13bcbc5500120c6c88738c92d6ba4c45d3ce252dde0bfa8414fbf38031f54868`  
		Last Modified: Thu, 16 Apr 2026 02:53:09 GMT  
		Size: 3.8 MB (3816527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30dbb64d5949ca1300c16811b77dfcad242c81a692cf30958bf41484e90f4171`  
		Last Modified: Thu, 16 Apr 2026 02:53:08 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:effcbc96791a8fddcf1099fc527aa0faa76b2e1ac930b2795f02054dfb043ef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 MB (216669898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2285c38e1dcf5ad76b07ff8c7bbd10d136ea39d77266e387730d88b858517f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 18 Apr 2026 04:06:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 18 Apr 2026 04:06:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 18 Apr 2026 04:06:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Apr 2026 04:06:01 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 18 Apr 2026 04:06:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 18 Apr 2026 04:06:02 GMT
WORKDIR /tmp
# Sat, 18 Apr 2026 04:07:45 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 18 Apr 2026 04:07:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 18 Apr 2026 04:07:45 GMT
ENV LEIN_ROOT=1
# Sat, 18 Apr 2026 04:08:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 18 Apr 2026 04:08:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 18 Apr 2026 04:08:01 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 18 Apr 2026 04:08:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffc354dbc62d2fe426028f99b2388496dd161130055d4d78bf40c555ad79b11`  
		Last Modified: Sat, 18 Apr 2026 04:12:12 GMT  
		Size: 142.7 MB (142662936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0717673ed024b9743dbb4ebacb36e8efdddb6980328dcc32f305f7f429f5c1e5`  
		Last Modified: Sat, 18 Apr 2026 04:11:55 GMT  
		Size: 21.7 MB (21696127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a320f28b6c9fbe49d9803cf5df6f68a11d6fe7b552c2143a0a9cbeba7c183e3c`  
		Last Modified: Sat, 18 Apr 2026 04:11:50 GMT  
		Size: 4.5 MB (4517778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e87e49e92a22d1f69ff56f913e1ef13c8e06759a862622bad7ff1893ade490f`  
		Last Modified: Sat, 18 Apr 2026 04:11:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1b1efb3ade5dd46da5c0bacf0a453c74e68d528ca267f9b8938e43d867f86446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3822481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0892fbdbf396abd491a7a2bcb470b1a82e0a1a21c71443b1d2029bbf3cc00e59`

```dockerfile
```

-	Layers:
	-	`sha256:56c7174a42c05ec55974911137a49270400be28c5f64dce93f6c458494854c3b`  
		Last Modified: Sat, 18 Apr 2026 04:11:49 GMT  
		Size: 3.8 MB (3804085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7084ef9eef883912bc125a8abef2486d019aca664a7f5ed65f52945c9ad36f5a`  
		Last Modified: Sat, 18 Apr 2026 04:11:48 GMT  
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
