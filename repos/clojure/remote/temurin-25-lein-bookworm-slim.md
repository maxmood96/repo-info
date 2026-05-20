## `clojure:temurin-25-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:3a0e65516e2a859fbd131ed9fbe68c21fc243da39ed0baa2694a252ba4b49960
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

### `clojure:temurin-25-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:499bdefaf6b026a5a339320df8e6932af1159100ca3cadc5c8b5554ce7ffe3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143086528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f89b8aa9c5cc400c1f1bb0b919094d8fabaa91c3dc4af5aaea2c8ed61c5c8e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:00:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:00:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:00:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:00:45 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:00:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:00:45 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:00:59 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:00:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:00:59 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:01:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:01:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:01:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:01:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ff1f6325c97f1fcdbf05a281f90e6a30aaa9366ab5587a57f896310bbe1b59`  
		Last Modified: Wed, 20 May 2026 00:01:21 GMT  
		Size: 92.6 MB (92574586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd73868b608d5d6b18e6cc70b1aaf18961bdc420240aa693278ff7720b58928d`  
		Last Modified: Wed, 20 May 2026 00:01:19 GMT  
		Size: 17.8 MB (17760255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b00cf6572dfd36d3c844ea65e083314ac420744bb711c0e0e01867cbf119d2`  
		Last Modified: Wed, 20 May 2026 00:01:19 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542a5d4d551c21ec4530d2f2f73cde53fe8ab0365ab47bfd1f2e26180e2e4f17`  
		Last Modified: Wed, 20 May 2026 00:01:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:661a397aed3e9f1b350c65b117567c604483791dee46b99d8997e4f70baee3dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec570d15587a1a4f05ef4f39ae4c84b8c89ac1d114654e6ca6fbdebbfd12c6d9`

```dockerfile
```

-	Layers:
	-	`sha256:28267f684b988b987f2043abe7b0fc6600a67650acde5c7f61dde4f2f102080f`  
		Last Modified: Wed, 20 May 2026 00:01:19 GMT  
		Size: 2.7 MB (2698751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:571ad892264ee0ae298cf79e2324acd082e8876bfa1093174b980b2253f11eac`  
		Last Modified: Wed, 20 May 2026 00:01:18 GMT  
		Size: 19.2 KB (19211 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b3c3736d921823994d04e1fcb2bbd34d8450ccb5d03fa9eee17ec0dd44f58435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141769317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1887029e352f66053a6b60e93597a391093fc15e83f49b48a3bd50801b405f8d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:07:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:07:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:07:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:07:38 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:07:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:07:38 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:07:52 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:07:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:07:52 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:07:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:07:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:07:54 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:07:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8dc3ec435dd42bf1159ee0240f038786482394ada4de4ae6caa1f37689d7c7`  
		Last Modified: Wed, 20 May 2026 00:08:13 GMT  
		Size: 91.5 MB (91542260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a755c13ecbba953f9836e30d2f623dc2123e9a33e5d9878f888b45a32a1268`  
		Last Modified: Wed, 20 May 2026 00:08:10 GMT  
		Size: 17.6 MB (17593848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30368fe456046d792f979ac3019b5bb85ddbe51394c5be6fe37cc8b3fae4f701`  
		Last Modified: Wed, 20 May 2026 00:08:10 GMT  
		Size: 4.5 MB (4517736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779503ab51d0963a0a29465e5c534afd0eb77759ae7c0dfa5b0e3ec5ce9fd576`  
		Last Modified: Wed, 20 May 2026 00:08:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:75793bdb5f19ca12a6828e3a92bce050ec337c1bc5557c588575d39f8fb50a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791d30106d3ab9c7d1550a2342cbcef986fef52da26ef4c037cc7fe128a8bed5`

```dockerfile
```

-	Layers:
	-	`sha256:1a822e56f470269171d0d96690d0e8f58e1bb07d2a522c4ecce6d9ebf44bacf8`  
		Last Modified: Wed, 20 May 2026 00:08:10 GMT  
		Size: 2.7 MB (2698387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4939aa6f3ad54dd6e060ac64977747c0a0d18aa6b2f310aff516f6967649b418`  
		Last Modified: Wed, 20 May 2026 00:08:09 GMT  
		Size: 19.4 KB (19357 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b96e8ffe0406ef47eb07b4271f88ce5c6be60774c3e3af1ead5dabc35434e42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146471282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58217c536765f750296b93e5c42e647423ab85b8037b17acd72c2defd1c9866f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 06:05:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 06:05:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 06:05:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:05:37 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 06:05:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 06:05:37 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:06:10 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 06:06:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 06:06:10 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 06:06:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 06:06:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:06:14 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:06:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78ded15bc8f36026eaea9b7d9a5e84177cac4980a3a75d55268b17ef4c646c9`  
		Last Modified: Wed, 20 May 2026 06:06:46 GMT  
		Size: 91.9 MB (91914030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0bc8344c9f8bc6e53459f8384c05f323c16094933288125ce5d6d41915c73f`  
		Last Modified: Wed, 20 May 2026 06:06:44 GMT  
		Size: 18.0 MB (17963376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b784271c67a89b13cf5f7da9540fb86faaf47ca814898559c935ba0fb79267e2`  
		Last Modified: Wed, 20 May 2026 06:06:44 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e7fb99e7bc8a866ca1ff56ad96ea49aea32305b0efd2963e99e750a3a4ea01`  
		Last Modified: Wed, 20 May 2026 06:06:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7643cc5de641b37f0211d08499e5417df94d8c76e08492efe30cdfd60af1fb44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2703175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cdd0f18759f3b85613e585bed02eb24094a7022a8549dae09c99f962f10b500`

```dockerfile
```

-	Layers:
	-	`sha256:dcd1065ef7dd6d43c7f9acc768e222bec70ee0f3222e70b304ff3a5a0cdcce94`  
		Last Modified: Wed, 20 May 2026 06:06:43 GMT  
		Size: 2.7 MB (2683908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6017b5ec9561b6fe9b20f85425a84514292e4713c19ec353e500ae6c083c5f`  
		Last Modified: Wed, 20 May 2026 06:06:43 GMT  
		Size: 19.3 KB (19267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b75211b750f0ddc2c32ecd5374a7f95a82219e89bce582e14028b1afc66e5ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137250781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a285596f3e70a8f603614cf9fb130e01614b81048171b04129bcc454c4fcb0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:47:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:47:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:47:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:47:21 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 01:47:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 01:47:21 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:47:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 01:47:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 01:47:31 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 01:47:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 01:47:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:47:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:47:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97a7b8dd4e00998de1e83e107f400dfc58074c7f5a41552803d432819995991`  
		Last Modified: Wed, 20 May 2026 01:47:59 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbaf39ba4d0cb63223595210c18b2e2efe67f04dc5d76a2b4b678f5ed277bd18`  
		Last Modified: Wed, 20 May 2026 01:47:57 GMT  
		Size: 17.4 MB (17423700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4e425498fe3bd750566c40caf1a2b2f426a6856c724a48446a17cc2022adbc`  
		Last Modified: Wed, 20 May 2026 01:47:57 GMT  
		Size: 4.5 MB (4517736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f53f8cb2565f60d8f8619de29b5da5265238d0d78a1bf3b661c55e5fe1b18d`  
		Last Modified: Wed, 20 May 2026 01:47:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8cc97eb569ef12370c2f9be6616bcbc31edf988d782042c25b55e19a4c8c51c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e917425029ec23795b6a5fb1dae197acdd23d6bb7f8c11ea5d6339fa55f65ef`

```dockerfile
```

-	Layers:
	-	`sha256:5d83862b99c4c3a8e9d6df6e79cf73091895a8eb4fa8ae3b429cf598b28739e5`  
		Last Modified: Wed, 20 May 2026 01:47:57 GMT  
		Size: 2.7 MB (2675127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a280285500bbca103a925afc6a1230220432ecfcd44e18b5a03835ef15c611`  
		Last Modified: Wed, 20 May 2026 01:47:57 GMT  
		Size: 19.2 KB (19212 bytes)  
		MIME: application/vnd.in-toto+json
