## `clojure:temurin-11-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:ce0cdaa67f168bc292fe2383cdd3eb73f8e4a99a8d9eeac3ebfd38a094b5665f
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
$ docker pull clojure@sha256:148079482407007c9bb31a1f3c95ff006fe195a1c97fcb3d93e36659c509b76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196399841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb24418cb08cf1af4d31d41746d4a4984816153eae4b3be8bef43bb73857d76`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:15:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:15:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:15:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:15:40 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:15:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:15:40 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:15:54 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:15:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:15:54 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:15:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:15:55 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16935cb50cc3404a01bb976ef389ea7f67d93d300918c389df19919f01fc7d6c`  
		Last Modified: Fri, 08 May 2026 20:16:15 GMT  
		Size: 145.9 MB (145886217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b68e4ec564dace21e5f65800ddc526b51360c34d9baed82ecbf838d1af9292`  
		Last Modified: Fri, 08 May 2026 20:16:12 GMT  
		Size: 17.8 MB (17759592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a4a4f5719741ccf1714458510ec05732127ed0a20fe6a087c7eb95fdb998f6`  
		Last Modified: Fri, 08 May 2026 20:16:12 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2180dd96fcbe06a6141ff32a621358a4bbe1f899b87970f9f230392f6a47955a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2766759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8d508050de3b4f5c9a24b8692a389f506ba14dabb5b84f8c4920e6f0fe49da`

```dockerfile
```

-	Layers:
	-	`sha256:3e445877e15b97b70b0e1badc778738946fb7bb179326568975d964202725e63`  
		Last Modified: Fri, 08 May 2026 20:16:12 GMT  
		Size: 2.8 MB (2750193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:299f89912789a0565d9ec6feef352ea645490aeb23e5b2acec74d915cdb5a06c`  
		Last Modified: Fri, 08 May 2026 20:16:12 GMT  
		Size: 16.6 KB (16566 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0fd1804eccdb939d813c40626ed4745361d5a53cde259bf081c16a302b3c965d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192809177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c136cf3fc54646c8fe5c35dc68a12616e56de18ceee80338e03b8e0f0dfc70`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:19:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:19:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:19:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:19:39 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:19:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:19:39 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:53 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:19:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:19:53 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:19:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:19:55 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2170ef7a9c32e4d06b2d1b4e85de9d911b5c25bdcd28854a99b2a973aba6be`  
		Last Modified: Fri, 08 May 2026 20:20:15 GMT  
		Size: 142.6 MB (142582223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39ef42f16141bb2f3cfec76aaab126fdbe96b5953d2cb23733890f4534a0d99`  
		Last Modified: Fri, 08 May 2026 20:20:12 GMT  
		Size: 17.6 MB (17593005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b5569c24913808317a00cb3764fdb1800b7ad65b7860593e0c6f7d621bec84`  
		Last Modified: Fri, 08 May 2026 20:20:12 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d0014be0c644a761d0e27a282bd945034178026a82cbc4a8b47e424a2bba930f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2767113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720126d6eea9ef89975b43f572c191b16663e83d7fdb1a36f3e007e2b64903ae`

```dockerfile
```

-	Layers:
	-	`sha256:9329c008e7590d73e18ff2c984bfeab8183d53d270a5d2ea87cee411aa7f3e6e`  
		Last Modified: Fri, 08 May 2026 20:20:12 GMT  
		Size: 2.8 MB (2750426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cae81300afb1c56be9d71f96e5a66c324d36ad39bf5562f08ed0b9fcafba377`  
		Last Modified: Fri, 08 May 2026 20:20:11 GMT  
		Size: 16.7 KB (16687 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3120e04bcff76f6924df91d20b527dc604ea80f156d1e27b9b770dbe73505d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187667649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06add360ba3df834759b49dfa950ce3bd0c7ad2e19517d83b33b1890fb25a48e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:32:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:32:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:32:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:32:03 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:32:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:32:03 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:37:50 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:37:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:37:50 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:37:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:37:54 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76ccb486cd38d4bc6e81d6a758dc0756e8388df36970ae898570b04b2565a95`  
		Last Modified: Fri, 08 May 2026 00:38:30 GMT  
		Size: 133.1 MB (133110145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c791f3c3459d541f7acd5246b21fe3d03cd54e2754cad81bbebbd87de910bb92`  
		Last Modified: Fri, 08 May 2026 00:38:28 GMT  
		Size: 18.0 MB (17961314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b841541b2a77d7a35b8cace7b8bf76f5051fd9e4e207791b1d6fed8d81a6704`  
		Last Modified: Fri, 08 May 2026 00:38:27 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b3ca5df562840c9419cfe0a06acffc71823f1266257976755e5d79816b695ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2768021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90b4c73991b853320babe073c8972f6c379476427b061d8afcd341b5663beaf`

```dockerfile
```

-	Layers:
	-	`sha256:bdcd46f44bf199bfd6b16f1698186a4795d46bccb2d5c04bbecd246d4792ab19`  
		Last Modified: Fri, 08 May 2026 00:38:27 GMT  
		Size: 2.8 MB (2751411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7293a5b5d3d888a94d55feefa21e3fdd0170d8aa4003e47f3ec82138fe06d85`  
		Last Modified: Fri, 08 May 2026 00:38:27 GMT  
		Size: 16.6 KB (16610 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:fd9f1fd667347bf55fd0d3a3ab7d086b60218700ffcd88d13416d1ae7a2466b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175483114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc64927e3301fac8e0e4611a78e157751840bbc940c0a2e8444490568f34e478`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:12:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:12:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:12:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:12:56 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:12:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:12:56 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:13:06 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:13:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:13:06 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:13:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:13:08 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ea993f684cb01e3eea5d725a6fc9f80d3d869ccf66211510f5ac3a0bcde03a`  
		Last Modified: Fri, 08 May 2026 22:13:35 GMT  
		Size: 126.7 MB (126651719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d88c8e8c5c840ecc5afa4173b9c17d54402439814b1b4ea4cbce6f9f2f395cc`  
		Last Modified: Fri, 08 May 2026 22:13:33 GMT  
		Size: 17.4 MB (17422020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032bd04a6a07fa7ccc39e173cc90336c0f0e42a82274200de74205093ea5c59f`  
		Last Modified: Fri, 08 May 2026 22:13:32 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:982032677a5105020f6ccc1cd01eb2f7a7d988f04d55c2d14c7051f7517f02fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2758576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2661181ad148b13b7838d5661e60685ba0948b1b27b2ba2d61a3199c8d1868f6`

```dockerfile
```

-	Layers:
	-	`sha256:b3743866d4a8f9130ea5a53c6ca1c64b44f4cb3b85a5029588f2630a99f14c8c`  
		Last Modified: Fri, 08 May 2026 22:13:32 GMT  
		Size: 2.7 MB (2742011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d961830134e28d822e25542044356ea800712dd11ea72c8e848bccf7ba9abcc`  
		Last Modified: Fri, 08 May 2026 22:13:32 GMT  
		Size: 16.6 KB (16565 bytes)  
		MIME: application/vnd.in-toto+json
