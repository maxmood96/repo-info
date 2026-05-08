## `clojure:temurin-25-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:77f9e988f2953793524df00e36c8fa43a9f85a3151e80afecc7a941385e2d9ee
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

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dc3d0e43bc596fc88b97131b850fde2915d94446f9a28050894ad27c0a0ee7a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143321034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce47900a63977d2db59112ecaabfeff9dbe8051a26fd9a9485fd26fb5fd73269`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Thu, 30 Apr 2026 23:53:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:53:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:53:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:53:07 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:53:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:53:07 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:24 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:53:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:53:24 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:53:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 30 Apr 2026 23:53:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:25 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c74bc258cd48701a909d10f02bf0477d4cd697e2e9c30dca617a73abc6c7a1`  
		Last Modified: Thu, 30 Apr 2026 23:53:44 GMT  
		Size: 92.6 MB (92574598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e33d4400ad9d6b1f18410b1b6da93ba6628c65d79bd0a32ec47acf946d02e6`  
		Last Modified: Thu, 30 Apr 2026 23:53:42 GMT  
		Size: 16.4 MB (16448134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0132580e247d831dac1d1fb4e4854814fe67b97f82b08e3d1fbf1eec5da16eed`  
		Last Modified: Thu, 30 Apr 2026 23:53:42 GMT  
		Size: 4.5 MB (4517700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3d0c3552733c62c01a645c2ea7aae074c194da8d25f4590df165bdb1843e58`  
		Last Modified: Thu, 30 Apr 2026 23:53:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3a95466704ee17a8ceab070f212e92958f92c06ef54398c68b94c091929a3dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2352497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3699a8307155e4b9a54c53cd00d7ab0fe5f67e186de3677032433bc51c5994a2`

```dockerfile
```

-	Layers:
	-	`sha256:7bf608ad2785d6174c5c01eca5300c73c0128ab3b88c85691b5d53a32b53e358`  
		Last Modified: Thu, 30 Apr 2026 23:53:42 GMT  
		Size: 2.3 MB (2333463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5842411e0d1b345bbccb4e944368ab4ef993cd539c5337169dda285a995c9558`  
		Last Modified: Thu, 30 Apr 2026 23:53:41 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:94d2a234a72a851cc799cc525a2141f046e8e6a47ade5bfe0a0eb285c0622359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142618069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27c02be9a10d60aba987e06caba37220b220211bab66a0243af972ea6056dcb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:27:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:27:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:27:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:27:31 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:27:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:27:31 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:47 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:27:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:27:47 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:27:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:27:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:49 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef63fd72d72d6a4bfd1012df7e13bb81aca8ddd513978142408f6a271e982c6c`  
		Last Modified: Fri, 08 May 2026 00:28:08 GMT  
		Size: 91.5 MB (91542278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb01d3b1a9f1562f7250d34c67959ded4cd9256018a645deafeb691ce83cf139`  
		Last Modified: Fri, 08 May 2026 00:28:06 GMT  
		Size: 16.4 MB (16414027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d418937c71562a7929dddc6e2973708153645c8aa8ae8d46a2dd7bb4ecfc75`  
		Last Modified: Fri, 08 May 2026 00:28:05 GMT  
		Size: 4.5 MB (4517728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d32a025029891ffca2da17231e880c6e4e8c3f73ab5a27902032a76a091148c`  
		Last Modified: Fri, 08 May 2026 00:28:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:089357b38df0d37e1eb22551df4cf4050cf930adc897dfb2cd6af86a24ef3d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2352435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfb6e3625945aa1a865a6c85e22f4d884fc7ddcbe24ecee91df037ded638621`

```dockerfile
```

-	Layers:
	-	`sha256:02a0057012f7770955aa505135beb49fdc7570a16fec8ccc67aa86a7ff5cf073`  
		Last Modified: Fri, 08 May 2026 00:28:05 GMT  
		Size: 2.3 MB (2333102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32115c75d4de781aad032057bbca9196037e5a24628e6d9e5b0e7dc795831595`  
		Last Modified: Fri, 08 May 2026 00:28:05 GMT  
		Size: 19.3 KB (19333 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:906dac32a818fb20c422075140653ecb2dc3d41327e955f4f0e7ae2500d553af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146515738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd44dc1a2383e703f2e21fedbe290bf49577c6f6ed7bfcc062bab60905ffd56`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 01:45:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:45:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:45:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:45:30 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 01:45:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 01:45:30 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:48:48 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 01:48:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 01:48:48 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 01:48:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 01:48:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:48:52 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:48:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50e227b32fab760ab734a722d523335c702357014ac0ce34693e4421965f3b9`  
		Last Modified: Fri, 08 May 2026 01:49:25 GMT  
		Size: 91.9 MB (91914037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100f7736f5ed81fae07ac846c57fee4619fc248e27f6363faad6b73bdd256b4d`  
		Last Modified: Fri, 08 May 2026 01:49:23 GMT  
		Size: 16.5 MB (16485477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0db791afcb6bb2f6c04ad68571cf32420f2268c1393cd3b72f787e9d34a5de`  
		Last Modified: Fri, 08 May 2026 01:49:23 GMT  
		Size: 4.5 MB (4517763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89a9e8e00b10b0bf35c7e990021dc345f7f9c8bf4ca6513859131004234a768`  
		Last Modified: Fri, 08 May 2026 01:49:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b7fe4cfa91ad21fa80caad0353f5f62d01bff1e3a0a6c16ca2bd0c3da38f7c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2337011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59556a1e073bf30db4e4232a941d931320db333e949af2c3d4e8914535960c4f`

```dockerfile
```

-	Layers:
	-	`sha256:ad9467ebc87e4e54564e3ac64db8bced16307bb0c8fb85523adf78eeba891885`  
		Last Modified: Fri, 08 May 2026 01:49:23 GMT  
		Size: 2.3 MB (2317767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b854abe76d560ebf92581b474797e82c3f82c7bedc2855bb63b39a5e9c51db43`  
		Last Modified: Fri, 08 May 2026 01:49:23 GMT  
		Size: 19.2 KB (19244 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:900cbedf8dca9b67300d5d8bad3769a90379ef10440bfe1cee2fbc89c581559f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140211419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a03af4b185cb035b42ee926157033521029908df8389e3bcce8bc1e45746908`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 01 May 2026 01:17:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 May 2026 01:17:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 01 May 2026 01:17:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 01:17:25 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 01 May 2026 01:17:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 01 May 2026 01:17:25 GMT
WORKDIR /tmp
# Fri, 01 May 2026 01:18:58 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 01 May 2026 01:18:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 01 May 2026 01:18:58 GMT
ENV LEIN_ROOT=1
# Fri, 01 May 2026 01:19:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 01 May 2026 01:19:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 01 May 2026 01:19:14 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 01 May 2026 01:19:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a463537893b115e8f6bf5847dfb28b93d1015ffeaba8f0acf52e10133dfcf3`  
		Last Modified: Fri, 01 May 2026 01:22:48 GMT  
		Size: 91.0 MB (91014937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afe464ad1976fb5b9efa95b108a07377f29e8f3228ca04fa66e55042dbc3650`  
		Last Modified: Fri, 01 May 2026 01:22:37 GMT  
		Size: 16.4 MB (16398071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a825bba06ff3acbd94734a7a0a9e7117dbaa3d9e38b04292a6d5d9b64f0569fb`  
		Last Modified: Fri, 01 May 2026 01:22:33 GMT  
		Size: 4.5 MB (4517787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f019656c71b82322c680c851338fc1e20b860bd07fcf5d51d78722328d87f4aa`  
		Last Modified: Fri, 01 May 2026 01:22:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fa02d2492bd0e379f1278e8347aacc1bb0bf932fad84cb785852a7f466ba9198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2326624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc67c2ee42ff833d0f803f6de0bb83f44dcda2d35ba1758c747e37460e1a3a4`

```dockerfile
```

-	Layers:
	-	`sha256:c2d2a776c55825968393e2e40687efc7c9b8507292060f5393002cc3b4d2b48b`  
		Last Modified: Fri, 01 May 2026 01:22:32 GMT  
		Size: 2.3 MB (2307534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd73606e40f77c5dd00dbd8631ce9b549001ec06fca7d3eac4daa808015b8c49`  
		Last Modified: Fri, 01 May 2026 01:22:31 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:bb4e4d814024423703bd89083a98561e1032048e7a7f64fc4afcd4991d466bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139262629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c79b965c341b94f762e2e377668d42b9508552aceaa2d376853b2c081077f8a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Thu, 30 Apr 2026 23:50:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:50:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:50:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:50:52 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:50:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:50:52 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:51:09 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:51:09 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:51:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 30 Apr 2026 23:51:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:51:11 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:51:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ee46c033b5990060b9acaa5985a11a008290bfbbb27b32d546e2487a9a5e65`  
		Last Modified: Thu, 30 Apr 2026 23:51:37 GMT  
		Size: 88.4 MB (88420341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523afd9b62f1795baadd2185569a751dd5082141fb4f0f8322d9dc9b09c99841`  
		Last Modified: Thu, 30 Apr 2026 23:51:36 GMT  
		Size: 16.5 MB (16483803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645b659ebaf53520c074547b7206b5af5fe035f9916a8a7f08ea760d32145e9b`  
		Last Modified: Thu, 30 Apr 2026 23:51:36 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e4191ceb6ee98929859ce55683b1d4e9abd7cdc51701e4dfd14dc62ae33e8b`  
		Last Modified: Thu, 30 Apr 2026 23:51:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d5c821d05e95d69be696eace9fb4c022d0b12d1b32594a49247b4d8ef0b863b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e444a609d8de1c294be157f9fd782480ca306e83015b973f37205a66be2334`

```dockerfile
```

-	Layers:
	-	`sha256:5c50df65421221d643ef971d0c1b781a1c4c4f376659e9722c99fa63b38463bf`  
		Last Modified: Thu, 30 Apr 2026 23:51:35 GMT  
		Size: 2.3 MB (2314452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7300d89fbb7dc14a7e13f934cc6f266a807503c99402ec89820c77ef01d13142`  
		Last Modified: Thu, 30 Apr 2026 23:51:35 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json
