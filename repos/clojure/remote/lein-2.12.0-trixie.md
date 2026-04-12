## `clojure:lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:ff8e07f11df6a06707cdbac08c0dd13475c9ee3d85589fcbad7b7c772a25fc86
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

### `clojure:lein-2.12.0-trixie` - unknown; unknown

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

### `clojure:lein-2.12.0-trixie` - linux; arm64 variant v8

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

### `clojure:lein-2.12.0-trixie` - unknown; unknown

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

### `clojure:lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:77336e75da62daccbb2f72a0bfeb1d2179cd9d25642845318c8ced898fb4d589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167910708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b57a62eab1e09ea30ce026c8248b49b70f1e63d48e5c91af66309ebe600e1c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:55:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:55:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:55:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:55:46 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:55:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:55:46 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:56:27 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:56:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:56:27 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:56:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:56:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:56:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:56:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3326c6b4216bde98266a981f1f1fb92f86315b90e8c006d1aadb7310dd7d4f`  
		Last Modified: Tue, 07 Apr 2026 14:57:06 GMT  
		Size: 91.6 MB (91633006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eaf73ccf363dc5d7e17b6f8ea485aeadda89dd8be7835e22357db372361009`  
		Last Modified: Tue, 07 Apr 2026 14:57:04 GMT  
		Size: 18.6 MB (18640848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dfd6a4d46d38cbf23175c56eab1146bb55fec1cf47e53d5e6e7fca111383b4`  
		Last Modified: Tue, 07 Apr 2026 14:57:04 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e197b634a019470f3b59a99faf0cd40862cc41660290141059b4601b776400`  
		Last Modified: Tue, 07 Apr 2026 14:57:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ee93fbd79dcb4a62f7e51b35bd10428d0bb2ccedd10a5b754e3b32a3df9d1a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a56f751a59196cc5a5f424fea5202fea94e0c78c40e3029ad5293abb5396d73`

```dockerfile
```

-	Layers:
	-	`sha256:6f10cf71430827e85a6cc3c2493ed0ca0684e3dfa2d04904a6eb97325d779dc4`  
		Last Modified: Tue, 07 Apr 2026 14:57:03 GMT  
		Size: 3.8 MB (3767883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d000359060b419b618749956428de3011e907e2f0eb79f2264ad3d86ce43d02e`  
		Last Modified: Tue, 07 Apr 2026 14:57:03 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:65e004b7b404793fef4fefd47b1f1be89638bb2e7d19c5f4ceac411e8dc83f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164780419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95425362c462b6d3fdeb0b1d4307602ff9ba155b3bd6bf6ee0dcb4c1e858305`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 22:33:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 22:33:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 22:33:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 22:33:17 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 11 Apr 2026 22:33:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 11 Apr 2026 22:33:17 GMT
WORKDIR /tmp
# Sat, 11 Apr 2026 22:34:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 11 Apr 2026 22:34:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 11 Apr 2026 22:34:52 GMT
ENV LEIN_ROOT=1
# Sat, 11 Apr 2026 22:35:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 11 Apr 2026 22:35:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 11 Apr 2026 22:35:09 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 11 Apr 2026 22:35:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7224fd307fae2068f62ccce22d637a96c5204dea7af1d7b9116b5323460f86`  
		Last Modified: Sat, 11 Apr 2026 22:38:56 GMT  
		Size: 90.8 MB (90773425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3cee8b7858b6e47a6142136700e3a8c00971ca2899b3e905d79cf95926ef27`  
		Last Modified: Sat, 11 Apr 2026 22:38:46 GMT  
		Size: 21.7 MB (21696155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca377022b8af3a58916923f4fdd929aa705a15a0725212b93712ff7be44a253`  
		Last Modified: Sat, 11 Apr 2026 22:38:41 GMT  
		Size: 4.5 MB (4517783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4899f012572b5a96438d13f91ee2fc973c7f36c565fcfbf1e72cf05a02ba0b45`  
		Last Modified: Sat, 11 Apr 2026 22:38:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ade6fcb3d67049d0a3c5bc90050def8e7352c218c423833cbb6a3a966784e5da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ccf68ed424dee997b234c9aab2bb8faaf8fe13b2716b9da1811e5f27834da6a`

```dockerfile
```

-	Layers:
	-	`sha256:7b92c7045a34f98036522ef013f25497e4e9478ca2e367c87366dd82ec91d533`  
		Last Modified: Sat, 11 Apr 2026 22:38:41 GMT  
		Size: 3.8 MB (3756059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce5c4511cc11635b411c9071f1f590820b3d03c011f5ab9c3d3d07cb09d9ff65`  
		Last Modified: Sat, 11 Apr 2026 22:38:39 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie` - linux; s390x

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

### `clojure:lein-2.12.0-trixie` - unknown; unknown

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
