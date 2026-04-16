## `clojure:temurin-26-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:90b5c957ca1caed45feb46ec031309b7820ad73958b28cb928f2dde2ea9a403f
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

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7d262d67a106a79f28074c7cbc81fd0a54d65dd935b4ab5507bac7e15e5afe0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (144969770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f2ddddeaf47ed1164c2a51ff9460ae8391282a255e9d5880eb5c0aad5bd10`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:07:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:07:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:07:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:07:23 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:07:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:07:24 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:07:38 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:07:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:07:38 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:07:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:07:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:07:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:07:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5c001de0d5464c89c85c6327cf799f7e511fdee4d3bb362c2c1d7e40e9e34c`  
		Last Modified: Wed, 15 Apr 2026 22:07:58 GMT  
		Size: 94.5 MB (94455691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7c118d6728d3822a60233566fc81379a144d5b1e4d44325850c239e1a635bd`  
		Last Modified: Wed, 15 Apr 2026 22:07:56 GMT  
		Size: 17.8 MB (17759585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ecae0bd118a0f50e7c566d4b2529c9defc70630aadb3eefdf57d390702a7ff`  
		Last Modified: Wed, 15 Apr 2026 22:07:55 GMT  
		Size: 4.5 MB (4517733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ef4f7cf31a3a62ad4c995453d244ce15b6441f53df5f5a6b7d922b1d3e248d`  
		Last Modified: Wed, 15 Apr 2026 22:07:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0758230d344594588f0634119f3907c4ccab02cebfa8085937c168f7aa70eb1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2713950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7ed16748976c92dd0e6b52a7fcc651adf7e05e5e42d585f3c40f996b82667c`

```dockerfile
```

-	Layers:
	-	`sha256:75f9b3d8c33ad2755748cb4d93281dd0d9416adef590d5d4b83c32292759d945`  
		Last Modified: Wed, 15 Apr 2026 22:07:55 GMT  
		Size: 2.7 MB (2695554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2254a2cc7adecce9fff9889a79d426befef09dd4338a7900becdbc1807e408f5`  
		Last Modified: Wed, 15 Apr 2026 22:07:55 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f47db71739091c66e266a184357fcb4234f155c2a4bca94f0262b6cba5b0de45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143622547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd940f62e49cf76bbd982518eaba7480b0276db69866731fa4e54ce77a41bd7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:19:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:19:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:19:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:19:11 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:19:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:19:11 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:19:26 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:19:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:19:26 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:19:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:19:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:19:27 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:19:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aad69bc5ddfcdd55ce194b33c256ba4a263fb064687d2bc25adc5d329368dbc`  
		Last Modified: Wed, 15 Apr 2026 22:19:46 GMT  
		Size: 93.4 MB (93395199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da4e24a023eccb43847bc4e29e5b92b239a288a8ed2a5df409ff639e191fe35`  
		Last Modified: Wed, 15 Apr 2026 22:19:44 GMT  
		Size: 17.6 MB (17593038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4912516cb7b470abcc741c3d2dcf6338e8ad101c031bfaac9ec583402c0ef544`  
		Last Modified: Wed, 15 Apr 2026 22:19:44 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e369e42038f9ffc111057fe30d7a0c86e328ab7f0142fabef20d49b28a6a49b`  
		Last Modified: Wed, 15 Apr 2026 22:19:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:efed2464f30587c79691df263add0aa8486cc92e5562aed3baa454d7b9311846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2713683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c49967599de3a2f522b34e6b44c9fba7df9efb48eaeadd467ed73a629f5ed60`

```dockerfile
```

-	Layers:
	-	`sha256:dfbe8194ecb877f6059d710705fd1ca755107c20e7df728bdfe99882c6351012`  
		Last Modified: Wed, 15 Apr 2026 22:19:44 GMT  
		Size: 2.7 MB (2695166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31ba98ecc250881b54feb63dc09f431a82ca6f42e95793c7ec7884e6ae163e5`  
		Last Modified: Wed, 15 Apr 2026 22:19:43 GMT  
		Size: 18.5 KB (18517 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6c17efc445bfbe0ef77a0e9c6ef84ad74fddcc2c23778b076559bf3e7853651c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148339476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73008806e5b6213b53d214b7c27633ca6d9adaa43a6108e84f94e2f26b6b8286`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Fri, 10 Apr 2026 00:50:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Apr 2026 00:50:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 10 Apr 2026 00:50:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 00:50:35 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 10 Apr 2026 00:50:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 10 Apr 2026 00:50:35 GMT
WORKDIR /tmp
# Fri, 10 Apr 2026 00:51:07 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 10 Apr 2026 00:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 10 Apr 2026 00:51:07 GMT
ENV LEIN_ROOT=1
# Fri, 10 Apr 2026 00:51:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 10 Apr 2026 00:51:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 10 Apr 2026 00:51:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 10 Apr 2026 00:51:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecfd0096cf42a4b346149c8884e2883a5327fa6421d13906fd62b73146a1a3f`  
		Last Modified: Fri, 10 Apr 2026 00:51:58 GMT  
		Size: 93.8 MB (93781481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad0fbf3e1ecbbf0669e4b03587f323afb7aa3575a91846d71ba266a05e6c6a6`  
		Last Modified: Fri, 10 Apr 2026 00:51:55 GMT  
		Size: 18.0 MB (17961351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49023ada903b3d745ee4badf76fe5f8237ac7f8f22171c166a11b59e4ef0a61b`  
		Last Modified: Fri, 10 Apr 2026 00:51:55 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0988cb60a31b7a53e9235db8a37da9fe5d517cfa9eea999a0425c94d53f105c`  
		Last Modified: Fri, 10 Apr 2026 00:51:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4a550b25d562baf13d4bae4f5df6625e860c82268536792bc2256ce390d48ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23964c1ee89d86656d448c66f0ad6971eb597c3d2d50c6c34e36b57b23671548`

```dockerfile
```

-	Layers:
	-	`sha256:cb790e2d783cc96aabd8e94b0d076548802e58426684300727f43b3299d08c2c`  
		Last Modified: Thu, 16 Apr 2026 03:15:45 GMT  
		Size: 2.7 MB (2681323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:818a12b7092d3fe89de578253a7b497f1818ac2845d5b2ddf006b3ec83222840`  
		Last Modified: Thu, 16 Apr 2026 03:15:45 GMT  
		Size: 18.4 KB (18440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d6c3808cf3ea0a8ec52e6baaf4989c7d7da5d173b0913cfcd1e653c05afdb0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139379447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1124e3f0a35c871f7994bc1cc43f4091d34575ea03aa262cc92404568fefff9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 09 Apr 2026 23:45:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:45:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:45:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:45:01 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 09 Apr 2026 23:45:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 09 Apr 2026 23:45:01 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:46:09 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:46:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:46:09 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:46:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:46:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:46:12 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:46:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37956ed1201c9f27285d3d4f966a731d8f7ce39846b58d097d35d447fa5c8676`  
		Last Modified: Thu, 09 Apr 2026 23:45:45 GMT  
		Size: 90.5 MB (90547693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de407e24ed72f8d0f0d528664eb1aca11d8fd7378a535390bed3cc5328f30123`  
		Last Modified: Thu, 16 Apr 2026 00:46:26 GMT  
		Size: 17.4 MB (17421954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2108c1211edfb39692aac3eed12f9434e91fa4a865ebc91fed79d831e3b77d`  
		Last Modified: Thu, 16 Apr 2026 00:46:26 GMT  
		Size: 4.5 MB (4517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98063b8b39936156d6de6e4b1c3d09f7d2704d74f9cc37173296d78d4351efc`  
		Last Modified: Thu, 16 Apr 2026 00:46:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8056d835cacacbaa1baae1e1276a5be13bc579d1285ffe05a5c3ef45ae32bcc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2690950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9788c0ba36f72a23e7713d8914270a70d069fd40533975efda5d6fbb3a0e714`

```dockerfile
```

-	Layers:
	-	`sha256:d38d2cfb60836c41398a1b3b32e37e31fbcd78626b09f85c58ceada400d52180`  
		Last Modified: Thu, 16 Apr 2026 00:46:25 GMT  
		Size: 2.7 MB (2672554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4364a700b1848fd8cc739122e783ccfc293bd4fd26e3ab9a22c2c1e5de645765`  
		Last Modified: Thu, 16 Apr 2026 00:46:25 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json
