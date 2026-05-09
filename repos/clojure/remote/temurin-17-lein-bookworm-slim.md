## `clojure:temurin-17-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:8903fbcb4cd8aeb89c705ef3fc20bb46f88a2d41c422b03e16d3f3fa12baeb0a
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

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-17-lein-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-17-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d060d8452f7bc3fb370c23586fe0e591d0e211d5fdda4876d914d25e41b40159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200324034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a4cb25c089b85b17e22f5bb4e6cc230f44085b73dfd53371ee678906c7ccff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:30:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:30:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:30:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:30:41 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 09 May 2026 02:30:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 09 May 2026 02:30:42 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:31:07 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 09 May 2026 02:31:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 May 2026 02:31:07 GMT
ENV LEIN_ROOT=1
# Sat, 09 May 2026 02:31:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 09 May 2026 02:31:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:31:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:31:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebb50b599e2de909acaf0c0d8a3d5a70b8d0e3b34206b32960ca5e3061a8a17`  
		Last Modified: Sat, 09 May 2026 02:31:50 GMT  
		Size: 145.8 MB (145766111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cf954f0ddbe1cba1159a136741488c233d0683eab95ace33314b7720ec9adf`  
		Last Modified: Sat, 09 May 2026 02:31:47 GMT  
		Size: 18.0 MB (17961301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e3b6bdb42261a57bb75b558527a72750131c3cb3d9218e900a4683edd0aa73`  
		Last Modified: Sat, 09 May 2026 02:31:46 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881b0a788a6abce37953e2926607a3312992bde94959db0e48db7d1274eb7f5a`  
		Last Modified: Sat, 09 May 2026 02:31:46 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a02e13168d6d31174bb0a0e43051be6c7cdb49043c7e40f05a3fcd9a1197fcb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0690182eec66d90815c5f8609325cfa33fb79e8da6f263dc272ac6bcbc134ccf`

```dockerfile
```

-	Layers:
	-	`sha256:a54ba603db4fc3bdb4ccc149f559171feb4547f4915aff22bf803b24dc863081`  
		Last Modified: Sat, 09 May 2026 02:31:46 GMT  
		Size: 2.7 MB (2732510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:201bf83734417d82ff7ed97f13f9abdad78ad349718729c6ee4645803f5857fa`  
		Last Modified: Sat, 09 May 2026 02:31:46 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; s390x

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

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

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
