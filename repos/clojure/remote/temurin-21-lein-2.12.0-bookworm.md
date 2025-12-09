## `clojure:temurin-21-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:c56c43d6ba71cfaeda4707cab47082f9c6200ab5ff18970b3fef46e9a940d412
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

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:8a8cc210505bbc0763af53331a58b620bfd3899db9be29d79c417d1e681dd944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230627740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6309f5b92bf312d3e2968d25eacab1a1ecc1930834791675deee817e72b807a9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:11:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:11:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:11:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:11:29 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:11:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:11:29 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:11:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:11:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:11:44 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:11:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:11:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2e1d0e492652a26dadd3edce733469157fbece64ed1760dff07fb2c63640f0`  
		Last Modified: Tue, 18 Nov 2025 08:35:36 GMT  
		Size: 157.8 MB (157825966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f05eb6ba786ac55e9ee15c42052f715f121ba152e07fa9ab00aee47d3e25235`  
		Last Modified: Tue, 18 Nov 2025 06:12:16 GMT  
		Size: 19.8 MB (19802836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d4a6353c7f8d7f0581f1edb888432f21d66b0dcb54e44dc295043032a997e3`  
		Last Modified: Tue, 18 Nov 2025 06:12:13 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfed211c983da38cc8a787c5f2a5aa9a9ffa3a86c8a862a2064d736fdbf270f3`  
		Last Modified: Tue, 18 Nov 2025 06:12:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b5f73f09ae800b580e1db838fb3c42c88280ca0211c56be4741ddb0a92abebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e049409bf18d3496c6ebc02159566c6dedaa617d5b6410a2d342deb95fc8254b`

```dockerfile
```

-	Layers:
	-	`sha256:02bbf1ab99d45c8ecaf6bd331f6742608197efd04a10360ff45fc5da3fa5512d`  
		Last Modified: Tue, 18 Nov 2025 07:44:25 GMT  
		Size: 4.3 MB (4283588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bad0edd30065f75f7fb5e8366b58d42dafe891b46809fa807f2e2250937fd2ae`  
		Last Modified: Tue, 18 Nov 2025 07:44:26 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e30fb14b7da8c1c08a091d1b1ccd767cf4f204bd690dcd09067c486ad3ada9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228616987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da095446cf1ef2f2ae307f9d7e6ae62e8ae3a7bd98fa8d0531bd8211febd70c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:05:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:05:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:05:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:05:59 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:05:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:05:59 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:06:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:06:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:06:13 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:06:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:06:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:06:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:06:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b6d96bf738eca8f099272f0e47e6aadd0613f9b79a6e927ee36d2076338f9c`  
		Last Modified: Tue, 18 Nov 2025 12:07:38 GMT  
		Size: 156.1 MB (156107579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238926e48e2018b8b69d002cb4216af0ac25e8b07ec3eedba6adbde778bd4182`  
		Last Modified: Tue, 18 Nov 2025 05:06:51 GMT  
		Size: 19.6 MB (19632125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec1fe86d5b725b9e2e5faae6f88d8185e9d70668990c471340be2d55c5697ec`  
		Last Modified: Tue, 18 Nov 2025 05:06:45 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b151d6e4899bd2e66575f39db9ee42c3c1e376f93d8cee2534b56b888076166`  
		Last Modified: Tue, 18 Nov 2025 05:06:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bee175ec9562ed15db76dec2d3a0cc2d989232adab241be9144f8844faf03600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52213ddf2162656bced73afe86d718d2cd53c092843b790091ccb6e0c6aaa90a`

```dockerfile
```

-	Layers:
	-	`sha256:dbdc31975aaf59c41c3bc01bbe93daa9c50cbfc6ae8e961d3773095fc9f193ac`  
		Last Modified: Tue, 18 Nov 2025 07:44:31 GMT  
		Size: 4.3 MB (4283227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a804c3742f0aaabe49361426dbb0561d8f74571aa6585c0f3181edd64c5efc6`  
		Last Modified: Tue, 18 Nov 2025 07:44:31 GMT  
		Size: 19.2 KB (19163 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:9538671482e04802378da4630c22efdd460f3e3500e72803f626e4d44544e16e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234809731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1ca27db2be08e89dbddcf61e80ca6253890ef2bd7d27ab794d5d97ae49b1ba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:44:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 22:44:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 22:44:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:44:05 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 22:44:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 22:44:05 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 22:44:38 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 22:44:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 22:44:38 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 22:44:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 22:44:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 22:44:43 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 22:44:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84193563598712b437e18d1f55a29d0760b80aa62c9cc1125eb6b86822607f7b`  
		Last Modified: Mon, 08 Dec 2025 22:49:33 GMT  
		Size: 157.9 MB (157942939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cc24c9cce496ef73514731238d92506e4ca425b414fef1e034e69e2809dc82`  
		Last Modified: Mon, 08 Dec 2025 22:45:40 GMT  
		Size: 20.0 MB (20021630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c85d88eaecd4673f28b0ab60ad08f01fe4155d82e01b90bcfe334b68d34d41`  
		Last Modified: Mon, 08 Dec 2025 22:45:36 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29424ff691d360cbdce12420d22a33f11a04073f81fd981113c41ab50561ab39`  
		Last Modified: Mon, 08 Dec 2025 22:45:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0236b99c16d17856253c72862d44afc434c18faf7760c6e4e1a21392a40b53b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4d717db4e7443b1aec4bd649401e9f29df24a2d14a8194efbe7b0c82f7c7b3`

```dockerfile
```

-	Layers:
	-	`sha256:d56d83043619bac01653237297859ab9404cb648220546221c87a8a963831b2f`  
		Last Modified: Tue, 09 Dec 2025 01:37:40 GMT  
		Size: 4.3 MB (4285459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ac68d36f447434731b6adfbcc107aafbb608e7b70fdd20b1157b344e47b73d`  
		Last Modified: Tue, 09 Dec 2025 01:37:41 GMT  
		Size: 19.1 KB (19074 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:f4f39d7b97a4c0f3aa6dbade1000cde79dd0837e8457872bb18d28f3f53a3a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218186421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d33eebae9cdf222e8d549773511d4d52d14deb70eea3227d921df7a50a749ec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:27:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:27:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:27:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:27:33 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:27:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:27:33 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:28:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:28:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:28:14 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:28:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:28:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:28:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:28:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a4c2d7559d27df7dde4cd8b1f0f676863b5a0c885adc1250cf0bad409e4500`  
		Last Modified: Tue, 18 Nov 2025 08:05:38 GMT  
		Size: 147.1 MB (147069839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef24be45f571847ad14a35cb00c56382a44e4e4fd842df07513b615d69aa57c1`  
		Last Modified: Tue, 18 Nov 2025 05:28:52 GMT  
		Size: 19.5 MB (19460766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c8807f4e313768f2cec418c8b35d1714bf93d85d99316445597c2683db34fa`  
		Last Modified: Tue, 18 Nov 2025 05:28:51 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c32195df45fc5471795b1719a8d34846d05dd4c64acdd3ea35950f19ee177df`  
		Last Modified: Tue, 18 Nov 2025 05:28:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cf6dfcf3b891894ebb39c78739a1c4365bb1f7beb448269e12fe8dcc3772b546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9dc91b66a2548a0f22d82c48ce2d2fa83b78b9e956b47755b3d091c12af7ad`

```dockerfile
```

-	Layers:
	-	`sha256:76f745968e046b9cfe7fe80f4a9f2ab337b21ed307a06ac561cd0b5af6b71061`  
		Last Modified: Tue, 18 Nov 2025 07:44:43 GMT  
		Size: 4.3 MB (4275402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:290f34c225c09aa69c9e1be4f4e8246cc8451592f8c7485ac732a9642f845791`  
		Last Modified: Tue, 18 Nov 2025 07:44:43 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json
