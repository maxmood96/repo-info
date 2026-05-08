## `clojure:temurin-17-lein-trixie-slim`

```console
$ docker pull clojure@sha256:3df5bc80e60d2974e7436657f1be2e2feca6533302b60530239c03dca58873d0
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

### `clojure:temurin-17-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3c12126adb6c6079e6173178c3baa1bc52a4ffb464c0a8c56f4cb1158089ec2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196651824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df940a355e0699027584d74d8b8449410ad8b164ea8fe6bd05a0d2856d51b211`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:07:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:07:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:07:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:07:33 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:07:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:07:33 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:07:49 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:07:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:07:49 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:07:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:07:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:07:51 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:07:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb45019040808fbdb5bf893cbbf1a023c8b9746bbe276cecb677374d851265d7`  
		Last Modified: Fri, 08 May 2026 00:08:12 GMT  
		Size: 145.9 MB (145905487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c04d91a5d0e942861c9007a0738f0c6573a985514fc6a6f08b6f1bf6f5186f`  
		Last Modified: Fri, 08 May 2026 00:08:07 GMT  
		Size: 16.4 MB (16447988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beffd9d0b7891a11e5c20f2a4fdcf9cc132f707e6467fcc1a7823a216c300c7e`  
		Last Modified: Fri, 08 May 2026 00:08:06 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078731f43246a5e218f0e3756a3045323d8fc863879d37bc31b80054a11acb4d`  
		Last Modified: Fri, 08 May 2026 00:08:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e59ce33275512a34b3aa7a905d514d19a5b1d63c09bb0c0e7c8916efb2ece325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126c02806dda3c301758738bbfe7521b0d54eb0db0b098bc8269de881d02809f`

```dockerfile
```

-	Layers:
	-	`sha256:b0c56140468b0bdd8f616a3b48b6aaf319f511130b4fc3ebc8b1adaf38dbdbbe`  
		Last Modified: Fri, 08 May 2026 00:08:07 GMT  
		Size: 2.4 MB (2365415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:692a3d3e9b39d501c7f9e3714c43b11cbd1ce0cdf7c0f191292e739cc1788a1b`  
		Last Modified: Fri, 08 May 2026 00:08:06 GMT  
		Size: 18.5 KB (18541 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:036b1c34e198f6c602d2e7c29200d86691f14664c5a8d9d527189e5b4c585da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 MB (195800100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a28de861300f895648e45d63aa703bcb7c4edcd9e9c456d90149bd45dd5d2d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:09:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:09:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:09:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:09:16 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:09:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:09:16 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:09:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:09:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:09:31 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:09:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:09:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:09:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:09:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405f83b5ec1f6091696f43cd2b637ebaecedb4134c5a3fe59a85a66eec0ef4c2`  
		Last Modified: Fri, 08 May 2026 00:09:51 GMT  
		Size: 144.7 MB (144724334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10476ef344d0a1f8e4cc1139868bf64cac1f5de11aa564c3df2f272b4b447781`  
		Last Modified: Fri, 08 May 2026 00:09:49 GMT  
		Size: 16.4 MB (16413986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8e5006b386cd688f5ae13acf950837fa0d2924403e6c5651b2ed5cf4e7c505`  
		Last Modified: Fri, 08 May 2026 00:09:48 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d65ae232a55e24a0d409d96d68bbcb64e62067deb90106dc9c5e9f0293026b`  
		Last Modified: Fri, 08 May 2026 00:09:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:05b36245cb84a71a1982953e5110fa56d3b0ce382ea21ffd7bd7909d1d3617c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80688f6637b4712f1a498dcd34a84b3e08e5f8c72f64eeaf57f6279a716f1f45`

```dockerfile
```

-	Layers:
	-	`sha256:62e9bf755394076dbf81d511a950b7d2be8f2fcee034badc6eb7ae7fc0abc8c3`  
		Last Modified: Fri, 08 May 2026 00:09:48 GMT  
		Size: 2.4 MB (2365033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2879b854663aa3fbf8d37ed0f4cd86b9275fa5c499ec40abf66a46c5d077a085`  
		Last Modified: Fri, 08 May 2026 00:09:48 GMT  
		Size: 18.7 KB (18661 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:eeb228f1ce920c11920d2c4bc2bd13737707a239c9f5ba7fd04b93d2768f138e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.4 MB (200367799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60f567a0b891a9cde8dba43d3418fdef34c2cde4cb39dedc306f8c5b6be5b62`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:45:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:45:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:45:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:45:58 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:45:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:45:58 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:46:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:46:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:46:32 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:46:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:46:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:46:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:46:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937b7eb5aea1a56bc2fcf2ec92c34b7b899cf187331f6afa218be284e921541e`  
		Last Modified: Fri, 08 May 2026 00:47:15 GMT  
		Size: 145.8 MB (145766229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4a42956f81e38b8bc4413aa8ca0d36e788a04ed725c8516a6ee7ba996ea252`  
		Last Modified: Fri, 08 May 2026 00:47:12 GMT  
		Size: 16.5 MB (16485406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd00e1276de0d5ae9654ff50d26e717239d0dfd342767a400ac2826b24afd8d`  
		Last Modified: Fri, 08 May 2026 00:47:11 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e402ca0a7ebfaa69739b879ffb332c1364d04707a2fcb788a1ea51368fe3f16`  
		Last Modified: Fri, 08 May 2026 00:47:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cace51be528c597d12b3c31b5efb5d59f6ca3ddd6bb434df58bcd024cc7f9f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7578b009a217340b07eaafdb19e96297ea65574b9134af9a603b3c912da623`

```dockerfile
```

-	Layers:
	-	`sha256:e642e4eae4d723ca168adc6e0258e3254b9241da63b04797f640d3227c9e26b2`  
		Last Modified: Fri, 08 May 2026 00:47:11 GMT  
		Size: 2.4 MB (2366395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16232767b72c0c083c6fb1357424f2833f20ff9993bf3bc1dc0a1f1e84989f0a`  
		Last Modified: Fri, 08 May 2026 00:47:11 GMT  
		Size: 18.6 KB (18584 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:f061e3a46c2867c60e62b9aceeed551d5b6f7d4f0dd9cb5a6d18bb8e85926280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191859448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977485e2efb1353503f3ac6180bbe46d961c9250c1f4b1ca693336b52d3e1a40`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 17:48:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Apr 2026 17:48:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 24 Apr 2026 17:48:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 17:48:07 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 24 Apr 2026 17:48:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 24 Apr 2026 17:48:08 GMT
WORKDIR /tmp
# Fri, 24 Apr 2026 17:49:43 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 24 Apr 2026 17:49:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 24 Apr 2026 17:49:43 GMT
ENV LEIN_ROOT=1
# Fri, 24 Apr 2026 17:49:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 24 Apr 2026 17:49:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 24 Apr 2026 17:49:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 24 Apr 2026 17:49:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839a829e8fec6662efa3cab7ad2470690879a00890c2cd0f31b7ec868d89805f`  
		Last Modified: Fri, 24 Apr 2026 17:53:53 GMT  
		Size: 142.7 MB (142662943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a63cb7f24431be7843c560553bfc41fd321192fa7ace6c612a765eaf4478edc`  
		Last Modified: Fri, 24 Apr 2026 17:53:35 GMT  
		Size: 16.4 MB (16398086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5393fbb19d4380082fdf0f934a236944b80689cb977467b59f0afda874f740a`  
		Last Modified: Fri, 24 Apr 2026 17:53:32 GMT  
		Size: 4.5 MB (4517794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4452329a97615c454a49f949ef3448a69bcd310d8a5e5724505f027657a99d23`  
		Last Modified: Fri, 24 Apr 2026 17:53:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2ecc0bc4f738d47dd14b25a2fa0d3a7e2d3e03687a1b834ad422cd27691de715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d06150b11a8737b614cade529c32d54a0e5af48f342b31f35fd53a01237eb`

```dockerfile
```

-	Layers:
	-	`sha256:12b7cb006b8da21e6dccde98de8a8feb86e4d42c10bfcf97f7bebf4f442248d0`  
		Last Modified: Fri, 24 Apr 2026 17:53:31 GMT  
		Size: 2.4 MB (2354917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dc82aa0e0053ea9bc25c2e23df8e1085aa5b49f5b20ab9d265709775b1bfd2e`  
		Last Modified: Fri, 24 Apr 2026 17:53:29 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:deac9a19b4e6e6ef12f6546ccdd5c73f29a8c40c04e56236cf30be3e770736eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186752696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b648ad332ca9b51b29bdcfc82327ea3b44cd7dea3e6213664c79d8cd8aeab9a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:29:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:29:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:29:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:29:12 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:29:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:29:12 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:29:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:29:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:29:27 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:29:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:29:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:29:30 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:29:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1204112e814d55c55f0da727a3a795092e81572bbf3cddeca01025615533783f`  
		Last Modified: Fri, 08 May 2026 00:29:56 GMT  
		Size: 135.9 MB (135910433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b932a402a9e900351c58387906cb2de2726b66797c7a0421219f00bbd087b64d`  
		Last Modified: Fri, 08 May 2026 00:29:54 GMT  
		Size: 16.5 MB (16483785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b74eb8f269bfec1a7225e10e32ac835abc669639e6db12c9b25516b0ca0af8`  
		Last Modified: Fri, 08 May 2026 00:29:53 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab252a2de7b92cc43112652b62d97ff89a4165cf628b9fad9c65962a9e774dfb`  
		Last Modified: Fri, 08 May 2026 00:29:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:864fb99594b46f05f2855caeb2e74b599d3689dc44f3128423c731db45383c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e327934e58ff5f17e1ab43abc3d360e17282426ebf4a982689de91320043cf4`

```dockerfile
```

-	Layers:
	-	`sha256:b1b6aee2b229fb097052f15891d22f0869c30dff26e89729af7578917b449006`  
		Last Modified: Fri, 08 May 2026 00:29:53 GMT  
		Size: 2.4 MB (2361842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:920986303469cd7c867fd0349003471fe8391b88080dffdca85e676d4735d633`  
		Last Modified: Fri, 08 May 2026 00:29:53 GMT  
		Size: 18.5 KB (18541 bytes)  
		MIME: application/vnd.in-toto+json
