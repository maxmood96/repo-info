## `clojure:lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:fd39a9e614be312ac3e76c1c37b06b0700fddffb015140551945405f05b6bc11
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

### `clojure:lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:fcb0cf7e5873d21147af683e7d63976e054ac71226cb8e91d7c5d9396a6ca432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164428847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581b022cb5ee9cc7c7c99bdfa3d3ba85fa492075b6636a072c4520019bf3e24c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:04:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:04:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:04:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:04:38 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 02:04:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 02:04:38 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:04:54 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 02:04:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 02:04:54 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 02:04:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 02:04:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:04:56 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:04:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0ba47ac0ddf265d4f442e5d121697b7e4b2a2a0dd546a5947c324f31e88fcf`  
		Last Modified: Sat, 17 Jan 2026 12:36:46 GMT  
		Size: 92.0 MB (92045294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174e25958f9e1439c6625362c62d3503d7f228b49d92bae37d23fab09ddf8f3a`  
		Last Modified: Fri, 16 Jan 2026 02:05:12 GMT  
		Size: 18.6 MB (18579785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4dd012bf94603ad79a0a9de36ebf39fdd16bbbd6ac7cbcbbb4e42d5f05cedd`  
		Last Modified: Fri, 16 Jan 2026 02:05:12 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091825c3211a3d85afa85ee7e36581bd934929ded1ec9551b0538c3cfdce43a2`  
		Last Modified: Fri, 16 Jan 2026 02:05:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1082c906c68e10f19a6e0cd644253804658cfd198996fbc49acc486612086623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1f0eac67a5b7405abb45e39f0f82fe9eada97cc174e3d05bc704230d1601d3`

```dockerfile
```

-	Layers:
	-	`sha256:8a80df8d90ccbd75f456ba86e73c2d8bd1a95e4571ca90a9b972c12b78578abf`  
		Last Modified: Fri, 16 Jan 2026 04:35:52 GMT  
		Size: 3.8 MB (3765535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee414af03a058800b7ae051c2a090015d1d50756e987c49b87f7f406c15b25c5`  
		Last Modified: Fri, 16 Jan 2026 02:05:11 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8bcb9e7c92299bf5d7d6b79d603ae6487deae8ea9112af7a048f4d804008cea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163759426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749eadc7dddf366b4a937f7bba5f9570d3aa93ff659623c5668b75e9b6656d13`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:09:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:09:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:09:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:09:57 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 02:09:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 02:09:57 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:10:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 02:10:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 02:10:14 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 02:10:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 02:10:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:10:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:10:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d6fa6f7e598bf4a51eec1f2009a61688e75b55c510a2c12ae1a194db9f4a7a`  
		Last Modified: Fri, 16 Jan 2026 02:10:35 GMT  
		Size: 91.1 MB (91052478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290527421463eda860e4db84bd80ab11d8c9957cb9b8fa2c7b379d60d9d6b3a7`  
		Last Modified: Fri, 16 Jan 2026 02:10:43 GMT  
		Size: 18.5 MB (18540718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ff3929ae748fa4340f6198a7f93201ac59ce5d2d605d776f746849b66894ec`  
		Last Modified: Fri, 16 Jan 2026 02:10:33 GMT  
		Size: 4.5 MB (4517719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75355e8fd14527d5c0feb3c755eefaebefc592a1899098f5037d6fa8d627a5ae`  
		Last Modified: Fri, 16 Jan 2026 02:10:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d3f4e883ef497a6dccd5ac87936a90ee284b12c94ebb76f49d62e7466ff3ac6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320709faf1dd0c1bb8f6e92c1372a2ba404d116406fe7819d6d4933f226bd60d`

```dockerfile
```

-	Layers:
	-	`sha256:e6a7532a274b64594d967f06046136af525a882ac09c2cb908e75a3370b0e04f`  
		Last Modified: Fri, 16 Jan 2026 02:10:33 GMT  
		Size: 3.8 MB (3766433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd3c8d1800d6bf7e31e3b5c7888179509e9b88c61f0d79f01b824eeda43858d9`  
		Last Modified: Fri, 16 Jan 2026 02:10:33 GMT  
		Size: 19.1 KB (19122 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:3e94456761cea43d8026342fd2e1fea47a9b7f3af76a4a280cd11632245431e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167873226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0ed8b9957631c5df99541e87c8a97cf622689358ae9f3d3ad345d2d5d1cb61`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:44:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:44:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:44:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:44:39 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 03:44:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 03:44:40 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:45:48 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 03:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 03:45:48 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 03:45:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:45:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:45:51 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:45:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1f64ed71cadbfa0fdd0e4e5f9f9173c20301e99b8d557346b7aeda0ac3389c`  
		Last Modified: Fri, 16 Jan 2026 03:46:57 GMT  
		Size: 91.6 MB (91610765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17de3c92287919744b3896a502651763254b80443ce4025570cb8d29b7d9fdd`  
		Last Modified: Fri, 16 Jan 2026 03:46:50 GMT  
		Size: 18.6 MB (18637316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68b67140e39db4d8a9e26a20d33bbc7d2fe60a73644040efdfb23e746d7fc9c`  
		Last Modified: Fri, 16 Jan 2026 03:46:47 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c169d06b9f82c8bb796c446fb810d6ef6583bb58806ca25768d275487220514`  
		Last Modified: Fri, 16 Jan 2026 03:46:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cb38e3290ed4f0ae62d0ef02cdd61a876277c5e116e34e2035ea875a2612e9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7945d60dda0220177b3c81ede2141760c0def9b5d02e12584a92398067d85947`

```dockerfile
```

-	Layers:
	-	`sha256:11a860115e4f50334dfca3588c4e50699092db65b7580bd6ff2ab60e4b403463`  
		Last Modified: Fri, 16 Jan 2026 04:36:03 GMT  
		Size: 3.8 MB (3767845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a8984339237b90de25dad371d70c0ebc0db6c7ee57e91091821fe5a018ac623`  
		Last Modified: Fri, 16 Jan 2026 03:46:37 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:277ce0e3d3699fa794ea22619b2d4d55bfdff5f10bf9d489f745204d47cdcff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161573666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156f7d283f2601a985ab30188f3e94cb80f55104b6a4bef287108b1ec4ee2cdb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 04:29:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jan 2026 04:29:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Jan 2026 04:29:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 04:29:57 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 22 Jan 2026 04:29:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 22 Jan 2026 04:29:57 GMT
WORKDIR /tmp
# Thu, 22 Jan 2026 04:31:27 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 22 Jan 2026 04:31:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 22 Jan 2026 04:31:27 GMT
ENV LEIN_ROOT=1
# Thu, 22 Jan 2026 04:31:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 22 Jan 2026 04:31:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 22 Jan 2026 04:31:43 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 22 Jan 2026 04:31:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:559020494fc8527e77b291bee49cdac1db6bca66f8926cda195e0e4ebe7d2d3d`  
		Last Modified: Tue, 13 Jan 2026 01:06:14 GMT  
		Size: 47.8 MB (47770843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68915c625875c7ea3b1992ce94ece2c2d543657883d1675eb2625132930fbabc`  
		Last Modified: Thu, 22 Jan 2026 04:35:23 GMT  
		Size: 90.8 MB (90752894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f2a0896a57927db666b336f35acaa7313c269f176c919e4f34a21d94233ba7`  
		Last Modified: Thu, 22 Jan 2026 04:35:42 GMT  
		Size: 18.5 MB (18531720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47df26baa9ab0ae7043661e1ff2211fc9beb15c899c46d60101ff0d4e524cee`  
		Last Modified: Thu, 22 Jan 2026 04:35:08 GMT  
		Size: 4.5 MB (4517780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88b8d36a3e8e8a8a52af31f6f2faac052af3424d279b5f1d2cb4a0ebc15bafe`  
		Last Modified: Thu, 22 Jan 2026 04:59:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d01279e35f39fbb9d6b877ecb707c96a9bf32e4906f1ebb117be8c18cc253330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f07dee3ff125b61d25dbeb4ff882af4c6d0e6f4ffe283685cad7d2de127d0a`

```dockerfile
```

-	Layers:
	-	`sha256:8033ae8628aba07cfd6f2a1ed50b445efa5dcb96da8966a0858d763083a9be3f`  
		Last Modified: Thu, 22 Jan 2026 07:34:38 GMT  
		Size: 3.8 MB (3756021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:869613899b4bc31e39b17fa1356a9d1341569a6deb274bbe79dc7f2355d890f5`  
		Last Modified: Thu, 22 Jan 2026 07:34:48 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:efd218827aeef2b3ec6aadb9ba583d0810ab3b186acbf2b9aeca5827770c327f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160698285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58dedaeb79ded95d09b2b9590b9dfb056a83e2d3bc0c88e05e41d0b5095e6fe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:22:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:22:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:22:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:22:58 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:22:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:22:58 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:23:10 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 15 Jan 2026 23:23:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Jan 2026 23:23:10 GMT
ENV LEIN_ROOT=1
# Thu, 15 Jan 2026 23:23:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 15 Jan 2026 23:23:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:23:12 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:23:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9da15375349ed468c4d395178dea5e2fe711fa01064413f4605f3f47af67086`  
		Last Modified: Thu, 15 Jan 2026 23:23:51 GMT  
		Size: 88.2 MB (88210648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87663d8736bc88f37169881f97d4b06cd465ea23476fe5932b4634922906a22f`  
		Last Modified: Thu, 15 Jan 2026 23:23:37 GMT  
		Size: 18.6 MB (18620747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec099c7074d38c6f711e40ce47ff97f5239cdf18cdabb98f37469a9e9cfb87d`  
		Last Modified: Thu, 15 Jan 2026 23:23:36 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced5d24eccc92fa0722be1bf7e484856266bc403e431299d2a9e508867967b61`  
		Last Modified: Thu, 15 Jan 2026 23:23:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:36fa61fa02489ce448197773dafc131166c6794b413754891463009d276b184d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7360462a5ffb707c4329d016451b38ae038de70c45042456b6135ef03d89d515`

```dockerfile
```

-	Layers:
	-	`sha256:950e286bb921887041628127fe32ae86c7bc22d7f1a25ba606b3b214a7ac684d`  
		Last Modified: Thu, 15 Jan 2026 23:23:36 GMT  
		Size: 3.8 MB (3764510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5de2507488f3435093e50e6c061058e82fc79d9151ca3bdd6dff86029a4c6230`  
		Last Modified: Fri, 16 Jan 2026 01:36:20 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json
