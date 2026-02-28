## `clojure:temurin-21-lein-trixie-slim`

```console
$ docker pull clojure@sha256:15f0961e7fa2333c725e5414bef74b0abb9cbc3cfa47c2e5d9c6b678b2c89016
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

### `clojure:temurin-21-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:12c3426dbc20f0647488a828ae79a8b654a54b35cbf941cc0eb2edd109756b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208601056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2062c7a39cf8c88e40db581aa2f205733c59e5028a3eeee31a721cffedbd3d79`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:55:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:55:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:55:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:55:55 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:55:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:55:55 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:56:11 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:56:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:56:11 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:56:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:56:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:56:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:56:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e761c1825422df20f4daae206b4ad01732bccd2ad79b9a5aaed257127f46cc7e`  
		Last Modified: Tue, 24 Feb 2026 19:56:31 GMT  
		Size: 157.9 MB (157857058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930201b81857f2b997d433c8d8fb8c09c52ae55123b30c8a257ca7ae9eb22b25`  
		Last Modified: Tue, 24 Feb 2026 19:56:28 GMT  
		Size: 16.4 MB (16447202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8085309b58fb65b3b38de8bb3f899227c0fd934ee1d8f5ca9072fb72b55628f3`  
		Last Modified: Tue, 24 Feb 2026 19:56:28 GMT  
		Size: 4.5 MB (4517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27636bdd08cd8448a8515ed690da291cea17a5c2b937b3c43d6a43d251efeda8`  
		Last Modified: Tue, 24 Feb 2026 19:56:27 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:28b691a4d5c0f3c500c4d34c0dbf09ed831f10f850780b909dac76a1f2c2b8ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e700f6b0c599829d8254cd49d460b4cc2b1f5a511ee1d1bc8ec0eab149c94328`

```dockerfile
```

-	Layers:
	-	`sha256:43763a5e8dbcded8e2faf1da1fb1de382175681adaf577cee8473101f2fd0fd1`  
		Last Modified: Tue, 24 Feb 2026 19:56:27 GMT  
		Size: 2.4 MB (2366604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9ea14944a59318ffbbdd955025c2a52786193ebc8596864c066adf1a55c8034`  
		Last Modified: Tue, 24 Feb 2026 19:56:27 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e92cd3358d7d73e946e88dca14b6a0b22066368f4a34aa1fcf59f8b1628cf755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207204928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc06cc288ad5beb295406790132fe7c17e9e9019bfd3fcab4eb9390a50b001a6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:06:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:06:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:06:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:06:38 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:06:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:06:38 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:06:57 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:06:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:06:57 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:06:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:06:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:06:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:06:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c94e3358edcdd6ac1aef8c34bf7aa67e8a290a8492902766b457fb53e3d646`  
		Last Modified: Tue, 24 Feb 2026 20:07:18 GMT  
		Size: 156.1 MB (156133080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53b56514065fd89a3ded93829987f8fbbf9c954209b7d37078308ae5e44c38f`  
		Last Modified: Tue, 24 Feb 2026 20:07:16 GMT  
		Size: 16.4 MB (16413584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86894b21c232127c7eae726ad2dc54ef668850e463704b8058e93ba0f5af3ca`  
		Last Modified: Tue, 24 Feb 2026 20:07:15 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075534ed6e284b91d5eea04844fe10f3c9b448219eff47d6a8cf701875884d7d`  
		Last Modified: Tue, 24 Feb 2026 20:07:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:02351026944b86e93b26ef1269a068b9919fda68c09aa506ad51a63af773327b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6948b4f8fee1d3bbf4c2a977c66fccd72d5a4a6913efa234c75ea38e1bed377`

```dockerfile
```

-	Layers:
	-	`sha256:89beb39311113790a41bf417cf644827661a316bb16401980f737270081e9e45`  
		Last Modified: Tue, 24 Feb 2026 20:07:15 GMT  
		Size: 2.4 MB (2366222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf12d46c0fa277a8ba2796439e4bade4d8392d5225d0ef5c0154493ffbc0397e`  
		Last Modified: Tue, 24 Feb 2026 20:07:15 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6773cae21f7d55dd39b33dff1d515e382dd13bb7e3453bfed4a97bf4247d8bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212580668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d58cefa87a1a548279b7c0cfa6f0fc6eb6c51e135fd647386501d05556f665`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 02:08:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 02:08:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 02:08:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 02:08:05 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 02:08:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 02:08:06 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:08:49 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 02:08:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 02:08:49 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 02:08:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 02:08:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:08:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:08:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03e689c06567c80a28fd472748594e5fc56bc0f3f151ccb3aa20e431739eb37`  
		Last Modified: Wed, 25 Feb 2026 02:09:40 GMT  
		Size: 158.0 MB (157977516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9569138ef2266af4d483bf083e7aaf4b59f7e0b36af1d2256949eb1d670978`  
		Last Modified: Wed, 25 Feb 2026 02:09:36 GMT  
		Size: 16.5 MB (16484752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e8a14d8bb8ff891330d748cc72c08287abba53326f8e0510482e2545282d08`  
		Last Modified: Wed, 25 Feb 2026 02:09:36 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb805682f8e81f5d5a14608cace1329e0ea1af92a91d6fec3ba1c4ccc7b47d1`  
		Last Modified: Wed, 25 Feb 2026 02:09:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0056d1633d925a04131b80f2b4fdf8cf1ef249f907cd2b29ea3d96297d2599fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b444402adf7dbf7a6f477052ac8864eb3ae66820bd31fc01a6c8cd1e4a2c5a08`

```dockerfile
```

-	Layers:
	-	`sha256:07da0fc48688dd33d2a7d49331b6467c80f9a1b995bb84e14ea3c77e7284eb76`  
		Last Modified: Wed, 25 Feb 2026 02:09:36 GMT  
		Size: 2.4 MB (2367584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40977a381f4da3ba8ba99f4d054787d59edae7225490784df448b8b99e0cffcd`  
		Last Modified: Wed, 25 Feb 2026 02:09:35 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:2da654fd61a24dbf91820071e459e2389a6467a91ef131a6e7b647b86425c42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206409440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d495f3bd82c1857d2bb1d4aef0cf2a3682d77186166bbd1e533fab3a03005402`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Fri, 27 Feb 2026 21:55:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 27 Feb 2026 21:55:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 27 Feb 2026 21:55:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Feb 2026 21:55:11 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 27 Feb 2026 21:55:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 27 Feb 2026 21:55:11 GMT
WORKDIR /tmp
# Fri, 27 Feb 2026 21:56:46 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 27 Feb 2026 21:56:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 27 Feb 2026 21:56:46 GMT
ENV LEIN_ROOT=1
# Fri, 27 Feb 2026 21:57:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 27 Feb 2026 21:57:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 27 Feb 2026 21:57:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 27 Feb 2026 21:57:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9746c1013363a5626c8fa09c599400a2b807c516a2cab2a59fb56e33a746ff27`  
		Last Modified: Fri, 27 Feb 2026 22:01:18 GMT  
		Size: 157.2 MB (157216891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b538c84fe0a4a83ea8fb46ee3be17383c57df3dbc35b0d9ca1a262a2d83ef1b8`  
		Last Modified: Fri, 27 Feb 2026 22:00:51 GMT  
		Size: 16.4 MB (16397911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504360e4f4938dfdc78090d9c1ad65ebb48687a8c6a57f404b904e3b25850603`  
		Last Modified: Fri, 27 Feb 2026 22:00:49 GMT  
		Size: 4.5 MB (4517791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c415b422cc5f090bea50e64f71be0918b12fdc9c6f90a20e71a1c74dfcc0d1e6`  
		Last Modified: Fri, 27 Feb 2026 22:00:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a89993fd5395a0d5b356a87adaf8ec01b060e836b9fcad2dfd684a9b6bb92445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610aad10422a79718d603f1788a2af1bab84ca21c36390c9cbd4757f2622f614`

```dockerfile
```

-	Layers:
	-	`sha256:73c6adab9c78fe0231d4fea4a38cfd8fa5ccb3235ee1b150023994869775d506`  
		Last Modified: Fri, 27 Feb 2026 22:00:48 GMT  
		Size: 2.4 MB (2358652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48bf0f1aaa22b7bddfda3d4095febacdede02c3f5f15bd40c617666e72c35179`  
		Last Modified: Fri, 27 Feb 2026 22:00:49 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a40fc342ca2dc8ad459369bc7c65620068972596ff6c144bf7de91a746476824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197945191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461914412be540679c4161f31cd12df4901d518a28be1e86a9dc6b8508356a07`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:20:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:20:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:20:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:20:54 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:20:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:20:54 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:21:36 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:21:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:21:36 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:21:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:21:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:21:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:21:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba3f751715d38911c79b448b46bc6c08eef3e82ab7f523dfeabc737092f2a73`  
		Last Modified: Tue, 24 Feb 2026 23:22:22 GMT  
		Size: 147.1 MB (147105306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416a561ecce6fe65e69cd95cb64fd04754f424d506696797d7a704e2fc89808d`  
		Last Modified: Tue, 24 Feb 2026 23:22:19 GMT  
		Size: 16.5 MB (16483560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d43dfaafa7f063095b8e9d9fe74f70fccc2e62a3f9de670eca427dd94ece30`  
		Last Modified: Tue, 24 Feb 2026 23:22:19 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66af33a4dd9e8fa4cc8b95dd799db25cc65e809e68f3571eac9e7a53b75c968`  
		Last Modified: Tue, 24 Feb 2026 23:22:18 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9db6f2e80c4f625fea4e86641fa9e179ad38e8ced11c0d403d04d3188f4f40fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1de9aafdfc82d3245b8bf2fd5961a0d3b0dfa960ddad13bfe29b9ff0626a9c`

```dockerfile
```

-	Layers:
	-	`sha256:8ebb3e8dd5b3fd3ccd565373aef94a3a443ad302277ceb924fce296187d5e0e4`  
		Last Modified: Tue, 24 Feb 2026 23:22:18 GMT  
		Size: 2.4 MB (2363031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8d41bb4837c6d3257fca739ac59f083332ba574007456aff0f662be4202b18e`  
		Last Modified: Tue, 24 Feb 2026 23:22:18 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
