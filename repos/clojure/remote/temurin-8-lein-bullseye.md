## `clojure:temurin-8-lein-bullseye`

```console
$ docker pull clojure@sha256:ede3774e85990e73e02ddda231f4a0703eb45d08ea310261bf1d33abe877fd3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d56dce9ce4e63a3824e258176529f0aa976d8e4ec615b14ef1e38e3a67d90e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129612719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1376adcb2a746643c16e0739cd591ee3857af2a5d95c66c637994b33c85756d4`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b6f830cd306f01980373f1e0120f2d00018fbe51a9506b7262f5d9e4bbda74f9`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 53.8 MB (53756115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ed1e45c0a1978a9c9e239e8e1b68c9ec0efb4137ad37e35c39c41851166c8a`  
		Last Modified: Tue, 21 Oct 2025 02:18:31 GMT  
		Size: 54.7 MB (54731352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bdec2d818b3880f75baad37c70b035e583736ae0b73c6228e6244f28039120`  
		Last Modified: Tue, 21 Oct 2025 02:18:30 GMT  
		Size: 16.6 MB (16607516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0192e0fb6f9af5e78d0c1bd8d5a9fe4904dcb120fe1c2d621286cf52ad45af`  
		Last Modified: Tue, 21 Oct 2025 02:18:28 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:024d90568bb75cd813af39bcaba5a14bcfe4fdd38a36a741084d006dc622e5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4614213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43be2a3c7474de4abc85e62ba3026c5dff06a16d3b44284dc7397849ea920b70`

```dockerfile
```

-	Layers:
	-	`sha256:2d3da1a02f43e8711279870e73bb44fad9029acf24af5f1385d14e6e3fc1f5fa`  
		Last Modified: Tue, 21 Oct 2025 09:46:56 GMT  
		Size: 4.6 MB (4597800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d752c8a4bd3a61618a145d77d14b5badf31765864ea298abacc8c4af375b0b1b`  
		Last Modified: Tue, 21 Oct 2025 09:46:57 GMT  
		Size: 16.4 KB (16413 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f81c1fef9a668a4f7b2374fa59b8fea620b1cebd44333ada61714a8305ad35d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127205869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164e89906f8516eadd02520fab73ba01a5dd77869efa6346ab480be5eedfa36b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0a72c4e347b74aa6a0086cf3d1d928528ab02577a17bff4e22366a7df681f564`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 52.3 MB (52257444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5707e01fbd9d2e03da956fa65411e7f55a49ed187198a89f028dde6416ad2b`  
		Last Modified: Tue, 21 Oct 2025 02:24:33 GMT  
		Size: 53.8 MB (53835606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46ee22b47d5eb91de82f418d440b26f3928108ee815d1cff392060146978c01`  
		Last Modified: Tue, 21 Oct 2025 02:24:29 GMT  
		Size: 16.6 MB (16595041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0d2bed43cdd37c8c26d16e93e788ddc87fe4bd0ec76ed20cae41f1b8f1d45f`  
		Last Modified: Tue, 21 Oct 2025 02:24:28 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:68d09a2c87a476511dcdeb85da146d5fc15b0759f4d90f072ff1585ed473d940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4614006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e77007ada1fbb06b0804fad342f5196459c4d3dd38ae81dea4842e9ea2113e`

```dockerfile
```

-	Layers:
	-	`sha256:a0788d90149d4e1189c444c544265fdacc7873473b88838e9ebf42dfcab4a74a`  
		Last Modified: Tue, 21 Oct 2025 09:47:01 GMT  
		Size: 4.6 MB (4597472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3dc2dbacafc8f019c3c35157802f89973bff3923820716b02eb313bbefd0c9e`  
		Last Modified: Tue, 21 Oct 2025 09:47:02 GMT  
		Size: 16.5 KB (16534 bytes)  
		MIME: application/vnd.in-toto+json
