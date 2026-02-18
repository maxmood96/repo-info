## `clojure:lein-2.12.0`

```console
$ docker pull clojure@sha256:5d6946439072fe625e4ba5c7cfa1bde2c993c9c57a87934f6e33882d276b7ed9
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

### `clojure:lein-2.12.0` - linux; amd64

```console
$ docker pull clojure@sha256:e5f6a3d0c8eb2e3ca84c4980a5c0f535fa3389ff43dc618d40ea02a34545d180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.1 MB (165058824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b0f06db16daf5da8061088488d3469ffb1f77187d8ad3d608a91bfbc8316f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:45:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:45:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:45:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:45:15 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:45:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:45:15 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:45:32 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:45:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:45:32 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:45:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:45:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:45:34 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:45:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c67df34c58fc8c85a03c39f0422982696128a0d91114d700cf496ea7a3076c2`  
		Last Modified: Tue, 17 Feb 2026 21:45:55 GMT  
		Size: 92.3 MB (92256233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf92181428c06eaa98da40f0d6ec09aeb37d7bcf5136c0fbb9df483b46ee79f`  
		Last Modified: Tue, 17 Feb 2026 21:45:53 GMT  
		Size: 19.8 MB (19802924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39678ad64f5a6b4837d85d5d9655f45d717947474f9b2d3b80783a9db5c783c`  
		Last Modified: Tue, 17 Feb 2026 21:45:52 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637a07131b6955689eadd602b75793ccedee52e38281f77250e9614592bef8b1`  
		Last Modified: Tue, 17 Feb 2026 21:45:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:37aa30d9a13a610181ebd409b58afbe5e82c64d229fe3d36619726eaf26adc88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15aa47f301412ebbf4e984dfb0730d74632fd57852eade18bb3ffb096a77518`

```dockerfile
```

-	Layers:
	-	`sha256:2202f3dc4cbe40dfc7bfbc9087aeb187a17f496eba9948e2af9abdc1a4239d97`  
		Last Modified: Tue, 17 Feb 2026 21:45:52 GMT  
		Size: 4.3 MB (4251027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c1cc3e3fde2771b4296039ef79a9eab6810ae8c49e6ed4fbc40eaa642dc5d16`  
		Last Modified: Tue, 17 Feb 2026 21:45:52 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c73bbb0e000d866463517a8b2f2cc3224f05c312cc2418ccfd01cb5e9a728af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163805178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef797216c904f48c6ad483abef849b2eb3942c5d18562008eb9572db0fc41a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:45:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:45:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:45:16 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:45:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:45:16 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:45:32 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:45:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:45:32 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:45:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:45:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:45:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:45:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09be10188c2520da4a2d08cabe6725482d489d9bc774c3bdd94e1eb38b13834a`  
		Last Modified: Tue, 17 Feb 2026 21:45:54 GMT  
		Size: 91.3 MB (91288274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353ac9f33a69b9a24b51bd0a43f1b2dd6ecb1568b4894136e7c23fdd40ead338`  
		Last Modified: Tue, 17 Feb 2026 21:45:52 GMT  
		Size: 19.6 MB (19632817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6873871b02e4db6a6653f8b85f14f705251b31402ad68097a34bf8e497a979e5`  
		Last Modified: Tue, 17 Feb 2026 21:45:49 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c004dfca7003c10c3c21f140748b38c8890a9dd4b2d3b48f00cba11aa7869d0e`  
		Last Modified: Tue, 17 Feb 2026 21:45:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:0b93f2c5c6825bc7ace3d11c738581252f4aeb9549eb6b70f03a6cd5fcdb6ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98490b8c7507b8b5ead6c9ec9a3d8d4ba5e825879db95e09835ebeb3b8bbaa51`

```dockerfile
```

-	Layers:
	-	`sha256:064b0740c764838e0165e0f2e282af5d32398b292d107e6b3a46b0d658e5df9f`  
		Last Modified: Tue, 17 Feb 2026 21:45:52 GMT  
		Size: 4.3 MB (4250711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e510f67e2fc7d51ea922eb28a0a28d5dc5f95f7fcada3c01723d0680ebcca20`  
		Last Modified: Tue, 17 Feb 2026 21:45:51 GMT  
		Size: 20.5 KB (20452 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0` - linux; ppc64le

```console
$ docker pull clojure@sha256:00234dfbe5b4a1ac445699eb2987ed6ee01e9c6a390da000ac9c9d77e6085600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168502266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36168889ba8ab7964dcd8090fbb6332bda33bf68d81f7128c023bd4e46c1db28`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:54:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:54:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:54:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:54:17 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:54:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:54:18 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:55:16 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:55:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:55:16 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:55:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Feb 2026 00:46:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:46:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:46:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413bd0b8c6c326da16c676c4dc2f9ba6260e745418e4f97b3a2d3fb7fa2bf0a6`  
		Last Modified: Thu, 05 Feb 2026 23:57:00 GMT  
		Size: 91.6 MB (91632873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ee63883eb7370fe869840f959c32e522f55502f68e9aa093f5bd69c7b5fe53`  
		Last Modified: Thu, 05 Feb 2026 23:56:57 GMT  
		Size: 20.0 MB (20023902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d63a17432a85a5c1fa33b95c3df6d9fce8bda1634781eb8e0632debe5c1748`  
		Last Modified: Thu, 05 Feb 2026 23:56:56 GMT  
		Size: 4.5 MB (4517772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfd65280dc7b6ec09bbd5e27ee3984fc50a5a07ff964d02b008a2828f931b81`  
		Last Modified: Fri, 06 Feb 2026 00:46:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:f1f61ab4609c3ecb66a9e64f2ee73f0471a538f8921ee2857a8c576086cfb9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4256575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b369a77a04952d44f244c6a8558fa84e0145ecd4a5aa02de2289f0e8424455`

```dockerfile
```

-	Layers:
	-	`sha256:31bdd0d2ff012e0ad46b89d2fb6599c887014e755f6f60ede174ab7c724ce7de`  
		Last Modified: Wed, 18 Feb 2026 00:03:45 GMT  
		Size: 4.2 MB (4236236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aee858c09a426bb96505982f433510dcb8f7f678312325c819813cfe51b2c5c8`  
		Last Modified: Wed, 18 Feb 2026 00:03:45 GMT  
		Size: 20.3 KB (20339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0` - linux; s390x

```console
$ docker pull clojure@sha256:92df23b7033437ceec727558ff701fca9b64ddc3921cb17e02e5a3a397eec3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.4 MB (159353678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e08c9812023f215305a4c5f0ec322afb9eb6ab5cc72319993e1d19a9fc826eaf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 22:16:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:16:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:16:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:16:01 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 22:16:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 22:16:02 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:16:37 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 22:16:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 22:16:37 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 22:16:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 22:16:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:16:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:16:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba6fd0c0d82ea9631bef0d5f1a77cdb1ed5e84260880b88825e90f3037036e`  
		Last Modified: Tue, 17 Feb 2026 22:17:20 GMT  
		Size: 88.2 MB (88233833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87210cc66269eaa4e215877c1dfafc6316bebdfedb937813a1aad636993df84`  
		Last Modified: Tue, 17 Feb 2026 22:17:18 GMT  
		Size: 19.5 MB (19463313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa484103b8febec0fcde51e5f2e153c9d7712d2f83929061e902886ecad0daa`  
		Last Modified: Tue, 17 Feb 2026 22:17:18 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f21e1bf765908a1f9e0b5e01769669ad43efefbddbcaae319e9b2c3991a5a2`  
		Last Modified: Tue, 17 Feb 2026 22:17:18 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:e01620bfb4d551cfb0379db8b7e15b5e622904d00fc1b9d899632674d7462034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10bfc63ca51d22d5194cd0fb308cc6b3add8c881e81fd21d2dd6ed87037863d`

```dockerfile
```

-	Layers:
	-	`sha256:c97c357a16e2817c3144ddf163e8b2b505c3e0c6c4774b3847038eb6db9a630e`  
		Last Modified: Tue, 17 Feb 2026 22:17:18 GMT  
		Size: 4.2 MB (4227403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfe1e98c14588bcebad0e00311faab4fb98180c2b32634c9a050900c6f884010`  
		Last Modified: Tue, 17 Feb 2026 22:17:18 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json
