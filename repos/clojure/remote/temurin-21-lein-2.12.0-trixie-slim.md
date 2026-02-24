## `clojure:temurin-21-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:252c15408447d88b0c98526e9ba86254e747b172eac0ec2d21e22cac9a5cb1dc
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

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; amd64

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

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

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

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:47ae50e68a1abf5fd6b9d2102ae66c83adbb5a0c21f98ef92169cfd49acc9c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212580804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3923759fb16359eff6899a2c7089cd376f24b214f46e4582fcf9bcba130cb3c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:37:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:37:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:37:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:37:54 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 06 Feb 2026 00:37:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 06 Feb 2026 00:37:56 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:38:52 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 06 Feb 2026 00:38:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 06 Feb 2026 00:38:52 GMT
ENV LEIN_ROOT=1
# Fri, 06 Feb 2026 00:38:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Feb 2026 00:38:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:38:56 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:38:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d803d46010c6f6fae7ea82f881a836bc9d2bf4afad631cfb7ffd52616e4eec`  
		Last Modified: Fri, 06 Feb 2026 00:39:44 GMT  
		Size: 158.0 MB (157977492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac57f01c5b92fad24b39c36f9e6375f1fd3713ca19c23f5c2ef5eac1d73a501`  
		Last Modified: Fri, 06 Feb 2026 00:39:40 GMT  
		Size: 16.5 MB (16484945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e409008fd3b109f379b391ba22cc3f20a6c64f4b9e43e4b3a02877937109969f`  
		Last Modified: Fri, 06 Feb 2026 00:39:40 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cff37a16b7901e326316ec37f7901195f754605954dbaa47e9a1191600cbce`  
		Last Modified: Fri, 06 Feb 2026 00:39:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e9ed57d6c9d1110b4ceac0924b18b8f9448e0591386d9156a1ce6cd3435cd092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a15f801cb504f2d5df0541a0904a89b29f27b6cdea51a52b72182185bc3a64f`

```dockerfile
```

-	Layers:
	-	`sha256:5902a8c7cf512566ef8f873ba09cf694d46561990f1206ed6f55c63646a115f4`  
		Last Modified: Tue, 17 Feb 2026 23:59:03 GMT  
		Size: 2.4 MB (2367584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e8640411182d46594c5cbdf0fadb0779c1a6d40c79c8634482ea0ee50759c41`  
		Last Modified: Tue, 17 Feb 2026 23:59:03 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:c6730103b35faa75851eba3dda855f55e0e5cf77d2ab0aeed4f36ae90e5a1f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206409479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8f11228da84f659a0ffae8e94f53c875f4a7af396532d57feb8f10701cade7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Wed, 18 Feb 2026 11:04:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 11:04:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 18 Feb 2026 11:04:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 11:04:54 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 18 Feb 2026 11:04:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 18 Feb 2026 11:04:54 GMT
WORKDIR /tmp
# Wed, 18 Feb 2026 11:06:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 18 Feb 2026 11:06:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 18 Feb 2026 11:06:31 GMT
ENV LEIN_ROOT=1
# Wed, 18 Feb 2026 11:06:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 18 Feb 2026 11:06:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 18 Feb 2026 11:06:48 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 18 Feb 2026 11:06:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c1241f02353400467eda8df7776c998fe2e431d20bf997eeca9a8cae295c3e`  
		Last Modified: Wed, 18 Feb 2026 11:11:04 GMT  
		Size: 157.2 MB (157216934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9e6be2b53253944e51b8f4a814b0c116aa85067f184c7b269d72641e1425ad`  
		Last Modified: Wed, 18 Feb 2026 11:10:43 GMT  
		Size: 16.4 MB (16397944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf467af41e154f2fe7a8ae5cbed3ebe9c3a77c94e7d893d88fce5b7af521283`  
		Last Modified: Wed, 18 Feb 2026 11:10:41 GMT  
		Size: 4.5 MB (4517782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12df282b9a0d1d7545ba98a53815ae15b3a78502444eb1bf37174c42626a151a`  
		Last Modified: Wed, 18 Feb 2026 11:10:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1209c6165f9bc303151ea0945d2e8d6ce872cded47b3337a1519ab222c8c74ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8c8d09edba2928d049a23286d68285acf9da5f12d4c7843a52af1e2ca413a4`

```dockerfile
```

-	Layers:
	-	`sha256:8bf3c25e2b499a1f5580a21fcb54912a1089b691aeb293e5a8b34d738101b06b`  
		Last Modified: Wed, 18 Feb 2026 11:10:39 GMT  
		Size: 2.4 MB (2358652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f36e5f2af37d1e6f30e59b0fa89126a7bb5739daa654b986c93e2399c097d28`  
		Last Modified: Wed, 18 Feb 2026 11:10:38 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:1658e8796f732fd5cf8c5f5cbbc5b1399f77b6ae3c19e6b7f0e07f5d13b17834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197945156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c44f90f246adfa7812682997fb2d672c99d9b86063743cf38cb3ae6372a0e4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 22:12:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:12:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:12:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:12:44 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 22:12:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 22:12:44 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:13:23 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 22:13:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 22:13:23 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 22:13:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 22:13:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:13:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:13:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbcb2a4eb68d199106dfb710f086ecdf2ee7d722b55f808aa430670d4adeb`  
		Last Modified: Tue, 17 Feb 2026 22:14:07 GMT  
		Size: 147.1 MB (147105303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6491661bb3f13af1a882d7af80b725fe0c18339c2b9ead8d38d44f50585dcb`  
		Last Modified: Tue, 17 Feb 2026 22:14:04 GMT  
		Size: 16.5 MB (16483554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5ba34fcf91ea335876326c7cdf59f91bf40bb7cb07741e3ed6d80a9598ea25`  
		Last Modified: Tue, 17 Feb 2026 22:14:04 GMT  
		Size: 4.5 MB (4517719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c01a79a3c2bebdd8fa9f1c883e277f33887a5d62219096cfa0de21c198edc4`  
		Last Modified: Tue, 17 Feb 2026 22:14:03 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b25c53fc3ed6d23cf4b2b13cc11902327c283d981d425ce4686368192cdb5ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4f0d493b6be80d73bc293b97c9d6463aad60d6c7698165445be8fb78e04dc6`

```dockerfile
```

-	Layers:
	-	`sha256:d61547af6ea138c13323373a4aaac460705010056e749912236c57c7d7bc2e7f`  
		Last Modified: Tue, 17 Feb 2026 22:14:03 GMT  
		Size: 2.4 MB (2363031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9513fcfafeea3aafaae65698801814aac1e65c6cca273115d7e02e5b7260372b`  
		Last Modified: Tue, 17 Feb 2026 22:14:03 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
