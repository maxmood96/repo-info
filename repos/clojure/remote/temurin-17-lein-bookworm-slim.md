## `clojure:temurin-17-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:6c8a555c5070df9024063734dc9070665d341bfe869e56e3dba06f4828d86eab
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

### `clojure:temurin-17-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:701a8368b940b8919f2a115e089ae2366c448e6022cd2d65b117cc5eae0e732b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.4 MB (195352901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8276806a2ee0587c41c3e5c6ce38247cd5fbc5821f016b33755de9787f79f695`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:42:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:42:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:42:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:42:33 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:42:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:42:33 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:42:47 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:42:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:42:47 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:42:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:42:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:42:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:42:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75899ff2e657cf76f9094e38103afacacacc4826a476a2c1463fb9ed07fe3ff9`  
		Last Modified: Sun, 09 Nov 2025 00:04:40 GMT  
		Size: 144.8 MB (144848097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f9de8671cdb2b9153095b30b468c9a0d07361a1d7f1df7ae48853d1eb4d205`  
		Last Modified: Sat, 08 Nov 2025 18:43:20 GMT  
		Size: 17.8 MB (17758104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c865235d0c73d3ad190a46a73a68061be9b0fb15b27692864438dcfcefbe4081`  
		Last Modified: Sat, 08 Nov 2025 18:43:19 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497d0fc80d8fd7e3f830601c013951b4bef41d8823c09948f5938ca70fa1e784`  
		Last Modified: Sat, 08 Nov 2025 18:43:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:03a452bc060e2c0314d346f70c2bffad826aa88d41b14f03a0bfd4933d25ac0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2747190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba7ee4bf20f9e91f8b2856e22452118e725e8973118115933b36c54806d39e3`

```dockerfile
```

-	Layers:
	-	`sha256:8d53aa2bfe16a0a97fc315f8f20fd815c64f8548352321b7ab1c027aa8f7bf79`  
		Last Modified: Sat, 08 Nov 2025 22:42:37 GMT  
		Size: 2.7 MB (2728788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:798a148a80d8ca98b41d14ce5207f0e18cd91c55f3cd5163b495a6e2a5f7bcbb`  
		Last Modified: Sat, 08 Nov 2025 22:42:38 GMT  
		Size: 18.4 KB (18402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f4f7b250b6b7f0fea3abf2953ae39658e52e56fddb662207ccbf6b48d6c7e0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193891626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cbcaa7cffff2e048f0d29c8f3496b4fda83daf58da9ae7862704f92b9d34217`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:41:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:41:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:41:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:41:47 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:41:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:41:47 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:42:00 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:42:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:42:00 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:42:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:42:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:42:02 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:42:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0584566dfcd5827fd56da00a827bca477b6306d7d7fb2881c8d6d44502a4c6b9`  
		Last Modified: Sat, 08 Nov 2025 18:42:23 GMT  
		Size: 143.7 MB (143679948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f7859de1d322c967475973051d87fc17003e71dbfe139ea26338166486b917`  
		Last Modified: Sat, 08 Nov 2025 18:42:40 GMT  
		Size: 17.6 MB (17591124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6213147e354eff104c9ff51e3ef8275fc58674da357f88114d2bffd1dbce808`  
		Last Modified: Sat, 08 Nov 2025 18:42:38 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cb128fe4300e60a593fd8618bd3cad75d03b7593cb0ddc4a0b16bffa881e98`  
		Last Modified: Sat, 08 Nov 2025 18:42:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4db22c23bf3b042f80d01ff4fcba04c633000747953c9879fbbc5497896cf492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2746927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e43bfced7ad6e9575810097566753df25d5d59db2c551d76225b77d616b38f`

```dockerfile
```

-	Layers:
	-	`sha256:2120cdabcd076ef3fcb5012536a3afd73c7daac24a9156607c875ecfb0e508fb`  
		Last Modified: Sat, 08 Nov 2025 22:42:42 GMT  
		Size: 2.7 MB (2728403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25be06113bc6e727ea6f95006b7b774cb13ea84b56eabb76cef7a90b932ea597`  
		Last Modified: Sat, 08 Nov 2025 22:42:42 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3be473d3531ef03ae56cbeaa2cde2df9e95952908e469b3749eba17574c21f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199071859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb7fad41b5201acfc5557a5605ff112b5b10d1d0a68c8fa1552a469be3ccd70`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 21:14:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:14:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:14:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:14:55 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 21:14:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 21:14:55 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:15:25 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 21:15:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 21:15:25 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 21:15:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 21:15:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:15:34 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:15:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cc3022c7410c457d51287dbb7e81e407dc7badac69c919f9c8b9350ee668d2`  
		Last Modified: Sat, 08 Nov 2025 21:16:18 GMT  
		Size: 144.5 MB (144525137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62aca6f48550236eb06cb32979b5fb51a7bbe7883fa390153d35d3001f28fb63`  
		Last Modified: Sat, 08 Nov 2025 21:16:25 GMT  
		Size: 18.0 MB (17959646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ae0d9871381453ef0cbc1a315086960b1d75cf740867e12f5df5c70c985b13`  
		Last Modified: Sat, 08 Nov 2025 21:16:24 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1864c8474a592081a75b4ff1d386db005c5eceb7f4c5789fc7ae228901e6fbf`  
		Last Modified: Sat, 08 Nov 2025 21:16:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9e32a61180f3a82f5b2be1250cb4a88791150c1ffd4604d82a31ea2677a3e22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2749068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd43cb10f9a19cd64abdd0a4f0466c010636060448a80d0260f6574c28032036`

```dockerfile
```

-	Layers:
	-	`sha256:e4f620fd4b4e082399ecb80b8787baaad83f05aadeab772f7bc9aac32788161f`  
		Last Modified: Sat, 08 Nov 2025 22:42:46 GMT  
		Size: 2.7 MB (2730621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55e84162b16e87bd0f3832356b22b3fa37039d41b84110700766bf8613b5ee0c`  
		Last Modified: Sat, 08 Nov 2025 22:42:47 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:46ef7b4ce4f975377142e807fa7d96ee42ad1d5d68325f859fbc03a30d7b73d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183681646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd066de155425ab0a94c314e34913e2d0cf6d836a16ae751659602e08a2877f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 19:36:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:36:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:36:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:36:50 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 19:36:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 19:36:50 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:37:01 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 19:37:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 19:37:01 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 19:37:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 19:37:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 19:37:03 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 19:37:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336253f18c72c35afb6b4d26a3718343fb563b23438c2a33f099c29342a0ed12`  
		Last Modified: Sat, 08 Nov 2025 19:37:29 GMT  
		Size: 134.9 MB (134859055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6d1f172d7b588717771e4d60c7603616acb3087db8ba39efd23a1ed4e74bca`  
		Last Modified: Sat, 08 Nov 2025 19:37:38 GMT  
		Size: 17.4 MB (17419850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90d42bc5921825aab16d9883d698bbcad7d44401c06e2f082b47ad85dd71605`  
		Last Modified: Sat, 08 Nov 2025 19:37:37 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9767d6933a4c7e83bf4855f8c42182648ecdc8a4a08e705cd6cdc14be641a1`  
		Last Modified: Sat, 08 Nov 2025 19:37:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:63bb5fd1d20a253684b5d7e5f09889a80aaaa319e4a4c021c3f47e647584c237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2739005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d2def7fdee523783ff0d10f6534152244002f6435042d5f75357be1d9c71ea`

```dockerfile
```

-	Layers:
	-	`sha256:fa5b9d26b84d1cea74bd3ecfbb3b3f1421dcfa06135edf1c9462557fc8d03a4e`  
		Last Modified: Sat, 08 Nov 2025 22:42:50 GMT  
		Size: 2.7 MB (2720602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410ff2aea30bb20cf4791bf5ebdca4bb9bdb89656bb57190a50ff2269632f35f`  
		Last Modified: Sat, 08 Nov 2025 22:42:51 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json
