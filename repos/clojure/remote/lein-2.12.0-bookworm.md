## `clojure:lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:8b03b68147260d08389fddc3361043cabdac65a72754f2797f01ec149c207c05
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

### `clojure:lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:b275eddb6c284cb2f59aa50cc5d077cbc37810da8f3a0b4ac0918d026209f2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.1 MB (165066031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21119488287eb329522eb175c48e14692fd47d21c0cc254fab11b759669b07bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:56:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:56:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:56:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:56:38 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:56:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:56:38 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:56:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:56:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:56:52 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:56:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:56:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:56:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:56:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd096e7c40988423f6c77bc0fc7f410f4d75089c5730da8b282832fbd83a174`  
		Last Modified: Tue, 24 Feb 2026 19:57:13 GMT  
		Size: 92.3 MB (92256297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d961c0a6012dfb8ae17f60ef0733ed6366f8fe5c56109b191135f8fe9486216`  
		Last Modified: Tue, 24 Feb 2026 19:57:10 GMT  
		Size: 19.8 MB (19802770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff1664a307523ac15ac5928a5652d71bc995958206e8a767038bab8fe03aad9`  
		Last Modified: Tue, 24 Feb 2026 19:57:10 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb3ae9e7552a92324dda312bf9dcceef2d30d3b9691354ccbcba8b0c10a4b9a`  
		Last Modified: Tue, 24 Feb 2026 19:57:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e48a7eec10593bdce5ab054c7b0e766d99404d212496d05fdd043527b4f0ecc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3c4cc1adb575c957d03ed1724f879f49fa51a2728e5f521060717be38483a9`

```dockerfile
```

-	Layers:
	-	`sha256:ade93766ecbea5b0c93cb8b875f9e69b817012f0c3a967ffc24df160e51147e7`  
		Last Modified: Tue, 24 Feb 2026 19:57:10 GMT  
		Size: 4.3 MB (4251027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f477d7ee8df7a07597a15330a91acf3ede31f0da120f00cedfe3367e1fa4cf34`  
		Last Modified: Tue, 24 Feb 2026 19:57:09 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3f7f50433d4147cca008135cce18247df1d0cc5214e637afa026eb1ae5b82b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163812413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b020a3bee7fb3b9ca5c08c12271c4297e5a866dd2bff5efe1ee2c0b35124c6c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:07:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:07:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:07:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:07:38 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:07:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:07:38 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:07:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:07:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:07:52 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:07:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:07:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:07:53 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:07:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6d0193859402b46e871b8e097f8c9cd87d98e701d50734e47de49502b6e828`  
		Last Modified: Tue, 24 Feb 2026 20:08:13 GMT  
		Size: 91.3 MB (91288263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdfde4dca3a76d994209419dc46133390d2e4013e7c3439b055f1ac404e4fa9`  
		Last Modified: Tue, 24 Feb 2026 20:08:12 GMT  
		Size: 19.6 MB (19632810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e31d1e6887ae3c3c956043071c4e30376623a286f809514edd3680af108c4a`  
		Last Modified: Tue, 24 Feb 2026 20:08:12 GMT  
		Size: 4.5 MB (4517700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f51ed4d119626e1f15705ce1cb546bd5f27b38284e235842b2f1e5e164dd82`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b5c14d2e92bb18b5c13f5cca35eb4d950ecf9dce2e8fdb1c47be2f4f5b9c8e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d94c7452c8c148995fff8df4e0c2999125f6c8bddc3be272b5a4c48e3158c3d`

```dockerfile
```

-	Layers:
	-	`sha256:ea436c797d7eff11353e5f89e96f5f2359a00e132d5288d6eef738c254fd0c1a`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 4.3 MB (4250711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7859ff7584d97d44c02c89ba56a1b897628db02b059030bac59f9a2b663c140`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 20.5 KB (20452 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bookworm` - linux; ppc64le

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

### `clojure:lein-2.12.0-bookworm` - unknown; unknown

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

### `clojure:lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:c2f1b98c97c6996b4ce0e95d88d2cb4c074f36f0945b6c7943e213b03633758e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.4 MB (159363453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8935f7458cc27bc59af405f76ffc099db752566615dec62b1d73e16b30bfde`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:22:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:22:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:22:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:22:55 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:22:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:22:55 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:23:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:23:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:23:28 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:23:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:23:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:23:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:23:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a2c7f155ba43475a58ce53d7548c5de702bcc0cc952b4fe414a2ed67d07e94`  
		Last Modified: Tue, 24 Feb 2026 23:24:09 GMT  
		Size: 88.2 MB (88233846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0accba8e8bb193d30badc398ede5cd3a52d379e0697e202d2a353ae242b9fc5`  
		Last Modified: Tue, 24 Feb 2026 23:24:10 GMT  
		Size: 19.5 MB (19463370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bfc72ce3173d03aaba2a8ff34788bc2a481eb2fc9fb81a6e8fbbc0ced65958`  
		Last Modified: Tue, 24 Feb 2026 23:24:10 GMT  
		Size: 4.5 MB (4517721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96ef88544195ce61329fbc1b7f5f4512519ff70e67c75ad3b671679bc3bc383`  
		Last Modified: Tue, 24 Feb 2026 23:24:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dfee7ba01559eac1ec479380ddd3b6d13eb213e1adb34def4bac418512cfb3d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3aef64086b536c0bacc03056ded2cc59543df7fa5e894d92f591db2d59644f1`

```dockerfile
```

-	Layers:
	-	`sha256:c4bb2d92a1f74b357e0032c73271a4d69b6c40cc6da079937af07b6091cd314a`  
		Last Modified: Tue, 24 Feb 2026 23:24:10 GMT  
		Size: 4.2 MB (4227403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f31493ec117d4d59e1cb0a328d7df17e9ea69380a73d485e77dc76fb932266d`  
		Last Modified: Tue, 24 Feb 2026 23:24:09 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json
