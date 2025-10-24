## `clojure:temurin-21-lein-trixie`

```console
$ docker pull clojure@sha256:04dfdd4d83a6af37474beae9ad7a50ad2f66786f6e8623f2c88134baa8de120c
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
$ docker pull clojure@sha256:c74aea99350dbeed065dbd674b6ee7a3856aeda90e902f713dd2346bbfcfecdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230186970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9663f6d7945facbd26e9947fcdd2467243b52b8fcff7f197126bbe892e99c52`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
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
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e96dec7560b879deb6fe9d8634fc4631e55750c87c4b54160e686556d20aad`  
		Last Modified: Tue, 21 Oct 2025 10:00:55 GMT  
		Size: 157.8 MB (157804765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f00e0f8d7f544d451d008b302022790e4936d1c469403086c38cc7b9bdd3cc2`  
		Last Modified: Tue, 21 Oct 2025 02:23:16 GMT  
		Size: 18.6 MB (18579057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8682dd32c5a0e30ae88807f84b80c191bc9f66b20502821b9798fe8bc3a0458`  
		Last Modified: Tue, 21 Oct 2025 02:23:15 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbaa698a36641ae43f89b7200bf96110e0bfb4e675d5c42412721f043118fbf`  
		Last Modified: Tue, 21 Oct 2025 02:23:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:dcdcbc089c51aa438647ca20d3a7f925a7e3a9809a6504e9cb6d839fdbc59100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8a4daadd4ce5cc552b8381bf25aff0b136958264e82a03f655b10b85b75e80`

```dockerfile
```

-	Layers:
	-	`sha256:9acd6b27dfaaa0e4a6ef39643460582c6ba1ee898586140ff1666a0a058e4931`  
		Last Modified: Tue, 21 Oct 2025 09:42:21 GMT  
		Size: 3.8 MB (3816486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5a0a4d26c85fb0c8cc51a3ac78b413ac44ca6f5cc42277a72ed521cc27510e`  
		Last Modified: Tue, 21 Oct 2025 09:42:22 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f12a4b55fdd608e284f7f834a6481da104911a504714729198685fe7457a044f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228788854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0f78faceb6a0af28fe67edc970c8936af1c52aff7f2ec36fc2512f7f6d2214`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
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
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b35890c7d67c1307fec2948afae854b907d8865dd7e7eba2bc6bf88cd292951`  
		Last Modified: Tue, 21 Oct 2025 21:54:52 GMT  
		Size: 156.1 MB (156081200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662ceec2eadf9e07ecac8bc46c7a8519240b1dbd0396e14cb00e1b38e649ca26`  
		Last Modified: Tue, 21 Oct 2025 02:28:46 GMT  
		Size: 18.5 MB (18539770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e213aa936d0da989ab99f0575f35e4bd33a73cd8a3342fa9c549c5ddbca14b1`  
		Last Modified: Tue, 21 Oct 2025 02:28:45 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a96ebcb77809814b38e928f1b2cb1a95384db9d8560a1174fd162e3660334c1`  
		Last Modified: Tue, 21 Oct 2025 02:28:45 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6fcce50c3150d241913f5e7ab9954c700890f962b449ca93e43d8cd3315b44d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f4d4ac59152438c10a1acfc86325921551bbd1ca0dd50eec81121a63c0c907`

```dockerfile
```

-	Layers:
	-	`sha256:c5be0d23bfa9069867ba4e5df26809bb9a88b92f4f6204e3f4bcb8329246ecb3`  
		Last Modified: Tue, 21 Oct 2025 09:42:27 GMT  
		Size: 3.8 MB (3817363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:739dd94a79156a4c1275c94e86da7ed48d7e500fa5338fbadedadd96bc5320fa`  
		Last Modified: Tue, 21 Oct 2025 09:42:28 GMT  
		Size: 18.5 KB (18516 bytes)  
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
		Last Modified: Fri, 24 Oct 2025 02:20:32 GMT  
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
$ docker pull clojure@sha256:fa6db8212b9061232bc82160843ca151f5e71b366dcafdb35a47ccf3707bc465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.5 MB (219517156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a2eaea1d8b6f7ad5be0bc20a171f1a11d1f08c17d074d5228e0f25e60ab440`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
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
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56159dd64567535e8a55df9d0ae0cfaa55dc34f00b4178380ba1d5c2af374dae`  
		Last Modified: Tue, 21 Oct 2025 22:30:14 GMT  
		Size: 147.0 MB (147026969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a6cc02f6f302cbca0905d237b3b7d9ebe8c27b0c8853073fda7e25534e7a66`  
		Last Modified: Tue, 21 Oct 2025 22:30:21 GMT  
		Size: 18.6 MB (18620304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cacfd8eedc41bf6035ee79ee47afed8a64780ae77187c4f58bec7c972dd77447`  
		Last Modified: Tue, 21 Oct 2025 22:30:19 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae3ee1db4ccf7ece7adecf7d96ceae131745a8795ed42699bfafe819ea050c1`  
		Last Modified: Tue, 21 Oct 2025 22:30:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7554cbc0415286afc9b18df1c6edea9ef10fba881dad68b14e96f6d043783504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29a8a4b1bb42ab7febc3cf3b70fdca1cdf01d7efbd9fe554734a570c8638631`

```dockerfile
```

-	Layers:
	-	`sha256:2cd56244949314004f712e6718a5a70d52cbdca79c2bf9a34fdbea2829c70644`  
		Last Modified: Wed, 22 Oct 2025 00:39:02 GMT  
		Size: 3.8 MB (3812913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806b698eed80a65ba7f2b7a32b8caf90de151956435be71042b7ec753e772c94`  
		Last Modified: Wed, 22 Oct 2025 00:39:03 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json
