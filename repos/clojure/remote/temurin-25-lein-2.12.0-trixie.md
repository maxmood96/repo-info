## `clojure:temurin-25-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:ba95d1431d1068a9a31274aa2f3261e89028104f37ea9940a8ca416b3c5aa3a2
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

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:0651b32cabf42d5ed1e8e982ba9e867419fd897b909c2859ff7c6dbd264bc6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164662093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829f686bacd3b64fa0f5e1d1f8f1c4b2c99be2cd2bfdb62e067e1c1857b03d40`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:20:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:20:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:20:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:20:38 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:20:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:20:38 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:54 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:20:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:20:54 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:20:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:20:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:20:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:20:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb90a96c39decb67de5153339d3819d71ef9ad7fceee2b44dacd5f913103a83`  
		Last Modified: Wed, 22 Apr 2026 02:21:11 GMT  
		Size: 92.3 MB (92256281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30ddbe9eb30127df4ef7e56ac8be04b2156314fb8401443c58cd2ef44dafbea`  
		Last Modified: Wed, 22 Apr 2026 02:21:12 GMT  
		Size: 18.6 MB (18585575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc001bf055c1059c2fd605c7aa7bf1f962fef7d67c16505c7548c8796f48a4c`  
		Last Modified: Wed, 22 Apr 2026 02:21:11 GMT  
		Size: 4.5 MB (4517707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211d97af5414d7789fda4fe5e854b151c5986a030f37228142d1601866d01cb7`  
		Last Modified: Wed, 22 Apr 2026 02:21:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:56f5a1cf80dae352d552a0b13c55ecf56a45d3b02c07f6a40f03dfa77fbfee5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3802536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338208bd1db14470fc95b73dd74d8f26df1c95fb32580fe107d78d64ec2d20df`

```dockerfile
```

-	Layers:
	-	`sha256:d21aed32b4a7fd11b6a59cf32f4b3b45583270f9564a394d59278c577a87f5ea`  
		Last Modified: Wed, 22 Apr 2026 02:21:11 GMT  
		Size: 3.8 MB (3783559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5005b81036f29fd24e6666b9a7e2ee5ab1bfb915b12fc663a6015e00a0a05351`  
		Last Modified: Wed, 22 Apr 2026 02:21:11 GMT  
		Size: 19.0 KB (18977 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1e8ee5dfedb476d9aa6be13e2fe1938072399313f30071dd65bdcaa7d695e298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164021123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54197c36c7bf8619a648b80a75201e6ed707dd2fe3865f8be924338623aa987c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:23:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:23:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:23:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:23:30 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:23:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:23:30 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:23:47 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:23:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:23:47 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:23:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:23:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:23:48 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:23:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a9e010f0341f2dc14338bb6bc51107fa8dff0beba846ff50eb45298ad32ae9`  
		Last Modified: Wed, 22 Apr 2026 02:24:07 GMT  
		Size: 91.3 MB (91288309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d3e33b87719f2a60880d53aec65c5e54ce856a3c957efda4929ac0b7f25f03`  
		Last Modified: Wed, 22 Apr 2026 02:24:06 GMT  
		Size: 18.5 MB (18545437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac0280fc079b1947796dccb33a1ae2bbd839c00ca48695ac5034fcad0edc618`  
		Last Modified: Wed, 22 Apr 2026 02:24:05 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbfae368d0925e5cd9e42caf5589e5eaf835de0bb46ab61c4212d7c91b2d732`  
		Last Modified: Wed, 22 Apr 2026 02:24:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2c38d0e9dc71563636010280dcbd7ad07752583b1ea9c69bf3567da92b381a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bff0623b2322c72217df3145c78bff581d34b993fae62d3042275c6fd23075`

```dockerfile
```

-	Layers:
	-	`sha256:721544ac8085befebeeb632914c41ab280ba6a2aaff865b5d52a3c1b16307343`  
		Last Modified: Wed, 22 Apr 2026 02:24:05 GMT  
		Size: 3.8 MB (3784457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a255c6e490362b1ba9b9a0cb70cb6f3a2c388d59806720bb921a3777d7adf23`  
		Last Modified: Wed, 22 Apr 2026 02:24:05 GMT  
		Size: 19.1 KB (19122 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:cd11e08890becacfd03123fb6b071df00cae83ea44e65430b8fef2fd473d8d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171661518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7850dfeb52ee39c580a1bc0e61042954f3b00cd342b683c87f5185e49583af52`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 03:09:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 03:09:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 03:09:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 03:09:31 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 03:09:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 03:09:32 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 03:10:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 03:10:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 03:10:15 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 03:10:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 03:10:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 03:10:20 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 03:10:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04092892db89c3f0f8309ba50439fcd1d5f508bb90c8bab723af681eadbd6ebd`  
		Last Modified: Thu, 16 Apr 2026 03:10:55 GMT  
		Size: 91.6 MB (91633017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbca44cb0a5eda307f010a2768c0737dafb29f4abaa1bc0256bbcddb759fe9ed`  
		Last Modified: Thu, 16 Apr 2026 03:10:54 GMT  
		Size: 22.4 MB (22391696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca84ce05b2824951be14f3207da583520ee1685695f143332fc5571b1857bfbc`  
		Last Modified: Thu, 16 Apr 2026 03:10:53 GMT  
		Size: 4.5 MB (4517706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b87d1322a36e04b5dd8f2de8bd0effdce3649a878efff3b1f0a5111810eeca3`  
		Last Modified: Thu, 16 Apr 2026 03:10:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:686decc61ce0e8026a29bf2995df41f50f24a8a686528519317c3aa9389085be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5782e7946797387a5787d727d98460b9bf8a6d0a2b71a20cd12c43c2f778d6c8`

```dockerfile
```

-	Layers:
	-	`sha256:686f7c3c36203f5ea64a0de0b01ecbc223bfa59d1540a439dea78528cdf50298`  
		Last Modified: Thu, 16 Apr 2026 03:10:52 GMT  
		Size: 3.8 MB (3767883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6717992a73adfbd9287281b06d5df054a1d9e35e37b12f4d4a8433a0c17849dd`  
		Last Modified: Thu, 16 Apr 2026 03:10:52 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:713c62cc62b857e811022dc0ad6021f28159b350ee65a2da977f5433fd233825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164780395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f315c82e2997d52244767062b945bc8e9d9352aca7fbdb86344bc0ba5c30def7`
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
# Sat, 18 Apr 2026 05:20:11 GMT
WORKDIR /tmp
# Sat, 18 Apr 2026 05:21:47 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 18 Apr 2026 05:21:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 18 Apr 2026 05:21:47 GMT
ENV LEIN_ROOT=1
# Sat, 18 Apr 2026 05:22:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 18 Apr 2026 05:22:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 18 Apr 2026 05:22:04 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 18 Apr 2026 05:22:04 GMT
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
	-	`sha256:15f2a30adf76821106329954ef00b07f570d7c752969de531b86703f4c60992e`  
		Last Modified: Sat, 18 Apr 2026 05:24:15 GMT  
		Size: 21.7 MB (21696131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be69aa747a0ee50e3fabba7511388f717a9b3126a43424f447621d5556d52b85`  
		Last Modified: Sat, 18 Apr 2026 05:24:13 GMT  
		Size: 4.5 MB (4517783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d44b60e80530fc5b6865ab25421dcbef5c0af834c53352f463c1044db1c30a`  
		Last Modified: Sat, 18 Apr 2026 05:24:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8d0f63a13ce3b330860b3d37d274908b08f6e3ab7665ad70a7a45be0b2262ad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684ce20a55e8e3b49090e51aed765f3a1a3a605da66e6b2923c612b97affb7cc`

```dockerfile
```

-	Layers:
	-	`sha256:911cfc0a239e5d4ba9a6c035af5f5aab572d76b7288b70822d93ff5d6ab6a521`  
		Last Modified: Sat, 18 Apr 2026 05:24:12 GMT  
		Size: 3.8 MB (3756059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcc5e90a71864fddc8c714c95204fb6308f40cef834169d60a653649e5e88a99`  
		Last Modified: Sat, 18 Apr 2026 05:24:11 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:3abee8c35d4712f34de9d4486f58b96a3721d5c61e9b6e2723763c21fef82cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.9 MB (163899313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba5f9d6900852692b383a204a6d720216a6b4bbe16d3e248183696a2c7a08e6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:44:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:44:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:44:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:44:04 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 00:44:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 00:44:04 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:44:19 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:44:19 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:44:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:44:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:44:21 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:44:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af85e16ff2a5e4ef4e7bca442eaf789074eba5dae2548a5309ae1cc069f92daf`  
		Last Modified: Thu, 16 Apr 2026 00:44:45 GMT  
		Size: 88.2 MB (88233823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8a10788c992ad2a15c6b837b8f02cf3b9493ad6ce66fe94ca1a10846bb9ce6`  
		Last Modified: Thu, 16 Apr 2026 00:44:44 GMT  
		Size: 21.8 MB (21782216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfedf9bfa03913f7768467ecd7a5f175b546a4c287711f6f60987543d110e42`  
		Last Modified: Thu, 16 Apr 2026 00:44:44 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54248441a45a7a3609e83ffe632d3a0798dbb64f87eddb461ae55f6261a4860`  
		Last Modified: Thu, 16 Apr 2026 00:44:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a26d265139c9975cf38a24bf81829c00f93da71d7693703ac2bbbc68e2672b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f818415d6f718bc3fcaa72bfd97d055bca4bc73505d1f246a1b11f41c1ba8e8d`

```dockerfile
```

-	Layers:
	-	`sha256:0f3f902eba7f21f9dc86a7ac6dba3fc141a87b321557c08ee787f1b23dd3f142`  
		Last Modified: Thu, 16 Apr 2026 00:44:44 GMT  
		Size: 3.8 MB (3764548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:353bfa886d97203a41b66ead1912fee372fe94689399f5e2e431bf5ebaef4ee7`  
		Last Modified: Thu, 16 Apr 2026 00:44:44 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json
