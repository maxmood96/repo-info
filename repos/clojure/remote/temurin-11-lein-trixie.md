## `clojure:temurin-11-lein-trixie`

```console
$ docker pull clojure@sha256:d0bdc7d0d956d4412e0e675f70705cd2c83d623ca17cc91d3c143c14b36624c3
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
$ docker pull clojure@sha256:91cdea980b49393c158f24109939ec8ad2bdd00aaf853681ad8edd5f9af9eb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218207327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedf746fd15f7aa9fbe553f2b19b079a4264feadc12d68983e6f623577b54b77`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 02:57:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:57:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:57:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:57:07 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 02:57:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 02:57:07 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:57:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 02:57:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 02:57:24 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 02:57:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 02:57:25 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d1c5b6757ae07bc6f88f6a73243177a66e1e9f32adbdc0aef38ceaa2a5179a`  
		Last Modified: Tue, 17 Mar 2026 02:57:45 GMT  
		Size: 145.8 MB (145806904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bfda6bc8f2fab2bcd2d63f3b9c69c300a0b8f3c75f71fd9f6ac91ce871c505`  
		Last Modified: Tue, 17 Mar 2026 02:57:42 GMT  
		Size: 18.6 MB (18585150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e915b1f0859165bf151646ed00333c049a9305b3ad785ef32772e85381870a`  
		Last Modified: Tue, 17 Mar 2026 02:57:41 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bb9858441e9b0277cc1d21ff24a65d4d06563ac876b69cd823580e1e6181b5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb254d3527f677eb416efdd4480ba71281009cebffbaf296324245a20ae126f9`

```dockerfile
```

-	Layers:
	-	`sha256:0f8b10fbb7248bd0c6452f8ba9b80da5fe32456ac4aaf148405b6983d7ab9b34`  
		Last Modified: Tue, 17 Mar 2026 02:57:41 GMT  
		Size: 3.8 MB (3835668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:423a2e24157bd6970ad05d28888c70c5cc4c4f1cacffb175a8c7c4e6e18ac70d`  
		Last Modified: Tue, 17 Mar 2026 02:57:41 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ad4de3a1bd3d65b63d0b7fc99e3358e813e41270d7599cee059db2ed4d0d277f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.2 MB (215227474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3670df1cb36217737a7edaa8b2b90bd8db93c62ddd94c5078afa449faa63da`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:01:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:01:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:01:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:01:27 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:01:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:01:27 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:01:45 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:01:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:01:45 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:01:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:01:47 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30674b4d213807cc4aa75b2bb10735859edcae2c2ed428cf83e30ffbf9c50d18`  
		Last Modified: Tue, 17 Mar 2026 03:02:07 GMT  
		Size: 142.5 MB (142500035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cce3ce751ba9ae5eaca3fb359eda7424d6fef1c21f97c5df00de9d16efe55df`  
		Last Modified: Tue, 17 Mar 2026 03:02:04 GMT  
		Size: 18.5 MB (18544713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aa8e392f3132fa83c240b16640fddfe0f4751ffd3162058414965e5fa65ba9`  
		Last Modified: Tue, 17 Mar 2026 03:02:04 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:635cd2c95744f40b70bb535ef794b93be86d7cbc3599f3f24a0e1a40cfd60d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3082e77b03f26d192cbb3cbcedbfc1fb46673b99678fbe7067211c37b44d86f`

```dockerfile
```

-	Layers:
	-	`sha256:247b53e301ed4ae86523685b2e407c05e5508081c3b20ac4df999d2cae6889d3`  
		Last Modified: Tue, 17 Mar 2026 03:02:04 GMT  
		Size: 3.8 MB (3837163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bcb00982ae9e9fe168b2cb7347f48a45e63c859e98c8970bf36584439bcf8b9`  
		Last Modified: Tue, 17 Mar 2026 03:02:04 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:5559a63d07c6c4fc5a9833fa77c3dce98526142b183dab8d0b8d99638d93f23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.3 MB (209265442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf0fb920ccb7c0bbf2db274e4beef114de56a75604c3ec6de5c29f05f9dc1f0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 01:50:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:50:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:50:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:50:51 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 01:50:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 01:50:52 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:51:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 01:51:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 01:51:52 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 01:51:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 01:51:56 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd587e6f98d18981b1fa39b879e07792b8b34045978a1c4c5b8a1982d2ae24e7`  
		Last Modified: Wed, 25 Feb 2026 01:52:39 GMT  
		Size: 133.0 MB (132997811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eeae89419bda9d4065ade61895cffc8935cf4d7c520c2f6252996f0150d533b`  
		Last Modified: Wed, 25 Feb 2026 01:52:36 GMT  
		Size: 18.6 MB (18637576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f336c8753f8a591d0e3ccf1d8fb211aea4db0ae9797dfa0648f9393c46bb7e`  
		Last Modified: Wed, 25 Feb 2026 01:52:36 GMT  
		Size: 4.5 MB (4517762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:40f73dc67b2d787357fc2faf5de86ca75dc35316898fdb14b1b737d9169000f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d28a15770147302baa200a9119cf508328ada6177b332e609e74fdf3960e3d`

```dockerfile
```

-	Layers:
	-	`sha256:2461f497f73eb554757ee9d5dc974a84f8aadd85bbd4a1d01ebbb8bff56c75d4`  
		Last Modified: Wed, 25 Feb 2026 01:52:36 GMT  
		Size: 3.8 MB (3836017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cad10bb33535c8cf949a7edaf59176b2ff1b40fa32aa5282738b38f66248522`  
		Last Modified: Wed, 25 Feb 2026 01:52:35 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:ec248f352fdb1b3b17eab7d75b5057c613bc08331ff919c6719d03a857802c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199055436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f229b50a7baedf12fe9aad6ef4654e9cf9c4a42eab483c953d4f0a17fff1f9e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:12:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:12:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:12:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:12:58 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:12:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:12:58 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:14:02 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:14:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:14:02 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:14:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:14:05 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf3ca8078f9a8ff06106e2ddc819bac030792db65741aa1c31b6c84c638804f`  
		Last Modified: Tue, 24 Feb 2026 23:14:35 GMT  
		Size: 126.6 MB (126562017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94986e899e765aca4ad65f2e12811988ad9171752b28ea1b04a36e132994f5d`  
		Last Modified: Tue, 24 Feb 2026 23:14:33 GMT  
		Size: 18.6 MB (18621126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2283c15c5a05ed7f2b26f7c8843b9964955dc7bd291e708411dd827ba3a30a2a`  
		Last Modified: Tue, 24 Feb 2026 23:14:32 GMT  
		Size: 4.5 MB (4517727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3f3e1fbbaaf327e9e9dbe91f8a042c041d3f2f0e2f0e7f84dac9c26a9ccb8a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3848426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b1b45dae9ea78a7d5d02f661c4bcedaaeb628054ee764f5006f5307ed24408`

```dockerfile
```

-	Layers:
	-	`sha256:a0e21ca6afd968290e029f3ce9b9cda30e2106add0b8e5b4ac7ca94d402a1093`  
		Last Modified: Tue, 24 Feb 2026 23:14:32 GMT  
		Size: 3.8 MB (3832063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffe410b9fc0b04ee2ef8d67f406ac2a4b790cd88583f5ae9d0c8ebb3ddc6f78a`  
		Last Modified: Tue, 24 Feb 2026 23:14:32 GMT  
		Size: 16.4 KB (16363 bytes)  
		MIME: application/vnd.in-toto+json
