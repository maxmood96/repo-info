## `clojure:temurin-21-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:149e8813add19b9a89384e07a10a202567e4943bedb756538be9cfcd38238273
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

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:40ad6c0bef43600549b3116a20069eec63bbfd4f4bbbe940ae34c0226d8f5883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230248441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a48ab7ef97a6bc60800eb50e0dd4cc8ab9fafe2a63ee0c0c5c54945b20841f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:55:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:55:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:55:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:55:49 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:55:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:55:49 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:56:05 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:56:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:56:05 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:56:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:56:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:56:07 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:56:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc657c50027fc4da190edd9bc5b6aadcd129d52322637f13ac9ac4d9c7a9673a`  
		Last Modified: Tue, 24 Feb 2026 19:56:26 GMT  
		Size: 157.9 MB (157857101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c769e96e725c3ded3c9b5ee44be7a625326baf4e6fbd1abbd393a89c5c843849`  
		Last Modified: Tue, 24 Feb 2026 19:56:24 GMT  
		Size: 18.6 MB (18580041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a7df2b531b4aa7e1399f00b68f90f246afe9e0a2ccee1daed874592858c148`  
		Last Modified: Tue, 24 Feb 2026 19:56:23 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0984079efc84357ec9c870dfe260f9362bbb854e79700f315c7a28cdb4f26689`  
		Last Modified: Tue, 24 Feb 2026 19:56:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5fc9661e38edb159a178da776011d6243d5caa26d8e9bf1fc1753ef7765f56a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33da726a901e21782a680dcfacfca16a17cf7d090bd4366d51437f967f3027f7`

```dockerfile
```

-	Layers:
	-	`sha256:9155a7213db4fa4f12e7248fdb6a7419ee80d93475b04e49d20ff9f510f0c8cc`  
		Last Modified: Tue, 24 Feb 2026 19:56:23 GMT  
		Size: 3.8 MB (3817343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a38f91def0fb2434339c2e990f75a870a32f819f5edf42432e2b226f18b1db0a`  
		Last Modified: Tue, 24 Feb 2026 19:56:23 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4e6197436f59d50dbc85a9a5d4dc605298fd5841e129aa34882d15cca317b948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228844853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5050d8438154a34b95adeb5da56fcfe8f61182147db6d2cf1b17d2850be162`
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
# Tue, 24 Feb 2026 20:06:55 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:06:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:06:55 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:06:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:06:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:06:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:06:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a71ab5f87ef15cb7963d5cd2be3c2f508ff239cf3993deccb955d0ff9e0edd`  
		Last Modified: Tue, 24 Feb 2026 20:07:23 GMT  
		Size: 156.1 MB (156133092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805997551436991c4e4dd643318757ad5c9b622a8194b97cc8953b06f7644c89`  
		Last Modified: Tue, 24 Feb 2026 20:07:16 GMT  
		Size: 18.5 MB (18541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bab8aa5df411675cf7fcac0cb6599f767620923eece2067743149a56c1f8058`  
		Last Modified: Tue, 24 Feb 2026 20:07:16 GMT  
		Size: 4.5 MB (4517726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7127c6fed4d8bab6584e9025da294e438e920af4e0208ad9051bebeca5d3be8`  
		Last Modified: Tue, 24 Feb 2026 20:07:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c94a202068937e17b2bcee104c4a0db9aa3a5b27869f6b473b5599634fb7e789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb235520be3302e2bf15acb5d889d830db0cc66ffd1ad63b7c0de7e3fa95664`

```dockerfile
```

-	Layers:
	-	`sha256:62646393044b40576a1944e1c40d0d75bb2c8bb5087ebb71dbc3c8456e7085b8`  
		Last Modified: Tue, 24 Feb 2026 20:07:16 GMT  
		Size: 3.8 MB (3818220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac99c307b2ca8a304878f7ed4c92af010e64eaa9b7d7a829a0e95484bb38f1fb`  
		Last Modified: Tue, 24 Feb 2026 20:07:15 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:5549e5469823101e14e11e3344eabcba714c113946ff632c7d87d3556ec6b411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234245465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c1ebd05479a0a0d19da89a216c33df2a0777e11d97244a8c7cd4b790b24e84`
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
# Wed, 25 Feb 2026 02:08:50 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 02:08:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 02:08:50 GMT
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
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03e689c06567c80a28fd472748594e5fc56bc0f3f151ccb3aa20e431739eb37`  
		Last Modified: Wed, 25 Feb 2026 02:09:40 GMT  
		Size: 158.0 MB (157977516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af3fb13b6e4e2d38124322bb5af19e5f527b444ba939b7a6e1d8c9f10e5e83e`  
		Last Modified: Wed, 25 Feb 2026 02:09:37 GMT  
		Size: 18.6 MB (18637504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9be93d19e0296d088454110a977e5900f64cdea926176353f0630602f2bae73`  
		Last Modified: Wed, 25 Feb 2026 02:09:37 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb805682f8e81f5d5a14608cace1329e0ea1af92a91d6fec3ba1c4ccc7b47d1`  
		Last Modified: Wed, 25 Feb 2026 02:09:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bb9c837d178a66423df3ee2e02f6482cf4c4c4b56e8bdd79eb357fe13a325e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0706ec522f6d94bbb07bfb33ac72de88f33f87e87eb5d28592ff5c16b86bcd`

```dockerfile
```

-	Layers:
	-	`sha256:58b38ae0b75708d384b1ef8150b526cbaa1147c208cc7c0e5569fedbf49c6747`  
		Last Modified: Wed, 25 Feb 2026 02:09:36 GMT  
		Size: 3.8 MB (3818343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d0f53c96b34e59f4f4129863f833dbafc02672f0fa88e02418cc0668c6ded19`  
		Last Modified: Wed, 25 Feb 2026 02:09:36 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:f3fea45d415cc05e161c3e05b47e50248edfed6a48d2f08b635a978a12afc951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228043834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed6f336e25cc70592dedc31d8f9eaf91cd3dc7c70d0e27c224d431235186ce8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Fri, 27 Feb 2026 21:48:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 27 Feb 2026 21:48:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 27 Feb 2026 21:48:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Feb 2026 21:48:21 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 27 Feb 2026 21:48:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 27 Feb 2026 21:48:21 GMT
WORKDIR /tmp
# Fri, 27 Feb 2026 21:49:55 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 27 Feb 2026 21:49:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 27 Feb 2026 21:49:55 GMT
ENV LEIN_ROOT=1
# Fri, 27 Feb 2026 21:50:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 27 Feb 2026 21:50:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 27 Feb 2026 21:50:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 27 Feb 2026 21:50:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3be247472b67578a1d05739722d8adeca41098796e5d6210800176db58046fa7`  
		Last Modified: Tue, 24 Feb 2026 18:57:42 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569b6a73e2afe821c7f2aa52aff4b98ad632d38789f3835b1ff7afa6ab8bd067`  
		Last Modified: Fri, 27 Feb 2026 21:54:37 GMT  
		Size: 157.2 MB (157216902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38264f34120440d296ccbe11f2e70c2befbf5415a078bcd57362b2b7fc598ece`  
		Last Modified: Fri, 27 Feb 2026 21:54:17 GMT  
		Size: 18.5 MB (18531790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf7f720dbd8c8eaf7e1a2e895c2aed16336de93f2c1cc0b7476b16084cb2161`  
		Last Modified: Fri, 27 Feb 2026 21:54:13 GMT  
		Size: 4.5 MB (4517776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3033600406f0cccd5e834d0c98a42296c8f7f0ef8f2028bd71712138b12f1bf`  
		Last Modified: Fri, 27 Feb 2026 21:54:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8a3894e9c4ca5c5de2b1328ea01ed61a4fa4cc81e91a1fd4580d9d43fcdf1b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3826215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3faee52a00b49cd3918ea4d1c2e6a32016a39665bcd91ba2d2268a22ed1e26`

```dockerfile
```

-	Layers:
	-	`sha256:68a013edbbe2a8d37135783d32fdd363ea2578d289323fbd2e7562714b53989a`  
		Last Modified: Fri, 27 Feb 2026 21:54:12 GMT  
		Size: 3.8 MB (3807820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cb5d964835611890f6ca4c47be8438dae91c82bfc3d3aa76e79136c6110430b`  
		Last Modified: Fri, 27 Feb 2026 21:54:10 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:38ff8baeb2ad7540b7bbc3064bad097863f81b25fab62846182f8d8defa0e1a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219599296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee6de81a5e55c2ea146886cc18973b2de3bb22e89b7bc90a674d6d5e7d05b34`
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
# Tue, 24 Feb 2026 23:21:38 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:21:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:21:38 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:21:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:21:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:21:43 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:21:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba3f751715d38911c79b448b46bc6c08eef3e82ab7f523dfeabc737092f2a73`  
		Last Modified: Tue, 24 Feb 2026 23:22:22 GMT  
		Size: 147.1 MB (147105306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b416df537cc70d5953e237f1424adfa2fe405aca0ce51774f2992fc0e0a082`  
		Last Modified: Tue, 24 Feb 2026 23:22:22 GMT  
		Size: 18.6 MB (18621314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13f95fca0604fdb52a65fc9f6c0814edfaa0ada78d6e9627f16c940aa754adb`  
		Last Modified: Tue, 24 Feb 2026 23:22:21 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9af9452b4bf3650186b006e022849d1e7146b7bdefebfb20ec6ec4882a7ba1`  
		Last Modified: Tue, 24 Feb 2026 23:22:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c8de26563c7895766cf6427999ea3265b4e47ffa8d798f10857aa0abdd988c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65fd1574b75d81e054478763ca5e5c4c226b866af125795d71c95ca088030585`

```dockerfile
```

-	Layers:
	-	`sha256:47bb63c789fc85117dc21243a94a1312c268633ca1940365b69f0ecd7608b095`  
		Last Modified: Tue, 24 Feb 2026 23:22:21 GMT  
		Size: 3.8 MB (3813770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:010a05fc68df5c2be0b2c151a9a306aaae92002c381939140bfaa261e5d13694`  
		Last Modified: Tue, 24 Feb 2026 23:22:20 GMT  
		Size: 18.4 KB (18351 bytes)  
		MIME: application/vnd.in-toto+json
