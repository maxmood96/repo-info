## `clojure:temurin-17-lein-bookworm`

```console
$ docker pull clojure@sha256:b436291ee673b48b48b8b02029956234716fe1bb21bd78d4ef6c5ff1dccc7a4c
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

### `clojure:temurin-17-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d6a1082291818d74751d6a37447697372a5bc35225a72d1855d680955e95b660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217650162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5f6f4d3023a2f247d1f0544475a975c487d05ab2d416eef685a01fcc861960`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:51:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:51:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:51:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:51:26 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:51:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:51:26 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:51:40 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:51:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:51:40 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:51:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:51:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:51:41 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:51:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ceaa3751367195079a65bbf3cd4d33ead68742b6947e08d345249d0e789855`  
		Last Modified: Fri, 16 Jan 2026 01:52:28 GMT  
		Size: 144.8 MB (144847972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b67dcc7c4d1bb661e61efe46b8a0134b4ae266cde26d3f9cf8cd25040a2ae1d`  
		Last Modified: Fri, 16 Jan 2026 01:51:58 GMT  
		Size: 19.8 MB (19802398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac508cc8e20cd00efd71f95f59effdd69c93ef24954ef2f411a1a2a8a0973f4a`  
		Last Modified: Fri, 16 Jan 2026 01:52:07 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e81c1089d1637473f12c96a3609296824ea5d3825b637937546e779caac8061`  
		Last Modified: Fri, 16 Jan 2026 01:51:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b5530b1c81e9f2d0a4396d059c8b93d4cf370bd63fe71683214b211a8a4aa152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4298847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e026f15299416d08ac49fa71d6ed3197b9f83e579fe6ab687f61e496e6861118`

```dockerfile
```

-	Layers:
	-	`sha256:3b0201045bbe549cc7d9d2f331535b1dc65cbbe5f704d9ac8a9b048348892a24`  
		Last Modified: Fri, 16 Jan 2026 04:41:53 GMT  
		Size: 4.3 MB (4280479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d06ded492170b68ba3b6b88daf54a4419f6046f81cf37d25328d1820418a94ff`  
		Last Modified: Fri, 16 Jan 2026 04:41:54 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1ab48b63827170073adc9f54e74fea7ee55f1e5bd2073976403301ddf567ec66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216196835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9a191c82e8d7835f3f9d9d76281990bee7bcefb2a0e150bbb1cf9d46ea5f15`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:55:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:55:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:55:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:55:41 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:55:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:55:41 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:55:55 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:55:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:55:55 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:55:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:55:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:55:57 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:55:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b21821b57dc968c35d47f20ebbda3dd474d77308a0fe3dd6ad430c0ba26424`  
		Last Modified: Sat, 17 Jan 2026 14:38:26 GMT  
		Size: 143.7 MB (143679931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6937f5e83bc136856b09ef21af5cb41a8f91f3c021d867151f29553483582fc8`  
		Last Modified: Fri, 16 Jan 2026 01:56:24 GMT  
		Size: 19.6 MB (19632693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a303c22983b61652a0ef531a74aaeae9580d6ec4b595284c918a5f20564ec31`  
		Last Modified: Fri, 16 Jan 2026 01:56:22 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf23896bd8e8db4d843454ab90852a06a5dc99ea9bfd21a334bd52e10f533e58`  
		Last Modified: Fri, 16 Jan 2026 01:56:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6d57f6d783243a136b8828649959bdd60ac02c5b048a9438f6e5d7265238dd7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4298583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb1d6a1f997079f823f6f02b6a723729bf17aede56bfede5e3da6ec4bb305f4`

```dockerfile
```

-	Layers:
	-	`sha256:5330212ca3a0163e8bb104efe72f302ec887d9c9595665a85b334e8f3c67f590`  
		Last Modified: Fri, 16 Jan 2026 04:42:00 GMT  
		Size: 4.3 MB (4280094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4164430732c721f0c755ccc7aed0b64120bad81bb05bec890671903dd850f68d`  
		Last Modified: Fri, 16 Jan 2026 04:42:02 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:28a0321b2b0f78bcaa6c220dc4a91202664c01ab480c721e3ce24b13cd1e40cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221392952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63211b9d44274ce8cec8b60091f75fe0c9c70ba250cda7bfde773db9f3d6ecf7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 03:12:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:12:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:12:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:12:06 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 03:12:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 03:12:07 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:12:57 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 03:12:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 03:12:57 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 03:13:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:13:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:13:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:13:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7649ae7dd81da82230511111108bc60a688b861fec794a0460e34e68ea9084`  
		Last Modified: Fri, 16 Jan 2026 03:14:01 GMT  
		Size: 144.5 MB (144524732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9b309f240303efe66a07933f60e68ca4a844581658a6c863dfdd10eecb524e`  
		Last Modified: Fri, 16 Jan 2026 03:13:55 GMT  
		Size: 20.0 MB (20022675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a6bfd417154896a13c2a24f96e4e656f4bd79cd02963f95f7e1354b619bc0a`  
		Last Modified: Fri, 16 Jan 2026 03:13:54 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddc62daa537aa5c9caa88d887218270fae13e0e1017a9bc112670c7ca741593`  
		Last Modified: Fri, 16 Jan 2026 03:13:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:91d2873b2ffd4ec8e9806b1efafe4754f77145276d16bf282935de77831f181a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e223b96ed033cb02db9c4e260e50ab69cfb5c74b8cfc012a3835c510d8dceb`

```dockerfile
```

-	Layers:
	-	`sha256:5fe76c7fb9c69afd4b01b550689605d13552e53f84a3d4598ae032725ec2494f`  
		Last Modified: Fri, 16 Jan 2026 04:42:07 GMT  
		Size: 4.3 MB (4282340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf1cd52364c8de92da61c0bc533c9095e6cb94736bf8f4871cf35f38db9866e0`  
		Last Modified: Fri, 16 Jan 2026 04:42:08 GMT  
		Size: 18.4 KB (18412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:86bd93f74dadfe3f40ad9c51cee78be90905c1297c9b258df3968f1154b75cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205978383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f6f9a1f09fff1831a130762805b002c74eb0324320b609e303f7cb65ffa1bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:13:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:13:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:13:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:13:37 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:13:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:13:37 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:13:48 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 15 Jan 2026 23:13:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Jan 2026 23:13:48 GMT
ENV LEIN_ROOT=1
# Thu, 15 Jan 2026 23:13:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 15 Jan 2026 23:13:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:13:50 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:13:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:05 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac3b1f7ccd0fe409a1e257a52e40422d728bbba127f4f188372cdba4f17bb4c`  
		Last Modified: Thu, 15 Jan 2026 23:14:16 GMT  
		Size: 134.9 MB (134859770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc35d0af941d7b083cfe14ff42b35aeb6d2e10fbde791970027b1f01969f6e1e`  
		Last Modified: Thu, 15 Jan 2026 23:14:14 GMT  
		Size: 19.5 MB (19462001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc5faaef022861e219fbca82eec59e757afdcd723b61cf4017631939787a6fc`  
		Last Modified: Thu, 15 Jan 2026 23:14:13 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b187a25335f7f475307647800add73c384a919e6b13e821f93665e16090b8f7`  
		Last Modified: Thu, 15 Jan 2026 23:14:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:001667d08a50f2686f5ebe1c7cbb9a69908dc7af698c0aac787181872c4b4674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4290660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a6819fe7eac01eead664f50f8f72153e6751e59c5404543251ad351f47eabe`

```dockerfile
```

-	Layers:
	-	`sha256:856ef731c9c6d0251e013269165cd4a8d07f1368f21fe3a12dfae27d22386972`  
		Last Modified: Thu, 15 Jan 2026 23:14:13 GMT  
		Size: 4.3 MB (4272293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a955559a747c33e9dedd4adeeb5dbe63677643faad8715221f1b2a823c45ec7`  
		Last Modified: Thu, 15 Jan 2026 23:14:13 GMT  
		Size: 18.4 KB (18367 bytes)  
		MIME: application/vnd.in-toto+json
