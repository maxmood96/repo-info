## `clojure:temurin-25-lein-trixie`

```console
$ docker pull clojure@sha256:4c68c211590e299e030812cc7b5c9fc296cc3fd94366665462330190eb94dc4d
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

### `clojure:temurin-25-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:baacd64c5e152d28fc3582a8914f23aacf8c7cfebae9b08930006ee18427c6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164647599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22375a520632574cc569567abdbc9b5c8492bf5ea247127beaa7cc217aa9994`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:57:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:57:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:57:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:57:07 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:57:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:57:07 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:57:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:57:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:57:24 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:57:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:57:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:57:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:57:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bdaa5ae7f8607c3b0f2f20a05eb7deeb64caa1874f569103af7825749c2e4a`  
		Last Modified: Tue, 24 Feb 2026 19:57:44 GMT  
		Size: 92.3 MB (92256297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20a3ac59aeb52f777933f7442efdf773c4b3d5972065566e760c128d86f7bbf`  
		Last Modified: Tue, 24 Feb 2026 19:57:42 GMT  
		Size: 18.6 MB (18580041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02898894494a2e641a9f61046d17c7573460d1def07371538c496f9757df3e3`  
		Last Modified: Tue, 24 Feb 2026 19:57:42 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32d5bb3f31a565e9baba53f659530cd5a0811c0df3dd8b16f16e5cc5f1abd24`  
		Last Modified: Tue, 24 Feb 2026 19:57:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:61b00e72c3fd022abc9f9f0bb6480da004c5172f863b2902b297a0b0e5c90649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3802502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6095de46af9b2d34e23029624cde3238c4cb3e21f58cbca59327e65f23586435`

```dockerfile
```

-	Layers:
	-	`sha256:84b528fe85fd264e076fc99b35a0a4ac7ea5ff51e5314b02a2134a6e1eeb98fb`  
		Last Modified: Tue, 24 Feb 2026 19:57:42 GMT  
		Size: 3.8 MB (3783523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb3ad4cc7d04a700354beb586cdc5e72dce9703e3cb78005f01cfcac5d143201`  
		Last Modified: Tue, 24 Feb 2026 19:57:41 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a6162ece27c1cbdec71e4d15979748ddc31e8407046cdeefd505a5d4d21b36cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164000066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547cd2cfdc42d24ae0f7a1379bf40107d32577f25b32d0b5a4f2020a7d7a4767`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:07:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:07:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:07:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:07:36 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:07:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:07:36 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:07:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:07:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:07:53 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:07:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:07:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:07:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:07:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6d0193859402b46e871b8e097f8c9cd87d98e701d50734e47de49502b6e828`  
		Last Modified: Tue, 24 Feb 2026 20:08:13 GMT  
		Size: 91.3 MB (91288263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652fc95e87473cdeb7fc6dc2818c197f03b146e699f9f21672ffc9b48973ea37`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 18.5 MB (18541462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6231906259dbaa6120ab704bbf9e36c3f8c41d8528c18e023a77dc0c20dc8dd9`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b5bc2163fd53455af236d089700d9d7f74a9aa81b57edda5384f6f218ffbf5`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b835058b5c2114132cc9bdcab52499f6af11fc8b7b49e9b5d595e53728f5f205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5150305f75ef6c99006a59b8cb8ad5c075dc3d3feb31b0c38505cda2cf728cb4`

```dockerfile
```

-	Layers:
	-	`sha256:a3f288c7ca7c2a00d9f7b923e766c8014cc3df18185bb6be62ed9c7d5f249fa1`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 3.8 MB (3784421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4c9136a44a604d9e27cc26de29c69f891297e4969bda23b7e2fdda32c0dfd87`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 19.1 KB (19124 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:67454ff47120ee0b108adf09d409e7a46ac3eb53d03debb4a5cdfb1b32013442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167900700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79acb1409382f4e9e8c2853db63119abfb3e217faaa1286e0c21c5b4db610f2d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:48:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:48:05 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 06 Feb 2026 00:48:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 06 Feb 2026 00:48:08 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:48:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 06 Feb 2026 00:48:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 06 Feb 2026 00:48:59 GMT
ENV LEIN_ROOT=1
# Fri, 06 Feb 2026 00:49:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Feb 2026 00:49:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:49:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:49:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3230ebb877a1444adbcad5521afaffb1c41773004c4324fe65c2c551a9cc1544`  
		Last Modified: Fri, 06 Feb 2026 00:50:07 GMT  
		Size: 91.6 MB (91632873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3592aef72592656244b79421c8d2881c7ab4347c4dae6ce8aa981feb882d243b`  
		Last Modified: Fri, 06 Feb 2026 00:50:05 GMT  
		Size: 18.6 MB (18637526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587ba20bb2ee02d46106a001def44a07dbb7cabaa6022d338c73fe3b855b3852`  
		Last Modified: Fri, 06 Feb 2026 00:50:05 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa996e2b368b508e8135f75a167c37d450e8907d36fd8f22e066feb03ed873a`  
		Last Modified: Fri, 06 Feb 2026 00:50:04 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8f4597096230f9e24ab70aada22493ac548b8bcb75d27ee48192cf965aaabf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f707393f9d081bee2b320dda6671e47b52211c15747b1ac561578a0c0f622df`

```dockerfile
```

-	Layers:
	-	`sha256:38d1bffe3dcc6f64365a775eaa15cae474b67cad360b59879d3274dc7f59cdeb`  
		Last Modified: Wed, 18 Feb 2026 00:04:21 GMT  
		Size: 3.8 MB (3767847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:099a59b2a1d20ad099181ec0bf05a60dd3c2af5f1b868f6f33d424d7f73a69aa`  
		Last Modified: Wed, 18 Feb 2026 00:04:21 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:6936cdcf8c4843c1f70d8bcd100bc8f7ffd015b4f30bfeaa136a23c818bccc6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161600266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482a82f70071da5da9a76115ea6cfca465a52576b121e785e7d6c475cd309a83`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Wed, 18 Feb 2026 11:49:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 11:49:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 18 Feb 2026 11:49:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 11:49:18 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 18 Feb 2026 11:49:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 18 Feb 2026 11:49:18 GMT
WORKDIR /tmp
# Wed, 18 Feb 2026 13:12:16 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 18 Feb 2026 13:12:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 18 Feb 2026 13:12:16 GMT
ENV LEIN_ROOT=1
# Wed, 18 Feb 2026 13:12:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 18 Feb 2026 13:12:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 18 Feb 2026 13:12:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 18 Feb 2026 13:12:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0c08292c273f6fa94290477f212196176e148c5443e72d590aa78d4b504c5d`  
		Last Modified: Wed, 18 Feb 2026 11:56:49 GMT  
		Size: 90.8 MB (90773425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a4fa34c44266bcdaa95e9c003ce6ac0f425d8ea75ef6bd3f09ef4ebe3d9fdf`  
		Last Modified: Wed, 18 Feb 2026 13:14:40 GMT  
		Size: 18.5 MB (18531846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75f81327f9103dbf75d53c2ad906b5f23c7c7a10107ce723b7c30710de3dc37`  
		Last Modified: Wed, 18 Feb 2026 13:14:38 GMT  
		Size: 4.5 MB (4517802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be28f227f700a214e6fe2974d5854a553ddc1eaa32609a87490a8a181931345`  
		Last Modified: Wed, 18 Feb 2026 13:14:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:65aeaff25c6b4a3ecdfa0b88bc653e4a9073d333e5bb7538b72044bdbed26c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e7974411bce539459c68db9afec592eb7524dc7308db3d8b7fb28bedb15f1f`

```dockerfile
```

-	Layers:
	-	`sha256:ea81b455fe7f324d5b676e9939a09c4a0dd5c536eb253b15f8bb7996c5d8c147`  
		Last Modified: Wed, 18 Feb 2026 13:14:38 GMT  
		Size: 3.8 MB (3756023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38761fda52b42e86c41b119ad66b816a6eef4a240017307c7ec30199683d9533`  
		Last Modified: Wed, 18 Feb 2026 13:14:36 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:c8be8a4be721928d325989834758387fe124ba32af647437d074bb02679d21d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160727724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19043f8290467573878ffc1718685e450685417320464ee6e57459512c2158cd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:24:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:24:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:24:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:24:44 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:24:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:24:45 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:25:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:25:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:25:23 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:25:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:25:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:25:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:25:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17752fdef1f284b40fe320bd54d7f9eefb1972a0ccd86993bc2287b508f560f7`  
		Last Modified: Tue, 24 Feb 2026 23:25:51 GMT  
		Size: 88.2 MB (88233869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416ff14df2418c67019f78a6065974f59167588791b663e1b60ac7ddd8336346`  
		Last Modified: Tue, 24 Feb 2026 23:26:01 GMT  
		Size: 18.6 MB (18621168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd0470f13c36090d6b19a2be41f7d76133e9d24e93b5ca2a7ed7d6fbcdf81ed`  
		Last Modified: Tue, 24 Feb 2026 23:26:00 GMT  
		Size: 4.5 MB (4517724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0074f8cc737ff967b181856c175defe55ea6cc3c60efe7716abf5ac74478de64`  
		Last Modified: Tue, 24 Feb 2026 23:26:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c5b49e5d410b9ddf026f832a74a3466303c7e81709ec5d79e8e3d5ace80482a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6043172e49664f88e5891ce424dc0ebea02852952a3910ed3ef5c2cd92a15fb`

```dockerfile
```

-	Layers:
	-	`sha256:d7ac437f3ead469e8bdee12903afcc8a026662090f5497083c3ef496461a22c2`  
		Last Modified: Tue, 24 Feb 2026 23:26:00 GMT  
		Size: 3.8 MB (3764512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b0fdbc916e48e3b3b9bca8cd1eaaac1c4360ce81267b8366b88e6377d3c0c8e`  
		Last Modified: Tue, 24 Feb 2026 23:25:59 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json
