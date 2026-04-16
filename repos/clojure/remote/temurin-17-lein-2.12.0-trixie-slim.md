## `clojure:temurin-17-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:0e65ecde36971f8525083bdf53745e4413e8c2c7e7dfa7c38c59772db60c8fef
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

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:88d4ce6d2a82ff020993c973f7d57537cb6b576b284c4d77ff0afa0d8fd0126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.3 MB (199324517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa67e0dc774c16eb0cb36845d53b3f6288b29b0a25ce6ac3422dca177e04d5e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:03:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:03:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:03:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:03:50 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:03:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:03:50 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:04:07 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:04:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:04:07 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:04:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:04:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:04:08 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:04:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cfc3591047fa48c133600bbdadeef78aab921461c51633ab66b4f983522245`  
		Last Modified: Wed, 15 Apr 2026 22:04:29 GMT  
		Size: 145.6 MB (145628761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def0c2f6ea9279bbc677e2cc3afbc13804a8d4ef3e0b0a416478d89445e38505`  
		Last Modified: Wed, 15 Apr 2026 22:04:27 GMT  
		Size: 19.4 MB (19401975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e6eacf00e86b1919edbf3ac333b8aa1f83fb568c33c5fb8eed69d30f9a3c2d`  
		Last Modified: Wed, 15 Apr 2026 22:04:26 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b811fc5b553611fa407c378e32a6e69b9868020ad56172ae0a048411365411`  
		Last Modified: Wed, 15 Apr 2026 22:04:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6a9852e95029774b882442d1645fb7fba45fdc7c0882a926f0a7cb5f02415858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c7aeb1a6fa9622530f1d91065366d529b71dbae9df6f9b0bce90c6b5271c58`

```dockerfile
```

-	Layers:
	-	`sha256:4c2a2db05f4f61583f6731ab2a9b64055660ed5068149e1300543d918161ab1c`  
		Last Modified: Wed, 15 Apr 2026 22:04:26 GMT  
		Size: 2.4 MB (2364788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f67c491ad173b436a36eb7c8fd4a25613e6e1d98910f9bc399d4b51099c36d94`  
		Last Modified: Wed, 15 Apr 2026 22:04:25 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2ce4869063443b3d7a886d16f3be82d8df1b61d4be33caaad5d68fdb70a28b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195506877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27609dfd1310da2e74603cab1ecbdc5847f71919bc5fb7b81b219d3731c699bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:25:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:25:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:25:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:25:37 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:25:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:25:38 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:25:54 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:25:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:25:54 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:25:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:25:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:25:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:25:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368c68d1237430bd9255a23e573199d207c4ad15bfe8e749f109a0cdca5bd160`  
		Last Modified: Tue, 07 Apr 2026 03:26:15 GMT  
		Size: 144.4 MB (144436224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5da09f4a708a9c154beeed3c4868d483f07c412e329ff846e695eb330b91032`  
		Last Modified: Tue, 07 Apr 2026 03:26:12 GMT  
		Size: 16.4 MB (16413961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ec6008f8903a888bae0ec89e403f471deafed6f896c22527c89dc95df68eea`  
		Last Modified: Tue, 07 Apr 2026 03:26:12 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa1ea5817a0f3ad70cabbcadcb4387489d83a698124bd661bf9fedde4693443`  
		Last Modified: Tue, 07 Apr 2026 03:26:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:05dcc5c8e673d7e0e995df864087b3232d983e5039795066579515544d12ed87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8dfd571af407d19695e7c15070b1ad0da8b1060636d4a10b63cd975ae13f0e`

```dockerfile
```

-	Layers:
	-	`sha256:a53d28c227b8d68663a889b4bd5eb57b021eae67720747a59bde15b5564167b8`  
		Last Modified: Tue, 07 Apr 2026 03:26:12 GMT  
		Size: 2.4 MB (2364406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f887c86548f6e80f24bd7c78d9c4d8930b6dd690a803f7412baf77adc6773b49`  
		Last Modified: Tue, 07 Apr 2026 03:26:11 GMT  
		Size: 18.5 KB (18507 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:bad4ecf97673d662dfeb4949473e1a6995ea01ed824f8958ace3f96654ef2ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.0 MB (200034746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db74c1f5393d352960ac704a29843533297ddd9307d97d56369480ce296fc88`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:40:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:40:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:40:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:40:02 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:40:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:40:03 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:40:39 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:40:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:40:39 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:40:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:40:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:40:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:40:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3932a79f80dcbdd923f767310a5e86b8d32b8b0ffe1fd3bdd6bfa835cbf4e1d1`  
		Last Modified: Tue, 07 Apr 2026 14:41:24 GMT  
		Size: 145.4 MB (145438259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454859a5e4288654bea049c8b2262020103eb10491c42c95de1cd4203dc30bfd`  
		Last Modified: Tue, 07 Apr 2026 14:41:21 GMT  
		Size: 16.5 MB (16485287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25406bd2d98e6fe55dfb0201004642e04ab3c9149fd1d4796337287c9bc3fc81`  
		Last Modified: Tue, 07 Apr 2026 14:41:20 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9273fb154fded1cd1b68b3e6a15c8241d98489ec2f5c71de55d314c9f1b5edaf`  
		Last Modified: Tue, 07 Apr 2026 14:41:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f1541bf29d7b8fd083f148cba7671b21cbce9542e2c1029f13506285a022b712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c9724ea341c535f2db20c3d0fe50799ad885d7a482f68f5b4d9cc3b99ee7bd`

```dockerfile
```

-	Layers:
	-	`sha256:b5c7a9ce474e4d581b2af18ecc03fd9124e0ce03fd0618991ae87a1f16ac3260`  
		Last Modified: Tue, 07 Apr 2026 14:41:20 GMT  
		Size: 2.4 MB (2365768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce67cc28571d931128a17d62f8eb86f29fc57644ef1a223be718e830b52e8d87`  
		Last Modified: Tue, 07 Apr 2026 14:41:20 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:cef4351742ddc956c1abbe250ba98e93bc4b7c145fbb4d138fd3624b89170cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.5 MB (194475035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0b0e883e2ab9bc1abce054f70438bead468c511a83961442526a9b6634275d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 21:22:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 21:22:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 21:22:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 21:22:08 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 11 Apr 2026 21:22:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 11 Apr 2026 21:22:08 GMT
WORKDIR /tmp
# Sat, 11 Apr 2026 21:23:43 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 11 Apr 2026 21:23:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 11 Apr 2026 21:23:43 GMT
ENV LEIN_ROOT=1
# Sat, 11 Apr 2026 21:23:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 11 Apr 2026 21:23:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 11 Apr 2026 21:23:58 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 11 Apr 2026 21:23:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627211ea53d67d631f36471af626424406273922e1c797e45253f9483f38b907`  
		Last Modified: Sat, 11 Apr 2026 21:27:49 GMT  
		Size: 142.7 MB (142662927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16e456739b85ac78e850bad06edb6ecae01a40629490e4309d6c1abc4a0af74`  
		Last Modified: Sat, 11 Apr 2026 21:27:31 GMT  
		Size: 19.0 MB (19018117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84524c3b45171f85ee391db9114e0004d9adb941ccee2840066d4ba0dd32e56`  
		Last Modified: Sat, 11 Apr 2026 21:27:27 GMT  
		Size: 4.5 MB (4517783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bada9d142238a0c26a30587726e8ec6d21bb1ee893447902dd42741eb757962`  
		Last Modified: Sat, 11 Apr 2026 21:27:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7c12e78cb508d1df99b1fc9713c77a4879e943044ecd2a9343aca3f65fa7df93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecbe410c8a8cdc368b9b3a1bac48369dee03a9909bbd789b6dab1bfe72b4581c`

```dockerfile
```

-	Layers:
	-	`sha256:454aed1deb8c7ca4007aa6c1c26a4fb2e6980f317cf7af43f3a4e29140fc6756`  
		Last Modified: Sat, 11 Apr 2026 21:27:26 GMT  
		Size: 2.4 MB (2354917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f13798090cadd7b0b0fc5388e7c7bc4d14731acfa2bf2a1f2dcb9bc31b3c45`  
		Last Modified: Sat, 11 Apr 2026 21:27:26 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:5402497823be891853a56cc986d94e9af860eb8da8c92ec1891ef54011d9e61b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186464247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607231353c5d459125faefd27807895ca9b3c4b6477f841bd99fa2b9c133e0b6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:42:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:42:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:42:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:42:18 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:42:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:42:18 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:42:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:42:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:42:31 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:42:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:42:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:42:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:42:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5be30173782ac514fe3cc2acff6571642739faff5843cc6d1d0067cb9203c3`  
		Last Modified: Tue, 07 Apr 2026 05:42:59 GMT  
		Size: 135.6 MB (135626852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823367612693523eddc55e37d4605afc6581d1e22f5f79cc2cc87e1d3d64a524`  
		Last Modified: Tue, 07 Apr 2026 05:42:57 GMT  
		Size: 16.5 MB (16483816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b8a5f8bf899abbd9b5c31bf30f3907ab12f00b6a9975d476dee145cec04c50`  
		Last Modified: Tue, 07 Apr 2026 05:42:56 GMT  
		Size: 4.5 MB (4517734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3564c9aed18e7e2d104d7fdbb2b8351c1df24479b04d748eff3273c90fe633`  
		Last Modified: Tue, 07 Apr 2026 05:42:56 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f73d4dbbed85c014ca12f8881b9f930afa9d4fb6a7bb5566f48124c3812e9714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4882fab3cf8eb6b41bc6e6c3660145cc1d2b9220b9f77567f6e18f1f88e2c9`

```dockerfile
```

-	Layers:
	-	`sha256:509141902dded53cd65c694532128d8866e648546ed1aba303d48f51e03d9855`  
		Last Modified: Tue, 07 Apr 2026 05:42:56 GMT  
		Size: 2.4 MB (2361215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48632633c3234378e4192351443b39acda532d9a3d69713cf6cd67f5f85fc84c`  
		Last Modified: Tue, 07 Apr 2026 05:42:56 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
