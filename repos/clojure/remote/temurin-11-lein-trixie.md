## `clojure:temurin-11-lein-trixie`

```console
$ docker pull clojure@sha256:1999d247ca9d25f1e82743a68f2a0df50bc068f0628b2a46bad208e35f2d3a93
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

### `clojure:temurin-11-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:696efe2e1bf5f8da45db1c33df41f5a639007cec197bdb81b90d470161148262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218291662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db45eae2c8be30673362a5b156810562e7b83b7c1120b0550d90b63466c29ea`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:06:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:06:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:06:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:06:16 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:06:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:06:16 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:06:32 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:06:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:06:32 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:06:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:06:33 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a6ae4dc4731fc00c215b9baa7c42405100db9aa74941c672de144cbbeb4a7f`  
		Last Modified: Fri, 08 May 2026 00:06:53 GMT  
		Size: 145.9 MB (145886193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f3c337d0e4deabe31a5aa12ceaef91e41d663e77c0da0552a8cb4d0c4686d2`  
		Last Modified: Fri, 08 May 2026 00:06:49 GMT  
		Size: 18.6 MB (18585632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e07cce2aaabc41c95b604f96ef562c6b10e2d380362491299ff1341d647ae3`  
		Last Modified: Fri, 08 May 2026 00:06:48 GMT  
		Size: 4.5 MB (4517703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ab24c454d489ef253b6cc0352cb13a87a1a6e1ade63e9285c04a7cc0dfcab8df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa817fb399c4da61d0015f9f8a8ebfb89e7b75ded753f27c9dc4645ded01ce5`

```dockerfile
```

-	Layers:
	-	`sha256:23dae0719dbfbb91aa4fe787b9bb4720ed18520a5548143fc40ac4152cfb6381`  
		Last Modified: Fri, 08 May 2026 00:06:49 GMT  
		Size: 3.8 MB (3835670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c4b6486aa5a91e22b8aad35c83e42476a83eca7e664f6b7b6b9f12345657c52`  
		Last Modified: Fri, 08 May 2026 00:06:49 GMT  
		Size: 16.5 KB (16515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3ab457d875aed389de6edd9b0d00b62344580490a475f457e58ec0750c45d9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215314600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca6007b51c6216259d5a504611815099c5709a759fd8fb2594601e8ef5bee6c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:07:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:07:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:07:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:07:59 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:07:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:07:59 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:08:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:08:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:08:15 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:08:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:08:16 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875f2dc580635744be052b927dc99c7a229ffaae07d9c7f101ddcb551e6f2885`  
		Last Modified: Fri, 08 May 2026 00:08:37 GMT  
		Size: 142.6 MB (142582244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13c3f5c1241e7fb0d6e82d68cb68278e596fdb022a733f855a930b1d210cfa3`  
		Last Modified: Fri, 08 May 2026 00:08:34 GMT  
		Size: 18.5 MB (18545365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc776cb0990eaae2ee507584b3c3a8491cb153727a45b9b1803e675e5052c621`  
		Last Modified: Fri, 08 May 2026 00:08:33 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:39239ab1dc6ee65009a303e56b7915d44284cbb0daa15d658119acf654686055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcc088620bdd266c3bb25579b486a02bbc3a5e9ec33765b2f8f65c14d3f6c75`

```dockerfile
```

-	Layers:
	-	`sha256:e5a9990a7e634fe81d8af63e580f2fc2f64669d3a9795e7c320d331d44ef0466`  
		Last Modified: Fri, 08 May 2026 00:08:33 GMT  
		Size: 3.8 MB (3837165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e73febe75b6bf0d7deec2adb620f1c591bf30cdf13b0d0889d55e573daff27d5`  
		Last Modified: Fri, 08 May 2026 00:08:33 GMT  
		Size: 16.6 KB (16638 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:956a463a2e882101e6ff84fde7f7181c18daa2b70710b08b698489572594bfb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.4 MB (209391973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d450f4e773d233de902fb7af7f0da2f064f85828fee34fb7648d3319faf22961`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:38:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:38:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:38:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:38:54 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:38:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:38:54 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:39:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:39:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:39:35 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:39:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:39:38 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd298a1e1654753929706776995581c6d8e0ae8db97ccd3dd0cbc779069c0bd6`  
		Last Modified: Fri, 08 May 2026 00:40:09 GMT  
		Size: 133.1 MB (133110194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4e759d1eb620b89303f1147e757db529c3bbb6ff3d84fc771f24eaffb505f5`  
		Last Modified: Fri, 08 May 2026 00:40:08 GMT  
		Size: 18.6 MB (18641010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03de2819446d9f9d05500f33321506f944cb4c25ddc7f02b6e7ca356b0e7792a`  
		Last Modified: Fri, 08 May 2026 00:40:07 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:dd344254df58ff6c6dc43e51d7da3b0fbe501b4d4e02595d936be441d3b5d603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d743dc65034f55ff73f2e00fecd17c1bcaa80a6ded178151e97dbaeaac1a89`

```dockerfile
```

-	Layers:
	-	`sha256:941f4b2869572606c7f6221edb7cfb35c8f1b6925d7513d60e77d02dd3c405c0`  
		Last Modified: Fri, 08 May 2026 00:40:09 GMT  
		Size: 3.8 MB (3836055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abfdba560acc017d6915845369835d5f3728692f493a70d01a84dd4f33e052da`  
		Last Modified: Fri, 08 May 2026 00:40:07 GMT  
		Size: 16.6 KB (16562 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:2d57cb1358e21616037aeb7fac34ce9d80d333b140d9b56dbc481c9950c1790b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199169317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2785c19a43f025337a80736c06a0c394993376f0fbf8caf8a58bb40eb3fd4add`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 29 Apr 2026 23:13:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:13:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:13:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:13:53 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:13:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:13:53 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:14:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:14:11 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:14:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:14:13 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3e96a498eedeba06f7eeeef03757ec4a5de489cdb2735c62011540f27ec753`  
		Last Modified: Wed, 29 Apr 2026 23:14:39 GMT  
		Size: 126.7 MB (126652714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d900321ae0c64c69e1e6539c1f1a0da4e0f902966e1018136bc628056ba905`  
		Last Modified: Wed, 29 Apr 2026 23:14:37 GMT  
		Size: 18.6 MB (18626705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e51f7901d0e61751a68dc6c15d35cbd3f377cfd405f270d41f69a86958853a7`  
		Last Modified: Wed, 29 Apr 2026 23:14:37 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:da9f7b6f4b30519c30359392e945b66ab353e1ac6cff28af3e79934bc0dd3d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3848465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8173e214b1497abc78fdca9b67b8e2934f55743be6ba0d488f6b07b254ed124e`

```dockerfile
```

-	Layers:
	-	`sha256:db15ad82c9bc7bcba9573bdfb4cf5e219303005270eed0b0793177e7888e7591`  
		Last Modified: Wed, 29 Apr 2026 23:14:36 GMT  
		Size: 3.8 MB (3832101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b180d4e68e3f32f2942a6904279e7c94dba63b9c183ca9431c6758452635fde`  
		Last Modified: Wed, 29 Apr 2026 23:14:36 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json
