## `clojure:temurin-17-lein-trixie`

```console
$ docker pull clojure@sha256:b1527e4813084bbc7355ac8016a3375c43ae185286034e2531f1a8ce3930bae9
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

### `clojure:temurin-17-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:223e488b8480faef87dcad511e0f0854f4075ca4b248b9f4f8bdfd9aa8fb0fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218330638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7309040ecd09fa086b49e55bf5584e4c1a9f968a777b25ad04501dfd28b4a05`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:18:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:18:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:18:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:18:53 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:18:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:18:53 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:19:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:19:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:19:11 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:19:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:19:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:19:13 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:19:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da84f642af1d50a798cd9795b30ffbe13b00dcbc48118571eed114ed5d6f54c2`  
		Last Modified: Thu, 11 Jun 2026 01:19:25 GMT  
		Size: 145.9 MB (145905445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac1d02a067beff618ef4c44008a60359991a7b9ed4ac41661a4f728540f8711`  
		Last Modified: Thu, 11 Jun 2026 01:19:35 GMT  
		Size: 18.6 MB (18589907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5631fcb112427fb3d751d999ec5917873d312823b6158618cdfe222c8aa16801`  
		Last Modified: Thu, 11 Jun 2026 01:19:35 GMT  
		Size: 4.5 MB (4517736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e966b36255b69c2e1b70705e75853d822e93d1ca9a8c9db379a4249a08878262`  
		Last Modified: Thu, 11 Jun 2026 01:19:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3875697989c3f6b83aa4ed5728e3c51a17629ebeff9358cc632027601b1074e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ce3b5a28ad15db5cf6dc23589406efc7642b6a5a76c5cb02398806248fd423`

```dockerfile
```

-	Layers:
	-	`sha256:7e4f81b453ff8b730082ea6125ccc93f8ecc4caaf272b24a69331ec9cc47a71d`  
		Last Modified: Thu, 11 Jun 2026 01:19:34 GMT  
		Size: 3.8 MB (3816196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e69d59377dfe55c5aa2cf8bb28910948bd1609f56454457989bcaf109083d04`  
		Last Modified: Thu, 11 Jun 2026 01:19:34 GMT  
		Size: 18.5 KB (18504 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:48be9c0f4c40b70f15988fe3218390e4430b57c103d5c3a7facaa501f2e116e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217468821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20490e2d1efdf47c06c32fea012ccff0c7727cdf211583c5983a16b2f0064e8e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:22:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:22:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:22:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:22:33 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:22:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:22:33 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:22:55 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:22:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:22:55 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:22:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:22:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:22:56 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:22:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5caaa80e63e14c6c2a5b4732975e4e9e3a19c7a64d19f4291c8a1effaad2329`  
		Last Modified: Thu, 11 Jun 2026 01:23:20 GMT  
		Size: 144.7 MB (144724360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354c6bc4530babc16d9317f57c1bfb5630805d2eebc88816dcebd4ed5e1f87e5`  
		Last Modified: Thu, 11 Jun 2026 01:23:17 GMT  
		Size: 18.5 MB (18548167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82982c823b17dab79c3ce8b86daeaa0ce2f63f2f71f94b63d971215fe4828689`  
		Last Modified: Thu, 11 Jun 2026 01:23:16 GMT  
		Size: 4.5 MB (4517697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabb0143c0551cf71cb376cfb9d36a25e7491b80e9b7bcb8acab4b154f7034b2`  
		Last Modified: Thu, 11 Jun 2026 01:23:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7dfadaf3ab3a4aff27a05bae997d867cb0f03a6a6d76e2b20d015d80ca95b601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c0fd3cb3b95feae8e8d0be9db7e882de8734a07ecd1be2356d5513127b6136`

```dockerfile
```

-	Layers:
	-	`sha256:967691166a43a5c6de3ac018bd265f65dbc6adfba7c9088cd072df5f3c16fff9`  
		Last Modified: Thu, 11 Jun 2026 01:23:16 GMT  
		Size: 3.8 MB (3816436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c4d885997e4fc885fda2d71d1f50872f2bbcb8a4d4f4ed9c486d173c100bef`  
		Last Modified: Thu, 11 Jun 2026 01:23:16 GMT  
		Size: 18.6 KB (18626 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:5e3d54db9de4b5b850a879bce0ba43fc9b26fb334d477f85f88c505cb04d3bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222067461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd223028664d6c86e07e0d13ea3fcd815475733b3bf58d006266408813bf531`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 09:31:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:31:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:31:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:31:37 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 09:31:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 09:31:38 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:32:22 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 09:32:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 09:32:22 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 09:32:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 09:32:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 09:32:25 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 09:32:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaefd5d828c1f6e77237a4e4803b3841b044469ab5a54cc48151d84d7468775`  
		Last Modified: Thu, 11 Jun 2026 09:33:01 GMT  
		Size: 145.8 MB (145766092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b7847b51cd40e771f8b00ef1023831e7766fc7569a3eb3d479d1215d827425`  
		Last Modified: Thu, 11 Jun 2026 09:33:00 GMT  
		Size: 18.6 MB (18645302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85b36146294edef885eff563d4d6b375bd2ca54cb1ec2ceb96f85b714122646`  
		Last Modified: Thu, 11 Jun 2026 09:32:59 GMT  
		Size: 4.5 MB (4517700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a359df89c5448aa91ab59c0be90a8d83ff8b73892b8c3581bf66fb0bc72766`  
		Last Modified: Thu, 11 Jun 2026 09:32:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1b08333728f3fda6ab0eac1c5482884fd7d04c1271ec53752b4c11c1a54bf00e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8aac526fc62c4c84a1f0907d44f1a0ae2d84efb2b9a34dc88eca2a9d6e346f`

```dockerfile
```

-	Layers:
	-	`sha256:dfc2640f74a70c1f768eab3f833c37d1898fcc0f2a55ce49241fcb186202d5a8`  
		Last Modified: Thu, 11 Jun 2026 09:32:59 GMT  
		Size: 3.8 MB (3817196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47645e00de4701634fdcf0cf56c9e360d08615f5f14a008a4b4edde5721d57c8`  
		Last Modified: Thu, 11 Jun 2026 09:32:59 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:aefdb0a47ef85c38861df2e0ce08e00a85e3e4fa0012edd88d61a426f44f0e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208445606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d3276ddc72961fc526b947bfb827c5d22bc77f842b2ebe9da90a25d52b4510`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:09:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:09:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:09:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:09:10 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 03:09:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 03:09:10 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:09:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 03:09:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 03:09:23 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 03:09:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 03:09:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:09:25 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:09:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a727f4eff59ad89139dcf74c95cce8838b028ff8c9fba9099a34d7f75c8ce93a`  
		Last Modified: Thu, 11 Jun 2026 03:09:51 GMT  
		Size: 135.9 MB (135910421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a4263bbab52d734776fb66bcbea6633bb977c64df86ae88739bc7a1e923331`  
		Last Modified: Thu, 11 Jun 2026 03:09:50 GMT  
		Size: 18.6 MB (18631103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a51b0fc442c95bdd32357b601e3560dfc54f96de3b5a7c71dd83b7622cf7f1`  
		Last Modified: Thu, 11 Jun 2026 03:09:49 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e65324cdd52db5a0bc0ae7dbe04ba8eee26e11794112362993df879986aa06`  
		Last Modified: Thu, 11 Jun 2026 03:09:49 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6658f9a4788677266f118acbcdd2669e5fd41ebdb2c3cc3580cbc4afc358bb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332fc621ae16be060b6f58e2e7bf69538b81f474964a1a9de650fe775a990566`

```dockerfile
```

-	Layers:
	-	`sha256:0556d38fd81afe0e880cb913bd36d4a6c551bea7871c53255d84e9637d2b519c`  
		Last Modified: Thu, 11 Jun 2026 03:09:49 GMT  
		Size: 3.8 MB (3812623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a209f3b49191257199bbcb557d44abe3adc313fb7bcf2264a6a957d6a5772aaf`  
		Last Modified: Thu, 11 Jun 2026 03:09:49 GMT  
		Size: 18.5 KB (18505 bytes)  
		MIME: application/vnd.in-toto+json
