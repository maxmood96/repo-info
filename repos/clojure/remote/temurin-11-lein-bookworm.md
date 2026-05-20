## `clojure:temurin-11-lein-bookworm`

```console
$ docker pull clojure@sha256:548cfb705d35d8256c92c9255823c6afde764d601d9b0f7e6ae3097369d61f50
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

### `clojure:temurin-11-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:8b7f1c416be4d90cdaab8d31c385cc30ffceb77ea10940c7207c4d8cb23bb198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218711178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0e032db75d31af91746a3ac230b3431198007a01e3eb5b53faa02cb32e54b2`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:57:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:57:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:57:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:57:01 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:57:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:57:01 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:57:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 19 May 2026 23:57:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 May 2026 23:57:15 GMT
ENV LEIN_ROOT=1
# Tue, 19 May 2026 23:57:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 19 May 2026 23:57:16 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9b492fa3653f8ba75b86667a3d2c7101f92b2697c2bce3bdf6d57590f6a134`  
		Last Modified: Tue, 19 May 2026 23:57:36 GMT  
		Size: 145.9 MB (145886263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd11af6a6262586870bd41d00e5aa059f0da1936e9ed0e02fd2340714e78a31`  
		Last Modified: Tue, 19 May 2026 23:57:33 GMT  
		Size: 19.8 MB (19811719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2e43c2abf3064936fe00f10178d4bdefda0e4e35ab24af0530da44357af97a`  
		Last Modified: Tue, 19 May 2026 23:57:32 GMT  
		Size: 4.5 MB (4517732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:54914d11e10b3493da9d8f4fd2e722e615f79d01a462e2f390c22f9e4b4eb45d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4318428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ec9fdeafff115289279143ced5236d8e68a82b56973599954727b02f2aecb8`

```dockerfile
```

-	Layers:
	-	`sha256:cd1d9695c4e3a9c17bfd954fc54675f9c6a1d38d1cfc838b2a2e8eb98fed6f57`  
		Last Modified: Tue, 19 May 2026 23:57:32 GMT  
		Size: 4.3 MB (4301892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58161808761048904323d64c5798758eae11239ccd5926dc7f34b7b47c1830ce`  
		Last Modified: Tue, 19 May 2026 23:57:32 GMT  
		Size: 16.5 KB (16536 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eb584b02a0dff2764f73881523d8003841bcddf946fa335c7e1d58ceee963f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.1 MB (215121278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025f3a31051d879bf29d6ff2f0604ec0281212e3b3f04da6e35c60ab5dd15541`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:04:12 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:04:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:04:12 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:04:26 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:04:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:04:26 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:04:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:04:28 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c9ed6b2b7cc58fc1c58ab0c5c1363006f4cf4bdc094d534050f11de5717bd5`  
		Last Modified: Wed, 20 May 2026 00:04:48 GMT  
		Size: 142.6 MB (142582230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c2505f3036b18498b6716537ab525b74805ecc1134feaa09239915a3e61fa3`  
		Last Modified: Wed, 20 May 2026 00:04:45 GMT  
		Size: 19.6 MB (19641833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dfade01b9c2c7d5d091de56cda21bc6ec2aad3e7cbc677a25278cec62064980`  
		Last Modified: Wed, 20 May 2026 00:04:44 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b1bec97e09636a560fac1fcfa20532821d7fff262dd5e1bf2d77a4311002b977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4318782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10aba039e92d9750fbb9f909e4d72d3578d416be363dd89688bec6c8cfbad909`

```dockerfile
```

-	Layers:
	-	`sha256:ebd1f64efbd3f5e1e47d77cd33a973d8c602f1c6250fd85de4f339920708620b`  
		Last Modified: Wed, 20 May 2026 00:04:44 GMT  
		Size: 4.3 MB (4302125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a903308314e946d6da0fb09c866a95163a74d59dab59d13930ca989f07c0ff`  
		Last Modified: Wed, 20 May 2026 00:04:44 GMT  
		Size: 16.7 KB (16657 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:12b2ffbfa9c76c2858ac4ac9ac3b7a767009f80e6b1fb36daf4f1cde4b7604ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (209995289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d7acd73c1a297ca06d98f927933f48b1842f07c66e71137b2f4774e97b3d53`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:25:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:25:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:25:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:25:03 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 09 May 2026 02:25:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 09 May 2026 02:25:03 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:25:29 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 09 May 2026 02:25:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 May 2026 02:25:29 GMT
ENV LEIN_ROOT=1
# Sat, 09 May 2026 02:25:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 09 May 2026 02:25:33 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cbaabc187f4e33faa4937073e6b8d37c4b4ee8836b24edba986c27660880f2`  
		Last Modified: Sat, 09 May 2026 02:26:07 GMT  
		Size: 133.1 MB (133110168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad14def98e035e0b145f466bacca173fa97581bf02f54b4e47c1fa8e66bc28a6`  
		Last Modified: Sat, 09 May 2026 02:26:04 GMT  
		Size: 20.0 MB (20030544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5629985390fb62202c0b99c61c7bae17a29b5be264c5fc9783750b0a4f4422`  
		Last Modified: Sat, 09 May 2026 02:26:04 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4b8fbdc4454d075c5204d9233c414dd3bc032eb1526d5a318660e049b6c7ae95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76fbcec9c4cda66042e09dd8f83f23e4ede98d783c7474ac797fcc7c5685e590`

```dockerfile
```

-	Layers:
	-	`sha256:be6e4d26da5bdfdb67ae4c88a1c85422336dfaa623da58748882d95206e7bab2`  
		Last Modified: Sat, 09 May 2026 02:26:04 GMT  
		Size: 4.3 MB (4303120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d68be89328545dc913a24f88445c400e1e97564b4c1a77fff1a0dd6039d1f478`  
		Last Modified: Sat, 09 May 2026 02:26:03 GMT  
		Size: 16.6 KB (16580 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:98cfc891b215a4229d4b3b41ce5367f8acff63b65653337e9cd60cc79c037234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 MB (197798895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e926e58cb0729f0487af65a902a84ebe2c082f0c04e19aa67f96b30a7267db64`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:41:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:41:32 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 01:41:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 01:41:32 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:41:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 01:41:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 01:41:44 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 01:41:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 01:41:46 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d517d3699a232ef2589d952b25b33f3580fd7988f3a577091e4faec6269c9289`  
		Last Modified: Wed, 20 May 2026 01:42:11 GMT  
		Size: 126.7 MB (126651734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55b30f241a797df282d93ef9dfb80ea120d68e5fa07602030e2d52be2a308fd`  
		Last Modified: Wed, 20 May 2026 01:42:09 GMT  
		Size: 19.5 MB (19473786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec4fb2f2df44881f87be172d9fb8f8c794b14cac633cc1891755f811859efc0`  
		Last Modified: Wed, 20 May 2026 01:42:08 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:88f0da8422816d469bbaaff3e27169a1a63061ebd71ec4a974ee3d335cca827b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4310244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d775a90c5de46677d4a0c3519228392cc13b3d1e7395e26eb43247af649c12e1`

```dockerfile
```

-	Layers:
	-	`sha256:be6d8769d66b7ae36d0c600b2a90dc26f34609a498a0f43665d5d17c7fe3997e`  
		Last Modified: Wed, 20 May 2026 01:42:08 GMT  
		Size: 4.3 MB (4293710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cc2f9540aa286046d6b1e393c4e847f677a2e125d7d880d926296ee9cd82c9c`  
		Last Modified: Wed, 20 May 2026 01:42:08 GMT  
		Size: 16.5 KB (16534 bytes)  
		MIME: application/vnd.in-toto+json
