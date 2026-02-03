## `clojure:temurin-17-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:99ace9f553b630bb13e8db85fa75d97cb4a96daafadac700a5e569634e287d97
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

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:86385e2ae034d7996a56ab3b49b0dbcf1960372034b1861066118159a42c8e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217650440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b75aed4f9a6eb245df4638ba3e299748fa449d7932ffeab921b10e507d3ef0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:20:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:04 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:20:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:20:04 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:20:21 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:20:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:20:21 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:20:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:20:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:20:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:20:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf439f6c7d53fe038c5edcea978da32848e4cfcc244bd5650a21811a74a65f35`  
		Last Modified: Tue, 03 Feb 2026 03:20:47 GMT  
		Size: 144.8 MB (144847923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a161d1ec73582552b706297b436e259714a54811de25da2a5825272273e1aa4`  
		Last Modified: Tue, 03 Feb 2026 03:20:45 GMT  
		Size: 19.8 MB (19802881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9d2db3c4be36b8300f86ee4fc9383defe682d3aed82b936d0ad02213a4f289`  
		Last Modified: Tue, 03 Feb 2026 03:20:44 GMT  
		Size: 4.5 MB (4517723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a9951fa937eaaa7386acfc59c171bad260c6800db7e9542ca4fc8599298350`  
		Last Modified: Tue, 03 Feb 2026 03:20:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:54548a1b26f14538ee5aca54efd4c045589632fef1da5e077cea83915100c1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4298846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9833208fabdc2a771197a0ca12316f832f3943015935475b8e91c08e5ff74330`

```dockerfile
```

-	Layers:
	-	`sha256:16143e1513722c2f0faf9173eeaa89d97326871da5b29e12424ca5d7c589c16d`  
		Last Modified: Tue, 03 Feb 2026 03:20:44 GMT  
		Size: 4.3 MB (4280479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1edcdd869134ef0531e0dc274d5c40c861d88f1ac16630a02edd62f4c24b8490`  
		Last Modified: Tue, 03 Feb 2026 03:20:44 GMT  
		Size: 18.4 KB (18367 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:edfc96848a5b872e16b20a49e86eeb8f58c721d7d3b03e1950a2ba74b8c2cc59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216196942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c503cc0e6a5280e4a0994cdcc554bc5edb93902e79064ad2bbad38c00ef31`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:22:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:35 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:22:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:22:35 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:50 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:22:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:22:50 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:22:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:22:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:22:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:22:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d32482ecdad16f6ca45a1dd00258d92493cf18c1148da1032aae80fbaa11e4`  
		Last Modified: Tue, 03 Feb 2026 03:23:12 GMT  
		Size: 143.7 MB (143679933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f76556496e0090ccd97ea68150f8a47f66731346e69d4815e442035775dad18`  
		Last Modified: Tue, 03 Feb 2026 03:23:10 GMT  
		Size: 19.6 MB (19632874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59db04b5ea23b3546fc8a71f395b34a79f88a05b9d82e29d74980b6931dc3061`  
		Last Modified: Tue, 03 Feb 2026 03:23:09 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a39f50f1dbd674f63a3a3df03a39b6487f6ba518eb5508ca128a2f72dd9953a`  
		Last Modified: Tue, 03 Feb 2026 03:23:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:37ef3433d403591cab9b3fd4c35ee91874b996c8bac0c302cce86a5abf9449c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4298583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de435c049ec6682bd313424acaf24e44ccf0cb8ea6a36f87ea614298a8f740e8`

```dockerfile
```

-	Layers:
	-	`sha256:3af69834a279ac9a656ec3cedb022bb3012d818ac76af9d6d6ded16401600d81`  
		Last Modified: Tue, 03 Feb 2026 03:23:09 GMT  
		Size: 4.3 MB (4280094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd5b2705c7742ed42fe89694dcb32aed899cf74b3738cf91666605a01191ae01`  
		Last Modified: Tue, 03 Feb 2026 03:23:09 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:30993d1d6eace8114af60fd385d5ba5751685e6e83ca4f7ea74778cb9af43ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221393878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cdaeece69a98d119f8f7824e3afe56e1083397b6ab63a8a7babd08bec57aa2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 09:40:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:40:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:40:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:40:11 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 09:40:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 09:40:11 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:40:46 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 09:40:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 09:40:46 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 09:40:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 09:40:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 09:40:50 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 09:40:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd550e5f8ece35827a8b1eb152f6b31f524a10742630dd50d90839282e1353f`  
		Last Modified: Tue, 03 Feb 2026 09:41:32 GMT  
		Size: 144.5 MB (144524718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1ab9a1f9d9435694ec24f9f4c33861f7ef2d27b52477fbf08d20a07a5aa159`  
		Last Modified: Tue, 03 Feb 2026 09:41:29 GMT  
		Size: 20.0 MB (20023724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47d1dd162b5add5a659d7cbc9d8c6e359b85ac1e7c99314900dcec8068a6d41`  
		Last Modified: Tue, 03 Feb 2026 09:41:28 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f528f1a373e2debaa86bc2f14cac7780cbe3f7fd2ea7be146c6be152476e1a`  
		Last Modified: Tue, 03 Feb 2026 09:41:28 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9d858c6274e3e9e071f7b570a0347bf11d72df373e40ffa471a8d463deb9ffd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3042483a1e5c53a9783105c6038f568ad11f4a564ab7637f95cf291a4de935fd`

```dockerfile
```

-	Layers:
	-	`sha256:615e0a025ca6aeca1fb17bc78f8a0b80bec8fd0ec0a0230c907d66f1bbdc469f`  
		Last Modified: Tue, 03 Feb 2026 09:41:28 GMT  
		Size: 4.3 MB (4282340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c851255edbad566554b92e785af2abd987fe3479de6206b9961e3ce21b20b58f`  
		Last Modified: Tue, 03 Feb 2026 09:41:28 GMT  
		Size: 18.4 KB (18411 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:8664d986c80f05f42c20bc987baf21863e547f57a47f0df755eb11d878621dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205979401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46242ef148712d05695f3b09abf424e7460bfd11ae796c5ac9e8d526129c0f34`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:01:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:01:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:01:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:01:48 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 05:01:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 05:01:48 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:01:58 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 05:01:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 05:01:58 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 05:02:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 05:02:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:02:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:02:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4faed5ad2aeef46262b9c59020e76ce12e2c432bdaf6860f05929430b5ffa9`  
		Last Modified: Tue, 03 Feb 2026 05:02:27 GMT  
		Size: 134.9 MB (134859780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030683c3ab7fdf88250931deeafd686a83a82d4ef7b1858357ce90dc3b1a1d07`  
		Last Modified: Tue, 03 Feb 2026 05:02:26 GMT  
		Size: 19.5 MB (19463112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae61e35f51005b9092a81e36f43eb9e9b8be1845807a6ce1323e4022e50d489`  
		Last Modified: Tue, 03 Feb 2026 05:02:25 GMT  
		Size: 4.5 MB (4517736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0883da3c8ea84cd55a8eaa4db81649c838ad48597cd3de76426d503763a47d00`  
		Last Modified: Tue, 03 Feb 2026 05:02:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:818fd70951b9ebe03b0543a701f209b94c39d37007429a7cc82488e26c7d1f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4290661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95efd14fb5be2b197b567c32df1d2f8e4953388ce968d3de3749b267ae94dddd`

```dockerfile
```

-	Layers:
	-	`sha256:559527b76ee3cd76bd7f2cd6b178509d8f31f2fc113a8cb0016ba22873640a2a`  
		Last Modified: Tue, 03 Feb 2026 05:02:25 GMT  
		Size: 4.3 MB (4272293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d1e34af8f007975fcd13c650287b779d90cff861131ee69757219b08f216c2`  
		Last Modified: Tue, 03 Feb 2026 05:02:24 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json
