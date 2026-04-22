## `clojure:temurin-21-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:b13a313523d9c49e52bdf40ae7ee34cb62baea7f527ef7483dbb08097c5f2559
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

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:15f6822c06e2a0adc5d36fc68161154b428f777b8b79cc7981e72498373ac107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230670404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7189c7f478f642636fbb6c064f3f345bc2d8bf4a282b636badcb8a3ae0de97bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:19:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:04 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:19:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:19:05 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:19 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:19:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:19:19 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:19:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:19:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:19:20 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:19:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70639dbe883abd9164d9209cfa5dae977a3d26ba1adbf7c007dc1175f1c41ce8`  
		Last Modified: Wed, 22 Apr 2026 02:19:41 GMT  
		Size: 157.9 MB (157857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d287f06fcd3be1badf8ef5703cf1e15c79de73fad1c1c0193c694f804d1845`  
		Last Modified: Wed, 22 Apr 2026 02:19:38 GMT  
		Size: 19.8 MB (19806559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93d47c0491d08cd5ec82236ba418e5d8af646f142da8953dba1449a910a3b88`  
		Last Modified: Wed, 22 Apr 2026 02:19:38 GMT  
		Size: 4.5 MB (4517709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f654fac9c12e9800a18039372896eb618a33af446fdd5b341e98e45a3eb894c9`  
		Last Modified: Wed, 22 Apr 2026 02:19:37 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2bca790bc48ba8a22967496a9572b039bb76343e8ed60d398457454c9aec37a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d854521f9d94e2a0b9ed9b87f5039885e9e9ca6417b1e47c1f8877b982671f0e`

```dockerfile
```

-	Layers:
	-	`sha256:355e862d1230521f5168809b8688b9b6c70b4b0945db8b8d7d9527f71097eada`  
		Last Modified: Wed, 22 Apr 2026 02:19:38 GMT  
		Size: 4.3 MB (4284233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efcd5a445d1d22156b59d973f29b3d5ac0a942a6ea150dddc987d0d0404940bd`  
		Last Modified: Wed, 22 Apr 2026 02:19:37 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4b6746123baf90ae4561f2428c2901e8570dbb3b43f83d72ef26a675e0ec3d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228661301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e970a9c91394531050fc846e4b364ea1266ab483e4ea497c4ae878b15b25c57`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:22:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:29 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:22:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:22:29 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:43 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:22:43 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:22:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:22:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:45 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c887a62fcdd2ad5d4147ea49511fcef8f46f03302bc709f7b1eb2f3739fb43`  
		Last Modified: Wed, 22 Apr 2026 02:23:07 GMT  
		Size: 156.1 MB (156133044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154413109723423cabbb0763056d84b1932a97a03228a98dce6cee91e66c96f2`  
		Last Modified: Wed, 22 Apr 2026 02:23:04 GMT  
		Size: 19.6 MB (19637048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc16bf29685fd19ffc30d632478a4ce4993a2d7f61180efe627e07fa3fbd6b4`  
		Last Modified: Wed, 22 Apr 2026 02:23:03 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c896f5e6de077a3f6a39d20fab5194421f0d0170fa0597b21934b57afa67f71`  
		Last Modified: Wed, 22 Apr 2026 02:23:03 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9da654173ef4bd8409d2de8079566388b4ff811888aad975417c0b297f2a8218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e69584bfe283bb18ac9865754ba6935f4e6d4c714a044c55fb38d670b2c3f76`

```dockerfile
```

-	Layers:
	-	`sha256:45e3ee6f5f43a974060b84f830e3ecec07e8568b9be4d11be757029f75d10c0c`  
		Last Modified: Wed, 22 Apr 2026 02:23:03 GMT  
		Size: 4.3 MB (4283872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8915fda0956a8f648c371d6fc0246718d25b1d9e4313dccc12f2569a99ea5d3`  
		Last Modified: Wed, 22 Apr 2026 02:23:02 GMT  
		Size: 19.2 KB (19163 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:6fcba32cbe6b436ff7c1dbc3a7ba0fb477186e184b8abdf44a9db9cd896782cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234863178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b1a67fd073d50592e7d9e90f519123350b29f4db46492c4dcc81e6d08c8ace`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:58:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:58:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:58:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:58:26 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 02:58:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 02:58:27 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:59:08 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 02:59:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 02:59:08 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 02:59:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 02:59:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 02:59:13 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 02:59:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1250e3e4882e6e928fe5b248de7b760cd787cd434e4a4d31f63aa8ed6c00e040`  
		Last Modified: Thu, 16 Apr 2026 02:59:56 GMT  
		Size: 158.0 MB (157977483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52eced50255b2445be26e4ba9df905a56248404bc70ba6178c98f13bd03295c5`  
		Last Modified: Thu, 16 Apr 2026 02:59:53 GMT  
		Size: 20.0 MB (20030586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1211ab31bf1635607a5eb61b82eeb9a6dc5b4d0e784b686ada9f6e7b677e9ae5`  
		Last Modified: Thu, 16 Apr 2026 02:59:52 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8560b9b1965701f61c7c0a43cbffedd0a23f752f95fc912b4c72d04856612bfa`  
		Last Modified: Thu, 16 Apr 2026 02:59:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:711296dc3f078cc14353e8366076207c7ec601c9bdb96b3f423594de91e56b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe3c570a69f594ad46c8b5dac848af2dacefe33e6e67226685dbef847fa444`

```dockerfile
```

-	Layers:
	-	`sha256:6c38707655e273a08f8f9b6a0eb5fd8b4021665bab877bed556b510c46d44939`  
		Last Modified: Thu, 16 Apr 2026 02:59:52 GMT  
		Size: 4.3 MB (4286106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc286ef5160a3760b56097ee4580716250ab8f85aac31c9258461b720f4a5e20`  
		Last Modified: Thu, 16 Apr 2026 02:59:51 GMT  
		Size: 19.1 KB (19074 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:01682b605d8c6344528535c68d0810dd93d9f5a9e30a9c51bb0f9a7ccbe1a256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218238162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95dc2be0e1161f099e4efbf44a95b0359859ce9b5b5a741f650eb52ed7e7d02`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 04:02:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:02:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:02:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:02:51 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 04:02:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 04:02:51 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:03:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 04:03:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 04:03:03 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 04:03:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 04:03:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:03:05 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:03:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823a94a034a486e2e5ad070f6a03cf5992927682e92a4d8ac4bb69d1ed8dc2bb`  
		Last Modified: Wed, 22 Apr 2026 04:03:34 GMT  
		Size: 147.1 MB (147105251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fc716cc5c406fab87a4a83e76effed44345382cfd45668eafb82a50d40a387`  
		Last Modified: Wed, 22 Apr 2026 04:03:31 GMT  
		Size: 19.5 MB (19466776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625e0c3b42156b7a9bb7d872cdb6e38a221487c81bfd86a4568f05302d14ed0d`  
		Last Modified: Wed, 22 Apr 2026 04:03:31 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255d14a2f90b312bb672a0228cb78c26add9aa6b5189c2fd24225329d823a78e`  
		Last Modified: Wed, 22 Apr 2026 04:03:31 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dc093c7a24de859e11bf1f318f4c29edc6016bb9001ec756c3f25fd73191c21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4295065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26cd8f2868f8445ea52f8805e532a8a9892453c4a1a9206ec77dccf394d930bf`

```dockerfile
```

-	Layers:
	-	`sha256:670590443c28bd6764c80bfe606adf2408d4f58a65707d866f08f63a840c9f69`  
		Last Modified: Wed, 22 Apr 2026 04:03:31 GMT  
		Size: 4.3 MB (4276047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:814dae891cd2d3e9001782abafab911244b0c235880f1ec3f1eafbd8c76bc572`  
		Last Modified: Wed, 22 Apr 2026 04:03:31 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json
