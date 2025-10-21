## `clojure:temurin-25-lein-bookworm`

```console
$ docker pull clojure@sha256:cae13dfb42230253dcc5e120f3f6e85bccdf854cadce6a94271af08036364d94
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

### `clojure:temurin-25-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d59d776d4a0df62578f64fc3672d25fde88cd7b2ce9ca1e00875175940e2f58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164837785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7f7fbb67acf3723ebc1a4ff16b2280c1ade67177dd63e4f9daa514f980c8e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5d0e52550dd1d9a9ee643aa5d0d13600a6609911f6bdb3a9246cc499f0e346`  
		Last Modified: Tue, 21 Oct 2025 02:23:50 GMT  
		Size: 92.0 MB (92036030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0cf4bd7d064e9a2c87531245af8151bb9c03913318a4d8126d453992939ba3`  
		Last Modified: Tue, 21 Oct 2025 02:23:40 GMT  
		Size: 19.8 MB (19803002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b4ebb7c05a9ed52bf021a69fae8e69cc3b763dca5669a0ba8a9d81289fb5d8`  
		Last Modified: Tue, 21 Oct 2025 02:23:39 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be96cd31e74a4c21510fc01cef3cf835330412824e25353c51057dae7cf3ae92`  
		Last Modified: Tue, 21 Oct 2025 02:23:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4e4ff3fffa4d76e3b13b206f6edfbf67f1f1c1b537b0cda804f13895f2c99f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c524f77b8829170365fe3786e637f491fb1fb58f8acd72d40b6b2af7305f96`

```dockerfile
```

-	Layers:
	-	`sha256:815325c029d014ebb49b37560ba3b13a43fff3ba0aedd8c8c9212e18198ae91a`  
		Last Modified: Tue, 21 Oct 2025 09:34:30 GMT  
		Size: 4.2 MB (4232382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61677a01a1fe066650f67704fc69d49ec984bac59f59f09b56ce0b326f2d1bf9`  
		Last Modified: Tue, 21 Oct 2025 09:34:31 GMT  
		Size: 20.3 KB (20301 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cb6a7d821556aac2cc154e9971ba6dd05ae63b51c24fb2d93241c206d35cd383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163554475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752a075d345b5290c479a16a1ab7d0f26f06bf8a05f3dd46a0b55a5dd2c8e702`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0d69d5599fed259c8ba4214afccce985178520360f911617276b2df237bb47`  
		Last Modified: Tue, 21 Oct 2025 02:29:25 GMT  
		Size: 91.0 MB (91045228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37aae9661ef209c1b4212c40dc76aaa7e1738e93395a092f989d353596759745`  
		Last Modified: Tue, 21 Oct 2025 02:29:15 GMT  
		Size: 19.6 MB (19632121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8fffe41bcaf27f0964e74d999d7d78fa8f1534bd4498b6e410fcd94640da9d`  
		Last Modified: Tue, 21 Oct 2025 02:29:14 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ab7bb3800597434ad245a4bf51a5e83d2a932f81bfbe3020b2cad623f106ce`  
		Last Modified: Tue, 21 Oct 2025 02:29:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1575040944dcac62625a779f87a3a206638ec284b066be51bb95a7691f80220b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cacf016deb503d41a3696171ddcaabffd8e1df29a335b7554bd323dc63059a9`

```dockerfile
```

-	Layers:
	-	`sha256:a449534f5c938c8ff4970d8994c2228abc03828cdd661a15d6a6ba1b2e2b7a92`  
		Last Modified: Tue, 21 Oct 2025 09:34:37 GMT  
		Size: 4.2 MB (4232066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c0fee8253c494ef625b41549381e96cbd862680d6e7accbec378e6ab46bbc6b`  
		Last Modified: Tue, 21 Oct 2025 09:34:38 GMT  
		Size: 20.5 KB (20494 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:9273f7cf8b26718fe58de630e19c2dd81f9ca95ad1d8a4380e6511b007bcbbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168468316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93893a5830ebab3c3ac6345f26f028b09db0e03f20383936c9c402c3442ed4aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0781477181b5af5ec1c569a15deaf01c73878e068638e740e70d8e99fef2b4`  
		Last Modified: Fri, 10 Oct 2025 04:40:19 GMT  
		Size: 91.6 MB (91601717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db362206ecb79a1976a1e203b1bbad41b29384f9e4d97bb28af8ca77ddee73f`  
		Last Modified: Fri, 10 Oct 2025 04:40:03 GMT  
		Size: 20.0 MB (20021627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8dd704df43e3cc3abc4da5806eed5760de2ef9b2406bb299017134c75edb487`  
		Last Modified: Fri, 10 Oct 2025 04:40:01 GMT  
		Size: 4.5 MB (4517780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db22097fca60a86c01ccf80781206f00ccde64d5aa8cd2c082566697ce23d0b2`  
		Last Modified: Fri, 10 Oct 2025 05:52:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e9b623337ad508ed197de45822c1b8ac16c63444d3961afbe6f158eaacdafaff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4255957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca09b91391fb0c4c8e653522d4aa909f6286ef0c272d7587f68611679ba9694`

```dockerfile
```

-	Layers:
	-	`sha256:9418668b54330379a6e613e5cc78403709061d73a43d7c5b94de9bcdd4d4235f`  
		Last Modified: Fri, 10 Oct 2025 06:34:48 GMT  
		Size: 4.2 MB (4235575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:481ffb5eb8c0567bd0f539bf6b9d67a742efcfb6360a7858f68a298e204a1fb3`  
		Last Modified: Fri, 10 Oct 2025 06:34:49 GMT  
		Size: 20.4 KB (20382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:463b1581a39f023f7ed971d78bea926e392ab4d1ddfa0f3eecc17d4aba3de4ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159322794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0de5203d5deaf145e2ec8db429825b0b15aee6c59fe0f70b5111a5186d6d25`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:87d1bec83b35277b636c6e05b9418301b2f025752d7539cecae442f0b94d8fbe`  
		Last Modified: Mon, 29 Sep 2025 23:33:26 GMT  
		Size: 47.1 MB (47137446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0377f9dba375d95cb49de92a8238c46c38f8e06ec3ab5ee54df5d9cfa7d596c`  
		Last Modified: Thu, 09 Oct 2025 22:50:23 GMT  
		Size: 88.2 MB (88206454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115539499636717841e61265a04cacb0d546bbdba4a383168de4fd4275ba1777`  
		Last Modified: Thu, 09 Oct 2025 22:50:19 GMT  
		Size: 19.5 MB (19460708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e652e053a85605664400aee04e4da6c949d02d156baa4a9e06c783231eabe7`  
		Last Modified: Thu, 09 Oct 2025 22:50:17 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e399f008ec753b0c599a32d6c3b8295ee82452c1bec2fccfda0fcd03e0fe1b2e`  
		Last Modified: Thu, 09 Oct 2025 23:36:33 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d89a0f960b792abb22d27b2b10a2f3679d92a9faf81757aadea733c6b1aebbe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54871560d88069756bbf4a80fa35012534e93c8fda7bd53beae0f9581d5d100f`

```dockerfile
```

-	Layers:
	-	`sha256:2c47bc2c9b3d24a11776f2007c1262579fc13cbb15fb7f87700e3612eca15749`  
		Last Modified: Fri, 10 Oct 2025 00:34:52 GMT  
		Size: 4.2 MB (4226744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ac68751babc19b7c726505875f2c9e1d1c781c392f4356aa8dda09238d1d637`  
		Last Modified: Fri, 10 Oct 2025 00:34:55 GMT  
		Size: 20.3 KB (20302 bytes)  
		MIME: application/vnd.in-toto+json
