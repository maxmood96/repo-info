## `clojure:temurin-25-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:360a12efac7f43cb154bfc56b85ece5b4b3542af432191c60d9638bb1c1da9d1
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

### `clojure:temurin-25-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1c2422689cf5ebb7796ca0ae85f4c69587d1bd3a9f141cf8def54025c06ecb45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142770272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a769838d6c6295a497eef695bbbbf8af0e44974a4bda86bc391b313dbb12dbb5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:20:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:20:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:20:39 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:20:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:20:39 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:52 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:20:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:20:52 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:20:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:20:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:20:54 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:20:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb90a96c39decb67de5153339d3819d71ef9ad7fceee2b44dacd5f913103a83`  
		Last Modified: Wed, 22 Apr 2026 02:21:11 GMT  
		Size: 92.3 MB (92256281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f875ad0baf49f9af3bdec05bb960a4aa7b684734804f37d858b02c8bc9561d5`  
		Last Modified: Wed, 22 Apr 2026 02:21:09 GMT  
		Size: 17.8 MB (17759573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cdcf21f30556ae88dd774983640d85bd7af1073eee85290b1c0b25166c67bf8`  
		Last Modified: Wed, 22 Apr 2026 02:21:09 GMT  
		Size: 4.5 MB (4517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48dd39be675acd1b15a96edd9533d9f4556589dd2cacf108ee97d73a83f3928e`  
		Last Modified: Wed, 22 Apr 2026 02:21:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:29facc17b4449b14ec0943c33b076b160440ebd2d4e2df54c9f890f6a372b4a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10c3e6243e70ec20797906e0a908b772c3f739849b9aaba91f1a57a29b73671`

```dockerfile
```

-	Layers:
	-	`sha256:a75631584cc4e2825bc2696857238f029abc5ef16b16b9849c9e824a033d6449`  
		Last Modified: Wed, 22 Apr 2026 02:21:09 GMT  
		Size: 2.7 MB (2698110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1104e5f2f690d5ee06fae0cf9fcd437285af032a7c2a0d6ada4042ad5c0e963a`  
		Last Modified: Wed, 22 Apr 2026 02:21:09 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6327f37f9ee029a628e485cacd5b3851011de461f90b6f153036c812860695fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141515601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d53cd9119de2d96fcc565d597ee78c07203f7bb45988b3e5483e65ea46ac09`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:23:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:23:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:23:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:23:24 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:23:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:23:24 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:23:39 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:23:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:23:39 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:23:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:23:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:23:40 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:23:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b7c47939a8d008bc083814af87c41d0faf3bc6a7a9e8f029d7fb3bce123c4c`  
		Last Modified: Wed, 22 Apr 2026 02:23:58 GMT  
		Size: 91.3 MB (91288310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a34f78ee0c77921c25607cd182b6e4354abd1838d5d5847ab7e4a1bcf5c72f`  
		Last Modified: Wed, 22 Apr 2026 02:23:56 GMT  
		Size: 17.6 MB (17593046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031e1fc03119dbd22fcd5a245dd18e7375ead2423f0b219e3436816034c3e840`  
		Last Modified: Wed, 22 Apr 2026 02:23:56 GMT  
		Size: 4.5 MB (4517703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950bfe22c5ed7038b529ff742594036e6e508502325a20575820972f6635afeb`  
		Last Modified: Wed, 22 Apr 2026 02:23:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:53a2605f8fd43a4e7286baacff6bc3c01e571b027695e6e5ed9d5210a407bd76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2716948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac76b97718abb8ad1ed7a2be2d642f31da3bb81b17005ef20284ab7aaaedb129`

```dockerfile
```

-	Layers:
	-	`sha256:bf43db429e6aa25cf122c08c02505ee0fde7343c4a1eaf3371919401341f7a73`  
		Last Modified: Wed, 22 Apr 2026 02:23:55 GMT  
		Size: 2.7 MB (2697746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be419f2beac81a33bce715c7ed0dfd3f9aef18c51fb62e8292144ab2f0dc3afb`  
		Last Modified: Wed, 22 Apr 2026 02:23:55 GMT  
		Size: 19.2 KB (19202 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:66e373c53ce7721aea6362ef05691d1e094c88d011588c56ac45c564701bae51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146190787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07317d314a8d964b115f92f0d5fffbfa2516b86a77dacf2fd363ad6e39e740dd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 19:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 19:13:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 19:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 19:13:50 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 19:13:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 19:13:50 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 19:14:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 19:14:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 19:14:27 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 19:14:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 19:14:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 19:14:31 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 19:14:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186825ad1954e238f9d41fa43dbe8881cdc35374805d5861befa0e42e394c10e`  
		Last Modified: Tue, 07 Apr 2026 19:15:05 GMT  
		Size: 91.6 MB (91632990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428c136c5e4d1b39849f44776d5c465f6e4f9bc09426c43d7cb81f4d42618b2d`  
		Last Modified: Tue, 07 Apr 2026 19:15:03 GMT  
		Size: 18.0 MB (17961133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e59a45118f3cd04c33c341632c7480a07080f8521e1fe191324e9a4c9dd5fa`  
		Last Modified: Tue, 07 Apr 2026 19:15:02 GMT  
		Size: 4.5 MB (4517771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefeaadb79b63b4c959c7885773e62927a2c55a294280f73a36d4fd7957f0bff`  
		Last Modified: Tue, 07 Apr 2026 19:15:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:16654e263ef1455af78e8bfce0771b9a0b07670415e43aa9584866b47c7b011b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2702381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa6d28e37593df2201e91cb8d007c3388913105e98d4ab19f7bbd8f854914e8`

```dockerfile
```

-	Layers:
	-	`sha256:ce8f6f7922eb0013f486ca6517b1320a85fd663c12a3c041978d08dc903e895a`  
		Last Modified: Thu, 16 Apr 2026 03:09:01 GMT  
		Size: 2.7 MB (2683267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f3d329d4fb0478225e1e4f0f36e27dcfe60cce19215ce3f8dd290a7a33dc5f6`  
		Last Modified: Thu, 16 Apr 2026 03:09:00 GMT  
		Size: 19.1 KB (19114 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9f67fd0233f3efdeda6af5ac406bee5785b36fc85653b8ca80d597c73cf9e995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137065552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcea86653b9e0cf207707c292620bd8e3a13a123c81ac98a93dd9c3a66be2925`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 04:04:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:04:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:04:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:04:57 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 04:04:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 04:04:57 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:05:08 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 04:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 04:05:08 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 04:05:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 04:05:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:05:10 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:05:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe371a317b1e8d0173b45c71ab2e942734aba17edbcad4ca0dc90ba9f9057987`  
		Last Modified: Wed, 22 Apr 2026 04:05:36 GMT  
		Size: 88.2 MB (88233823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6498ffcc1a50cb20f27a9a77e3415b44fd9e0a853bcbd7014506c7e0581612`  
		Last Modified: Wed, 22 Apr 2026 04:05:35 GMT  
		Size: 17.4 MB (17421983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f97b716daef2b086620b1d9da6fc67cf9d8430ed5f38dbd98ad82f93a5f2dd`  
		Last Modified: Wed, 22 Apr 2026 04:05:34 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58913b185f95d97483e910d9242bb565d73afff933b7f4f98e3de54be74cb7c5`  
		Last Modified: Wed, 22 Apr 2026 04:05:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:883be0740f8bab69740af18d2fecb5543ba9bc417904a67846adf65f264476ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b6786d01f528d1910a10c538ae660ce06dbdfb2d15790b8f15165b895eca03`

```dockerfile
```

-	Layers:
	-	`sha256:2cc69a57f16a11df1e05a0857fe2f76612323f2acea756652ba9a4b177e51778`  
		Last Modified: Wed, 22 Apr 2026 04:05:34 GMT  
		Size: 2.7 MB (2674486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:900d3fa985e85f53a3193f3080570ab3e411148ab72a94c580fddbedbac23672`  
		Last Modified: Wed, 22 Apr 2026 04:05:34 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json
