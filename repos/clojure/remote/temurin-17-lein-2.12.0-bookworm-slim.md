## `clojure:temurin-17-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:729597237fa4abcbc736f4a9ead8ff48d86d94396887140aae627c672b62d334
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

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ce3d92b363e1c4fd5a26f5e58a377db50c667206620fba6f3adc404b94a08a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196419510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bbc13fcf317627578a3e75d2e378b5db928d51a8fc087fb498593f287865566`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:16:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:16:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:16:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:16:40 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:16:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:16:40 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:16:55 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:16:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:16:55 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:16:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:16:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:16:56 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:16:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57de1768531db4157d0ea52d288cbeb8e93bf6392f86cf5bb679ce21b0fb110`  
		Last Modified: Fri, 08 May 2026 20:17:17 GMT  
		Size: 145.9 MB (145905479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0a37fca6be69cca2ae839c6e5d61b0cb1b480355990f04c4a8e732b92aacb7`  
		Last Modified: Fri, 08 May 2026 20:17:14 GMT  
		Size: 17.8 MB (17759607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0aa6b7e5698d4f1994e6004d5a9091064c1fa1b14d3095d80579db3698a552`  
		Last Modified: Fri, 08 May 2026 20:17:13 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4212189e8aecd9b354e868c394eea8d18a4cd3c838bb46a830c1cb8279a86d`  
		Last Modified: Fri, 08 May 2026 20:17:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9162e3599a1a315a2c840e14d8ee820008b123bc1ca29bdef2b08fc5f4667b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2749234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db801e968677f04f5e0d8dec93916a221f0a11650a855bae3239761460c68758`

```dockerfile
```

-	Layers:
	-	`sha256:33333f7769fc129f5a873ba5745ddadbbe47472ecd6813d8a2c42e4037903b39`  
		Last Modified: Fri, 08 May 2026 20:17:13 GMT  
		Size: 2.7 MB (2730677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18d970740b5f8aa2938812186b5ee5e5662df73a7845b216c4067bcdbfba4df4`  
		Last Modified: Fri, 08 May 2026 20:17:13 GMT  
		Size: 18.6 KB (18557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:97a52413a8835b19e3b997104e9cc0a8269972b5d4fd9d2c92d9f0be947a19e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (194951645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d02f85176a84582b129102194bb04a9a311991ef60fef42163d679671330b77`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:20:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:54 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:20:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:20:54 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:21:10 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:21:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:21:10 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:21:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:21:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:21:12 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:21:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca10b129785a33eb1605abf8a0db9dc5e5476a2bb4992aaa66746530d874cf1`  
		Last Modified: Fri, 08 May 2026 20:21:31 GMT  
		Size: 144.7 MB (144724307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa666f5035452eb37e4dc59b391cac4e2778ca6634beb251f47e2ea159a77f7`  
		Last Modified: Fri, 08 May 2026 20:21:29 GMT  
		Size: 17.6 MB (17593001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c66fceb95cf40047b988cb7d11176138e87fa2d7c94ebeb00fbb9ca2383c55`  
		Last Modified: Fri, 08 May 2026 20:21:28 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60da754cf35b0a4444a4cc0e1a17556d90bcbe6231af61dc7f0f6bb05218dae`  
		Last Modified: Fri, 08 May 2026 20:21:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:733874cd024f48b69f44047771d1e910522a311368fa03bed771e2d9633a87a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2748970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ec7707f91e1271c064af5171d846d981885c262af17cb2c070589d7f168438`

```dockerfile
```

-	Layers:
	-	`sha256:f13ce9b1d475cc70995e9c37e565ffa716670e94b1d922360ad598212f937554`  
		Last Modified: Fri, 08 May 2026 20:21:28 GMT  
		Size: 2.7 MB (2730292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b2d8dddf7368355aa9013a4b993ed091cceb089174887c4e9c854b89b7edf93`  
		Last Modified: Fri, 08 May 2026 20:21:27 GMT  
		Size: 18.7 KB (18678 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3ff1238873d38e1b6f5046e94f6b020ce92593525ef8c54d8d4c838adf828aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200324210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef7b82ba6fcd651ae06911ab9e023193c3b308dcfd062ef6dc149543980e0b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:43:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:43:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:43:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:43:06 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:43:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:43:06 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:43:45 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:43:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:43:45 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:43:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:43:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:43:49 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:43:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1a630844f3ca330b4aeb3cf62ea83634554dfbe591d28cdf3d1bbe7c2c4aa2`  
		Last Modified: Fri, 08 May 2026 00:44:30 GMT  
		Size: 145.8 MB (145766245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819e472c4766cf9ea40efb3b9c08f7fd3468418a4472aa44dfb09bf68e442cdc`  
		Last Modified: Fri, 08 May 2026 00:44:27 GMT  
		Size: 18.0 MB (17961387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d500c564817091fed38473087aeb346962ab1de450974b6c98e4aa26396cc217`  
		Last Modified: Fri, 08 May 2026 00:44:27 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15b6a7fe371c402e603ff3ea22913483cf88a8b1c1a38c78e9e623eb283d54b`  
		Last Modified: Fri, 08 May 2026 00:44:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:53a491495b7084300be08ddc888178a5c0e1cfabb903f92e188d3b38574dd125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121a572fa02cd87315f4000693ececdf8a7a21e5dfc1bd26755bed3d19a79510`

```dockerfile
```

-	Layers:
	-	`sha256:c7ce72d7ec3554e588ec833980350fb2794945f808e69141d32b8e4ab6c712cd`  
		Last Modified: Fri, 08 May 2026 00:44:27 GMT  
		Size: 2.7 MB (2732510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acb3cd23358147e7a5f64460b4c8d1bb44945e56c7389f06722cbe323d4edf5a`  
		Last Modified: Fri, 08 May 2026 00:44:26 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ba830d25e09c00641f852324d166cbb8e49d7254329e96652fb3e3b2590d91c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184742166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b11d0af13b8f8525508258a3bb637246d0e52bcf635329cdf92a3814db33ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:14:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:14:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:14:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:14:57 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:14:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:14:57 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:15:09 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:15:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:15:09 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:15:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:15:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:15:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:15:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c10a6897782f771d3606e3e80b8e1017d240690fd955802892aea8e434131f`  
		Last Modified: Fri, 08 May 2026 22:15:37 GMT  
		Size: 135.9 MB (135910446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51f8334385615c36baddd05ab4ae51d55262646805e9bed5a9bc9a701946e02`  
		Last Modified: Fri, 08 May 2026 22:15:34 GMT  
		Size: 17.4 MB (17421969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3822371a4f435b9f354c73a442b32665fd8d1e91ef772413b48f579bebfb83`  
		Last Modified: Fri, 08 May 2026 22:15:34 GMT  
		Size: 4.5 MB (4517722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93da3ebcb74fb38095769b032c732cca80ecb2032c3e7859fe7d8b367058143`  
		Last Modified: Fri, 08 May 2026 22:15:34 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2a682912450fc85c48c4898a80666d4c916b1e6651a29413b02f16752cd8a82b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2741048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19c278ab3517502cc537c35d8c4fd704f0289327bdb6a515f729fe1a9e461c3`

```dockerfile
```

-	Layers:
	-	`sha256:b331a176049b3595aea28c8d85fd18392d03f114631306569a70968e3cd40aed`  
		Last Modified: Fri, 08 May 2026 22:15:34 GMT  
		Size: 2.7 MB (2722491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78170e9c59dc961bde781283bdb7ea14bf32df0227c0152cb03d40e4a13b6d61`  
		Last Modified: Fri, 08 May 2026 22:15:34 GMT  
		Size: 18.6 KB (18557 bytes)  
		MIME: application/vnd.in-toto+json
