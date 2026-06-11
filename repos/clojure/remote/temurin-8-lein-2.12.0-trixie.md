## `clojure:temurin-8-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:e2590f24be8f7baf23fcbf2dab8ab64c6ff0178aee51e57125f0b61c627d9ba5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:438cc7f4cb95d68145f742efd10e06f26837bdaf8dbe9a4c04145d4ead85df1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127623647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f63d62843189324182837e823a5e286bd9fdcecb38f9a82e50270f8232b1a1`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:15:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:15:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:15:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:15:47 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:15:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:15:47 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:16:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:16:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:16:03 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:16:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:16:05 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f2a10c9e0919873abfc77c653c59aa5a1108b87f890949c154f54dd1d3c5ce`  
		Last Modified: Thu, 11 Jun 2026 01:16:19 GMT  
		Size: 55.2 MB (55198716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e187901bd2868642b596c5cc91dee65dac533d5934c490aae03710bfbdfb0cec`  
		Last Modified: Thu, 11 Jun 2026 01:16:18 GMT  
		Size: 18.6 MB (18590020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6694ac9f5de4b68e516a623852e55a8b4e5899300f6bf494f3bb793feae470`  
		Last Modified: Thu, 11 Jun 2026 01:16:17 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:db7e2b074d08a10babc9a4c562d0dbba42044962547856a890fe3beba1ab68d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec1bdaff3951722247418f1bafa69d1e9e548e079ed5217ef49337c1817ff9f`

```dockerfile
```

-	Layers:
	-	`sha256:7130eb241e18ee9c32c5d81413ba151f5e96ce412143e01db734658c78b1f9e5`  
		Last Modified: Thu, 11 Jun 2026 01:16:17 GMT  
		Size: 3.9 MB (3936558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef0d0c49d5481736ccf4728c3f03ccfa258822a095d030afa19dcf162c2fb857`  
		Last Modified: Thu, 11 Jun 2026 01:16:17 GMT  
		Size: 16.5 KB (16505 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b4043f20ebe6de63ea81a48e207e8bd4687c40e697ebd74ef8202459865e943f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127017113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7608afbb2c80e9d6c2c9ef9df69298046a2f88bdde6b0604b61c8a30ef42c39`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:19:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:19:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:19:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:19:53 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:19:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:19:53 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:20:09 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:20:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:20:09 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:20:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:20:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63d7f1ce31d05a62238525ce8cf3ea30d1cbab129a966e41e305b63e1d63390`  
		Last Modified: Thu, 11 Jun 2026 01:20:24 GMT  
		Size: 54.3 MB (54272927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b8d2bb124ee5033fabe9a3a5622afc4c20a05c3ae3bf5386605fb1e4f96424`  
		Last Modified: Thu, 11 Jun 2026 01:20:23 GMT  
		Size: 18.5 MB (18548235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09aad5f07f3dc819d57a16fd70d75eebb9471c37d321fc3c23443700c39de7be`  
		Last Modified: Thu, 11 Jun 2026 01:20:23 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a8c5c7345de45ffa6227eee6a97706e6d10f101509ff811dcffc961da809f9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025cbf2f81010abfb7ac459ac258b83aa3b692bca54765cc0c7a98d52ee140d3`

```dockerfile
```

-	Layers:
	-	`sha256:4d060d0e868d2011672a8d0cf8ab60bfac166414119786c2502d67e348348560`  
		Last Modified: Thu, 11 Jun 2026 01:20:23 GMT  
		Size: 3.9 MB (3937498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bf18222801a439748ac30b4cdfad550390e0ff08abbfa91926a4629da8c5ed5`  
		Last Modified: Thu, 11 Jun 2026 01:20:23 GMT  
		Size: 16.6 KB (16626 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d671cb0949dce2e92462b42bcafc514c65636d79c3df8d046a84036b2235f127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (128970019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9dd7be025daaccab0c8180a6dd8e3b05089c617e302e7e58cb549f8de02f68`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 09:17:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:17:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:17:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:17:18 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 09:17:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 09:17:18 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:17:57 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 09:17:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 09:17:57 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 09:18:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 09:18:01 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf754746c3f17631e9d8f036f4e175f1bd71812587b986fa8fc268bafa219a2`  
		Last Modified: Thu, 11 Jun 2026 09:18:32 GMT  
		Size: 52.7 MB (52669138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9637d5fc1625a5dc70e4b0e3e1caed0bc644dae4677fde1bac0ace095ec3a0f8`  
		Last Modified: Thu, 11 Jun 2026 09:18:31 GMT  
		Size: 18.6 MB (18645203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9a5bbabe4c3283d477cf5555aae6f201af41aefd67fb10efe8fb840161c1e1`  
		Last Modified: Thu, 11 Jun 2026 09:18:30 GMT  
		Size: 4.5 MB (4517707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ee5624e35ee3287bea18df7ea3931032af21174299bb367dcdd756b08a0e8a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c58b363a5ec76363e2ca41311e3b961ad8100b5aa98bac83543c27c03da5ce`

```dockerfile
```

-	Layers:
	-	`sha256:56214e4549055b6e9f825f1a91c579c3298182ca9ab317de1320e6b35c7d0c6c`  
		Last Modified: Thu, 11 Jun 2026 09:18:30 GMT  
		Size: 3.9 MB (3938153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96c8cdc6fad6a70682e6155a2fc4a186f8f4582772558ef6c4250d0199c1ef55`  
		Last Modified: Thu, 11 Jun 2026 09:18:29 GMT  
		Size: 16.6 KB (16550 bytes)  
		MIME: application/vnd.in-toto+json
