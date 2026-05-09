## `clojure:temurin-21-lein`

```console
$ docker pull clojure@sha256:0f1abc26692556f90aa1ea8261242353f45882be9e37cfe4a2ec57b61563e0bb
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

### `clojure:temurin-21-lein` - linux; amd64

```console
$ docker pull clojure@sha256:649ca60ee638ad3a35de2d39a0890a413fb9c456816e908f9ed4d3e8f6c05c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230980266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55a814115ddc7267249616536ea0f9805c86fc54629c44d08032c31fbbcede0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:17:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:17:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:17:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:17:44 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:17:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:17:44 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:17:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:17:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:17:56 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:17:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:17:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:17:58 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:17:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d32ad71259e71d871a14a7ed9c62f2e935dccc287a98904375e5508fa3cf8e`  
		Last Modified: Fri, 08 May 2026 20:18:24 GMT  
		Size: 158.2 MB (158166924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0d2f8d1ec4e20378e2f3cfd2c92b10e5df670471861b1abaae727831cc5434`  
		Last Modified: Fri, 08 May 2026 20:18:16 GMT  
		Size: 19.8 MB (19806499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc6b6984e4ccb84a0d002ddfe5fb32d19b91b4df2ed834d26a617d4b8b49540`  
		Last Modified: Fri, 08 May 2026 20:18:15 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0c6d42addd29446ca646ca968445fd4bb40877abadf00ad67ea1877acdb138`  
		Last Modified: Fri, 08 May 2026 20:18:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:e369514bd5e3fda725c97777fb149063e4a1a94075b3a93ea52141b11b900604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b814b5c90cb017c7b3c51837b50ff1ea3f7be4a5a0bc7f1863557e3986c3fbe9`

```dockerfile
```

-	Layers:
	-	`sha256:17163b35993095e561d6e0b9293fa57a1d9318c9148b694f475a7b0c7bf24825`  
		Last Modified: Fri, 08 May 2026 20:18:15 GMT  
		Size: 4.3 MB (4284860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2c260a920e4b6b9f5e8a3b7149ac8b5d3321093c2ccc6a08fb06672419bac9f`  
		Last Modified: Fri, 08 May 2026 20:18:15 GMT  
		Size: 19.2 KB (19172 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:71ea4a35f33f2f40d73395a3122e3690c594ef5454ab0063ad33965e8fcd0816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228989606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14402575ef46a0cb20a943021414ca9ed3630182997596537627317fd95007b2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:22:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:22:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:22:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:22:02 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:22:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:22:02 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:22:16 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:22:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:22:16 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:22:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:22:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:22:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:22:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40137c603298391c92215f54c578c7249c2b8b4c98ab6475eb767cedbb90813`  
		Last Modified: Fri, 08 May 2026 20:22:40 GMT  
		Size: 156.5 MB (156461226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b255c4394ae5438e8514e3559dbf9b0dc60d249208c8c1cb20b194d548a75673`  
		Last Modified: Fri, 08 May 2026 20:22:35 GMT  
		Size: 19.6 MB (19637088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2340aa913a915028cb7ca42d3aa9d5e1ea66851bed603903fcfa1d08f1bf32`  
		Last Modified: Fri, 08 May 2026 20:22:35 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0499ac834b793742a15aa23548fd29a43b598ea4fc320719e059e72b42c6d140`  
		Last Modified: Fri, 08 May 2026 20:22:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:dfdfcd2098a5798ca57e2bfd7cb578c1f4cc3d0d531000b70ade892695ff75c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550fd18d56e7ef3ffefcec50829801a725aa5e922e80e3a3f1f87bcdf83d19c2`

```dockerfile
```

-	Layers:
	-	`sha256:c4451f53346a6e4d476f25e6cb0db6219fb85db68d4d2ddbdc6370f9cce3d6a4`  
		Last Modified: Fri, 08 May 2026 20:22:35 GMT  
		Size: 4.3 MB (4284499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1e26e789160a46ea3073567e41e8234f063b4608db69382c166bafdd5ea6da`  
		Last Modified: Fri, 08 May 2026 20:22:34 GMT  
		Size: 19.3 KB (19317 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein` - linux; ppc64le

```console
$ docker pull clojure@sha256:cda5e3cea133b5a1a1fd49edb9d1b9a946d4f640f68107151515c6fdd03c38bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235228643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44186dca7312c123e901a2cf2b9aaa40803561a77ee00ab7dcbb0adda6a7060f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 01:35:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:35:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:35:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:35:27 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 01:35:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 01:35:27 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:36:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 01:36:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 01:36:13 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 01:36:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 01:36:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:36:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:36:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0398f5f2459bce57485cbf20c7c00c0cc4acd23743ed54d0ac36f4b1a739a3a`  
		Last Modified: Fri, 08 May 2026 01:36:55 GMT  
		Size: 158.3 MB (158343239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541c5703a7b7340507844b07f8d626073251d495efb65ccf0abba853af9fa90b`  
		Last Modified: Fri, 08 May 2026 01:36:52 GMT  
		Size: 20.0 MB (20030483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088ba6f28e124233c168e6fa2940e67395ef6ecc70f915af44d9579c97386ce1`  
		Last Modified: Fri, 08 May 2026 01:36:51 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0362590cb2d90b00932e39ba3a4c486c5f75995d0bad62a98ee37994c2b65`  
		Last Modified: Fri, 08 May 2026 01:36:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:52d79e74749c3b78aeb88160ae0cd5a4384799d21df9d15780c144dce3a4a8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930aa8d66a5d1b702bba596dafbd52acd1d5c75512877818c5bed150c971959d`

```dockerfile
```

-	Layers:
	-	`sha256:bb184743dcf9d4630f1d1976eab5baa103172ee362c6649632a3b47196dc4358`  
		Last Modified: Fri, 08 May 2026 01:36:51 GMT  
		Size: 4.3 MB (4286733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd93ebee90bd62fd0559638452e406f272606081c49e5fce467e095d15ac7a7e`  
		Last Modified: Fri, 08 May 2026 01:36:51 GMT  
		Size: 19.2 KB (19228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein` - linux; s390x

```console
$ docker pull clojure@sha256:2d0b713863a5847262128b23e3b949ecac45147a8b744ae6f9e8da5b416b4121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.5 MB (218521275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367378846450004390706f158a7a7dacd808a7646853fca17c569a4028bff664`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:16:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:16:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:16:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:16:57 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:16:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:16:57 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:17:08 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:17:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:17:08 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:17:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9927e4ebf9213259a4ef5a3246c16010c9dc3952f2cdaf14171591311e8b7dc5`  
		Last Modified: Fri, 08 May 2026 22:17:39 GMT  
		Size: 147.4 MB (147388334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ca540c8ca5326a2a235a955ed097074f2a23718bd19ec1a01368044e0a2aa5`  
		Last Modified: Fri, 08 May 2026 22:17:36 GMT  
		Size: 19.5 MB (19466786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723f9284d002d490cebdbd6b1f8445b5a66fbc59bfc796f873b90fb6ee55b1a6`  
		Last Modified: Fri, 08 May 2026 22:17:36 GMT  
		Size: 4.5 MB (4517703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df72922d315ce542ff68f76cfaf5e5ea06fe0a36a01b7fdbadc77c51107740`  
		Last Modified: Fri, 08 May 2026 22:17:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:87aa2100f14db4b092d48935136fd3ec59c2e55029cc2682780c77fda3595fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4295845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f395619c0bc4248a6c5ff8ee5e44313abf894dd06028b9161cbdc57ca4c719f0`

```dockerfile
```

-	Layers:
	-	`sha256:75d1614d6ae575a8f7aa9e768ea555026bebc0615a205fb2aa0eaebb0bf54f70`  
		Last Modified: Fri, 08 May 2026 22:17:36 GMT  
		Size: 4.3 MB (4276674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c76d879f9dd0f4072ad4d9e86636f6e532ddb1501cba17beece42003105f9847`  
		Last Modified: Fri, 08 May 2026 22:17:36 GMT  
		Size: 19.2 KB (19171 bytes)  
		MIME: application/vnd.in-toto+json
