## `clojure:temurin-11-lein-trixie`

```console
$ docker pull clojure@sha256:dc45eb85de0a542f2a59da9f05dd14e0921f94335c65851ddaca988c5024a859
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

### `clojure:temurin-11-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:44cb59132abdc6fc5c3f230676f78d2160ce9bfa4590d0810de26b441a6ec87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218311160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9918544a73aa7a43837ff58af024786346ec7287d04b0e28024361b4e2d94dc3`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:17:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:17:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:17:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:17:24 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:17:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:17:24 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:17:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:17:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:17:44 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:17:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:17:45 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0e47f9679361fe8551237c94ad1ee27420d19561e4437341ae0c3c83dc5ad1`  
		Last Modified: Thu, 11 Jun 2026 01:18:06 GMT  
		Size: 145.9 MB (145886263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f8ca99adc07333c61d5f07cb443be2ee37627bfff9e6c2baed4ba467956f5b`  
		Last Modified: Thu, 11 Jun 2026 01:18:01 GMT  
		Size: 18.6 MB (18589984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3116a6f8a4d8d5e59afc494e42c6632617ae71ba49b201f2feff2f97e7d9827`  
		Last Modified: Thu, 11 Jun 2026 01:18:01 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fd342324958e268f51ed965fc7cc835016f19e1babc002d26399a71bea193073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44015c83908e3b6a28e0f158ba81b3f4ac9573418f2138ff2792a36c58839fc`

```dockerfile
```

-	Layers:
	-	`sha256:3f4c8e00df109b9ad9b71754fd2b221ca3fd6c42852eb88e1c1c104aaee95e8c`  
		Last Modified: Thu, 11 Jun 2026 01:18:01 GMT  
		Size: 3.8 MB (3835712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66db7838baf79b2b80a71c8f12b2c9d768da14a93bb2b8b88bf6b0581c090354`  
		Last Modified: Thu, 11 Jun 2026 01:18:01 GMT  
		Size: 16.5 KB (16518 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0d506670d3f536bc41f9c035697a26f9be0ddeeeb1788d00d721c29bc15b1b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215326448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991a2fecb89d21c5268ea4cba3680278f0f6689cf55eae8b83eb539b631b56fb`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:21:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:21:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:21:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:21:25 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:21:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:21:25 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:21:42 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:21:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:21:42 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:21:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:21:44 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19078219ccef24b3f447ede802289597acc059ab9e91d0d7ab43b1cfb004476`  
		Last Modified: Thu, 11 Jun 2026 01:22:03 GMT  
		Size: 142.6 MB (142582231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaee5e95b4f9bb7129dc737328ed48dfb263d2f7f43dee806750e73506e6b7b9`  
		Last Modified: Thu, 11 Jun 2026 01:22:01 GMT  
		Size: 18.5 MB (18548270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58783d0503950bb8f61d4470a3f00ab10cf2781cb05f333b589dfa2cb462ebe9`  
		Last Modified: Thu, 11 Jun 2026 01:22:00 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c3f40b3b126a206d23ea61122f66ab1854bab3a2cbd67a31b5d66171c88be642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04707c743530065824d5b7917ab70b94ae54d1d21f633e1abfe382c372df6c3`

```dockerfile
```

-	Layers:
	-	`sha256:a06e1345bc869b0ea8fa201cbeadb97cccd7723a59dfb32605f48b59bb6350ff`  
		Last Modified: Thu, 11 Jun 2026 01:22:00 GMT  
		Size: 3.8 MB (3836570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fdcf1ca3cffe2e435f28f3f8a766cc4996056a6ccb86ec01d85ed9be96e1672`  
		Last Modified: Thu, 11 Jun 2026 01:22:00 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:29d828ca3182cfa4c934374110ab1c5747f2879e8e43a6889f15f8a3dc150156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.4 MB (209405020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812c27f68d4fc035ea3a464658334edb1820fb6ded07d90ebe7e41e9de87e620`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 05:49:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:49:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:49:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:49:47 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 05:49:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 05:49:47 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:50:21 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 05:50:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 05:50:21 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 05:50:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 05:50:33 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9fef26d6c90c0453bfba8b1ff5cca1a32387bdf0466d3503a6eea28f899b8`  
		Last Modified: Wed, 20 May 2026 05:51:10 GMT  
		Size: 133.1 MB (133110168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987e692c777195f931ded0b2407b915117dfefbe13e0d6b16f39ea21eedb7a2c`  
		Last Modified: Wed, 20 May 2026 05:51:07 GMT  
		Size: 18.6 MB (18644894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9036bd6bffa12e51f0a2628888192c6aa0dca78b41b16e3eac7877a4136119bf`  
		Last Modified: Wed, 20 May 2026 05:51:06 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:74aa86ca9cb8a3e838e7f7c1a6c96305dc1eabc541835cdd3f2e0a38be4cb4a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd67aa501b5c816b96da49208244c201d47abd36dcdfbc19bdf21a18419a6d0`

```dockerfile
```

-	Layers:
	-	`sha256:5e618716be01c6749820017a51cccde853982818677ced544f1c8c47ec7812f6`  
		Last Modified: Wed, 20 May 2026 05:51:06 GMT  
		Size: 3.8 MB (3836097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db49dc8e7b85686b2fb7b2e8a010444b6421041ee4a0712c90797c6b66a0d997`  
		Last Modified: Wed, 20 May 2026 05:51:06 GMT  
		Size: 16.6 KB (16562 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:2ae4c2b3d6b09e890f8236e485b0e08238b0aaecf724b84aac7822b05d731f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199186473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ae08984aba72b94a5197577aa83ebb7aaaee32b8f0d9f0fba69ff0d3e42073`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:06:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:06:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:06:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:06:55 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 03:06:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 03:06:55 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:07:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 03:07:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 03:07:11 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 03:07:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 03:07:14 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c97d8205f9a0577392faa69937ce07f45a0f333503df39ff6079a7df8f8d98`  
		Last Modified: Thu, 11 Jun 2026 03:07:40 GMT  
		Size: 126.7 MB (126651735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb671cc6cd1e5eeff711df16572f8f07ed82151b7d3daf7bc0d59109e87c6d7d`  
		Last Modified: Thu, 11 Jun 2026 03:07:38 GMT  
		Size: 18.6 MB (18631059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91be9fc288cd3d570248c3a93a41fbac888f887e8781742678089d76a8f50f5f`  
		Last Modified: Thu, 11 Jun 2026 03:07:37 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:195f77e20c239e3862c430b7c2fa70ee1cf889722a302057261e84ad13d39d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3848661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c1acadaecb4b35165e3b1fa13a21d7e440e0c338f137878b432d6e56b0cd06`

```dockerfile
```

-	Layers:
	-	`sha256:b9ac518bd0b595b493cb3dbd0b191e34f77c5fbb35c83db57de51e8f77677076`  
		Last Modified: Thu, 11 Jun 2026 03:07:37 GMT  
		Size: 3.8 MB (3832143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbce2eb5fe626100754e3c12623ac1971dc16debddc115c2ac6d1600f8acb3f6`  
		Last Modified: Thu, 11 Jun 2026 03:07:37 GMT  
		Size: 16.5 KB (16518 bytes)  
		MIME: application/vnd.in-toto+json
