## `clojure:temurin-21-lein-trixie`

```console
$ docker pull clojure@sha256:9e79e162bb7d4d324c8b1487666040baa56af8e5a78faa1a304008390dbef211
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

### `clojure:temurin-21-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:0618aebfd4e298bc7566cb04dd26d4070024cae730e2105dcdcaad647dd281a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230187603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a67755f8218915f7b0b675527514267c5f17be69e5145e18a67a8291e25055`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:30:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 04:30:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 04:30:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:30:59 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 04:30:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 04:30:59 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 04:31:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 04:31:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 04:31:15 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 04:31:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 04:31:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 04:31:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 04:31:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2863544bc52096bd524afef6916017b0b7dd0f7e36f07560eea36fb87353963`  
		Last Modified: Tue, 04 Nov 2025 10:54:09 GMT  
		Size: 157.8 MB (157804741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5e427e7d7f8b2d473e1d35ca57bfc07ccf63ff24ae829724a4f90cc3cd1a11`  
		Last Modified: Tue, 04 Nov 2025 04:31:43 GMT  
		Size: 18.6 MB (18579065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38beb30e7f7a76b563f6a3b6852197ab4ea11f52b6dbba31a86ad2eea04152f2`  
		Last Modified: Tue, 04 Nov 2025 04:31:43 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe330c1df3e959a907aad5275521a7668283a3f6dbe0b3ce0824afe5215fccd0`  
		Last Modified: Tue, 04 Nov 2025 04:31:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e96b3c625679c74920008840edfb228ad59f2351c583e99bc0297d57bb2f799b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695124119d69c45f96531dd396fab3ad3fdb3dd371cbab81edd04580263ad0c2`

```dockerfile
```

-	Layers:
	-	`sha256:b1c5f00657b189bfec2571d926b31f795efc8c95df181f59521d72d025e23a98`  
		Last Modified: Tue, 04 Nov 2025 10:43:44 GMT  
		Size: 3.8 MB (3816486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98a76ba74335d8cbe7f3b7e9491a04b14d94aa8850c94341094451921d3a151b`  
		Last Modified: Tue, 04 Nov 2025 10:43:44 GMT  
		Size: 18.3 KB (18349 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3973b1c676cec4f57a32fba0ccde489669c2fe6c485ad3f7be61ea098970f223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228789715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f72ddd440a97767cb9881b861b30a89cf0daf93c05e1b8659f321d2c7f6586d3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:45:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 01:45:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 01:45:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:45:04 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 01:45:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 01:45:04 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 01:45:21 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 01:45:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 01:45:21 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 01:45:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 01:45:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 01:45:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 01:45:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3408337256e7c6882b56700f38051f1ba13e542788ff7b562696e82f2e35e3`  
		Last Modified: Tue, 04 Nov 2025 01:45:44 GMT  
		Size: 156.1 MB (156081258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037a8fdbb775b0ab4f41bdb6ec67fcf11d40ec96c85c3b24604942de99317731`  
		Last Modified: Tue, 04 Nov 2025 01:45:53 GMT  
		Size: 18.5 MB (18539889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d24ffe8a6a0400670528fcd3c832b1007553760d0f419174b81823412297b5`  
		Last Modified: Tue, 04 Nov 2025 01:45:50 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7172279837835f1c21d0fa3b68fc023c067eb1f82d353c5010f4534eeb853c4b`  
		Last Modified: Tue, 04 Nov 2025 01:45:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:45790c1aac792bc44a62b5169fca72aba7853efcf854367082c55c4320973d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539b355b2b51ee4ce2586a6e24691b3dc086d0b7c1780a916a8e5c3a92351633`

```dockerfile
```

-	Layers:
	-	`sha256:e74511b0f8e0c6c57b221776ff670ab60e99e4ba6088e6ca11d626131608ef2e`  
		Last Modified: Tue, 04 Nov 2025 10:44:06 GMT  
		Size: 3.8 MB (3817363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b1b67ab1e404f3dfec78089af136ed6db1cf488573fb9d1c1d62adb234af6f0`  
		Last Modified: Tue, 04 Nov 2025 10:44:06 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:0f3833793dc7f72d58c241b83f6b4f14313b41e323c5f9872fa5c9da641d5846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234227710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0c0181531f8d88cc283bda3ce46cd443b1000f40f5a7011d6403b0217759ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:047d1b265d8a7d20ef8b3ccb9f133c3c5f1e4f9c92089889756590b7f20452b5`  
		Last Modified: Tue, 21 Oct 2025 00:26:24 GMT  
		Size: 53.1 MB (53109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c6c2adb11d1bf822a4ed7d95e85ad57bbda0356914f170499c7159171b8476`  
		Last Modified: Tue, 21 Oct 2025 21:48:14 GMT  
		Size: 158.0 MB (157963459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c29e5c54c5573f4f0427b5c8291126d919b40bf1bd4aadaf71326852b6dd82`  
		Last Modified: Tue, 21 Oct 2025 16:06:35 GMT  
		Size: 18.6 MB (18636584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bb0d90c0506ee7bbeb6a9a924fb7089ad1b50a91ba868213fa0d9e324b38de`  
		Last Modified: Tue, 21 Oct 2025 16:06:35 GMT  
		Size: 4.5 MB (4517762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ee78f359e7f7724c5c9b7a802f25eaae445fa5c07eec32815b41de6c637228`  
		Last Modified: Tue, 21 Oct 2025 16:06:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7469278cbea3460ee5b877275ea6767d45c76ecd0494375d83e1c0ada6529bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67c1515afef4aa05661b009e3be471130a1bc4dc7cd5a4a3391289731a3d6d7`

```dockerfile
```

-	Layers:
	-	`sha256:9b8e1779e60b86c4df81f5d765e00d15abdf4e5be9b026530443c304ef5415a8`  
		Last Modified: Tue, 21 Oct 2025 18:39:07 GMT  
		Size: 3.8 MB (3817484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dd57b4b740043a6e039000db506f1c55e79384dabd646a78fa2ca2076b77a5e`  
		Last Modified: Tue, 21 Oct 2025 18:39:08 GMT  
		Size: 18.4 KB (18439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:8249475b3a7063865fa1ab947f6834c17f2655d73788095a0e7d6bd121735355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224413109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332c0dda98390d04c403d7410a1674c2461a35526ea39b6aee10da182f262134`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f99bc11a75f6f7a676f3f49bda98f8ef1b59f2c8ba74759e5fa155fda025bf88`  
		Last Modified: Tue, 21 Oct 2025 00:35:52 GMT  
		Size: 47.8 MB (47770306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c919e0563d2ba43d590847a0df035631a9927abea74ba8e6729fe0f35e3b33fb`  
		Last Modified: Fri, 24 Oct 2025 22:04:57 GMT  
		Size: 153.6 MB (153593526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc32e101155842a8277b76b058495ae10bb7fd8c4ffe11ce3a552da4de216c5`  
		Last Modified: Fri, 24 Oct 2025 02:20:42 GMT  
		Size: 18.5 MB (18531055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb5880548c036a00e35ee9cbb61b66523e0755e93e6fb399a3eebcbbe98cc5c`  
		Last Modified: Fri, 24 Oct 2025 02:20:41 GMT  
		Size: 4.5 MB (4517793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dff63982e7708ecf90162a8c4877841832d12820809dc7526b101e4582dffb`  
		Last Modified: Fri, 24 Oct 2025 02:20:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bdf24c6f50e2ec0b5938b586121ca38af0fc4fe21c7db9c01aa894a735481006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3825400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd14940cfef7b6a493c6f3be29310e17a733b904d8a9d8de3b206c4882321750`

```dockerfile
```

-	Layers:
	-	`sha256:b35cc106ca3b53244d42736c7a405e2c191358bd3435c6b577946a611657de37`  
		Last Modified: Fri, 24 Oct 2025 03:36:19 GMT  
		Size: 3.8 MB (3806961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:614c04bda119114e82a5f522be4f9f9f3a0b865d2314fec67f6be3394fb6fac6`  
		Last Modified: Fri, 24 Oct 2025 03:36:19 GMT  
		Size: 18.4 KB (18439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:0b69bd37fdc5f1d289c11b8cc5a4c2819e62f3cbf37529ad39c6cece73095b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.5 MB (219517718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af937920ec25a063cf6aee18a91cc8cdf21dabc1e5712a9532a79ebdbcc69e22`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 13:04:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:04:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:04:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:04:15 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 13:04:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 13:04:15 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:04:26 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 13:04:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 13:04:26 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 13:04:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 13:04:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 13:04:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 13:04:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8cb87dbc56dd0ceec8ade80dbf4a583ffd88c64721f2008d818d3b7e00891ad`  
		Last Modified: Tue, 04 Nov 2025 13:04:56 GMT  
		Size: 147.0 MB (147026991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235ea0e98ef4639bb4e1009e2faa95bf9cfc450d99c15432c4783a00f21d41cd`  
		Last Modified: Tue, 04 Nov 2025 13:05:01 GMT  
		Size: 18.6 MB (18620253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eee47b2ecfbe5c0f5a12160bb2ef8a8a8e229097fa2bf89cc49c74c63527949`  
		Last Modified: Tue, 04 Nov 2025 13:05:00 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c430a529eba4693398ba2d6d6512f69677c3bb5b9f945e0801b1c7b91388d5f6`  
		Last Modified: Tue, 04 Nov 2025 13:05:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6978cc3c928226956d40a52cf1e0bf2c24a8185811fc991aa3ffeb4b2e594fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58e3ab18d95ea60f7d8b6d6abab3ec15784b8aa869e1d1a4019347b074e44ec`

```dockerfile
```

-	Layers:
	-	`sha256:13324846ce50844efd3aa43e025438e4774b52ef66559aa46350502c4f4caf86`  
		Last Modified: Tue, 04 Nov 2025 13:37:02 GMT  
		Size: 3.8 MB (3812913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88077d1589b23c65e9a69cdc9aea0ba5e33b89d12b474a7f9b97db15d45dfc4d`  
		Last Modified: Tue, 04 Nov 2025 13:37:03 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
