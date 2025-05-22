## `clojure:lein-trixie-slim`

```console
$ docker pull clojure@sha256:eb02a56b5154620ea82f62d5645f5a6ea71a9bb8c150644039c9bf7f98c2e178
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

### `clojure:lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3598bcbe8eea8b59150e2da0290647af1939afbc581d302b97f703b5003bb052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.7 MB (245717755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0f82deb13213ff84ef6b2ba17c1d5870358cc31972ec1c54932806d35239e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Wed, 21 May 2025 22:27:59 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a243254c8a1c79d6d595db3c435c22a40689b85d53a1643d3159feecbaf0251`  
		Last Modified: Wed, 21 May 2025 23:33:23 GMT  
		Size: 157.6 MB (157634544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38cabada45d0a6c8c5eab565056f32878fa19c4e615cc0d0787e617218d2ac34`  
		Last Modified: Wed, 21 May 2025 23:33:21 GMT  
		Size: 53.8 MB (53813196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e31565a88a69c4610477e73c517374d84e118f5a6341803b4ddeeec2ed1b32a`  
		Last Modified: Wed, 21 May 2025 23:33:21 GMT  
		Size: 4.5 MB (4514203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcbbc3001aa4c088f4e3c3f74edc45cc096b877536c0d1b6b0ecd8a789c787c`  
		Last Modified: Wed, 21 May 2025 23:33:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:61e537203cff454d7c520722d6f1a7f6888109d0845e99e2878f812c156a404e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4af59691b8e1f0f8c19575db682c2b0c63a1eb3493388fc0bed35d6ba2c7bbc`

```dockerfile
```

-	Layers:
	-	`sha256:21a81a0765e6a9cf8292e03b08c0fd643232fab94729939120ca626208845c34`  
		Last Modified: Wed, 21 May 2025 23:33:21 GMT  
		Size: 4.2 MB (4167468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e37dca933b1a3fca5f003a912a5a4ca077a642ad57597d4d2bad99c5014a67a`  
		Last Modified: Wed, 21 May 2025 23:33:20 GMT  
		Size: 19.1 KB (19091 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:293918310f2aa1567f743ffd05fa287c411ddacf4672af5cb98c9d4379a3dad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244430793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d971eedb720fad81f2d2b92748c19fd07c6a1d32b7f5f76c0d03b4d537efc0de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d0342bfffaba1a8be0950e44b5334c6cf9a05d9eedd81a042ec7813ac91850a4`  
		Last Modified: Mon, 28 Apr 2025 21:23:36 GMT  
		Size: 30.1 MB (30130233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0151d89edf53b7ee6d783f7001ce04a78ae3663d78e9c1b824dc8cae0849315`  
		Last Modified: Tue, 13 May 2025 18:05:25 GMT  
		Size: 155.9 MB (155928823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b059f5a5b9e090ad53f51e2c8b2af7bc015fa2c97cf7ac967fa4c867072ea35`  
		Last Modified: Tue, 13 May 2025 18:05:20 GMT  
		Size: 53.9 MB (53857109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bc04bc0d0c9ee84c76d3daa87b763b62e85fad347d72f4a77e40e414f5f552`  
		Last Modified: Tue, 13 May 2025 18:05:19 GMT  
		Size: 4.5 MB (4514198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1196ee67c268e62c331626ce114f34f6eaea42100bd77cb701833cf7609bbcb2`  
		Last Modified: Tue, 13 May 2025 18:05:18 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a0c9039f0bc77734d78eb1c5382e2132d55ec40b3c8897e7eed91940f5b08d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4213424288cfb0e493b1ffd2632d4ab38a1bc1641245add00cc89aa0fc83bbf`

```dockerfile
```

-	Layers:
	-	`sha256:10a5370cde779f76a0a4e43bee854e5f0b1bca9a70dde1c262e2032daacec685`  
		Last Modified: Tue, 13 May 2025 18:05:19 GMT  
		Size: 4.1 MB (4129260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9afce782d2a03a822f5ff25c731046bc79c636537c66bc6ec90c5ea067a3468`  
		Last Modified: Tue, 13 May 2025 18:05:18 GMT  
		Size: 19.2 KB (19237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e69f9402e562620ebc4f03962955c4b567d917bb9531e31a0b37f8708f0d3141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254772433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f2fefd0cade4385dd8f1968cbc96dff36300344001e21b891bbfe372606dc9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a739447e8599431e1e4996b4b6d4022822d37eddea9a3737acbea74b8a860d49`  
		Last Modified: Mon, 28 Apr 2025 21:25:59 GMT  
		Size: 33.6 MB (33577694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42b4bcf42e5cf6f5aa92e1672f803cba9978d3d2220c0765df793902e8549a5`  
		Last Modified: Tue, 13 May 2025 19:18:51 GMT  
		Size: 157.8 MB (157804905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c48983f737419bd7532e4b4df2909ed7d59bc3eda2509327ab8656b86a85e2`  
		Last Modified: Tue, 13 May 2025 19:18:48 GMT  
		Size: 58.9 MB (58875242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e67c04d931a28ffef9193d656c2fe5cc47436cc971b6ee3dfcc99b9f8c5bcba`  
		Last Modified: Tue, 13 May 2025 19:18:46 GMT  
		Size: 4.5 MB (4514162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e930260fce53dc63be26e40cf57cf2784a2893ea50d371faa72b0a6871e774`  
		Last Modified: Tue, 13 May 2025 19:18:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8c2e2122f08812c3a4e7b3fc5e94a43f13f1107ede3536930882415019c9551f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e149152df6b9d1d35602a41748a5c9420193dc88beda5b00773730df4eef9c46`

```dockerfile
```

-	Layers:
	-	`sha256:4a9f81ad3653fb9dfbca54ed22d7c62a96b0dbcbaff0342e79f74cd89f1231ba`  
		Last Modified: Tue, 13 May 2025 19:18:47 GMT  
		Size: 4.1 MB (4127460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f02ac5cbccffb3830c6c10b4b0b9e96860a48963e444d90a483831e90027395`  
		Last Modified: Tue, 13 May 2025 19:18:46 GMT  
		Size: 19.1 KB (19148 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:231d4e369092e6e1238b3ac2b6b38cdf172e5946ac981f0a36ee3fe3dda5f1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 MB (239223009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d61b2bfeef63fbcf3f5a82d04b486c89308befa4ff7e72f43196c870ab1488d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f092cb6a76bde9a7b3c337ea49e8a7adec71062dc5df097be99d3975e92bc53a`  
		Last Modified: Wed, 21 May 2025 22:38:21 GMT  
		Size: 28.2 MB (28245354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2f883243c7cda03adcd9f44b58b22feb78b4904813045b15aec217a35b4569`  
		Last Modified: Thu, 22 May 2025 00:12:37 GMT  
		Size: 153.4 MB (153449674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0672f1dcef9efdbd02ac0c1fd100bd081989f16550b529333a4b1ca54e1aac48`  
		Last Modified: Thu, 22 May 2025 00:12:23 GMT  
		Size: 53.0 MB (53013323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c938905aa3f12731ecad915972392a0337ff7a4f8749ab9bd1f337bc36162971`  
		Last Modified: Thu, 22 May 2025 00:12:16 GMT  
		Size: 4.5 MB (4514229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7722ea07e4baf26eb21d9130fd2e0489146cf239b673204ca0e8eb2ecf5a8bef`  
		Last Modified: Thu, 22 May 2025 00:12:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:530c766ba481b1b20ca0adddd0fe8506cfa69e8ae6d878a42da7a4bfb457922f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cdfd2a2c4985170639fba94f6001e021ae839b83148003972c26ac31426901d`

```dockerfile
```

-	Layers:
	-	`sha256:c4c8fef9d69dbb23ec962cbd66fe50520e081f8f41f34b6ae68cbe2f2b19b47f`  
		Last Modified: Thu, 22 May 2025 00:12:16 GMT  
		Size: 4.2 MB (4156859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c603f49e39f053ae1003f7292c77635c7f4ce61314ac9ebb7eb3442e22ecb46`  
		Last Modified: Thu, 22 May 2025 00:12:15 GMT  
		Size: 19.1 KB (19148 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:350705edcd5bb3c51ed8ef39f542719af970670b98d910a718a14a7e4e4f57dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236130000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cddba2ed54dc671d8a798bdf247f969e5d788405d9bc73d10967aeb13fe890f0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7cbda353d6047374e3da60bdf79ae89f8047840010f0964c87a8f2714e146106`  
		Last Modified: Wed, 21 May 2025 22:32:10 GMT  
		Size: 29.8 MB (29829620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4125f64ccd594bf8ca4128edd7e99193b6d38e00c6963505c94cc81277b3aa35`  
		Last Modified: Thu, 22 May 2025 04:00:23 GMT  
		Size: 146.9 MB (146910924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273c8c6e97a817367667a18bc456bd21a6753546e501679ad2fd93fd96771a1d`  
		Last Modified: Thu, 22 May 2025 04:00:22 GMT  
		Size: 54.9 MB (54874893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8c53b85d3eee15dbb8996064c52664c770f5d48bbdb0b8466a937cfee930a1`  
		Last Modified: Thu, 22 May 2025 04:00:21 GMT  
		Size: 4.5 MB (4514135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e5cb89f6de568ee31262ee25fd900d68a233cd8425fe606689fd6a9ac7a217`  
		Last Modified: Thu, 22 May 2025 04:00:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:84179b9e57c5b2dde93c5bd2168d6155e6a520fdd5033e0436b5fa916e610669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4182539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0399ef513d41c2015db7582d9e93147e9bdbfa6ad67ec8ce19a9aba975da14`

```dockerfile
```

-	Layers:
	-	`sha256:c5a429d14c7bb5caa309e8fa1c7c9927c7386079978de7463e214b261d3d510c`  
		Last Modified: Thu, 22 May 2025 04:00:20 GMT  
		Size: 4.2 MB (4163447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:815cb93f3122ab3375f0ba2eaecbf055f725c028dce8364d51a6cfbeb251b1f4`  
		Last Modified: Thu, 22 May 2025 04:00:20 GMT  
		Size: 19.1 KB (19092 bytes)  
		MIME: application/vnd.in-toto+json
