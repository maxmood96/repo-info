## `clojure:temurin-25-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:570348fbd08e4aa6614af033a6fd376d9b8cee208df735d9c7ff555b44d63442
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

### `clojure:temurin-25-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c9a4531e321347becfc6f66aad9e2fc809a0233fb6f19254079e9f05091b95f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142550125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d3e22d5ffef337f5c6a6d4e2f2bb64cc0df021a2e7eae4c9514df9c96c4f17d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:45:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:45:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:45:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:45:34 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:45:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:45:34 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:45:48 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:45:48 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:45:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:45:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:45:49 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:45:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c8a60e94c78695ba65b21138421554f1166e3aa4697184bcf918bdb8c9b515`  
		Last Modified: Sat, 08 Nov 2025 18:46:27 GMT  
		Size: 92.0 MB (92045302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2821fca687f19e1223c28e1b1b27add731ea3894e3e79161060736ea541aa0d7`  
		Last Modified: Sat, 08 Nov 2025 18:46:22 GMT  
		Size: 17.8 MB (17758116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74173da023a93ac7c6369f3ae64c39ee6ae0385c24a22c9310d4b3b7cd7260e9`  
		Last Modified: Sat, 08 Nov 2025 18:46:21 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28393501226f3dcf85c57c740fb9a041e84b30b92a7a125097a579ab8824f55`  
		Last Modified: Sat, 08 Nov 2025 18:46:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a7e4da912a42513f79c26f01ff9c89c00787fbcd31f8877f437bcb8f544ca19f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5484a3d74e3fe65f275314622976ff32074b013a854262f445e23e2f033bda1`

```dockerfile
```

-	Layers:
	-	`sha256:366619fc7ab425993a8aeca1f26d38b11dab22e053dc97033b23d0ed1713505b`  
		Last Modified: Sat, 08 Nov 2025 22:35:01 GMT  
		Size: 2.7 MB (2680112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad576a65503f8261eb20cdbbc3090f48092345a9ed7a66b85d12f63049957d3b`  
		Last Modified: Sat, 08 Nov 2025 22:35:01 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:99c2189f0344e8b19f0ff2626e3f30a003c957017c1aa18c52e28d11e92b2077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141264168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4def5b98258ca1d6edd27f973f6ff45c2d457173bfda2de49f7b565e2a3f6a64`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:45:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:45:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:45:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:45:01 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:45:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:45:01 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:45:14 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:45:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:45:14 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:45:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:45:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:45:16 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:45:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84ce8f0f4ec8f142f931c4a956331b335a233356d7dea2e3aa0370a84b3fcb5`  
		Last Modified: Sat, 08 Nov 2025 18:45:47 GMT  
		Size: 91.1 MB (91052503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c449477f69a9710feaa72b179285dbd486dd2886ad9ac25d8f78c43a27106b50`  
		Last Modified: Sat, 08 Nov 2025 18:45:42 GMT  
		Size: 17.6 MB (17591118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa7136f849cf4b95348908ee52c365d6fec538eb5ea11d680c7ccdcec6972f0`  
		Last Modified: Sat, 08 Nov 2025 18:45:41 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c1d6286164bfbb9fbdd849c35adcd15eb1106c1c7126789caa0365dfa642ba`  
		Last Modified: Sat, 08 Nov 2025 18:45:41 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f3d78c27ceb76dead9a5082ab8d8312a4e890da790feb5d8190bee67b2f477c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b238ea73f0554af347b90507ca0dd4261a7e0dccacec35cc7247dcab7d04fc`

```dockerfile
```

-	Layers:
	-	`sha256:84afb1ed0429adbb492e746846de5de7fa095129e02ac3a9f83eb995824d4342`  
		Last Modified: Sat, 08 Nov 2025 22:35:05 GMT  
		Size: 2.7 MB (2679748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80f07b5ecfcd9c3a28a4178adde2b7e5f3fc59d18b2ef0aee2be44b071db5c83`  
		Last Modified: Sat, 08 Nov 2025 22:35:06 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2bb626a03702d1cccc4559a3ae535716742d2e8aaef7fc8b22a6a37e44648c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146157447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efbe297ba08120545b19ed4870e5ea593073074fc54476f289f5eb5631721158`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 21:46:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:46:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:46:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:46:54 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 21:46:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 21:46:54 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:47:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 21:47:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 21:47:18 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 21:47:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 21:47:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:47:21 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:47:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1965d7bccb021209291d1051f699e8f11ed0f5b51517e9c23eee8d574faad746`  
		Last Modified: Sat, 08 Nov 2025 21:48:12 GMT  
		Size: 91.6 MB (91610745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29f7e7ca735561712738676d5a33f10d08e8606b31f7f0bf16afd5454f6ee44`  
		Last Modified: Sat, 08 Nov 2025 21:48:06 GMT  
		Size: 18.0 MB (17959621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bf5db0113e1ddf91296cfa663227a4a8cd7cdddef8830520a6c76361a8a2f9`  
		Last Modified: Sat, 08 Nov 2025 21:48:05 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bce19dd1dc6fc57aec7ada237fbb42ebd957424dab4347617b773c0e064792`  
		Last Modified: Sat, 08 Nov 2025 21:48:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:52b5ce13ade969a03cc920751640c3ee5f9b3ff3e3b363f88989048c9a20c8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2702368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e32d12d5a89db94e910cbb902a6d14fae02addff33df838ae666f787fec5c4`

```dockerfile
```

-	Layers:
	-	`sha256:d51de5897d50d9859749f6cc330731fadc63a11161c0224313c7cf6f40fef341`  
		Last Modified: Sat, 08 Nov 2025 22:35:10 GMT  
		Size: 2.7 MB (2683255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8594b68cd2cc2b4dba2a10917fb48306f6932e0072c7f96d415b7ed3e5e51c2`  
		Last Modified: Sat, 08 Nov 2025 22:35:11 GMT  
		Size: 19.1 KB (19113 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d5b82aea9aaca95bd8fafade79a25ce0949263f339fcb7f731b028253e498461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137033274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef04a1af023f836281dd6afc059b262cb47762d3f932418da373c3d49654071`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 20:37:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 20:37:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 20:37:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 20:37:37 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 20:37:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 20:37:37 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 20:37:47 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 20:37:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 20:37:47 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 20:37:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 20:37:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 20:37:49 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 20:37:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15694db20fc231107b78ae3d18f60c3e913b30a3c838b3ce528e37cb812d9985`  
		Last Modified: Sat, 08 Nov 2025 20:38:23 GMT  
		Size: 88.2 MB (88210738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b52f3a14e4e40f82be0d3786dbae392481ccee2a1a4e6c904563431d6c5dc5`  
		Last Modified: Sat, 08 Nov 2025 20:38:20 GMT  
		Size: 17.4 MB (17419804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2035dd26babcd5be7d2d17f41a2cfa3e4271d04544a07330cb27b88ef1460ebf`  
		Last Modified: Sat, 08 Nov 2025 20:38:20 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90004f0950fe8e06076dc99c1edfd66be1c6405a3e37ab39bd797610b07e878`  
		Last Modified: Sat, 08 Nov 2025 20:38:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8efd1e971fe4d8e4916dccdbf75de488ca1ed33dd7dcb82666438ae4951335fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37534a01735736f3a2d28cc2fd56b9a0f14d0292b7c19830b7fadaf81773c60c`

```dockerfile
```

-	Layers:
	-	`sha256:3cdc58c890e58e99344661103e64bd7a989f2ab09244ce931106065be77e9157`  
		Last Modified: Sat, 08 Nov 2025 22:35:15 GMT  
		Size: 2.7 MB (2674474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05f8df6a50a549269915fe880aa7ef01722b506ac96c679839214c488d0fbc6`  
		Last Modified: Sat, 08 Nov 2025 22:35:15 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json
