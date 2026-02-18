## `clojure:temurin-8-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:d9c3b45c64256bdab3430f0f564c3e1bc171211e30660d29f4a4e53c37eaf7e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1f2be11fbaca710a502b7a72553ee6b694332a4663395549fcbbd9b8d818c7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105913663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dddfead240fd6a75ea08b95fe4aaa2ac39727fd7ddee584d67c45a4d85ce94d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:40:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:40:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:40:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:40:39 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:40:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:40:39 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:40:56 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:40:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:40:56 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:40:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:40:57 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d3b36111d8831964080d460b5d4e2ffbe9dbfc0f6615c6c401bc08268bba0c`  
		Last Modified: Tue, 17 Feb 2026 21:41:12 GMT  
		Size: 55.2 MB (55170164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77aa04eae5e3d22c7e9aef8db11c5480981fbf53f82578e3f0adae492e38c5a3`  
		Last Modified: Tue, 17 Feb 2026 21:41:11 GMT  
		Size: 16.4 MB (16447163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64376eb518148941049343e86b68ef7748a9809f4e3f86832b93bb32a13f39ea`  
		Last Modified: Tue, 17 Feb 2026 21:41:10 GMT  
		Size: 4.5 MB (4517708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3460d1099e41d4fec21e6b63ff101735e436f3a1456ce4e574c32b5ec52b75d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749749e45b9f115e0addae49d8f9fcd8782854a7d77f700e9bb975914f76a7f7`

```dockerfile
```

-	Layers:
	-	`sha256:b504d81700ccac7aa10ca133e121cfd48a327ff3fb37a5434d6226b4b446598c`  
		Last Modified: Tue, 17 Feb 2026 21:41:10 GMT  
		Size: 2.5 MB (2485741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43b44132305dabbbd11099124d28cdb43603f05cc9d5c72e092d00fb87f84a7e`  
		Last Modified: Tue, 17 Feb 2026 21:41:10 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4ed3b22e4acbd83e244481b422d3e86f9d1b3ecbd254c8203414b334de477a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105323005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5cc52804b9930a738f538bd89a901ddd3bea0a8145cef75db6e5fa5e85b5e7`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:40:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:40:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:40:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:40:27 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:40:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:40:27 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:40:43 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:40:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:40:43 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:40:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:40:44 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1b2c2eef8bb6bfbff10506797ce33a2cb4503dcce48a551827dbe55b0b4f0b`  
		Last Modified: Tue, 17 Feb 2026 21:40:58 GMT  
		Size: 54.3 MB (54251611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83551ed5c594d3f05c3a3928b7c37ec3855d092d6da2ca622befd3ec41da10b1`  
		Last Modified: Tue, 17 Feb 2026 21:40:57 GMT  
		Size: 16.4 MB (16413580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7326969582dc180bc923e06eba799de6b055eb7bd683f079f73c5a5796e1365`  
		Last Modified: Tue, 17 Feb 2026 21:40:56 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:69404bc3418cf227f1943b9cd786c31cd9fc3ca4250b66eb05423935e8c2843d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4551ba158cee4846bb9a6fae941765660fee6f17a1cda62daab9d6f65acd2eeb`

```dockerfile
```

-	Layers:
	-	`sha256:77bff7e75c287d61aede4e246c423afc64f9386c84b513e05b993dfcd90a85a6`  
		Last Modified: Tue, 17 Feb 2026 21:40:56 GMT  
		Size: 2.5 MB (2486059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea9cca3905ebdcc544f32e8bab82cfdbaa88e3c617c8cc56c25cf5a03650642c`  
		Last Modified: Tue, 17 Feb 2026 21:40:56 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2b5f02afba355159989b9a60ff27c2f2662203b990bd8c3b32e470963c779888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107253200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6cb801ab3011a34dec3773cd88d7971f19c0aa2cb6ea6991dfb968870b030ba`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:00:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:00:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:00:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:00:11 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 06 Feb 2026 00:00:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 06 Feb 2026 00:00:12 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:01:40 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 06 Feb 2026 00:01:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 06 Feb 2026 00:01:40 GMT
ENV LEIN_ROOT=1
# Fri, 06 Feb 2026 00:01:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Feb 2026 00:01:44 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e89dcc3b95f00f17f7b2d6872744c6220cb1fbbd573cd216d9413691c73b51c`  
		Last Modified: Fri, 06 Feb 2026 00:02:21 GMT  
		Size: 52.7 MB (52650394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed8d58b032e252a98729ba3b6451f53cafe6958b1ddae9cd899e3954ead220a`  
		Last Modified: Fri, 06 Feb 2026 00:02:20 GMT  
		Size: 16.5 MB (16484824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014720029e9f71d098f2ed8cbd2d743af40d45b84b1a93edfd83d9341816c2c0`  
		Last Modified: Fri, 06 Feb 2026 00:02:19 GMT  
		Size: 4.5 MB (4517766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5c1f404694ab7763ed2abbbc639c726c57879e168427f530b1675c65d1fc11ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337bbbde49f1519312f28a2af4f07dea0c1d048b5f1e0b4440aa15955abd108f`

```dockerfile
```

-	Layers:
	-	`sha256:555628df90213e3399684f3b49a0a920580ce10681e5c13673a9c895507580bb`  
		Last Modified: Tue, 17 Feb 2026 23:29:09 GMT  
		Size: 2.5 MB (2487316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31abc07a475f625b20c5e36030e212c9ed4ae8d7403b27d183de3208514ed2ae`  
		Last Modified: Tue, 17 Feb 2026 23:29:09 GMT  
		Size: 16.4 KB (16426 bytes)  
		MIME: application/vnd.in-toto+json
