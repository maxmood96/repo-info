## `clojure:temurin-21-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:dbdd1dbb38faf1f28df10ccb82ee1ef6314e37a7f5f2a22d98a3cc8c418f18cd
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

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; amd64

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

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

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

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; arm64 variant v8

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
		Last Modified: Wed, 05 Nov 2025 13:10:37 GMT  
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

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

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

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:2cca4ea3f9892e2c216cdd803ac2f5ac821a826bc19ab57576a82efb888eb7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234228277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e755e2ed43695bf94d998f2593ee0a56148b3978042127b58c961ed4f95a33f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 13:35:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:35:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:35:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:35:42 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 13:35:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 13:35:42 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:36:10 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 13:36:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 13:36:10 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 13:36:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 13:36:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 13:36:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 13:36:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8603f9efd678d7e42bb5392a1026619d0919c9539d7c56b601271dc48ce60b5`  
		Last Modified: Tue, 04 Nov 2025 13:37:00 GMT  
		Size: 158.0 MB (157963427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20509fe8a1d37f66de7f48efbe877bad48349c481c368abc31929f1e276db9a`  
		Last Modified: Tue, 04 Nov 2025 13:37:10 GMT  
		Size: 18.6 MB (18636544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e431f8103590e8ce6f4235b95eaa3acedc5c5b77de1df17ddf753fc7e619d8a`  
		Last Modified: Tue, 04 Nov 2025 13:37:09 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3148813bdefbedca0b71c866a5a109a26293e59ae0031bf467db10b9927c1e5`  
		Last Modified: Tue, 04 Nov 2025 13:37:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4cbfdfe4538bc722b9881deff6fa424bf5bd379757758660b7c1147c682c7d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e439607ff949c61fef7e825816348ec2ef7f0542a0fd805bc0bfa7060306f5ca`

```dockerfile
```

-	Layers:
	-	`sha256:d969ed9fab701c76c90f29ae66266f9e19e4ceed95ba8b1d9fdd03779aeb03f3`  
		Last Modified: Tue, 04 Nov 2025 16:38:21 GMT  
		Size: 3.8 MB (3817484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fcc8e487a9a703472d0078ee9e66d3e8492b47ed7ccda8e33ad9523baf4062f`  
		Last Modified: Tue, 04 Nov 2025 16:38:21 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:6dfd3d71224469fac5537c01695cdef530decb8c3bdf710e96ca212656b9bec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224413751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d55027c00dd85a88db90b4fe4eb86b7875275fd89f89d66bd266197bd63daf1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Fri, 07 Nov 2025 06:33:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 07 Nov 2025 06:33:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 07 Nov 2025 06:33:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Nov 2025 06:33:03 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 07 Nov 2025 06:33:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 07 Nov 2025 06:33:03 GMT
WORKDIR /tmp
# Fri, 07 Nov 2025 06:34:33 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 07 Nov 2025 06:34:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 07 Nov 2025 06:34:33 GMT
ENV LEIN_ROOT=1
# Fri, 07 Nov 2025 06:34:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 07 Nov 2025 06:34:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 07 Nov 2025 06:34:49 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 07 Nov 2025 06:34:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f02f73111e105921cc185c6c33251c2d50b1703e0a326d71d528fa31b308a9`  
		Last Modified: Fri, 07 Nov 2025 22:59:25 GMT  
		Size: 153.6 MB (153593539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eab8a0694c2a94b63bac43f71ae459023e117cfbd1b9c9dacc941b7a979c97`  
		Last Modified: Fri, 07 Nov 2025 06:39:18 GMT  
		Size: 18.5 MB (18531067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da927d70cedfee184c09d7bdd375b179d2defed535252f705d6ba2a7a7feb45e`  
		Last Modified: Fri, 07 Nov 2025 06:39:17 GMT  
		Size: 4.5 MB (4517792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dcd1f91d730fb4e534fe2a702fd1eaa806a168aae85b1ba229dcef83fe9a00`  
		Last Modified: Fri, 07 Nov 2025 06:39:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a4971809ed5ac115a4ab3b9af50bbf3b05f0b0e4c600cb274396939966ccc176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3825357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5604861d50b69ef768869cb0d601e771ef6ab35c88d92e3a3f92876e6cc8b901`

```dockerfile
```

-	Layers:
	-	`sha256:b92bb63b33d6bc04d613bcb4b2d15a74520889a84a09e6ddf7ca3b605cfbcbad`  
		Last Modified: Fri, 07 Nov 2025 10:36:50 GMT  
		Size: 3.8 MB (3806961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0f3b089a9cfa0b5110fc2106774113e422c1845f008bf73f616238823530e6a`  
		Last Modified: Fri, 07 Nov 2025 10:36:51 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; s390x

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
		Last Modified: Tue, 04 Nov 2025 22:42:08 GMT  
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

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

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
