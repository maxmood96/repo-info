## `clojure:lein-bullseye`

```console
$ docker pull clojure@sha256:85bce953bbe52c6c8e9a35bb075d5702f058ffe14911f50024d98faa71ffebc2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9a6d91e22031309a28d8c60a032648571557cd4fd392af27600ec1a6b3bce742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167188812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46e3e392f91b0573c8eab31122bcb26394e6ffede90c6f4e0df4759547dee07`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 02:03:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:03:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:03:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:03:37 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 02:03:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 02:03:37 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:03:51 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 02:03:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 02:03:51 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 02:03:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 02:03:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:03:53 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:03:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:36 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76dc3b61078d8eace6262cc2b2b877bc8107fb2bf21624436a3219c438b1678`  
		Last Modified: Fri, 16 Jan 2026 02:04:34 GMT  
		Size: 92.0 MB (92045322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0daefa248c2b2fdb2653ca48e73edd2464d426b095e6847d5ca4f6eb06ac2e0f`  
		Last Modified: Fri, 16 Jan 2026 02:04:10 GMT  
		Size: 16.9 MB (16868880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fe7c3bb6450adc9791324ab0b0c9c80abcb2d197902831d6564df976adfbe0`  
		Last Modified: Fri, 16 Jan 2026 02:04:10 GMT  
		Size: 4.5 MB (4517735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517585ae42c03dcd984215818ecdeffcd04242c9e0d6a30631558c2bb85bdfa2`  
		Last Modified: Fri, 16 Jan 2026 02:04:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:21f66a54ce1e62f2e0c75e90ff88b0c326c90e34ca144bd75b043f5278abd89a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4446497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8f6f7b07282f691184a3f7bc774c70abc7ed667f95b4ccf8c37723f8285c48`

```dockerfile
```

-	Layers:
	-	`sha256:6fa1b09abf640a5481b1b92ef3687b78ab7ba694f92265a8ec6bd330d8b1b91c`  
		Last Modified: Fri, 16 Jan 2026 02:04:10 GMT  
		Size: 4.4 MB (4427494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6432019498296dac800d01a263716b6117b7bcc9554c9e127d1ac1da1bada0c6`  
		Last Modified: Fri, 16 Jan 2026 02:04:09 GMT  
		Size: 19.0 KB (19003 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bacec6a4b5829d6616dbe275770f219b9b2eba77e59f2b403723d7f5f8140279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164685637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6c83d1b7777d0de631c65bf1343ba041e147f0ce7ace92c3ffe3e9ffc87076`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 02:08:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:08:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:08:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:08:36 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 02:08:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 02:08:36 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:08:50 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 02:08:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 02:08:50 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 02:08:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 02:08:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:08:52 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:08:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8049c4c18078b44e39fdafdbac7fad23e44e26050524177e17cd77e25f2c51c5`  
		Last Modified: Fri, 16 Jan 2026 02:09:11 GMT  
		Size: 91.1 MB (91052492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed550e89a7742c5659d4896eaea176758b011f13e55553a37626cfbf0a8af902`  
		Last Modified: Fri, 16 Jan 2026 02:09:10 GMT  
		Size: 16.9 MB (16857244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c36a19cd6d8d6fc4336b9d68aa4ebedcbd2fb1e10e33a8d14174db35fa2a63`  
		Last Modified: Fri, 16 Jan 2026 02:09:09 GMT  
		Size: 4.5 MB (4517703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8b1367d0c643c2a411f87bbd20551fd76d4130685ddd21a6ec7be56992807c`  
		Last Modified: Fri, 16 Jan 2026 02:09:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3aa0a755baa5b3aaf8e7df9381e149c8f95ed2c3a23cc56848393bf784778423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4445637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ef0752dcb7d6fbb19381b8edf83ac841d40a9c4866a04fdcf94ede79a749ed`

```dockerfile
```

-	Layers:
	-	`sha256:55f29e1dbbd70973b434f4f2bda3c85cae5f282cb274248ed7c6f9726c76a805`  
		Last Modified: Fri, 16 Jan 2026 02:09:09 GMT  
		Size: 4.4 MB (4426489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7623250fed3dbfc72d378a1b8d3350e058da0c6ae3e92b488d9e4e69594d628`  
		Last Modified: Fri, 16 Jan 2026 02:09:09 GMT  
		Size: 19.1 KB (19148 bytes)  
		MIME: application/vnd.in-toto+json
