## `clojure:lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:fe060c9b0b09a7106cbc02d2c6bfc2f9f3c0ffbab8570ff5b67e46d5b0ac3009
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
$ docker pull clojure@sha256:1a4eeb2092ea7c87afe5ecb2406658feae9413b3707bb31b9da750d3b428b93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143000248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643b58dd3fef1b74ce9970bed5a3c39c37adb9e9f4770b70a4dd697864c19dcb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:24:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:24:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:24:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:24:29 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:24:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:45:25 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:45:42 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:45:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:45:42 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:45:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:45:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:45:43 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:45:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d0b63a1d6ed834ba72f9d6877308634c61815630ec57289bffc64c8dad38cb`  
		Last Modified: Tue, 17 Feb 2026 21:25:20 GMT  
		Size: 92.3 MB (92256289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba229f85610a21386e0aeaa8ad00a76bd24f635fd04d2a38720a779d9bbbff3`  
		Last Modified: Tue, 17 Feb 2026 21:45:54 GMT  
		Size: 16.4 MB (16447204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c1a1ab4c662221482dcc28c02e601916db3baf565e9d44c9b167437d990b65`  
		Last Modified: Tue, 17 Feb 2026 21:45:54 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fad35a0eb374aea948fb6f40fbaf76f0dbeaa77ecf6dc69e98b7f4d3cc0bdf1`  
		Last Modified: Tue, 17 Feb 2026 21:45:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:30e740fd6bc81b74d15edea1d1c9787bcf98f918e14b8e5a273e5fbf327e430f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2351838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd26204d0d305382280773873b9f4c767ac33e8ac7b1c5ac8c2c1d561925697`

```dockerfile
```

-	Layers:
	-	`sha256:f09bf6d183121c17f50804da9a24a7e4b7d46f117b170fe16a287632aeea924f`  
		Last Modified: Tue, 17 Feb 2026 21:45:54 GMT  
		Size: 2.3 MB (2332804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ba8d293902638b9d4395b927fa17d7750093757e1c59e0f56a3301fefdf314`  
		Last Modified: Tue, 17 Feb 2026 21:45:53 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fcc6752875e0ab2fd8f4dcc6938f7ec3b0e29e4b820543b197cc3a0c463c62fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142360048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d44e2d4b38a957aebc103060d4ab87e8c77be440e5485156029e8350a3e85a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:24:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:24:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:24:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:24:38 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:24:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:45:26 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:45:44 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:45:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:45:44 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:45:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:45:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:45:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:45:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12566f8e35ae8d2780280fa4c358ba81665454b532f1ec3ec96b9a09fe6feacf`  
		Last Modified: Tue, 17 Feb 2026 21:25:25 GMT  
		Size: 91.3 MB (91288272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ac683772b0681da197fd1fe6499f954f5fd50a0626ae75a7663f81e6a42978`  
		Last Modified: Tue, 17 Feb 2026 21:46:04 GMT  
		Size: 16.4 MB (16413580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10731861a1d7a2bcd0f47f56a841f28490cba1824a5345b9c58416b3cadb0bce`  
		Last Modified: Tue, 17 Feb 2026 21:46:04 GMT  
		Size: 4.5 MB (4517701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8921021ef5fe2ee966f72c01156c49a9129cedad7986ed1e8197aabdcb1c452`  
		Last Modified: Tue, 17 Feb 2026 21:46:03 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d96e7975dd91a4113129ef685e8678e5327639edf66af4bb295b439e1d7a684b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2351622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eafd6886518579c004c2527489760c2bd4a23e497df8b8b6210a78155e1725d`

```dockerfile
```

-	Layers:
	-	`sha256:c034da5973727e6374adbf65c880b6ff404ce2974c33c6d0453b8538a9d31b48`  
		Last Modified: Tue, 17 Feb 2026 21:46:04 GMT  
		Size: 2.3 MB (2332443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d2209a6e047c7c3596bade09275f925a876cfa8f819a8074aa5a86564aedd2c`  
		Last Modified: Tue, 17 Feb 2026 21:46:03 GMT  
		Size: 19.2 KB (19179 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ebabfa7eb2cdb55aad95133c0942558d454cfbd977d9a298be80c50e0df1996e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146236113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5fc35f2d987698ae8da84bded7d55d714ce4975517c2cbf6b2a3cb2e371c50`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:48:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:48:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:48:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:48:15 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 06 Feb 2026 00:48:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 06 Feb 2026 00:48:16 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:49:03 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 06 Feb 2026 00:49:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 06 Feb 2026 00:49:03 GMT
ENV LEIN_ROOT=1
# Fri, 06 Feb 2026 00:49:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Feb 2026 00:49:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:49:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:49:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cfca27e4d0c0686d68682e7bdbb0f0c15c94dfea8c09b2d4c6306086826ff1`  
		Last Modified: Fri, 06 Feb 2026 00:50:04 GMT  
		Size: 91.6 MB (91632917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894231d804d466c1129b2652b8fd3ae0d85f739c294f715c8568c4e848dbf477`  
		Last Modified: Fri, 06 Feb 2026 00:50:01 GMT  
		Size: 16.5 MB (16484828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e842a307ac52379fcd836d1ab360cbff54a76e69fb44b8e7f88dda51bdbc568f`  
		Last Modified: Fri, 06 Feb 2026 00:50:00 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b837e3b312cabab5d282832cc8538ba0b641dffc7a8a7556aab4bb944fd8154`  
		Last Modified: Fri, 06 Feb 2026 00:50:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f5c07d03f928597cd8c2126ab3057d0ad2d2695c0a564056e89236f113aa68db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8352e9a87676f2dfde88b5e64a8d7a836ade83a84f62c1ab5eb84f0801ddeee6`

```dockerfile
```

-	Layers:
	-	`sha256:ad70b117accbed394500edc903803479cf8bd565cfeec31a4303308eef29a779`  
		Last Modified: Fri, 06 Feb 2026 00:50:00 GMT  
		Size: 2.3 MB (2317108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc20077349e162fe3ac5e6bbc051d6bf79b83df58e1d473e488118dec6891e8`  
		Last Modified: Fri, 06 Feb 2026 00:50:00 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:90da71e8a04c5b28ed6d235284553876bcdd5d453da5fad3e25bddf4cbaaee6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139965925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4e2cedac2cdbd217786a1dc7c4366e20fb864230c153e4906f6188bd826c86`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 13:01:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Feb 2026 13:01:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Feb 2026 13:01:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 13:01:01 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 09 Feb 2026 13:01:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 09 Feb 2026 13:01:01 GMT
WORKDIR /tmp
# Mon, 09 Feb 2026 13:02:36 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 09 Feb 2026 13:02:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 09 Feb 2026 13:02:36 GMT
ENV LEIN_ROOT=1
# Mon, 09 Feb 2026 13:02:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 09 Feb 2026 13:02:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Feb 2026 13:02:53 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Feb 2026 13:02:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3259c1d4e8b88a02ac6a13fb17b96d8d9cdc8d3493e158953ae177f9140e66a7`  
		Last Modified: Mon, 09 Feb 2026 13:06:37 GMT  
		Size: 90.8 MB (90773406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f547a333f793faeeb8f2a019f49fdcb1e0463989b955a61eebd919d19f9207`  
		Last Modified: Mon, 09 Feb 2026 13:06:26 GMT  
		Size: 16.4 MB (16397921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7eb42595b5a24e7cdde2eefb4abfd9cf650b78e134f7cb4feb266ec9415b17`  
		Last Modified: Mon, 09 Feb 2026 13:06:23 GMT  
		Size: 4.5 MB (4517779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61603bf76c8c19a271d667b6bc0409a531c67eba3184313658fdd7be0dc22a6a`  
		Last Modified: Mon, 09 Feb 2026 13:06:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:21135d2a895ddc6bce43c3a81380e3814a96989201a872eb48b5067e7891dfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2325965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae713194087aefcad629b07414ae444ac0f349eeec21b840238c94a30f9cc51`

```dockerfile
```

-	Layers:
	-	`sha256:32c4e32c99426e6e062ce4aae0a26e7d1f6a8db06901afb61e15db20f8dc58a4`  
		Last Modified: Mon, 09 Feb 2026 13:06:21 GMT  
		Size: 2.3 MB (2306875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b3bb0ee323a0dd8e35ef70dfcd561152b9b75a5567ef1fe1cbc3619d622209c`  
		Last Modified: Mon, 09 Feb 2026 13:06:20 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:bb1540c8ee87a47dae3698df1f4d8f5f54b0c68b4daf7aa11d89c0d357691f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139073498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db90b69cc1f1bd6e15a7312c10563d052485a8a531623386b29e186bee80e4f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:09:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:09:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:09:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:09:01 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:09:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:09:01 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:09:15 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:09:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:09:15 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:09:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:09:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:09:17 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:09:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f346e6c932681347824fbcb087b1626c7950a778909ec292081697fb26b29a3d`  
		Last Modified: Thu, 05 Feb 2026 23:09:44 GMT  
		Size: 88.2 MB (88233823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bda6421d1a7de87f64eacbb5958287dacaba2078de72dd75ac5be1f82e1553`  
		Last Modified: Thu, 05 Feb 2026 23:09:42 GMT  
		Size: 16.5 MB (16483358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b27f82c3f26cd5b1df536280d4207df84dec97949f44263e2044892a3aefda`  
		Last Modified: Thu, 05 Feb 2026 23:09:42 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b360f41aa1ac9fda4f2e8c14941391390274999293f52a9f32f9ba5bd5a0dc`  
		Last Modified: Thu, 05 Feb 2026 23:09:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a8054341c991f4d59b1c0ce16524cc1dccac9113bbb0cbbb73ddee2ce6ab99ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2332827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07463a1e37cdcd3453c0a48b6446b7c969b128a21c4139446502a79ee60f08c5`

```dockerfile
```

-	Layers:
	-	`sha256:9c386bd8603d25bcea1da0c63a138cd9cf53ee06c86b6000fd45965e37e22d09`  
		Last Modified: Thu, 05 Feb 2026 23:09:42 GMT  
		Size: 2.3 MB (2313793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd64c8d26fa45abfc7d9ae5842db7c99f36f4ff084b700a9576baa79876d5014`  
		Last Modified: Thu, 05 Feb 2026 23:09:42 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json
