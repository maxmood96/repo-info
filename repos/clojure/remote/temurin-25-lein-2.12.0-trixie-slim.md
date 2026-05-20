## `clojure:temurin-25-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:5cdec6d2ccd41fd4bac56098cdedee08af3342545fdad563b64dc4ae98d376e1
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

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0b64b8c5f2fb8ca6af5170beac4f01e21b5561ab7a9161b27b9a68b49968281b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143320731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a22c7182beb5f19faa94ce171eb7f1a8aac24cf315b74bbc4ba1f70161ebb15`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:01:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:01:09 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:01:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:01:09 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:01:25 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:01:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:01:25 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:01:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:01:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:01:26 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:01:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4d7c003a9799fd0b5028602ab76b4ce46b51602570aca46308f1fce1585208`  
		Last Modified: Wed, 20 May 2026 00:01:43 GMT  
		Size: 92.6 MB (92574564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8199283b391d7a0e5a4a11e0614b3741620f0bf7b3052920207092a71b88e48`  
		Last Modified: Wed, 20 May 2026 00:01:42 GMT  
		Size: 16.4 MB (16448110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843e907c53196254ff94cabe8fbff927b39a5bcc3d16a81ad58fbb6b9c65eb4e`  
		Last Modified: Wed, 20 May 2026 00:01:42 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d03f75c95837aefc81de9fd5fe462d946dffa029114414a3a8fd42c572b824`  
		Last Modified: Wed, 20 May 2026 00:01:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:73a54755cef8657147ba3cf1b8cd9374e7376a874c1f410ab842d2ec487bc715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2352693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3812252b3f0ed4304aa280312b8e6ca0aa69f3163ed63e7f02dc2ba23e776b0`

```dockerfile
```

-	Layers:
	-	`sha256:2e1f2d3cfd047699e204188a5668940d688532b558e0c9a93f7eb69b344d05ed`  
		Last Modified: Wed, 20 May 2026 00:01:41 GMT  
		Size: 2.3 MB (2333505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab7aed0ec490e004548a27afbc73a7da4a38ab65a847414b732f6d7a33b91a8a`  
		Last Modified: Wed, 20 May 2026 00:01:41 GMT  
		Size: 19.2 KB (19188 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1fc470dc778393e52c4532d62cc006b85d98cba9540198cc292ae0aa9a64983c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142616547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367d5240d72a79ef71da999d9fd48b49cbae96ba69e4ffe96ac30eac8e1dea79`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:08:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:08:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:08:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:08:03 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:08:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:08:03 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:08:19 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:08:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:08:19 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:08:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:08:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:08:20 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:08:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd7f3fc2c49cec5a30e856152fd93808158c8047b72166ddbe439e221e39379`  
		Last Modified: Wed, 20 May 2026 00:08:39 GMT  
		Size: 91.5 MB (91542261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83034ced915143a4a9e314ba2675aa3c559c143931a1964e50f666cf6d8300ff`  
		Last Modified: Wed, 20 May 2026 00:08:37 GMT  
		Size: 16.4 MB (16414224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87131cddc2f1089e8aac66f5785172c112fb14d1ab1a0a5fe79f7f9c8210ca39`  
		Last Modified: Wed, 20 May 2026 00:08:37 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11d134ca7d57096ec00645d2dd4f23df413f7d4290e56d3852302c7567eb53b`  
		Last Modified: Wed, 20 May 2026 00:08:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a70d1a7e888263d6e36e38cf078f7ea2a0e3efbc86f2f18eab088423baeddb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2352469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729a0589a6035b02a0fd154f45628ce36e8f6d52d135e3b50f97a539cfa7d1ad`

```dockerfile
```

-	Layers:
	-	`sha256:c59181de50f49f2cf345ca98faed4a3e918776b642f1b8107bff90c9450fd102`  
		Last Modified: Wed, 20 May 2026 00:08:37 GMT  
		Size: 2.3 MB (2333136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4c556e60249932db393ea38d40320e22df9601e0bdd3e10cb0bcdc47ca1b80`  
		Last Modified: Wed, 20 May 2026 00:08:36 GMT  
		Size: 19.3 KB (19333 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6645d8255f69b38380805140b22bfd316177a6f3be5e5f0e36b444747eceb748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146518663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2bd88e73933570bb4534511a00ba357256add9ff68924fce558217e7d6fd5e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 06:06:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 06:06:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 06:06:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:06:59 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 06:06:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 06:06:59 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:07:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 06:07:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 06:07:27 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 06:07:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 06:07:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:07:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:07:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe901bdfd8966081270b7ee3a299c954c200a642ef0bde8cc9488b26992dfc68`  
		Last Modified: Wed, 20 May 2026 06:08:03 GMT  
		Size: 91.9 MB (91914021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d24295425e23fe335db7051b75a79224d5e28f8d5ea93707a59f0001cd01c2e`  
		Last Modified: Wed, 20 May 2026 06:08:01 GMT  
		Size: 16.5 MB (16486031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e662017a3d5a92dc7470210e45a46407458197ff13b6b9a854540c1257371f0c`  
		Last Modified: Wed, 20 May 2026 06:08:00 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f8ebcf16720b4be819f5a2bf430926bdb0c266ef9949c686c9c4119f7790c2`  
		Last Modified: Wed, 20 May 2026 06:08:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7e586ed3cfcd960622773b1b471b0419751167e058d0ffcf5dbb4af920982a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2337053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17f9f619624ecc3cf632a3d6c8efc8e0ea1ae8c9050925e07143e9c0ebe18c1`

```dockerfile
```

-	Layers:
	-	`sha256:6b700f00214e965bbda2c80bc15fb86519a1d79af45ec791631280f7cf100c74`  
		Last Modified: Wed, 20 May 2026 06:08:00 GMT  
		Size: 2.3 MB (2317809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12e2679fbeef64c463d261b9f150a4e1c983537e13821a7fac0231675e1d3e0a`  
		Last Modified: Wed, 20 May 2026 06:08:00 GMT  
		Size: 19.2 KB (19244 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:fe9e71b91ea670e1b4f608b85df9a565e20c0b56340485eb8cc7c017ae5ead3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139268721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:705c7877085d440e40a5a9b67ab2b4677937bcbb9dd9ddcca0fcb22c68526eb7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:47:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:47:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:47:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:47:28 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 01:47:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 01:47:28 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:47:41 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 01:47:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 01:47:41 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 01:47:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 01:47:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:47:43 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:47:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe63f38fd6a445c3c5a37affce45515ef2df366f1a8ba589effaaec1088932e`  
		Last Modified: Wed, 20 May 2026 01:48:08 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8d662105e8d99b9b51bbafd273dcf066de52387d627e5ac7ec546b675ea252`  
		Last Modified: Wed, 20 May 2026 01:48:06 GMT  
		Size: 16.5 MB (16484296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02306c1ff2cf12f1527e718f91b81df2361df7acd33bd89923057df0ecc701a`  
		Last Modified: Wed, 20 May 2026 01:48:06 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c87cebca7e0f80e96aa3cee7cd48aeab54234f07feb9a5da3a2e9570e6c155d`  
		Last Modified: Wed, 20 May 2026 01:48:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:875f9ed9ac3092ff716a82f4d2885e485f0e1bab87dd255083981c283830a5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c72b8f1c7be41444374f3b6165320ef5b5e384a23fefc033724c9d40e264002`

```dockerfile
```

-	Layers:
	-	`sha256:22accb145d84b82d23bdd72491c4317b542dc6cfacabf0729fc97bedc7b7f20b`  
		Last Modified: Wed, 20 May 2026 01:48:06 GMT  
		Size: 2.3 MB (2314494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:733567058890c85633e51d12641ed7120060b73a5a265fa71b59ab64d36c0ae8`  
		Last Modified: Wed, 20 May 2026 01:48:06 GMT  
		Size: 19.2 KB (19187 bytes)  
		MIME: application/vnd.in-toto+json
