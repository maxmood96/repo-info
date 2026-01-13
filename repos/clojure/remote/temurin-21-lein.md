## `clojure:temurin-21-lein`

```console
$ docker pull clojure@sha256:ddb0867826b14852e7cf8d8244b2e7e95a7927a5260741bae4a3140909a93cc3
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

### `clojure:temurin-21-lein` - linux; amd64

```console
$ docker pull clojure@sha256:87a59024f4bb3534ac9499b82acda90e2f6a539ca2cd9e461133a4530a8ca62a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230628247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b561f06013f4b6132ed86922006d88cd930ceef9c585f85b3a36ac31bd6c54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:33:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:33:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:33:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:33:35 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:33:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:33:35 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:33:48 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:33:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:33:48 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:33:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:33:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:33:50 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:33:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7b85f51a41f3a208f45b7016040f04ab87b144417b7ae91a135ce2bfe562eb`  
		Last Modified: Tue, 13 Jan 2026 09:19:12 GMT  
		Size: 157.8 MB (157826042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7913f773e256f1b07d2d5d87226beb90e4fb13f9170dad7882a92c5ac14eb2ae`  
		Last Modified: Tue, 13 Jan 2026 03:34:19 GMT  
		Size: 19.8 MB (19802428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c0e73b2219e77121e9373367252e11eba5cd947f445a9d550ce059c34f3474`  
		Last Modified: Tue, 13 Jan 2026 03:34:18 GMT  
		Size: 4.5 MB (4517727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414d96bd9fea95599ec3b922e54c4d4a0cc1ad3218b6183659b970aef3658c21`  
		Last Modified: Tue, 13 Jan 2026 03:34:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:3000f4a8bb1133183df3eca722c3fdcee5e4572b9e269fd57af40155999ec136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e77da4180fdf5180d9d6f18b9fde75fe3adb3dec5edd775bffe7b5ed604f979`

```dockerfile
```

-	Layers:
	-	`sha256:affe80072ec81124a14e294f05b6454b3f61b4bfcf7b474c38075264f6fb5997`  
		Last Modified: Tue, 13 Jan 2026 07:42:59 GMT  
		Size: 4.3 MB (4284231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b98d0ef892ad390ce9852b6a1ce2e100457708ca9f6ef65d315ebd286b8aae1`  
		Last Modified: Tue, 13 Jan 2026 07:43:00 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b15decb9f160ea15aa38e3817e250d7f47a4be10260897b41369436e894970f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228624540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a3c757acad6c7b457103f5f56fdd78254ce2359bda5e082d8d11f9114452df`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:36:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:36:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:36:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:36:57 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:36:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:36:57 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:37:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:37:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:37:11 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:37:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:37:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:37:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:37:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d732a8fa8f6805605c963db6c7e46443b6bf575f2e9b491e5a093a1c114db85`  
		Last Modified: Tue, 13 Jan 2026 03:37:35 GMT  
		Size: 156.1 MB (156107580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fbb9c3371fa41b9fa8687510b4ced03906c0b4394a56f27d255e074df75b91`  
		Last Modified: Tue, 13 Jan 2026 03:37:44 GMT  
		Size: 19.6 MB (19632716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f4cde86014f7312f3a6ce8b96dc7eb1c4239c1475cfedf1213ece68c481446`  
		Last Modified: Tue, 13 Jan 2026 03:37:43 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682e96b31f21e2142ec23cfb9f0798bed1396c9c89a92a47323fd4b1fbeb3c26`  
		Last Modified: Tue, 13 Jan 2026 03:37:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:75985b5c9354b751bb4c2be513417314ce32c9c4c05b961e2be424a88e35b15a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e370b09aa2abe4249c20a1c912bffd0c7fbd73d7298ea776dc3a450f2d4ece1`

```dockerfile
```

-	Layers:
	-	`sha256:6bf6eeae034886883aa373262d1cff3fd1a526deda64b115a8fc697e37dc3040`  
		Last Modified: Tue, 13 Jan 2026 07:43:05 GMT  
		Size: 4.3 MB (4283870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a7fc8a5c6045b4135cfb2dc75e1b21e3d376b14ada1beb73521c7b6663bf625`  
		Last Modified: Tue, 13 Jan 2026 07:43:06 GMT  
		Size: 19.2 KB (19163 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein` - linux; ppc64le

```console
$ docker pull clojure@sha256:d7fcd1f9a52fabb5aa1df8a49b96124493e938228d2f193e16886443a4c8e42f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234811066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6f92898c36dd67ed3ac21f0d6f493a5265ffdc3e099568ee2810cf9e74f909`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 05:45:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 05:45:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 05:45:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:45:24 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 05:45:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 05:45:25 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 05:46:09 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 05:46:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 05:46:09 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 05:46:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 05:46:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 05:46:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 05:46:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:39 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8804680ddf0e6491c95d8d7bb1e9bc4a8f40508c1c43881c7cf1ac223df9a2`  
		Last Modified: Tue, 13 Jan 2026 14:04:38 GMT  
		Size: 157.9 MB (157942951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838ce5dcc275b9009e29aea90661ca7341942d5fdc22297037a716160e9b9cd8`  
		Last Modified: Tue, 13 Jan 2026 05:47:12 GMT  
		Size: 20.0 MB (20022542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eedb0c58de808a1a9140aa6822624acb8e75a972731d8ac1d5cf9f89f2db50d`  
		Last Modified: Tue, 13 Jan 2026 05:47:22 GMT  
		Size: 4.5 MB (4517767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e182f662f6fb1ed14d9350c6d89b0ac6c02ce18108c13e30d0d32cb28bc7621d`  
		Last Modified: Tue, 13 Jan 2026 05:47:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:e9424729449508e0da86a68fefc1106a3d0d67e31aab108686b5614273bb876d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd6f18f2ee71dc421bc00ace8c32da5025b2fb02c6e71c1dad7c22ec975e109`

```dockerfile
```

-	Layers:
	-	`sha256:0246fbe8258c12c1bce699d2188be739f9970890356f85221d6805b91c6b4dc7`  
		Last Modified: Tue, 13 Jan 2026 07:43:10 GMT  
		Size: 4.3 MB (4286104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:114fdb3616748a7c4ddd7985ff07c9bc5635c5607502fbafb89181d651550909`  
		Last Modified: Tue, 13 Jan 2026 07:43:11 GMT  
		Size: 19.1 KB (19073 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein` - linux; s390x

```console
$ docker pull clojure@sha256:91226fe21ed8931cf843c42e6de79275df42a8a51da47a59ce8e6f38e8611d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218188485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7867b613780ec321d34bb90c48d1b8201db84e5f5facd37ad326a908a569c78e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:05:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:05:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:05:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:05:12 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:05:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:05:12 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:05:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:05:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:05:23 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:05:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:05:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:05:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:05:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f4778709d6309aad2ad3cf29fbc96c579ca1e3384edc37a8fdf97673c6b3b8`  
		Last Modified: Tue, 13 Jan 2026 03:06:14 GMT  
		Size: 147.1 MB (147069834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30617b32c2b4cbee045781f7828ae2e29da0773830a49248e83a33f016df46f0`  
		Last Modified: Tue, 13 Jan 2026 03:06:00 GMT  
		Size: 19.5 MB (19462076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205839f5d8551c9ce77c1ab9a9624ae8f250bfe7b2bf8f964cd09b2f945951a1`  
		Last Modified: Tue, 13 Jan 2026 03:05:58 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb8b3e937c6e339c51bbaccdf67ae197ffd5885356cf3bd976e0dc591794f84`  
		Last Modified: Tue, 13 Jan 2026 03:05:58 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:7c9c258362e56f567c4bf89b56da4bfe64b6183d3455319f6fd3b8c151f67803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4295063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a369ca59c1fee64c65e6035baa77e44e6566b6b5aafd0ce90f678a2de88c771`

```dockerfile
```

-	Layers:
	-	`sha256:5bc51d3bd47f638d94eaebcc898c5daa8cbd6c412622b272c328b16d51a98667`  
		Last Modified: Tue, 13 Jan 2026 04:38:50 GMT  
		Size: 4.3 MB (4276045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:133e03d8aa65a0f08beabfc2c4eee5d998cb7229112c789c1b8bd1b3b59ff08a`  
		Last Modified: Tue, 13 Jan 2026 04:38:51 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json
