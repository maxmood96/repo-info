## `clojure:temurin-11-lein-trixie`

```console
$ docker pull clojure@sha256:b644c1d0dfc111a9aed2e05b0946722a6b92e08bbee2d76b138d3d01231b9def
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
$ docker pull clojure@sha256:7431b2e8b2dde2184a477cb5cd91858235302cba3f5c7b7867ee953777d9a603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.8 MB (265823203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6418b7c17c37991b28eccf714677745aa9a9b01b7da0fac044ebfb26c784d3c8`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
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
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f8c8542523ef5c08ca9bd5ab7d7265d12930a45ccc7c8364e909fde03c894479`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 49.2 MB (49248239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf71a1837af1bb180ec5f8c40bd47d51258240dc294422248e47edf7dc570c2`  
		Last Modified: Sat, 17 May 2025 13:51:17 GMT  
		Size: 145.6 MB (145635735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853a460f95b0cc592b387381b8cc3a8afb92e25ac306108ffaa881478b9af9ec`  
		Last Modified: Sat, 17 May 2025 13:51:12 GMT  
		Size: 66.4 MB (66424997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2065c0a7d4c0c57a204839a82baf4602a2595d2c1d276cd4a5c836dc1f7c7ac6`  
		Last Modified: Sat, 17 May 2025 13:51:00 GMT  
		Size: 4.5 MB (4514200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2d10148f0e7585f8c0690c439a795dd2dc797c2b9ab10c5541b578d824ac8f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6321794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6f7803ab39c5e145453fdd0c99ae9fb72da594111d36da7eb5e3ae945791f3`

```dockerfile
```

-	Layers:
	-	`sha256:eb6d52983d6341dec824ba7e9a145c5c63d071557eb8fd39b7011ba51e81adee`  
		Last Modified: Tue, 13 May 2025 17:53:54 GMT  
		Size: 6.3 MB (6305377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf34f753cffb6725b2272b9fba9bbbc6f16856b5cf2744f17823ad67715bb23d`  
		Last Modified: Tue, 13 May 2025 17:53:54 GMT  
		Size: 16.4 KB (16417 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:addc8800ddf319bb4037664dde89415da4199d0d31ee71c264d29459535f1944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263015932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49baa4afb426d4caa99da7011e40d0b9401b9d7c5bd5468ab678bea3fa3f112b`
-	Default Command: `["lein","repl"]`

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
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:288a1cecb0ea762427d39b072c1ca965d193e927e04da652f7b21eb12e9b2acd`  
		Last Modified: Thu, 08 May 2025 17:11:50 GMT  
		Size: 49.6 MB (49624118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa81e2617996b590287af40ced269fbafb204b4143062c93006401b1b1e34c4`  
		Last Modified: Tue, 13 May 2025 17:57:09 GMT  
		Size: 142.4 MB (142420736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e76af499736aed70f6dc035bb40cb351abcb1b41ec8ecf253b61153d0cf8fd`  
		Last Modified: Tue, 13 May 2025 17:57:08 GMT  
		Size: 66.5 MB (66456836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d7b1099e52dfba8cb19b24e0a545240bb49d08d16a37c453654f4f384b90c9`  
		Last Modified: Tue, 13 May 2025 17:57:06 GMT  
		Size: 4.5 MB (4514210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:75d0712023a10d84cc8a915deb5fc0feabf3292698421ae36ac749d85e9ab977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6329498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab99e7aa985b47b267cd3ca94600e65fb0e84efdfd75c2a4ea954e425ed7bd4f`

```dockerfile
```

-	Layers:
	-	`sha256:b60a7129405e852415a0e5bca28bf820041396db4532380c3af14a89ee209a55`  
		Last Modified: Tue, 13 May 2025 17:57:06 GMT  
		Size: 6.3 MB (6312958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5908894cd6b62943c60027f12e5fcd6e66036e02735cfac2ceb7bda18e8a9b0`  
		Last Modified: Tue, 13 May 2025 17:57:05 GMT  
		Size: 16.5 KB (16540 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d4473a635e299fadd148e670496924819bc319b123c16e3e63a95ea92c1398c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.9 MB (261902349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d5ff9adef3329121a5fb7aa1d7589498cb8061932c9b1249b960133343a4855`
-	Default Command: `["lein","repl"]`

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
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:03ebb30bb37cd398ea8ab1a268c301664089cf5a54d23466e4338782afb5f9cf`  
		Last Modified: Fri, 09 May 2025 00:28:48 GMT  
		Size: 53.1 MB (53072552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cae647bc37778358b907d22b7bf35eb9da015bfb7b8a8800a879a20173b410d`  
		Last Modified: Tue, 13 May 2025 18:34:18 GMT  
		Size: 132.8 MB (132809833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c90060580e27738b033c4ee605daa0bbfcb6ee12f17b0ef71d4c842d5d5d18`  
		Last Modified: Tue, 13 May 2025 18:34:16 GMT  
		Size: 71.5 MB (71505787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25c92bcc16969ce7c9ed74c555aaec51bfbf7db699cec7a209f170f11dd9fc0`  
		Last Modified: Tue, 13 May 2025 18:34:14 GMT  
		Size: 4.5 MB (4514145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:14e9abd82210f2f9b87792422ad05016cdf06f8501a33d391c309095f731d86f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6325179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19858226099baa3c5e7d676ff31fd27d14593f391b5b0fa397c2dacc4309cba1`

```dockerfile
```

-	Layers:
	-	`sha256:e4ac7c1ca2551d361c4400420ba5c69ff35416389fe6e0271e77b35a568379ee`  
		Last Modified: Tue, 13 May 2025 18:34:14 GMT  
		Size: 6.3 MB (6308716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b7e8914301e93df755a8038f320f49eb12a632522f7bd8fc1482465e20e624a`  
		Last Modified: Tue, 13 May 2025 18:34:13 GMT  
		Size: 16.5 KB (16463 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:8433b6dfd2c2dd55e274482f6dc13ce19d2f0e90446d14cfaa7286ce37f520a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246917482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e220bb165a26d4fe5a038aa861d0f986ced8a66a5e750811bdf366d400924a32`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1745798400'
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
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:e1ec3b1570f7d822c5a6aa013529484429ad99bde8495d827b56c3603992fd3c`  
		Last Modified: Mon, 28 Apr 2025 21:11:06 GMT  
		Size: 49.3 MB (49316646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30965b6dc7dc6f235e602cd0f410e0e3efa7a40e49d969d8b610ce2a574addf`  
		Last Modified: Tue, 13 May 2025 17:59:51 GMT  
		Size: 125.6 MB (125585838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021969b94c2421d75779100faeb38e6c69ed14aa73ada005450f4729075cec6a`  
		Last Modified: Tue, 13 May 2025 17:59:51 GMT  
		Size: 67.5 MB (67500748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5ca196b19746d493cdab1eb4f89f88107c389e2dc3fe0d0e642ef841a05e58`  
		Last Modified: Tue, 13 May 2025 17:59:49 GMT  
		Size: 4.5 MB (4514218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9c6407ed849207aa029f964c9f2fe69c84918c9ff170bdda1e192cfe5da6026a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6317777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d17ba448c5c1b7a015060df131905e8cf95c2fd57ec1950c0a73b6b6c4df0fc`

```dockerfile
```

-	Layers:
	-	`sha256:b0ae44eea1db44c7a9578991d33f4197f8f770275958204ae32f3528f31a9b05`  
		Last Modified: Tue, 13 May 2025 17:59:49 GMT  
		Size: 6.3 MB (6301358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:920932c4599f1c4f209c85fee9c147f824bd1a9ab07fb840cc3cccc0ec106365`  
		Last Modified: Tue, 13 May 2025 17:59:49 GMT  
		Size: 16.4 KB (16419 bytes)  
		MIME: application/vnd.in-toto+json
