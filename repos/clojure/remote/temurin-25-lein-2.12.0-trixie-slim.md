## `clojure:temurin-25-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:d81fdb72f47c69f6135f6a15788919b9c9a6c0806d4afca644adecb978613480
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
$ docker pull clojure@sha256:6a6f73b69a72ec390a25f7084b9b1c15cd412937b5290568f21150bd195d48a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142789267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299bb5d72746e545e167dd882fd16dc2bad9772d50f2c1f872a287daf4d0d121`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:22:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:38 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:22:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:22:38 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:56 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:22:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:22:56 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:22:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:22:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:22:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:22:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8b56121e607a6c68d1d272940fb2dc4f926a318cb0cca259239f057601bed1`  
		Last Modified: Tue, 03 Feb 2026 03:23:17 GMT  
		Size: 92.0 MB (92045315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a6b4c246fea9b181d81e30c115f5c73c648090aa049035fbd0dc2b81b2088b`  
		Last Modified: Tue, 03 Feb 2026 03:23:15 GMT  
		Size: 16.4 MB (16447189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcf785d1501fdef48557f90b1c9654c5c52a696caf30e6935aacdac0260ff79`  
		Last Modified: Tue, 03 Feb 2026 03:23:15 GMT  
		Size: 4.5 MB (4517736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af0c20888f896f3d7639c4cae78f45e8547e2610ce65a43d5cdbe4ad0e5dd85`  
		Last Modified: Tue, 03 Feb 2026 03:23:15 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:22146376c82f14dbe295ce0290b56aacf66d269f883a4be309d64c65da1bc9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390f0e221fcb2f8518633fdf646fc0c66cd7cc628605a9790f8715508d514c5b`

```dockerfile
```

-	Layers:
	-	`sha256:61c8c14c0b715395dddc8408beb191428391f9c7f106eec34f99015266deebfe`  
		Last Modified: Tue, 03 Feb 2026 03:23:14 GMT  
		Size: 2.3 MB (2314816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e6746735ba3b22c9eab14ccd611b7534c1ced2e52b96799cbf46161a9f378f`  
		Last Modified: Tue, 03 Feb 2026 03:23:14 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:df512d78b45218befd01c7f12fd27fdae8d97da2e39b2edcca7f00634ebed6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142118603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce43cfe9c926b6d15458d2812fa2b910b892ef04732a00737da87c25b0d31da`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:10:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:10:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:10:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:10:17 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 02:10:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 02:10:17 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:10:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 02:10:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 02:10:33 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 02:10:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 02:10:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:10:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:10:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6a0e3c87a32b613f5a9f47ce1800a1b1c51b28ae8a0901d6ccd4ed5fa994e2`  
		Last Modified: Fri, 16 Jan 2026 02:10:53 GMT  
		Size: 91.1 MB (91052460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86b80420568384c81bf59d8a5af5d9f96a05946167a021277038c0c81087e0f`  
		Last Modified: Fri, 16 Jan 2026 02:10:52 GMT  
		Size: 16.4 MB (16413937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afdf5d8f3ac74eb3c19c99d9f7ba23887b2010261ba333d5c0ad52a6feeb688`  
		Last Modified: Fri, 16 Jan 2026 02:10:51 GMT  
		Size: 4.5 MB (4517736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64e6168db5765d5cb17e26531c7d28a3c98fd5356b9b478138fe1b09c9c9bd0`  
		Last Modified: Fri, 16 Jan 2026 02:10:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3b22958fe6547a1860ceb2ea95c261fc93b10ec49d155c96ac9d2242bace4059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4645055d82da55c6e4c31472639f97002663372fcf69ad494ae962d2226cfb9`

```dockerfile
```

-	Layers:
	-	`sha256:33ec3953871cec84ceb8612534e220ce23ec68e95d5d486feeaf13458d6fcd07`  
		Last Modified: Fri, 16 Jan 2026 02:10:51 GMT  
		Size: 2.3 MB (2314455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14b96fda5493ffeda5c83efe07f79383ee2c237ca2f5f733ad41107e3053451b`  
		Last Modified: Fri, 16 Jan 2026 02:10:51 GMT  
		Size: 19.2 KB (19179 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3c9219c8c142a1f110e08a2f9c781eda4aee38ffc6d5ab3b0e0efe6ceb6cb323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146210004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207d080d615907ac0a31e731db4db1057d3a6626c41518950bd189096f1dd0db`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:44:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:44:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:44:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:44:53 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 03:44:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 03:44:55 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:45:58 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 03:45:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 03:45:58 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 03:46:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:46:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:46:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:46:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11e063d257c7fd0378d1844308cea571e43cdc3c6ef2206a9db6629a1520ee`  
		Last Modified: Fri, 16 Jan 2026 03:46:44 GMT  
		Size: 91.6 MB (91610755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2246e2006158f66cdaa3bace84b646348ea88497a12fefad6e2ebd992dc5fa6c`  
		Last Modified: Fri, 16 Jan 2026 03:46:41 GMT  
		Size: 16.5 MB (16485502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00af45bdef0f7e5ee487d595115ee9c3d4330035bc8f19f7b51331818da304d9`  
		Last Modified: Fri, 16 Jan 2026 03:46:40 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afb0817dc0f0ea743dc97f2d9291c0bb28bf08badba082482f92dc1fc050569`  
		Last Modified: Fri, 16 Jan 2026 03:46:40 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b03653d35b146d75d7dd06769461aef8ee5a80f6e3436b72b921cbf6a984b3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc75237e4a804dffbe74f8429b97d875639aade17bb62f3c4e5a0d2eab236db9`

```dockerfile
```

-	Layers:
	-	`sha256:199b4e9e19ae0d738a6c50d273c8b28f10d00bcd9eb61b19c2915c276d4f0ff0`  
		Last Modified: Fri, 16 Jan 2026 03:46:40 GMT  
		Size: 2.3 MB (2317106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3854a295dd88b74e952f2154ea5ed5fb21c5c6a97d819acd313f80b009a7289`  
		Last Modified: Fri, 16 Jan 2026 03:46:39 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:c071188e15d65f57b091b11939a14f7cbf37011183c0b6758955a66d8e2d5180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139940677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162aefd4fb798fea6f94a8ee7553a870ef6904d4ab925a97da9fb3db19c7c479`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 04:35:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jan 2026 04:35:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Jan 2026 04:35:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 04:35:53 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 22 Jan 2026 04:35:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 22 Jan 2026 04:35:54 GMT
WORKDIR /tmp
# Thu, 22 Jan 2026 04:37:24 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 22 Jan 2026 04:37:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 22 Jan 2026 04:37:24 GMT
ENV LEIN_ROOT=1
# Thu, 22 Jan 2026 04:37:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 22 Jan 2026 04:37:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 22 Jan 2026 04:37:41 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 22 Jan 2026 04:37:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c69cdd71ef06850eefda28596d4212304f3101cd9d101f44fb4cf0c74701f3`  
		Last Modified: Thu, 22 Jan 2026 04:41:12 GMT  
		Size: 90.8 MB (90752894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d432eb238e252eac4cee820a5bdcb5eca9693a30f0babf3f179d068bb4f2726`  
		Last Modified: Thu, 22 Jan 2026 04:41:00 GMT  
		Size: 16.4 MB (16397877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2121be5332f7e06e8c00c5175080fb8b025a018dbaeb30dd5ee9ccbdc828d39`  
		Last Modified: Thu, 22 Jan 2026 04:40:57 GMT  
		Size: 4.5 MB (4517790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430ffc66d7d3fecb7172637ad501c824a0fc4b8375d98787ff7efc7e794b2fd3`  
		Last Modified: Thu, 22 Jan 2026 04:40:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:de1992eebb3b0cf68dc70398d9768e59d2e660667c7665f9cc39e5314910e106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2325963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ccc05f86b1e8007fd9689c051402e9f948a47f600e07ddc81a29c609bce066`

```dockerfile
```

-	Layers:
	-	`sha256:05f77c833a41453c4e21d93caf444b679340b477e9050ec62cf4e13a045e97be`  
		Last Modified: Thu, 22 Jan 2026 04:40:55 GMT  
		Size: 2.3 MB (2306873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:880b4f1e61032268ebaef8ce26a06bb9550c656ae6b5c12935eea93b99fe70c9`  
		Last Modified: Thu, 22 Jan 2026 04:40:55 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:253703d5c9373cf3b91b49b5d9a0c0a2e9913b8ba4236595ea973dc1c244a196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139045356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ce53171cc49e272907126812140caa0417ba57b838269401cfe5086c38e29a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:23:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:23:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:23:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:23:10 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:23:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:23:10 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:23:23 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 15 Jan 2026 23:23:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Jan 2026 23:23:23 GMT
ENV LEIN_ROOT=1
# Thu, 15 Jan 2026 23:23:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 15 Jan 2026 23:23:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:23:25 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:23:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2b60cbc839537ac9d2d64e95bf99e1c19c3b75f06175e544fbfafc8cc5fea1`  
		Last Modified: Thu, 15 Jan 2026 23:23:51 GMT  
		Size: 88.2 MB (88210671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181ce5dfe9b484262a7d1f2d45a10d603a7e14f778b0f8a489988dd4ce969fad`  
		Last Modified: Thu, 15 Jan 2026 23:23:50 GMT  
		Size: 16.5 MB (16483100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee5d985dfd304bb5400ddfd11aad3324665d74ecb4ed4d0869aeff9c74bd7d0`  
		Last Modified: Thu, 15 Jan 2026 23:23:49 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ce7eddd94e5026e0958fcaa0ab9176e5eda37cac5892f32612ae81c227d5a1`  
		Last Modified: Thu, 15 Jan 2026 23:23:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:28fd4627b2b2576563b1e193e162c2d925fb850bc50927ac5fbdd56d242c6670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2332825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3366679e4c9a570b8896e6ac7411f4ba9ffa8454b161a3f36ec211425481fdfc`

```dockerfile
```

-	Layers:
	-	`sha256:773cbf54d3740f71f4006fde4dc4e34b741c366fde6351013464189f0e00851b`  
		Last Modified: Thu, 15 Jan 2026 23:23:49 GMT  
		Size: 2.3 MB (2313791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14f7230f5a07c1db1f981ab8137b84204c20ec470687f1cc244298f0c620637d`  
		Last Modified: Thu, 15 Jan 2026 23:23:49 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json
