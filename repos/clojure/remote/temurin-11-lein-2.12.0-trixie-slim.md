## `clojure:temurin-11-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:f4f383aa9378cd19dc5204c03c0368f0df4a76efee3e0f9e8be6f958f30282de
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

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1cf47d4853f93100c5b9d2570f4755fcfea2e72b3ece2329017d90e9f664a857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196632081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8f7c68f7980b2ea43b4eb5ffdba2a0a70aa7ba6310ecb3adb0b3eefa91b174`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:57:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:57:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:57:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:57:37 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:57:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:57:37 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:57:53 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 19 May 2026 23:57:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 May 2026 23:57:53 GMT
ENV LEIN_ROOT=1
# Tue, 19 May 2026 23:57:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 19 May 2026 23:57:55 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7bd793f845ad9348e8d7d52affb46dc767f34fd723843ba36129ab29187251`  
		Last Modified: Tue, 19 May 2026 23:58:14 GMT  
		Size: 145.9 MB (145886201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617acaaf8d79126d81272e47e20ff4a6a3d09289610ad33f46e6de705b686d20`  
		Last Modified: Tue, 19 May 2026 23:58:11 GMT  
		Size: 16.4 MB (16448170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31747e5374ad0e9deb6fc1398718e69c7a6f8c6dad920f44e8e1f9fe59441d7`  
		Last Modified: Tue, 19 May 2026 23:58:10 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:94d317e32f103adee007a2b97d7330b0404b5e0bf90751f51766e6078661bad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a76e71049617bfa89634ef810f7ad54b2374d0d77bf182a6f1a0c2026f0db1`

```dockerfile
```

-	Layers:
	-	`sha256:37d0e4ab57115c67baa5e5cfc4a68645ecaaba82e31e49b4d747685e6e3180df`  
		Last Modified: Tue, 19 May 2026 23:58:10 GMT  
		Size: 2.4 MB (2384973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5665b1d9e49297b5ce9f01da06ce2f4288b86df0d8a87e9e49da4e224af28fb`  
		Last Modified: Tue, 19 May 2026 23:58:10 GMT  
		Size: 16.5 KB (16548 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f17d28c0dde1f26295d3c73366cc7e77ae86b5a79c4672787886c277f3f0629d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193656125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6bc9b0c076c3813f44e2ea44567a657ed53f96f2e84997acce9af6d66cb101`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:04:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:04:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:04:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:04:38 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:04:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:04:38 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:04:53 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:04:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:04:53 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:04:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:04:55 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725ae0c5aef96817122bcecd9b790f02a5d70ded02a22fbfc6e5dcefc13ecdb7`  
		Last Modified: Wed, 20 May 2026 00:05:14 GMT  
		Size: 142.6 MB (142582234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e64bc455e7e287997bb66b4f49c17713e04f338e16060b21eca49db33622d5`  
		Last Modified: Wed, 20 May 2026 00:05:11 GMT  
		Size: 16.4 MB (16414222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7850707cbd33bf1503c6881fc6bebf409e12c46f8fab35fc746a895d3fc0437`  
		Last Modified: Wed, 20 May 2026 00:05:11 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:14924ac7c929ef9471a23374eee5468cf2b9ee26fa254c7ec3d0104f7b363519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c931a3a5934701265c1544713c7b883e772e52fa329af78f9488034bfc232d`

```dockerfile
```

-	Layers:
	-	`sha256:00090b3bb93ce1cb2898757c9df739560ca80fb7920faf551386a878cd2e3e85`  
		Last Modified: Wed, 20 May 2026 00:05:11 GMT  
		Size: 2.4 MB (2385201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0d086ff0a532446ebdaf5bc47bd787dae3c12e5e0ea6e57e4066e56f04e2f4`  
		Last Modified: Wed, 20 May 2026 00:05:10 GMT  
		Size: 16.7 KB (16668 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:9d453d66a0e6a739b38a358956bbcf561b65b6a30298250a29296481b6e6ad97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187714477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd44b82efa1cfaec24d98fab1cb10e9077a6fd8b686bead8349490cc0855e67`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 05:50:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:50:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:50:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:50:03 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 05:50:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 05:50:04 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:50:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 05:50:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 05:50:33 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 05:50:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 05:50:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af1c2a52fcf12729088136b65ef4038671f55a12f26a215e7c24989df640e8d`  
		Last Modified: Wed, 20 May 2026 05:51:10 GMT  
		Size: 133.1 MB (133110217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d6085acd4bb7957d5c54ca9c0a984b94b69e82e9045d8ec382493b313ef6f6`  
		Last Modified: Wed, 20 May 2026 05:51:07 GMT  
		Size: 16.5 MB (16486034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead507e441c2ed55e0d72b8ccbca89fb3e85ae3c97bc56fd95f505d99fed31a9`  
		Last Modified: Wed, 20 May 2026 05:51:06 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0740f5cf218645879db78b620c4859330fb760ee50f1ee5f02e8ac1dbd7f09df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68266358d307cd5db828f0fc17bc4ac0ddf8b5655832268e7a9d6b3938444d7a`

```dockerfile
```

-	Layers:
	-	`sha256:4f4db4f30794c5137e3daa86469a16ac6e33d0c1dbede12cffd344a0ff891959`  
		Last Modified: Wed, 20 May 2026 05:51:06 GMT  
		Size: 2.4 MB (2385338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a4837165d53fc432c6a42cfd134c1ad75c3afb8eb7ccdc05fcc4bdba1aae2ab`  
		Last Modified: Wed, 20 May 2026 05:51:05 GMT  
		Size: 16.6 KB (16592 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:3846517de4f35439c5c18f74a65a544dac8488a239c92fff699050b0a3e79892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177499532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752a5f7e9cfaa75f8ccd194bb21c3936ad0eafaeb5d6bf1678a3791ba0b05caf`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:42:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:42:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:42:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:42:01 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 01:42:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 01:42:01 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:42:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 01:42:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 01:42:18 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 01:42:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 01:42:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0389166517857b01275246c592e1b1023d8f38bd4a17cfadfd10346a353b496e`  
		Last Modified: Wed, 20 May 2026 01:42:44 GMT  
		Size: 126.7 MB (126651734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bf0c2d6cda57e112b24fb0fc0dc60c9c4d48c727aa80094b187586d072e6ef`  
		Last Modified: Wed, 20 May 2026 01:42:42 GMT  
		Size: 16.5 MB (16484112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af71c66f466e6056588c8558fe02d543729f24c25cc280f57a516b66198af5e5`  
		Last Modified: Wed, 20 May 2026 01:42:42 GMT  
		Size: 4.5 MB (4517730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9b5f3d4fc8160448fffce7b11b19ff69eb34878c3dc191567801dee0e45cb592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfea4c0e5be635459cca8fc7e54b56123186e4a0bfa06d6d9f022573019be0b9`

```dockerfile
```

-	Layers:
	-	`sha256:f130bad3d2637764d44d71c04bad7a313cc486c2d5f0712889865b08dfa764c6`  
		Last Modified: Wed, 20 May 2026 01:42:42 GMT  
		Size: 2.4 MB (2381404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9ec42cfc5f25a727dda704065e39214578ae3b8f819ad48dc23c91b2772e162`  
		Last Modified: Wed, 20 May 2026 01:42:42 GMT  
		Size: 16.5 KB (16548 bytes)  
		MIME: application/vnd.in-toto+json
