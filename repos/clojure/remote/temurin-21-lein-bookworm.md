## `clojure:temurin-21-lein-bookworm`

```console
$ docker pull clojure@sha256:2cb696fd6a7b7f7fc0e5de6bf69fbf017aa19657d88a1f778ed63d545d254886
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

### `clojure:temurin-21-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:13984d5914f1a00b9907caeca6611b2655c65ab5432f68c18d2ed25392cfca1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230627988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe1a9a133fc806bec7c34285048f13faca825f6f7ef72ce922ae18883b933582`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:01:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:01:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:01:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:01:03 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 01:01:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 01:01:03 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:01:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:01:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:01:18 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:01:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:01:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:01:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:01:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6302caccca32cda5752f9bcf891d1ad8fcc3eeb0767c2f7f19b0a556d466ae29`  
		Last Modified: Tue, 30 Dec 2025 01:01:56 GMT  
		Size: 157.8 MB (157826042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57212c57df684be720fa683e778334e036c9d6ade6d19f0d138c637bf2019d60`  
		Last Modified: Tue, 30 Dec 2025 01:01:50 GMT  
		Size: 19.8 MB (19803006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7322bf9eb4220399cb2fa5a174685eb8375f9b7d3b221565442155ca8df5361`  
		Last Modified: Tue, 30 Dec 2025 01:01:47 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab59ea61ace34fc924955051c51a6887c03b436688ca28ccad42a4971f9778df`  
		Last Modified: Tue, 30 Dec 2025 01:01:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:03ae7872b662ce390c79be23b133fbca4a09a6c7b8b19df4af3e762ea39b6c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f81826e79fbaf131d4277ddce0026540d32ca87987bed9ddf96c80b0c2d3599`

```dockerfile
```

-	Layers:
	-	`sha256:fcb901253a15277dee0da38d32bbd996cc69852d42adbcecafdae5f76de5529d`  
		Last Modified: Tue, 30 Dec 2025 04:43:27 GMT  
		Size: 4.3 MB (4283588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:873d89dafcdb8d003fe6b4ea2419550b30470ef0799beedec2e8a45cabdd3c15`  
		Last Modified: Tue, 30 Dec 2025 04:43:28 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:70936b89e6f78ddd3237d25a4f9329c6b00470b74c6f48e7e10ede170c498a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228617140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7297d7c660359665ee56319903f20f4724698833624e60a6f75201a0249d64c0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:02:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:02:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:02:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:02:19 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 01:02:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 01:02:19 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:02:33 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:02:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:02:33 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:02:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:02:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:02:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:02:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744000bf154ed9411b9b928e26e7796f03848939d9160ed9b1b49c76651c3b7f`  
		Last Modified: Tue, 30 Dec 2025 01:03:14 GMT  
		Size: 156.1 MB (156107673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c0a58b439633d9a9edb0e8de98bfffe992c60c7743f6b503a99c723254226f`  
		Last Modified: Tue, 30 Dec 2025 01:03:08 GMT  
		Size: 19.6 MB (19632192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a48b0f2b3ebd366c02b9df90fd29166ae365a9445211e354e29a506aaa6cb1`  
		Last Modified: Tue, 30 Dec 2025 01:03:03 GMT  
		Size: 4.5 MB (4517701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4cb504053da1d2719d5c351786ba7783f1b8ed2370858feec32a6738fc71f9`  
		Last Modified: Tue, 30 Dec 2025 01:03:03 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8ba173cac3bddec4a634d0a2f68456c2383d25c3e71754b226cd5e987d45d926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c539c5451a0c09c4785c26b30d77ede23b7db5aebaf5bf5a231ad80a072a9f79`

```dockerfile
```

-	Layers:
	-	`sha256:6a3d4585d83948a43c40820ffbe043b39e79cb506bcff45a0d21b7d740cecb02`  
		Last Modified: Tue, 30 Dec 2025 04:43:33 GMT  
		Size: 4.3 MB (4283227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a04f297c74d8c0d3f27fab925d7809c3352fdce6f3f9ffadc08b422306479152`  
		Last Modified: Tue, 30 Dec 2025 04:43:34 GMT  
		Size: 19.2 KB (19163 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:44953975ff691fbb2d665c07fe34be308b130433d016b5327d847bc136ae35b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234809832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef5e636d737cfc38749c494eac05b6bc4c0797f841187e493d79c77fdd5d018`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:43:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:43:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:43:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:43:53 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 01:43:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 01:43:54 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:44:33 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:44:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:44:33 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:44:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:44:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:44:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:44:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:48e256c4119c0ad256492d6a930e99d2b2d7f8d7920d619aa2de4f616c37076e`  
		Last Modified: Mon, 29 Dec 2025 22:25:39 GMT  
		Size: 52.3 MB (52326998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9d97546303efd08b59676c0ae34293278a22e0472a5e5aed8160ac03056604`  
		Last Modified: Tue, 30 Dec 2025 01:45:40 GMT  
		Size: 157.9 MB (157942939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6339bb075cc401c9c690ea396be261911842328822f7e3c422708de7dc3a808a`  
		Last Modified: Tue, 30 Dec 2025 01:45:32 GMT  
		Size: 20.0 MB (20021711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7fddec2ba4632edcb104c705e391387a45b65645ad6d8d2c05fdfd6e43a7c`  
		Last Modified: Tue, 30 Dec 2025 01:45:30 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f199e903ff6245089f32c352daf968cfb6306f1932967a344bfe4298fcc76c38`  
		Last Modified: Tue, 30 Dec 2025 01:45:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5cee8bb34777ba743734904343ed3da2a6f60841292d139e5f6e8dec27928e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d00f592fac4e6bac3cc9eca22b8c727808fb17199d6158784453120c6bb8e9`

```dockerfile
```

-	Layers:
	-	`sha256:50253e70ebb91b3344fd5eadf684fda6e6e871f649f389f38c5aa9111ae6f7a7`  
		Last Modified: Tue, 30 Dec 2025 04:43:38 GMT  
		Size: 4.3 MB (4285459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ef24c958711c80fe2e2a0d96d8e8237801bd97bdf88fd70198ea49faff3c618`  
		Last Modified: Tue, 30 Dec 2025 04:43:39 GMT  
		Size: 19.1 KB (19074 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:91226fe21ed8931cf843c42e6de79275df42a8a51da47a59ce8e6f38e8611d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218188485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7867b613780ec321d34bb90c48d1b8201db84e5f5facd37ad326a908a569c78e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:05:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:05:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:05:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:05:12 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:05:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:05:12 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:05:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:05:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:05:23 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:05:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:05:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:05:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:05:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f4778709d6309aad2ad3cf29fbc96c579ca1e3384edc37a8fdf97673c6b3b8`  
		Last Modified: Tue, 13 Jan 2026 03:06:14 GMT  
		Size: 147.1 MB (147069834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30617b32c2b4cbee045781f7828ae2e29da0773830a49248e83a33f016df46f0`  
		Last Modified: Tue, 13 Jan 2026 03:06:00 GMT  
		Size: 19.5 MB (19462076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205839f5d8551c9ce77c1ab9a9624ae8f250bfe7b2bf8f964cd09b2f945951a1`  
		Last Modified: Tue, 13 Jan 2026 03:05:58 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb8b3e937c6e339c51bbaccdf67ae197ffd5885356cf3bd976e0dc591794f84`  
		Last Modified: Tue, 13 Jan 2026 03:05:58 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7c9c258362e56f567c4bf89b56da4bfe64b6183d3455319f6fd3b8c151f67803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4295063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a369ca59c1fee64c65e6035baa77e44e6566b6b5aafd0ce90f678a2de88c771`

```dockerfile
```

-	Layers:
	-	`sha256:5bc51d3bd47f638d94eaebcc898c5daa8cbd6c412622b272c328b16d51a98667`  
		Last Modified: Tue, 13 Jan 2026 04:38:50 GMT  
		Size: 4.3 MB (4276045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:133e03d8aa65a0f08beabfc2c4eee5d998cb7229112c789c1b8bd1b3b59ff08a`  
		Last Modified: Tue, 13 Jan 2026 04:38:51 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json
