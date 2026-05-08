## `clojure:temurin-21-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:522bcd0530ef678410395f44060801c9ec62a3f8d3a3f952dc2a72282008500f
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

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f2c36d7cf7283c884ca7623221a46822a4b2bfd886331ee857fbfb97c02e8973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208603436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f208dde12fb33be54e1887546748658f5ae65ee336d7dbb53ed5bf3fb4c610`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:19:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:43 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:19:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:19:43 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:59 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:19:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:19:59 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:20:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:20:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:20:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:20:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e72bb403d9782bb56d35711d545701e6745ab31da83fa0baaf4bac1c44b438`  
		Last Modified: Wed, 22 Apr 2026 02:20:20 GMT  
		Size: 157.9 MB (157857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ca8ad8a750b4b700f28f3b9014cda09d0ccd22dac7e5b097944897ce223a45`  
		Last Modified: Wed, 22 Apr 2026 02:20:17 GMT  
		Size: 16.4 MB (16448023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3501434d406c3b5b5754836cc2719281b941f356ed2280e2d959141a0da0fe30`  
		Last Modified: Wed, 22 Apr 2026 02:20:16 GMT  
		Size: 4.5 MB (4517730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a37e7d98c2401dd4e0e3b748628cc1ec1bfadd930394b72aefd9389f60ba8b`  
		Last Modified: Wed, 22 Apr 2026 02:20:16 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:846551bf079506d922bc7165a14b97eb30e4e8c685d508564e776d8a86091902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd516b178d6159f2f6ca665cd093fabad10ec7fa77e4f03d9e473d01a5e731e`

```dockerfile
```

-	Layers:
	-	`sha256:4ddab77d943730f05d97ddf6fb3a268e810f28202ae86634522fbbc856494d55`  
		Last Modified: Wed, 22 Apr 2026 02:20:16 GMT  
		Size: 2.4 MB (2366640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:333b1de6201f23219e82d85e35167a18e370fb60178bb2ad63f4e77dd082afec`  
		Last Modified: Wed, 22 Apr 2026 02:20:16 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:531edc025899fe0ba9c6698e9de50ab89c073457da5816c9240d8984e52d05c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.5 MB (207536885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb67158d43a72123c77df0b31c749d4235fabdeda0d79ff659cfbcacc5030fd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:18:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:18:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:18:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:18:38 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:18:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:26:05 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:26:21 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:26:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:26:21 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:26:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:26:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:26:22 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:26:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df17385b598228bc3b13941999aec82b7dc64412fe80f40e13a945e15e4dfba`  
		Last Modified: Fri, 08 May 2026 00:19:43 GMT  
		Size: 156.5 MB (156461167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6fcc662284c89ff5c09e64a52bcad218a5f8aab8fb5c6ce69485cc47402b2b`  
		Last Modified: Fri, 08 May 2026 00:26:31 GMT  
		Size: 16.4 MB (16413971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d5391f333fc47d758ec1800063c11cf4e9a82c03d76ce388056574e7e14fd5`  
		Last Modified: Fri, 08 May 2026 00:26:31 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b856eed30c5736e802112c02619951abd2b014d17794afcc8bc3929a44433c`  
		Last Modified: Fri, 08 May 2026 00:26:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f14af5f58404dea1a08e9f4745e0f95004afb78561995442007856a0524d135c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a98e62525103933772696f7d393347fb37b3154a721d87de723470d17f767f`

```dockerfile
```

-	Layers:
	-	`sha256:89d69aacd3f5b992bbdf6c5bc1a165372d6214b1393d0f891c3ef579c5f3cff7`  
		Last Modified: Fri, 08 May 2026 00:26:31 GMT  
		Size: 2.4 MB (2366885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fd99736258fbbf9e5bbd7cca27aa84a1fb25ed741191b229d370561f9d0f518`  
		Last Modified: Fri, 08 May 2026 00:26:31 GMT  
		Size: 17.7 KB (17707 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:62e015b936df6f0cf7830c6bd5ece7279a375e5419cea197dbb290a2e13a1aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212944826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e6e5183d16d27db9fb495712eae4882dfbe6d131169602e4e8129b1071190b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 01:38:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:38:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:38:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:38:54 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 01:38:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 01:38:54 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:39:23 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 01:39:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 01:39:23 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 01:39:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 01:39:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:39:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:39:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679bdccfa02f117dfdaab6da4f7459875679357ae8fcbf2cafce50f771adcbf9`  
		Last Modified: Fri, 08 May 2026 01:40:03 GMT  
		Size: 158.3 MB (158343276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544d9c50ffe221e97993945b4660fe347c8bf0f59d46ca77c095fa10c39306f7`  
		Last Modified: Fri, 08 May 2026 01:39:59 GMT  
		Size: 16.5 MB (16485320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91009bfb5dbcd6ead45b8dda16b4f64ff909a0859196332f6a9061915628cadb`  
		Last Modified: Fri, 08 May 2026 01:39:58 GMT  
		Size: 4.5 MB (4517769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d197722788e50b115ca414d93771efb8a2bd7473ed37b1e9bbfeeee8bdbc4417`  
		Last Modified: Fri, 08 May 2026 01:39:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:41adaddee77d877711f16cd13a0d734b66576cb1a32e7e42c49650c8bd62b3fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eeadeed099372cce0d741f067201887ccac643049972bc456c3ac4ac37628fe`

```dockerfile
```

-	Layers:
	-	`sha256:3a49c42941bdb28d942a49b58d40f24f422a79fb1852e55bac0a555977a43922`  
		Last Modified: Fri, 08 May 2026 01:39:58 GMT  
		Size: 2.4 MB (2368247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9142ab09e7a15c14aecbdf3def194e5beaffc8011ba820dbadfd3b6819bb25b8`  
		Last Modified: Fri, 08 May 2026 01:39:58 GMT  
		Size: 18.6 KB (18585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:b3e5249c60e1ab16f6739bb1a53dd26dd0a35d1006a9b8036e14b33ed1331fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206413440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0d94ca7d63dd701d6239946f0c74f9b2414cfc414bdbc515a438aee1acc79c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 18:16:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Apr 2026 18:16:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 24 Apr 2026 18:16:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 18:16:48 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 24 Apr 2026 18:16:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 24 Apr 2026 18:16:49 GMT
WORKDIR /tmp
# Fri, 24 Apr 2026 18:18:22 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 24 Apr 2026 18:18:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 24 Apr 2026 18:18:22 GMT
ENV LEIN_ROOT=1
# Fri, 24 Apr 2026 18:18:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 24 Apr 2026 18:18:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 24 Apr 2026 18:18:37 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 24 Apr 2026 18:18:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad178a1c7448a34e9758387fe35c9fb467bae057770eff7c342592f312ccf326`  
		Last Modified: Fri, 24 Apr 2026 18:22:57 GMT  
		Size: 157.2 MB (157216929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d8d5bb99659ac446823bd986ba7aaebb4359d8245f51a158267b5fb9836090`  
		Last Modified: Fri, 24 Apr 2026 18:22:37 GMT  
		Size: 16.4 MB (16398105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed686f3e67b722a06180ab7dc921dbdb821a832d2dc2c4012668608966f06962`  
		Last Modified: Fri, 24 Apr 2026 18:22:34 GMT  
		Size: 4.5 MB (4517783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdc0929a98b5977e836091e1728431a5f0643531a73781aa0b844f6c5d65d0e`  
		Last Modified: Fri, 24 Apr 2026 18:22:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:83eac27c2435ef3f9fdb5c4e332cdf41674ade244acb58d2447dc86a0c59d7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2432a564daf558b97d26b1125dae5ebded413b703ab84e590298a095dd1f912`

```dockerfile
```

-	Layers:
	-	`sha256:8ec030d455dfa553e88eea42a437e49c5c78a73cb3a6c354701356e6de9c5a54`  
		Last Modified: Fri, 24 Apr 2026 18:22:33 GMT  
		Size: 2.4 MB (2358688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38d112fb32dff53d527d532d219cc28fa70443c447724962a4b21381e7424af2`  
		Last Modified: Fri, 24 Apr 2026 18:22:32 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ea909dd681f07bb802d8fde14f8fc73e2a75192ac76d59ba89c985273ad1abc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197947580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e15426b516320fbd87bf02ba4d1a62131c58d66ce1e0e29c81c85ed2c91da9c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 04:03:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:03:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:03:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:03:16 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 04:03:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 04:03:16 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:03:29 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 04:03:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 04:03:29 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 04:03:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 04:03:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:03:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:03:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc13e0424f9cc62cbd79bd2740a0337d43290a60f702b3f4c6b3ca57b188dac`  
		Last Modified: Wed, 22 Apr 2026 04:03:57 GMT  
		Size: 147.1 MB (147105211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefd825e80f3756285616747e84d082d20b2c0d341c740af95d744f15dc9376a`  
		Last Modified: Wed, 22 Apr 2026 04:03:55 GMT  
		Size: 16.5 MB (16483893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8dd0e94805bb7cd8aaa97da4305bb82c0b6ab97da6f2c82136f5fae0bbe8d`  
		Last Modified: Wed, 22 Apr 2026 04:03:54 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3fbf5333dcd457d84d2455b8e21a0a9b5712a390dcdcc0c831f70f6c100f67`  
		Last Modified: Wed, 22 Apr 2026 04:03:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dde72b1e3be0d16fcc6e2737a574177813afc76575d5f38c4f26ec071e527210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36e578312b7176a4c3a92b10e845c8c8b20ba6487dbb7d1d9dbb3a3552ecdcd`

```dockerfile
```

-	Layers:
	-	`sha256:34cd4e2651618ab7d0c60c7888fc663c3a82aef8e4afed7711d51557565e19b9`  
		Last Modified: Wed, 22 Apr 2026 04:03:54 GMT  
		Size: 2.4 MB (2363067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb6e721edd3d60047d1cdaec0b6a0a28fbd2702d323207baec64002952253ee4`  
		Last Modified: Wed, 22 Apr 2026 04:03:54 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
