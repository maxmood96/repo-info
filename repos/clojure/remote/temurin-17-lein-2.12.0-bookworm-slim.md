## `clojure:temurin-17-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:3d30b6a6ef6f198488a19cb6b9cd25548a9a90750c020f626952a2bc369f234b
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
$ docker pull clojure@sha256:94f7b072dd5c6cb438e42a7e16808359e7c010dab33cd17e13837e332ee35332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.4 MB (195353357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208841b60580e140bfc68d300c4fe2ce07e6f21788bb986a5ec9c64dbef4319b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:20:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:07 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:20:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:20:07 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:20:22 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:20:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:20:22 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:20:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:20:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:20:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:20:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e2aa8dc6908bde2c546fd29714905f6da0d9c4b8c066508871d25995f5f66a`  
		Last Modified: Tue, 03 Feb 2026 03:20:44 GMT  
		Size: 144.8 MB (144847906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4af5ebd0044140f744b2f29b4fa84aabaef21279fdf9ad68b65b2fbfa66ae3f`  
		Last Modified: Tue, 03 Feb 2026 03:20:41 GMT  
		Size: 17.8 MB (17758803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73886e8696f78e795bc903b71d063e61a42f826a4cc53cd0154f623a04c28f6c`  
		Last Modified: Tue, 03 Feb 2026 03:20:40 GMT  
		Size: 4.5 MB (4517731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69738c9552175b346e24cf56146da8059aa859459797a12acbf2de2d4a3e346d`  
		Last Modified: Tue, 03 Feb 2026 03:20:40 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6faa7a23a119893a17f24b7afae5a341375c330d71b6b4800abc0aed65e69eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2747200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94e695774886998f3f05e4ab7090c7d8af4f3adba21a5606a4d941ca665aa3e`

```dockerfile
```

-	Layers:
	-	`sha256:1ac02382f8aaa3f70f44b8605f7dfceec65a5f694d6c94c3d085f176813f11a4`  
		Last Modified: Tue, 03 Feb 2026 03:20:40 GMT  
		Size: 2.7 MB (2728798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa2c6c2eac835ec6fa84c8cccfa1f1354ce6d584e457e8bbbcede4cbe22edd8e`  
		Last Modified: Tue, 03 Feb 2026 03:20:40 GMT  
		Size: 18.4 KB (18402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2a39762f0de61d1477407e338c4bc8660a44973782974341fa0bdbd092bb9c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193897719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23689afe9cb72523fc64569681107202a4faaebc7a35aa2773959ea60a7d06f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:22:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:53 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:22:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:22:53 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:07 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:23:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:23:07 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:23:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:23:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86d06f3bdb792dc35afb58e22638cc5401237c311a6edd5c3a56e31c28e74a3`  
		Last Modified: Tue, 03 Feb 2026 03:23:29 GMT  
		Size: 143.7 MB (143679946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fe10af56ca62e3661d378c7cb6872af8cd808f9926007dfb3b9c2cc3e60e0c`  
		Last Modified: Tue, 03 Feb 2026 03:23:26 GMT  
		Size: 17.6 MB (17591772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c5cad43ed4d3be3dcdcb52062ba124d5cad39884ce96720bf525aa55fa9883`  
		Last Modified: Tue, 03 Feb 2026 03:23:25 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e717ac4b0313bc147bcdd6ef30fc857c8356d84e6d746880f548c82672dbc47`  
		Last Modified: Tue, 03 Feb 2026 03:23:25 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4230653daff66215b330fbf1ecee95193ed3731e2764d19f10b796afb9fd6a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2746935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e6ed3a08707aa9c54e62376b9358663066547ca51b15c7b75b11913a6624f8`

```dockerfile
```

-	Layers:
	-	`sha256:faf7f97b71dc61e119d2f00868b6f97f3ba21939371d3c7023181b00e42a5779`  
		Last Modified: Tue, 03 Feb 2026 03:23:25 GMT  
		Size: 2.7 MB (2728413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e133e0180f6f7f7098c32b969a3096012e6291e295b1b922ed46c9826bc02b0`  
		Last Modified: Tue, 03 Feb 2026 03:23:25 GMT  
		Size: 18.5 KB (18522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4727ca8d2585dba3353ba0e9c6dc8252bb1ee44a3012547455e2ab6d50056308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199072673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a0373b5607947133b9ee5391d88dbd6196bda5e009870684e8ed51b275d6fc9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 09:40:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:40:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:40:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:40:57 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 09:40:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 09:40:58 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:41:29 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 09:41:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 09:41:29 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 09:41:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 09:41:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 09:41:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 09:41:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8606fdbc7d8e323e8dade6f9c43ae149386b2cd9b6d68330671c91dd99473a3e`  
		Last Modified: Tue, 03 Feb 2026 09:42:12 GMT  
		Size: 144.5 MB (144524725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0c982bb38a8677264a28240736c2fab07f4a6b0087e23b141a4e676598e311`  
		Last Modified: Tue, 03 Feb 2026 09:42:09 GMT  
		Size: 18.0 MB (17961055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba5a37095c54346a8edde1e51f6fdde98acd09aedb7ed07adb54c8e241f2e28`  
		Last Modified: Tue, 03 Feb 2026 09:42:09 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618effc47b55599242e0c56fa0ceba02cbea84b6bc1d3f9c070fb9ea3359ed34`  
		Last Modified: Tue, 03 Feb 2026 09:42:08 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e28b0d1268962cc67f72a9222c55d3795e44a7181f986b015b49fb536fdde07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2749078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf2bb84c22560c226054060dbdc40fefb714732e68babb6cb0fe192ab62c80f`

```dockerfile
```

-	Layers:
	-	`sha256:a71a835f66c1f83ee5ded028b1e9a16dbd77c5820b8658847006fd2fa1c89330`  
		Last Modified: Tue, 03 Feb 2026 09:42:08 GMT  
		Size: 2.7 MB (2730631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:617f43934856ebd24db6ca7ce6da5733c465f0c35b7705a048dcc44a6a8e68f9`  
		Last Modified: Tue, 03 Feb 2026 09:42:08 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:367585bb6c17b45f6bfa90e7a21c691bdc75d62cb4566a944302d64e250177a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183683424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ac9fcceda2c53a5bb6d0df4e29e64771cfdb7e47480853a74aa779e6328b27`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:01:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:01:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:01:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:01:48 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 05:01:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 05:01:48 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:01:58 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 05:01:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 05:01:58 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 05:02:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 05:02:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:02:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:02:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4faed5ad2aeef46262b9c59020e76ce12e2c432bdaf6860f05929430b5ffa9`  
		Last Modified: Tue, 03 Feb 2026 05:02:27 GMT  
		Size: 134.9 MB (134859780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e869fac8d53e43742a6ee783c4cc0a770353af15cff1a16a766f4fab7ad94b18`  
		Last Modified: Tue, 03 Feb 2026 05:02:24 GMT  
		Size: 17.4 MB (17421089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305f948fb2f72d57f60f0822809b5fdab33746c4e0ddac37f869d5a7a0a154a7`  
		Last Modified: Tue, 03 Feb 2026 05:02:23 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0883da3c8ea84cd55a8eaa4db81649c838ad48597cd3de76426d503763a47d00`  
		Last Modified: Tue, 03 Feb 2026 05:02:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:89e8fa4b789731317315f3dd1ef0c190b625d70de2e4e5ec67fff4c2dfdae1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2739015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d7e9c069a1031d9c811903de645779aa54c48c2ca840a183061b29ac3939a1`

```dockerfile
```

-	Layers:
	-	`sha256:dd8598bdeed95d084f09fe016f6fcde8317bd0b3c1937812e0717e0f087a0d61`  
		Last Modified: Tue, 03 Feb 2026 05:02:23 GMT  
		Size: 2.7 MB (2720612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e5356dbbd97c536312fc8b21bad0ee9927ef6d8de5cb32acddd4114d47518c`  
		Last Modified: Tue, 03 Feb 2026 05:02:23 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json
