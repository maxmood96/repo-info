## `clojure:temurin-26-lein-bullseye`

```console
$ docker pull clojure@sha256:b1e2d90c6dbd53685b85bae2ec5d27a886dad6e5584c6d2e47afd243047f8055
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1fc3492063fc92113b7882a2d553db89491694ff7f677f83d811a986d72b69d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169366768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9103e989559cb9484cc5d2609ec6165d040aa5ec1ce99c2b3aa73ad11e65b8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:19:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:19:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:19:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:19:58 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:19:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:19:58 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:20:12 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:20:12 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:20:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:20:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:20:14 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:20:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287681396fbd0871c51b6284791aa5945a89d388e6c03cf029212dee9e8de976`  
		Last Modified: Fri, 08 May 2026 20:20:37 GMT  
		Size: 94.5 MB (94455681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d218d8e0337eec203854cf981b8cdc182f481531cddd6fc478ba15628c5cb4d`  
		Last Modified: Fri, 08 May 2026 20:20:31 GMT  
		Size: 16.6 MB (16629574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867db1a3064e9131aac92bdcc2cf4d3b035bf893d6288b44f9c68a2e5bd88ad0`  
		Last Modified: Fri, 08 May 2026 20:20:31 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bfdd12dcb84ee3900538d2290422be53b1c5c67b6fbadb1b06e76e7d967d41`  
		Last Modified: Fri, 08 May 2026 20:20:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:837f514313e697dbcdf05e24fe35af11e1ef7b24b037c810e5c92cd432565c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4469727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c8d0d4d4635a6c40114a7c73027c7c20281ce960466efceaf6c5b6ba25bbb5`

```dockerfile
```

-	Layers:
	-	`sha256:250f63e240de732f889b0930ce897e38722334c6bfa589ef6e258d509238ea42`  
		Last Modified: Fri, 08 May 2026 20:20:31 GMT  
		Size: 4.5 MB (4451366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00499d7e31dfe755c3f12ef8623b1a8b95af2b9f0a151789ec86be2d06f3d63c`  
		Last Modified: Fri, 08 May 2026 20:20:30 GMT  
		Size: 18.4 KB (18361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:949a8b02006c113411bceb250d9a55a9820372bb884eb676c332bd036a37b8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166783121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58810e0891fcef22afa839b270d6e802e36043c8efaed14cc2d3cccb764e20f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:24:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:24:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:24:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:24:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:24:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:24:20 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:24:34 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:24:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:24:34 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:24:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:24:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:24:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:24:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13635c091cd58a20a4cb2a6e3b8ca77af6faaa517fa5be12ba024d67d0409679`  
		Last Modified: Fri, 08 May 2026 20:24:55 GMT  
		Size: 93.4 MB (93395200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324a176d1ee6576631858309d2edb0a24afc82ed15b5d944f33fdc729f1ef3f`  
		Last Modified: Fri, 08 May 2026 20:24:54 GMT  
		Size: 16.6 MB (16616572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e82c02e552dd7e9e9fe64609aec50ac3b800c90353b33984765c5563c5f97e3`  
		Last Modified: Fri, 08 May 2026 20:24:53 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f1185580cd12b32b63063e0147dcf2b4a58d2e9f380401cbd0d8f2e4a945c0`  
		Last Modified: Fri, 08 May 2026 20:24:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d2393547a9d2b02a270c8f6e80e6d28f6609786ee7283dbd454242e2fb69aa13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1840dfd52cfa3346016a11cf37a24af7e68a9ae08bb50b914e5e486f9395b8e`

```dockerfile
```

-	Layers:
	-	`sha256:a2b41846a4dd689494d110a75640e5ba7e9fb8e6c59bf4080d10505f6ac91f28`  
		Last Modified: Fri, 08 May 2026 20:24:53 GMT  
		Size: 4.5 MB (4450337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd10e02cf3f6ba2cca5986090bb95f7321cbaa35221a6bf30b796edf881f3f6`  
		Last Modified: Fri, 08 May 2026 20:24:53 GMT  
		Size: 18.5 KB (18482 bytes)  
		MIME: application/vnd.in-toto+json
