## `clojure:temurin-11-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:4e1da671a713e5894be020726f5629b34c618b40ba7b5bf0baeec3281931785c
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

### `clojure:temurin-11-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:21febf9f5e6eee897ff9122b6d3ab741848d859af3d89b15b18b2946f87a442e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229847616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72811271170f9f697639c0a537c0061b599e3fbec4a5428012f5415a37d90c0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124c586f5864ed807cbbfc72564fac6da9081d19cf43ba747bc40e09fb677150`  
		Last Modified: Tue, 01 Jul 2025 02:38:12 GMT  
		Size: 145.6 MB (145635595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855a5ff81d54c3ed8b581c99e5813dbd9bea0598ccdf73b0ab198949cc427341`  
		Last Modified: Tue, 01 Jul 2025 02:38:22 GMT  
		Size: 51.5 MB (51467698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdce6c70e55cd7f7462299e2a14487336a359858784cd9d7cb7009cccf0121f1`  
		Last Modified: Tue, 01 Jul 2025 02:38:16 GMT  
		Size: 4.5 MB (4514148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d147d6f1e00cb936f44889480d106733a3ddefd49c5d16eba12f1380e8fc7acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30d5550d447f58daf8f823cc7bd5a201b20a56dbcd2140ce32f6e8cba7c18ff`

```dockerfile
```

-	Layers:
	-	`sha256:55a4573f14136f18f91fa6151c4155f937dcab460544c6559e881a7cb16cca22`  
		Last Modified: Tue, 01 Jul 2025 06:35:42 GMT  
		Size: 4.5 MB (4509405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc93ee7a27ccf25c9ce8e737bf4a63af8ad0f2451e76ca95050ca4d4ac6598d5`  
		Last Modified: Tue, 01 Jul 2025 06:35:43 GMT  
		Size: 16.5 KB (16463 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e136d4ed593271425fcdb6ea7a81364cb57e5ed844c415c1ba82d0aebaafcd79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226446402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe83fcd95438f15495355371e961657afe1ed0942884d91b77f91a7ef95330d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339f131b0c863dd40b5fd07ad70acb5f693f996675d13c5efd4b1e69e47b407a`  
		Last Modified: Wed, 11 Jun 2025 12:36:25 GMT  
		Size: 142.4 MB (142420687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d3beb32ff76a17a1c75a5167d2b2a8d47e60a5599a78a0d64bb25a7bb50fcd`  
		Last Modified: Sat, 14 Jun 2025 09:31:17 GMT  
		Size: 51.4 MB (51433840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c36a132a8c93332a70d1a7300cecb6b35b077177694d1e80b2d6e1457c3193`  
		Last Modified: Fri, 13 Jun 2025 01:40:58 GMT  
		Size: 4.5 MB (4514168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0621724592e88271028cd2ff4fab25f70b8cfbfdd2d9c85b76789181e38916b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4530943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98da35258f0bb8f81aa1c2354e74c26b6ee39bd2d9e4c26d60a6f14c906476b9`

```dockerfile
```

-	Layers:
	-	`sha256:7e67e23506a04f468009dee6869ecdaf20b3ce434bd6bf9e3b078adc32e95fca`  
		Last Modified: Wed, 11 Jun 2025 09:35:58 GMT  
		Size: 4.5 MB (4514359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b33c317e10a8a6a9b9af99f071551bb1dedb1a426abc851a38b4d8e8147cce6`  
		Last Modified: Wed, 11 Jun 2025 09:35:59 GMT  
		Size: 16.6 KB (16584 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:bf1efa8948d58a68319f05e8f8dc69aa9874cbd2039e151280b145fe4a18482a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226075286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35a97240a8000542ca23fbcf57207c115345414a9bb5d6698f1253da36d7c2e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02a4696a1589b7f993ec4c3885ec710d9efc34062e9aa63943ba38857696a35`  
		Last Modified: Tue, 01 Jul 2025 08:30:45 GMT  
		Size: 132.8 MB (132810523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a02ccd3b5920b262bc2ce8ab2b4da82e57d1a6f5aaa248b2d1437fd630a880`  
		Last Modified: Tue, 01 Jul 2025 08:31:01 GMT  
		Size: 56.7 MB (56677726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8d688a47610cdb1da2d0461afc2b5e8fda69b43f81800335a291c6227af80e`  
		Last Modified: Tue, 01 Jul 2025 08:30:57 GMT  
		Size: 4.5 MB (4514185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b96541e71593cf4f0e8696b316ee5da645170d9d8357b01e49e48141150619ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4530128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24de4c7a631c0a0eac8b1688228f7c8b418ff3f280bf1e3e5ca72f3326835373`

```dockerfile
```

-	Layers:
	-	`sha256:b07398f86bb55d47e9e5354021e24781454f8a62df171c26268a1f9e21a4ed89`  
		Last Modified: Tue, 01 Jul 2025 09:35:56 GMT  
		Size: 4.5 MB (4513621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a6fd91745826bd56a71c1e7a6ab30703da0c9f9b3e5d1924acd4e563c2e5bf5`  
		Last Modified: Tue, 01 Jul 2025 09:35:56 GMT  
		Size: 16.5 KB (16507 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:8c932569d9c5af98fa0ca64234b211cc3fc0b4af521ef7e6efc50439fd2ac374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.5 MB (207468520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2416bfce6ecda8fada7fec32ae28e684c340218b3342c17e950e4f7ed5f45667`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a6e69573d364f51e63b21b21091ef5b3b51cf18a353c8ef9a65a8a43966217`  
		Last Modified: Tue, 01 Jul 2025 08:03:06 GMT  
		Size: 125.6 MB (125585329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e81f9dba6b9966dcb93b2aa5551f518e2ae4cd7b5a19e076e32ee87f2f66546`  
		Last Modified: Tue, 01 Jul 2025 08:03:02 GMT  
		Size: 50.5 MB (50481132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de41aec7d88c1398f2cdd383b6e01ee442612a580c62e985f3caf95306cfc0c`  
		Last Modified: Tue, 01 Jul 2025 08:02:58 GMT  
		Size: 4.5 MB (4514216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:995969299e879e7af08a2054c272ead5e7ca08483e313389d22e25170bb237e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe3514c9e35524742e5c7857bd739260e1b27d4c53c440efe246b223dd0ce26`

```dockerfile
```

-	Layers:
	-	`sha256:55c57ac6415ee939ef64b3e4dbe4e776a97a14944c1baf58262090f11b45e4af`  
		Last Modified: Tue, 01 Jul 2025 09:36:01 GMT  
		Size: 4.5 MB (4500787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10ff652a0b8e3ef5aa9c9032bbf0398f243b2326ff2639bffc6bb686012972fe`  
		Last Modified: Tue, 01 Jul 2025 09:36:02 GMT  
		Size: 16.5 KB (16463 bytes)  
		MIME: application/vnd.in-toto+json
