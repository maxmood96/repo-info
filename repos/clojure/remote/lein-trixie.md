## `clojure:lein-trixie`

```console
$ docker pull clojure@sha256:94e1a16292156f6c047727175c0705462c574da0fa571222566a74ecdc747e9e
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

### `clojure:lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:ce623723590bbd46b02a4e34bb8a4d1c8a123d5718fd9686793769b28133f9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164657458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe4577cacfac281c357482820b8aa1f5c301f76ef9f7780a2156a6892e5d7f4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:16:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:16:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:16:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:16:58 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:16:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:16:58 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:17:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:17:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:17:14 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:17:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:17:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:17:16 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:17:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2496ed1e29eec9017750f73aef5ce4c3097faa7d8d34431b52201dd8acf95cf2`  
		Last Modified: Tue, 07 Apr 2026 03:17:39 GMT  
		Size: 92.3 MB (92256235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa430de1c69b198b9aa02447c09e3b12907875f6f606b203c267d1a36917617`  
		Last Modified: Tue, 07 Apr 2026 03:17:37 GMT  
		Size: 18.6 MB (18585208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a9b3f60610a7db53f47f984f69bd65ffff210fd9388d0ab8b1ae34045ce05f`  
		Last Modified: Tue, 07 Apr 2026 03:17:36 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d3381e8b768aceca3479401b328dd54de15041c7056017f02427f52b0eb366`  
		Last Modified: Tue, 07 Apr 2026 03:17:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8521ce2420473aced4dc4d5f32ef9a7b1b80fe35fa8c0ba7bde3f43287811cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3802538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290def5a06d53659212457ba2579781ad9ee92180c5009413a4e25175f2f27d5`

```dockerfile
```

-	Layers:
	-	`sha256:d70ca678569525634272ae86f55e72e54b29cb081e9fcdca3736fe1ba38f25b9`  
		Last Modified: Tue, 07 Apr 2026 03:17:36 GMT  
		Size: 3.8 MB (3783559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d381762d0e9bb5ddcaa602474f09a387f836330ee57dd1729f411c8703c3d6ae`  
		Last Modified: Tue, 07 Apr 2026 03:17:36 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:59f2ae122d94600fed86e002e868c200aec24050cd402896ad5369f8bc473e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164016491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230c4bacc509631d7306d13957fcf1b6ff4d7395e61135a3e23c93fc6a12855a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:27:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:27:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:27:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:27:43 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:27:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:27:43 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:28:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:28:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:28:00 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:28:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:28:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:28:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:28:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9250c3f0757a91ab7cf362ad18e9df3df7c5f7eab290ce1e3deee518e8c68f7d`  
		Last Modified: Tue, 07 Apr 2026 03:28:20 GMT  
		Size: 91.3 MB (91288266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b670a55a0bb65ccdca3d42a65386cdb5a3ba82597e268f80ccb4a089b58c6e`  
		Last Modified: Tue, 07 Apr 2026 03:28:19 GMT  
		Size: 18.5 MB (18544828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37ea67006eb4f9ccda93654776946573378d1bf06d3fc93ddbcc5431897dc09`  
		Last Modified: Tue, 07 Apr 2026 03:28:18 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640b3c85215a699e6a86083c180e0bb5c82f3696bb78d9f641c769cb10e7dff`  
		Last Modified: Tue, 07 Apr 2026 03:28:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b693f9198f5ff8c26a56131bee8b5d3cec9772a2785dda8c8fc31b67c7a8342f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393d1303af12a6ac74135234954d66dfec2a01404d85e1c3eb52ed56c759eccc`

```dockerfile
```

-	Layers:
	-	`sha256:8d3b896ef2ffbed31b65bac54aad5559fd0ae70a35ee0bba2898e5f169cf8018`  
		Last Modified: Tue, 07 Apr 2026 03:28:18 GMT  
		Size: 3.8 MB (3784457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61fa7fc5198b30e9857fb5c1246db8349dc2b896729e8181de04088cbeec9919`  
		Last Modified: Tue, 07 Apr 2026 03:28:18 GMT  
		Size: 19.1 KB (19124 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:bc067fdd557129b78641a93f74af15d4bf56728c85df1866c723d96d5086cb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167910134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e08b9f794a415a8b89fc9bc47693d8964e5f30ea5896d4c2ca94f0408eee79`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:45:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:45:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:45:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:45:53 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 18:45:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 18:45:54 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:46:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:46:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:46:35 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:46:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:46:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:46:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:46:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57dcd2e20d0ba59a0ceda7d174daf8edc831e31e2d722a352fbe87f7cac9ae5d`  
		Last Modified: Tue, 17 Mar 2026 18:47:13 GMT  
		Size: 91.6 MB (91632901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9482206034e5374f9e7c61a9d73a80bf5c5bc2316f12baa807cc19d87a93393`  
		Last Modified: Tue, 17 Mar 2026 18:47:11 GMT  
		Size: 18.6 MB (18640739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39d98aac8be0c9a4147959fe2d893a778d58a2de9036aaef0708ef09ba25c18`  
		Last Modified: Tue, 17 Mar 2026 18:47:10 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e402c1c1abe40369ee3111ca75c31b757ba81fc69aea656e88e90733f29cd03a`  
		Last Modified: Tue, 17 Mar 2026 18:47:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:27a1526970eccfdb16c9bf8c69ae79dfc420b233dd5ba199c7d5de9abbe7f111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7847b5b235e01a6071273b8c91b7ef46b560c5847aaced87ce11e4a95207bde`

```dockerfile
```

-	Layers:
	-	`sha256:fd2b992d5b4617ed23aad37cf124701d591db7b9b77ff186acda70ce7bdfa5da`  
		Last Modified: Tue, 17 Mar 2026 18:47:10 GMT  
		Size: 3.8 MB (3767883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d28d3622939342870566886ca1a315ef6694f9548e3e771910a5e3b1798952`  
		Last Modified: Tue, 17 Mar 2026 18:47:10 GMT  
		Size: 19.0 KB (19033 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:ec360eaf0c41f5aee82727b827a035dec24886aa802640f890dd40df3fb1ff91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161621598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0714abf912905a19f66224c94902a39b28a298c96a322d309cde93c6c09146`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Sun, 22 Mar 2026 19:27:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Mar 2026 19:27:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 22 Mar 2026 19:27:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Mar 2026 19:27:56 GMT
ENV LEIN_VERSION=2.12.0
# Sun, 22 Mar 2026 19:27:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sun, 22 Mar 2026 19:27:57 GMT
WORKDIR /tmp
# Sun, 22 Mar 2026 19:29:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sun, 22 Mar 2026 19:29:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sun, 22 Mar 2026 19:29:31 GMT
ENV LEIN_ROOT=1
# Sun, 22 Mar 2026 19:29:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sun, 22 Mar 2026 19:29:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 22 Mar 2026 19:29:48 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 22 Mar 2026 19:29:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:90acba8ac92ad141ae919a99e64549b2f417e5b2ec79f1a99dbc8efba0fea96b`  
		Last Modified: Mon, 16 Mar 2026 22:09:11 GMT  
		Size: 47.8 MB (47792328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45c9549b3fd22069333772ff17a0ac1235b4853c85fca137130bf290f6f49b1`  
		Last Modified: Sun, 22 Mar 2026 19:33:35 GMT  
		Size: 90.8 MB (90773420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62952e36997a82b558bb88cd1eb56f7475ddc6cd9e385bd12e9ad59fd0e9ee1a`  
		Last Modified: Sun, 22 Mar 2026 19:33:24 GMT  
		Size: 18.5 MB (18537640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcfade903762f5c9059d61d4883e1c269145f75873568018e7bf832b0137fad`  
		Last Modified: Sun, 22 Mar 2026 19:33:20 GMT  
		Size: 4.5 MB (4517782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44daf5efe080b554ff20bfff1c69ec112c391114727d02d20c1809b6585ebe95`  
		Last Modified: Sun, 22 Mar 2026 19:33:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bbea51163d22bc2cf83e5f7638bde5d1316f4c8a78af1c74c6dc01a8e9d103ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6223dfcde3107659a87976d6b4f2e783c4bdbbff1d82186c5bc483a1a41c12a0`

```dockerfile
```

-	Layers:
	-	`sha256:cc89220eb71d0f4ed92f78997f491b7bb2a346947325f16c2363d8abe355739c`  
		Last Modified: Sun, 22 Mar 2026 19:33:19 GMT  
		Size: 3.8 MB (3756059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f263e597e4b8e1809357cf99934d864c4c8814329479cc3f02ac36ed6f377618`  
		Last Modified: Sun, 22 Mar 2026 19:33:17 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:e451a46d571547235314f338135381220a7f482f8d2d8a3279969de5ed5fc422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160743293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c949b081bd5b70b1d3a287ca4c14d454fa50921b4d6b72294b3363bfaebbf3a7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:47:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:47:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:47:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:47:01 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:47:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:47:01 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:47:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:47:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:47:14 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:47:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:47:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:47:16 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:47:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c7eaa8c8a23a104ac473d92c9eba2cdd5fc44ea35fb00b4d090212fff5e828`  
		Last Modified: Tue, 07 Apr 2026 05:47:41 GMT  
		Size: 88.2 MB (88233796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c2754e72fe32268825b0c1f304e87efbf9b930686e378dda1db6f0109ad8f9`  
		Last Modified: Tue, 07 Apr 2026 05:47:40 GMT  
		Size: 18.6 MB (18626264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38d80d503ebe19faed0fd8d3ffa6bac7412c78f11b0b000c893ba12cecb8c72`  
		Last Modified: Tue, 07 Apr 2026 05:47:39 GMT  
		Size: 4.5 MB (4517700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7127ca8fb80534a9973ab4d90925bd42ac40168facdde34f27f1d4d0d3cf9d3e`  
		Last Modified: Tue, 07 Apr 2026 05:47:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0d499e1bf941d51ee283ebb6509bc4cf636c463673983cd1629eee9fd3fb7713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5691ddf87148aa032dd576d475554765fbbc0ac8245367af7bc3f22fa9067042`

```dockerfile
```

-	Layers:
	-	`sha256:72768497cc5beb6e019616ca72545ca18f69627b0900986f18b81edaf3d241d4`  
		Last Modified: Tue, 07 Apr 2026 05:47:39 GMT  
		Size: 3.8 MB (3764548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bc1da66d7b35419190f1d857d7cb6f1c57704b551f8617d074309fb6a4b5945`  
		Last Modified: Tue, 07 Apr 2026 05:47:39 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json
