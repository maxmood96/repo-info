## `clojure:temurin-24-lein`

```console
$ docker pull clojure@sha256:17565b4cf7595767c8a2550d82d0acd1857e8ef677f928b74c74474f4f800c59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-lein` - linux; amd64

```console
$ docker pull clojure@sha256:7819b3ed94c03aeaee52bc8b7c3cf26cae0ce967beff73be8614ae522dac6011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (205025952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f26d1ac6b911406ecc79a429c1d9bc01852281063cea964db808ae7fc2937a6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_ROOT=1
# Mon, 28 Apr 2025 17:24:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fb2ec56055b014d8a82b9b5958452bf2b16bc85ba0fb4330b3b68a8e31735b`  
		Last Modified: Mon, 28 Apr 2025 22:08:22 GMT  
		Size: 90.0 MB (89951966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40ef7cf3616407f70310555ee00cf05d0b80932eaca94099249e56bcc7a86c1`  
		Last Modified: Mon, 28 Apr 2025 22:08:21 GMT  
		Size: 62.1 MB (62068214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6235e02ace933543a835088ba4f3ab25ddb7cee93bb342edd93a76f5bc532cae`  
		Last Modified: Mon, 28 Apr 2025 22:08:20 GMT  
		Size: 4.5 MB (4514145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deec343a2e47ab0ffdbb53fdd91882623f5c843f7f38c99afb4f011d1a514964`  
		Last Modified: Mon, 28 Apr 2025 22:08:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:406d307744656edf74347b1d5d38b3cfbe46e12d644b183fe0a63833a9d771af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6506005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643ba2ef6c0d10ca5e8f5b7ed48177b2db133f4aaf3e44cb7f49dc8617082a97`

```dockerfile
```

-	Layers:
	-	`sha256:81a6e177ae360539e746a3663d15493813e41a80812ceb2a10be3081120845b1`  
		Last Modified: Mon, 28 Apr 2025 22:08:20 GMT  
		Size: 6.5 MB (6486939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d553d3a32394c5c32a325bdf91ec6d8f875e185365e02b56213d8515dafb897`  
		Last Modified: Mon, 28 Apr 2025 22:08:19 GMT  
		Size: 19.1 KB (19066 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a8aa5947a2a16e6efa17ffeaed51c18199ece7968f327a0c36b66af7ed07d9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (203969060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411014632d55a14af2dfbc95f6f375ddb5a9023a9092c91bc5cc9f7b549e4723`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_ROOT=1
# Mon, 28 Apr 2025 17:24:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289d29a9fc32a83e7866e7172e5148e804d7fa6b5e264bedd1edcbb3907d41e8`  
		Last Modified: Wed, 30 Apr 2025 01:49:38 GMT  
		Size: 89.1 MB (89091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f207d52eaca656e1e388d7f8915c95a41fa3060d8cd6723a06c6acedba7a01cb`  
		Last Modified: Wed, 30 Apr 2025 04:50:19 GMT  
		Size: 62.0 MB (62035563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a2b14ba3594a3b68b3fb43eb5b5c9f179b43cc3ab6f0afb8a98c87e6b0f945`  
		Last Modified: Wed, 30 Apr 2025 04:50:17 GMT  
		Size: 4.5 MB (4514190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666cc9ed956d464f3073cddd7eb59ce9d32ff9e26569354967956b00552619be`  
		Last Modified: Wed, 30 Apr 2025 04:50:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:dfa8f14dd4a74082cc8375c9b41c49784f73f273da74df0797d10f8e0f288815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6511865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ec8bd3a09d5f82bba4e5ec79cfafdf68fbbf05fb2423374d30744f6b9c02cf`

```dockerfile
```

-	Layers:
	-	`sha256:74f577807eb288d673c067097d2baa7c431050132646fddbba81f4123012cad2`  
		Last Modified: Wed, 30 Apr 2025 04:50:17 GMT  
		Size: 6.5 MB (6492654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b81c2bf73a22004b26d1b0e3af5a65e5a716d1621ab3df85d47d9322594aa440`  
		Last Modified: Wed, 30 Apr 2025 04:50:16 GMT  
		Size: 19.2 KB (19211 bytes)  
		MIME: application/vnd.in-toto+json
