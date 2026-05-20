## `clojure:temurin-11-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:ed846bee0e55fbcdceee97aa383ebb553dfe15fe50d9cf5f4a58f61a42509eaa
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
$ docker pull clojure@sha256:15f289babd75e537afec24f5a2584a96bebe191817efecef06728e033d5db268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187711421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb483f5993489d8f7a9d5531f84011df4ddf7dd11bef58b97b84d594e68523a7`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:26:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:26:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:26:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:26:45 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 09 May 2026 02:26:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 09 May 2026 02:26:45 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:27:14 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 09 May 2026 02:27:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 May 2026 02:27:14 GMT
ENV LEIN_ROOT=1
# Sat, 09 May 2026 02:27:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 09 May 2026 02:27:17 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96ee5b4d347c9b3ee6f86dcde18c044f7ee128c0ca544845fafbcc3bad0c1c3`  
		Last Modified: Sat, 09 May 2026 02:27:49 GMT  
		Size: 133.1 MB (133110179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daa56591d79e5c01ecb59be4d30a0d22893c0cdc7829f7fb3e92f5f7e8b9fc8`  
		Last Modified: Sat, 09 May 2026 02:27:46 GMT  
		Size: 16.5 MB (16485372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f835c50c63e233d03dd35beceacb1874e51b5d09610b101dcfc1623c186c78de`  
		Last Modified: Sat, 09 May 2026 02:27:45 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:58e7509679ad7a9b6c2e873e04dbf8880f76c1029eb107e24a5677a7106d6dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d2e0837e2556c79bc69cf6e0db5fc495c4e3a34c2601e5aaaaeef979a29da8`

```dockerfile
```

-	Layers:
	-	`sha256:7d5b47921ede1faa5daa49c28ea7dd9140b5f00070472f21a07def4b99fb8ce9`  
		Last Modified: Sat, 09 May 2026 02:27:45 GMT  
		Size: 2.4 MB (2385296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2d8851359fc394a7a43a0fe7d5765a50241f2d40f09b8c7e787b6b2ac33c467`  
		Last Modified: Sat, 09 May 2026 02:27:45 GMT  
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
