## `clojure:temurin-17-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:531d137d6c8dd8506ce58853286200fe4bfb1960b541fa1532b728ccf8d00472
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

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:a2f96eff458c71b679a91ba4f84c7cf935b7bfe357695ce279710dcd6e8a6e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.1 MB (217069404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d0df23a4986f9bdbc8952c949bc690b432f27893d21238c61f648626897f66`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425c312e445f6044b3c8a1cd0a637e1f544bdab53ea1991c44dba64041d95c60`  
		Last Modified: Sat, 13 Sep 2025 06:39:43 GMT  
		Size: 144.7 MB (144693322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707bf9ce3b965dbfd5d13da4d550972a6eeefe6a8dd11859a83bbc65a30c7e32`  
		Last Modified: Sat, 13 Sep 2025 00:03:57 GMT  
		Size: 18.6 MB (18578406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b3bdb118ce8e8aae9d37479577942aab9068bc7d03eba4cc5d1a2cd7486c69`  
		Last Modified: Sat, 13 Sep 2025 00:03:56 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6544be365da2c0363c67fe7a2ce83dc726412eeb0c636e71af4027e682327c24`  
		Last Modified: Sat, 13 Sep 2025 00:03:56 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a094029bbd0340ba069626722a4638fd973e626cea1e09b66d0424fb96c3b48b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d00bd3eb5b13a7cf2a14956862381b4bd604e3b11cded004c9ce85b47107f4f`

```dockerfile
```

-	Layers:
	-	`sha256:c3b3e48e574bf7e09629059048be7eb528a94cb5a0b4675563e2021f191ba6ca`  
		Last Modified: Sat, 13 Sep 2025 00:39:12 GMT  
		Size: 3.8 MB (3813330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:427f3226b1d71379f81a891fa46eb1a6447cbcdbcd9b8f8754edb26498c908f6`  
		Last Modified: Sat, 13 Sep 2025 00:39:13 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:329c3d8ac6b9d279cab40af630ed27ffdb5a14ff05bb4bd1c7d6100ed1e06d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216243228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5276655f903408a08da0c9a9a532774c5167edb86debac112e883806f3cc53`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f8ea90d2ef8afaacdfac1b2444dba853ecc7b89fd6bb6c176789f7004dad6f`  
		Last Modified: Sat, 13 Sep 2025 00:15:38 GMT  
		Size: 143.5 MB (143542151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b67ed9b47b3785d81c3d03d36906af4815ceb269ad89962b940b452046ad9e`  
		Last Modified: Sat, 13 Sep 2025 00:15:49 GMT  
		Size: 18.5 MB (18539184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa468128550d68f14bf33e06059db8524debbfd88c92264771c144b0737a9749`  
		Last Modified: Sat, 13 Sep 2025 00:15:47 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27310fbe67adcf364ad2224700b74a98cdfb91212ff257aae3825dc215af6e6`  
		Last Modified: Sat, 13 Sep 2025 00:15:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7e97a7a595eb0c614be47eb5a5773a4fb27cd97ac87cd2d2ea430796fdcff481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39c51343673275e256edf2cf64c0e0e41fabff6ad76e94ff3159d5368b91df7`

```dockerfile
```

-	Layers:
	-	`sha256:0dd74e6a97133df6ec83ef60dfbdaf6847060c6d9a6627464886179becfe2310`  
		Last Modified: Sat, 13 Sep 2025 03:37:53 GMT  
		Size: 3.8 MB (3814207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12a0bdaf81d12f425b6363117cbbab26624483fe4f2f467bc183ba6c4be12e3`  
		Last Modified: Sat, 13 Sep 2025 03:37:54 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:062b95b58d2fba48e9f4c955406553dfd945f171c4aef5f2ee524c967c2187a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220631295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f776844af58c7dd95e5acbcbb2d2647ead3a23b842f91d17b88be1eff8e24f7e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2554eb7f6493ae88deb07829ba1e159b21d1f74f78eed32a7119694c61531e`  
		Last Modified: Sat, 13 Sep 2025 03:38:59 GMT  
		Size: 144.4 MB (144372675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce53b319239ded4b2de0fb76efce5693dda74e436cedddb56dd04e9c8a4b9f9`  
		Last Modified: Sat, 13 Sep 2025 03:39:28 GMT  
		Size: 18.6 MB (18636037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba65079cabaa0353e5e9e9a4425fa3e9a4269abdd514f8e28fd2aae5252e196`  
		Last Modified: Sat, 13 Sep 2025 03:39:27 GMT  
		Size: 4.5 MB (4517720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a21f64d53674f8257e4cd6f229ffac34b8bc38cd496942aa45f4d4ae0dc7d8`  
		Last Modified: Sat, 13 Sep 2025 03:39:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9ea8d10bbb4a2ac6591b92966e94127075f181a9fe744c68cf9a36aab2f1ba55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f0aab7383f984ec894357dfc3f479e69dcc97928fe79ff270570f17781d2bd`

```dockerfile
```

-	Layers:
	-	`sha256:f435228ade8fa71448b6b9aeba09d51fd39dd27a495528d9f3c4e51c2f698454`  
		Last Modified: Sat, 13 Sep 2025 06:37:26 GMT  
		Size: 3.8 MB (3814328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85af075e04936ef0d7ef0274837cfbabbb0bb10cb5fa8651bd164f6f143e60bc`  
		Last Modified: Sat, 13 Sep 2025 06:37:27 GMT  
		Size: 18.4 KB (18439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:418c9cda459cbd708a666462e9beffb08a5946bba11d10707cd40801613ac5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207208555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb84be05b36da893b68fb63fad93b003f7b007086ee864c7b05b696910dd1e62`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3b65478feef64f886be1fb528c0198a5250fd24e4b0192c43ba359ec4eaf1a`  
		Last Modified: Fri, 12 Sep 2025 23:53:05 GMT  
		Size: 134.7 MB (134724301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c6d2b0444083ab0b88c21365304adb72402efb5d497ab182dac3ee49bf5b22`  
		Last Modified: Sat, 13 Sep 2025 03:11:31 GMT  
		Size: 18.6 MB (18619783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9598fb352bcb09e0b1691e35be89a2fed97cbcc7029f85d9c577da5985d43283`  
		Last Modified: Sat, 13 Sep 2025 03:11:30 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3982f770d4cc789f2b8cd80d5bb90522e099d9d69a32eb7c0d8aef7e87389b`  
		Last Modified: Sat, 13 Sep 2025 03:11:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:224ebac88e419ad3e16ae1c026cb0598db78eccd3ccbdb77d7525a7a067b6369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3828152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55ded9a34d79b1bca58e6991ed16361c6e9757e2d5314b9a06e3a9fe4877ded`

```dockerfile
```

-	Layers:
	-	`sha256:96817b110e8ce006df03cbee911daacbe53ee7cfe44afa1a651b341223248ffc`  
		Last Modified: Sat, 13 Sep 2025 06:37:31 GMT  
		Size: 3.8 MB (3809757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b5e933946bb79871d76263afd57eecde3ccb768ef3e04bebe2c956dcc868d7`  
		Last Modified: Sat, 13 Sep 2025 06:37:31 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json
