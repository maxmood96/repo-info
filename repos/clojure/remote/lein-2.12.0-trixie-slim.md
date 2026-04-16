## `clojure:lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:cbbfe095a7784079bc6b08a0b8de5b40e05801686a3327f5a553899af33d0c9e
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

### `clojure:lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a297ec54375718fec69dd8ef770d3d5fd4cde4d3cfee8347ed1c42fe483b7a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (145952045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f9e091d2443deca7952a1b272324c5483a27ace44fc1f525959dbead749f58`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 21:39:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:39:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 21:39:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:39:40 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 21:39:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:06:21 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:06:37 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:06:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:06:37 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:06:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:06:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c3adbd3c5bc63927fab129e6aea63e0edee67b95a91828b7951d7e2815261b`  
		Last Modified: Wed, 15 Apr 2026 21:40:35 GMT  
		Size: 92.3 MB (92256319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ece80489e3509bf258e4cf6d24b947d86de9c79cfde94b47e36c41bc498b3a`  
		Last Modified: Wed, 15 Apr 2026 22:06:49 GMT  
		Size: 19.4 MB (19401945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20391f7f98888e39ae4879be261acf494dcdfec750a0b671db2293507b3df7b8`  
		Last Modified: Wed, 15 Apr 2026 22:06:48 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5de2ca06210942eea5e946e7b3261c2265218c4d68fc9e56ea49630707ba92`  
		Last Modified: Wed, 15 Apr 2026 22:06:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ab6d295a9221f4ab99c249b9d1c0a2eb5b058def3f864d3973a130e7b95a1afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2351075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960e28785568e5f4039e4b133d1242c4f8e039c3fc91da7fa00c4b8c0916bf39`

```dockerfile
```

-	Layers:
	-	`sha256:879e9643e2ea53de3a68f1eb51caa3532024084c0c295868d4fd04f8b188941c`  
		Last Modified: Wed, 15 Apr 2026 22:06:48 GMT  
		Size: 2.3 MB (2332840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccf7d4d192dec3e698a59b84284cdf4326fb39820e81e4153bfcbb91e512d6c7`  
		Last Modified: Wed, 15 Apr 2026 22:06:48 GMT  
		Size: 18.2 KB (18235 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:04fbfe7632202efd35358cf187bc5bdd53240f9ffd2eef8df24bb057f6c84fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145679812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4f3d15ad856cb7ffa1564eb9005c0f5ac02089b2afcb614a7b6c7da3b067db`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:18:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:18:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:18:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:18:03 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:18:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:18:03 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:18:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:18:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:18:20 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:18:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:18:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:18:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:18:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2e11e955bc84ba71b02d6caf3041362949fa0816bbad06635890c00bc74df1`  
		Last Modified: Wed, 15 Apr 2026 22:18:48 GMT  
		Size: 91.3 MB (91288265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab622a2e0da118488056e591bf08003bdb13f1a8a0dc1267c75051e53ad8abf`  
		Last Modified: Wed, 15 Apr 2026 22:18:44 GMT  
		Size: 19.7 MB (19734856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ba792fa918a07a4894a25de7b370f540d559045a97760a25b9c5241b3f2b3f`  
		Last Modified: Wed, 15 Apr 2026 22:18:43 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34af0804e5bcab7c4f157c4815b67568982c6354b2490dafbced02ca1df529d5`  
		Last Modified: Wed, 15 Apr 2026 22:18:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:65bbe1572aef0829bdd2e50c78c026078afdbb36816c72e75765480c38f5e35f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2351658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be2f827570391f7b84d6176f9d82f15a7ac9d6902ef5da48645d7011bd86e14`

```dockerfile
```

-	Layers:
	-	`sha256:273a547f165c35b89233c5c92768badab23d50488d3660c9174515fe81eb5e00`  
		Last Modified: Wed, 15 Apr 2026 22:18:42 GMT  
		Size: 2.3 MB (2332479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a098443089102a67722375254a3de9f10a01912ba291deb6faed67de48ba383`  
		Last Modified: Wed, 15 Apr 2026 22:18:40 GMT  
		Size: 19.2 KB (19179 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4d07caf34c54931eb7734c6269eb87a4ee7161c4d0627d7a0fa4667549f622ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146229603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff90939c2ebd11908a38f3765441aa3b9b395ad59a3049e47c50f7b687fdd8c1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:57:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:57:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:57:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:57:19 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:57:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:57:19 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:58:02 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:58:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:58:02 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:58:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:58:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:58:07 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:58:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674dad765dcc78e0a3938a692ea5b290c37a0c10042e2a743ec14ddef8e6b775`  
		Last Modified: Tue, 07 Apr 2026 14:58:42 GMT  
		Size: 91.6 MB (91633035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4359f4078b2a359b8b7cf7e608e7ca692266f87110af72c3d79f1676732200`  
		Last Modified: Tue, 07 Apr 2026 14:58:40 GMT  
		Size: 16.5 MB (16485386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71bca17ad757efd692b50958add7e2130fad92f1619a5b9a792b58fa0ea9143`  
		Last Modified: Tue, 07 Apr 2026 14:58:40 GMT  
		Size: 4.5 MB (4517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdc7714982b41b4ef7cf48ba281ff8810edbbb033eb21178862f101e0f4e79d`  
		Last Modified: Tue, 07 Apr 2026 14:58:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6e32cab277b3b2d1c6d588867ff3a247b575d4eb7bfb551d5c096383cfa0766f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c104afee8566781fdc8381e1bb9fe50e64f40168fef2e242646b601fcc6a899`

```dockerfile
```

-	Layers:
	-	`sha256:338af529b07ea2fd02e2b1ed70045b2de07aaa95e6dece59ce7a6ad75ce18863`  
		Last Modified: Tue, 07 Apr 2026 14:58:39 GMT  
		Size: 2.3 MB (2317144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28bba5153d3a3d0e090a9161d2cdd92a9b0def33fc08850fc11e82f4dcc057ec`  
		Last Modified: Tue, 07 Apr 2026 14:58:39 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:afb41bcf2319c258e73fa73805569847262b3f31c491defa8eea81bda89ece82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142585533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fe45b73676da55d8c8fb86405276d49361c46c4c7cc5296e52e9854a735452`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 22:39:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 22:39:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 22:39:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 22:39:28 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 11 Apr 2026 22:39:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 11 Apr 2026 22:39:28 GMT
WORKDIR /tmp
# Sat, 11 Apr 2026 22:41:03 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 11 Apr 2026 22:41:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 11 Apr 2026 22:41:03 GMT
ENV LEIN_ROOT=1
# Sat, 11 Apr 2026 22:41:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 11 Apr 2026 22:41:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 11 Apr 2026 22:41:20 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 11 Apr 2026 22:41:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94187439743d0e4ea744bbf1c65c89e279a7b6b83ff5e8684b3251e143001c79`  
		Last Modified: Sat, 11 Apr 2026 22:44:45 GMT  
		Size: 90.8 MB (90773426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09e265e79973634b98e17c96492597f62b632f5b2860bc61b4cf134d60e953f`  
		Last Modified: Sat, 11 Apr 2026 22:44:35 GMT  
		Size: 19.0 MB (19018107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6baba1db715dc9ead6acfb6df9c89c7c26aa19b021b0d2a03663f780377afb`  
		Last Modified: Sat, 11 Apr 2026 22:44:31 GMT  
		Size: 4.5 MB (4517792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0f14514a23130bde9707a15ec989e5c7449e84bcbba98602c274e5884511e7`  
		Last Modified: Sat, 11 Apr 2026 22:44:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:83ace2b8249368152d9a742986aa29d78f9e91645c77693db7a6d275f09d255a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2326001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc08ebeadaf6b2d593123bbef2c84c5716fffae3e242f4ddc3fc84fcb593406`

```dockerfile
```

-	Layers:
	-	`sha256:e91c5ecfcdf6db276cbb2532c4db5636e77dbc65b35ad2a3aa40eadba995783f`  
		Last Modified: Sat, 11 Apr 2026 22:44:30 GMT  
		Size: 2.3 MB (2306911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11f988b50c6a8a2bf3b7b5cab7079dab9e4c38b7de7148eb6530c13ecfd03c96`  
		Last Modified: Sat, 11 Apr 2026 22:44:28 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:996d5523fe8f7355e7c15362db60b565316b7603e9cd2aa87ee52d1139f94108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141677574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96bd949e3df0b0744a417581f6709a4ddb774a12e131c99d3662103efe2e86b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:44:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:44:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:44:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:44:33 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 00:44:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 00:44:34 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:44:47 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:44:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:44:47 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:44:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:44:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:44:49 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:44:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8994c4e65dc27cd0254fb87db1df501d65655ac89363003981ef434a6d7353e4`  
		Last Modified: Thu, 16 Apr 2026 00:45:12 GMT  
		Size: 88.2 MB (88233823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c47ebd170ab33b4c07cd4a315b56798d833152415c1114b54f1ca8969074d2a`  
		Last Modified: Thu, 16 Apr 2026 00:45:10 GMT  
		Size: 19.1 MB (19090196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865514496cbc03733c30fc9bb82dd63e790460ac00ad530c7c750f4a905315a1`  
		Last Modified: Thu, 16 Apr 2026 00:45:10 GMT  
		Size: 4.5 MB (4517709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcff1d4e3696a0f42ef969cf20e3546cf409562880d15ac0df5f01ee144e8089`  
		Last Modified: Thu, 16 Apr 2026 00:45:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3a24e7911f9512a3ea5ab60160e1a66e5b8c7c49007f17a058f1d15b9d32c7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2332863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df480f6942fedb0604feaed5909f080d5b58701aace63bf5f29fc32a05b2a67`

```dockerfile
```

-	Layers:
	-	`sha256:6a5be0b1278f9479f798b6960faa6ffc70390b760850d02730d73c01aea41e37`  
		Last Modified: Thu, 16 Apr 2026 00:45:10 GMT  
		Size: 2.3 MB (2313829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8073e9728341a4f83f62c80dbe80dae1096765f0d95a15f39eb0e729ee3a148e`  
		Last Modified: Thu, 16 Apr 2026 00:45:10 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json
