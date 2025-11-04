## `clojure:temurin-17-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:fed4fc9f01ad462adf256ce3fdb9db5ebc8b69e73272331d3a0f7cf37764674c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4f1b45928f0dff2242e68c3093738f31e168e58f7da993d104f90fd84f488e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194788729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7e058831277272a2609a6ec02d37ffb7faf67183cf0a6c25d8a8ffe3883343`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:54:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:54:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:54:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:54:49 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:54:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:54:49 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:55:03 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:55:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:55:03 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:55:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:55:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:55:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:55:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5809284c64b79ece1f5cfe10d8e32a82cbf2a7a1712fb0fe5085ef05ea0492c3`  
		Last Modified: Tue, 04 Nov 2025 00:55:25 GMT  
		Size: 144.7 MB (144693303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c13e05b29d34e9ce32b07506ad544e7ad46bca8885d57e6669786c614d32ae`  
		Last Modified: Tue, 04 Nov 2025 00:55:31 GMT  
		Size: 15.3 MB (15318698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb4db2a532fee59e91183ced865278272198e994fa91c5dc76d53dcaefbbf03`  
		Last Modified: Tue, 04 Nov 2025 00:55:31 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1297e9feeb4cbf36949cfb652d16ba4c38c48b1b233ef46f1a6d711f8b5faf66`  
		Last Modified: Tue, 04 Nov 2025 00:55:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5c55551aaacc546d2290b31dfe644937a4ead291e5bc5966ed2768193c99a092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9431406c974f7dffd56c7e6aa9f879bf87f46f29627282b79af5fdde6c4171c3`

```dockerfile
```

-	Layers:
	-	`sha256:385493c5a71b4caa52b10aebe554e3f354cf08eaa9a871e8e3d041869c9ba3d6`  
		Last Modified: Tue, 04 Nov 2025 10:40:14 GMT  
		Size: 3.0 MB (3017908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92db0cd7597600bd8c8d55e37decedcddc70388761cc7043e26b7d30f1ff0bff`  
		Last Modified: Tue, 04 Nov 2025 10:40:15 GMT  
		Size: 18.4 KB (18401 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:edb7a7d08919edaad22f9f3e3a0b8bfb2821d0f60087c392220e8c6fac957b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192114666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a725f8e436ab85ec97a49b769c4555ae97f4ee4d61fb2f41542ca405f77dcfcb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:55:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:55:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:55:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:55:40 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:55:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:55:40 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:55:53 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:55:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:55:53 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:55:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:55:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:55:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:55:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d5c3daa00a3079f7276275155d9b81d86d6a955485a6b7b904e3c59bb2cf34`  
		Last Modified: Tue, 04 Nov 2025 00:56:17 GMT  
		Size: 143.5 MB (143542103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc27c3eb5e36ada8846d2535444f7541a1e2383b35a51e5edd298e41b063d0cf`  
		Last Modified: Tue, 04 Nov 2025 00:56:28 GMT  
		Size: 15.3 MB (15305824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be725b2c56c719132774427a3756ff571929af20d3a3a4c5555c73f2ba8bae22`  
		Last Modified: Tue, 04 Nov 2025 00:56:27 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc90fa380ad2218ba7b0e47e6336dc98f218d0541d004e457dfc64f44669076`  
		Last Modified: Tue, 04 Nov 2025 00:56:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8dcf9b331925f30e0ac5bd265dc3521f34cdf30f6177ccb3f0b34921b81c1047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3defc969fb63e5796f05c673c8f0e68ef976b4503084dc15448f58d9e78df868`

```dockerfile
```

-	Layers:
	-	`sha256:f95a99d2099952dea09231c8fd85463b73499f3a700f621594a228d7970be649`  
		Last Modified: Tue, 04 Nov 2025 10:40:19 GMT  
		Size: 3.0 MB (3017517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:735a10a67415b77454fde391c9bcdb3f49f29e21da8216d02ec5fd57c9f49bff`  
		Last Modified: Tue, 04 Nov 2025 10:40:20 GMT  
		Size: 18.5 KB (18523 bytes)  
		MIME: application/vnd.in-toto+json
