## `clojure:temurin-21-lein-trixie`

```console
$ docker pull clojure@sha256:5025f19d937a7fdd890f4f850ca8668e6828643d672708d2c0abc441a5f6b8b6
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

### `clojure:temurin-21-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:4b792cc6613bc14801b9eff19e3bdedecdfbafcd4adaef7fc322bb9eb411f0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230592063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214fc9700ff682fc0e8904e85a6e6b4e344538ff13864f643d2d3efdabda219f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:19:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:19:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:19:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:19:38 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:19:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:19:38 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:19:55 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:19:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:19:55 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:19:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:19:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:19:56 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:19:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94de3a313e81b4b9e28fe3129cbb52d0102acd8e818ec73a514735dfca98aeb6`  
		Last Modified: Thu, 11 Jun 2026 01:20:13 GMT  
		Size: 158.2 MB (158166939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fa6ea2bb6c19566f0997a81075eb07072383cd69ba9af4759a06e2664d773f`  
		Last Modified: Thu, 11 Jun 2026 01:20:14 GMT  
		Size: 18.6 MB (18589870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1b437c2f15b85e0fe11d7ba156762eed011f19b74f78fe272a8d3de0707f85`  
		Last Modified: Thu, 11 Jun 2026 01:20:13 GMT  
		Size: 4.5 MB (4517706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabed15b4810a08e8e42488a24ff460caa88c87a615ba4b5dc7f32a827df8021`  
		Last Modified: Thu, 11 Jun 2026 01:20:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f16fb7efd1c3642113d809a525bf521c4d66390880628ea5e14d472b7edc6749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2b4ef19aafa8b43d97bc0bc3f2ce11af366e69d42a6431f3f3cb533e794bbd`

```dockerfile
```

-	Layers:
	-	`sha256:63af911be948b5dbe2947837b78cbb7c420d87a7538440716f441e27228d1ce0`  
		Last Modified: Thu, 11 Jun 2026 01:20:13 GMT  
		Size: 3.8 MB (3818048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd3c241767aeadf21578bb14436e858bac6741eba724c2c41caa392f678d6266`  
		Last Modified: Thu, 11 Jun 2026 01:20:13 GMT  
		Size: 18.5 KB (18506 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8bdc1eee7f1f882820183543ecab06c65dca52a9eb3ef6c3a8ac1b0d81304855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229205915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf14b383df38c7ba8d3088df446fe9e1179b44c9053417a27e40db0c8d0b805`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:23:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:23:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:23:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:23:39 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:23:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:23:39 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:24:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:24:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:24:03 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:24:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:24:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:24:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:24:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa03728a2141abe16cd31abde70595b14f068b1f0f807cd9036611102e3574b4`  
		Last Modified: Thu, 11 Jun 2026 01:24:29 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c292ad23ee69831386dcdbc7340d450c652fa409414cf85bd13c0c786a7b10`  
		Last Modified: Thu, 11 Jun 2026 01:24:26 GMT  
		Size: 18.5 MB (18548285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1c4e566e638496d8e845c7bbf8eef04b55191db87e06cf65b4b58c76799f96`  
		Last Modified: Thu, 11 Jun 2026 01:24:25 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef56ab0d4381566fc4c5d189922041248fe72ff4820ba77720770765ec9737c6`  
		Last Modified: Thu, 11 Jun 2026 01:24:25 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f184bb02148dad71806c7b31b499fe9d4773fbde8941fa48250cb91e616bc1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00ff87526bc9ed0326c0d91ada087b79e676dca63302b0021858b41853a7ffa`

```dockerfile
```

-	Layers:
	-	`sha256:396bf38aeee5e60e7df3c4a71fcd32b1f9f9a817d49d2613f99b3d5cf8159b74`  
		Last Modified: Thu, 11 Jun 2026 01:24:25 GMT  
		Size: 3.8 MB (3818288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dec71fe2f398387c633a0aa41da133b2dc37d0d59e1727c18b54c3dfe798978d`  
		Last Modified: Thu, 11 Jun 2026 01:24:25 GMT  
		Size: 18.6 KB (18627 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:acde57fe5088f3084ad67eeb54d51d738155c4abd689ccfd1b69dfdb3a3c6df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234638428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9e644c74a1f9d2eafd7bd9715c6a3b39398ba2cbf316b4a82717902d2e37f1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 06:02:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 06:02:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 06:02:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:02:25 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 06:02:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 06:02:25 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:02:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 06:02:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 06:02:56 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 06:03:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 06:03:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:03:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:03:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b629dc606e724e659e7094cdede449bd2fe74e4594977f7749e2b2b2395027`  
		Last Modified: Wed, 20 May 2026 06:03:43 GMT  
		Size: 158.3 MB (158343282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079ced106a7143259ab31619c144e40128c884b6db84584b08e21ea649257ae8`  
		Last Modified: Wed, 20 May 2026 06:03:40 GMT  
		Size: 18.6 MB (18644814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb34cd3ea3d14556fc879e047075785cf6d65d9fb63215da2cc1114f3ff3da2`  
		Last Modified: Wed, 20 May 2026 06:03:39 GMT  
		Size: 4.5 MB (4517721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a0eb149ee39f546897b49a61c7698f21e46772905c736a59df26f1de415d6f`  
		Last Modified: Wed, 20 May 2026 06:03:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c0eca5e469382e713ae4cc7d0ac2acca831a99a77b4a752f17a62031147893d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3837598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb9d27454ed91c1a7cb06c3fdbbd13fce702ef2d6a6407635f93c4556f1c0e9`

```dockerfile
```

-	Layers:
	-	`sha256:afb45f690b17f7b45c69c2fc95eaf386bacc47412b1f3450a7ab3aceedb540fc`  
		Last Modified: Wed, 20 May 2026 06:03:39 GMT  
		Size: 3.8 MB (3819048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d32a53d5031faa9495e0fe6ff325d1659023423425b34838fc6a88ae5cce582`  
		Last Modified: Wed, 20 May 2026 06:03:39 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:3775be4678a389ed85aa2198c9c364af54a7b6b046a17886e1c54c18f9a351ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219923530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e55f780d242456d87a32fedf2933b25d98ed1aed490cc11d860acf76d46cd7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:11:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:11:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:11:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:11:22 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 03:11:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 03:11:22 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:11:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 03:11:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 03:11:35 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 03:11:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 03:11:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:11:37 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:11:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d283a83afe454a5e986887cabe845ba92525fe405ba9481c9381d96f0b53ca97`  
		Last Modified: Thu, 11 Jun 2026 03:12:05 GMT  
		Size: 147.4 MB (147388375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b87b244039897f15824ee94a47e45bbb3cc0ecfff3b1f99c05f7c0a2b7891a`  
		Last Modified: Thu, 11 Jun 2026 03:12:02 GMT  
		Size: 18.6 MB (18631086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcf7145055070ead44bfb5aff423288767a581923552d2a4a16017c17be9cba`  
		Last Modified: Thu, 11 Jun 2026 03:12:02 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bbdba2376d6bc480c2998989282f29c27cf3ad2b509afa2d06edf1f495fbb3`  
		Last Modified: Thu, 11 Jun 2026 03:12:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:87f5a0bf5afe34977d77ea2b6836cdafe47b04c31993792788815f1305933e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685827cc866d5b342917940c1230b22e4d063070c4f861d03c47729ec2c0ab77`

```dockerfile
```

-	Layers:
	-	`sha256:033f6fd4c9f0d52de9b050c109ed893e4255794c56a458352528962883540577`  
		Last Modified: Thu, 11 Jun 2026 03:12:02 GMT  
		Size: 3.8 MB (3814475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de169d7cc43fb19c8e2116a9cf869bd99ce08e76990ac04b82b31db37f3b544`  
		Last Modified: Thu, 11 Jun 2026 03:12:02 GMT  
		Size: 18.5 KB (18506 bytes)  
		MIME: application/vnd.in-toto+json
