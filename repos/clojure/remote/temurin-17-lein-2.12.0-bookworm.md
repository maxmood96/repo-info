## `clojure:temurin-17-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:2ba5dacfdd9302e0f1f26648ea6f21ff3c27f7ce3a681a05010da2c25aef2a6e
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

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a67a3bcf135081768394f33c01eaeda7aceee6b62d4444632a212fdb358f311d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217650260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9d8f7f27e643aa18fe0f57b1105f109d30bdb9ec8045e2eea2a18081ee3985`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:52:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:52:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:52:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:52:05 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:52:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:52:05 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:52:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:52:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:52:18 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:52:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:52:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:52:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:52:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526769ae0ce57b9e78fd04f68076262f002084e3123e4ca54dd6808a6a5079ec`  
		Last Modified: Fri, 14 Nov 2025 12:07:44 GMT  
		Size: 144.8 MB (144847974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514bae0a4415ecbe656e6c1ec761352c48b42ea77ae95ff1d83b0d3f28aa0779`  
		Last Modified: Fri, 14 Nov 2025 00:52:50 GMT  
		Size: 19.8 MB (19803045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1e7d5f5c00123f4fb282818171d0305a959c228cffbd3e72ab89e769d2ce86`  
		Last Modified: Fri, 14 Nov 2025 00:52:48 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607c86664bc09f458ccd43fe7042cf7c685fc5577a08d25f213240f59257c9ac`  
		Last Modified: Fri, 14 Nov 2025 00:52:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bd7ca0747cd4f3436ea1b6e9c451bd36e79eaf6dae4bc4a7630b13701d2bdb36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4298204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4801b405ba27edfa67ae32a7095c2017fbd9cc1e088f1fcf4ea663b91f19d94`

```dockerfile
```

-	Layers:
	-	`sha256:e29d8b83e2a009b69e5b7e8fb1c366438e8e64fa6ec6694e281b687a94647714`  
		Last Modified: Fri, 14 Nov 2025 01:39:37 GMT  
		Size: 4.3 MB (4279836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5db6ed58d083454f91c3645a4a0e7ceb130ad0f73e86155b1a88e3283f7902b1`  
		Last Modified: Fri, 14 Nov 2025 01:39:38 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:840a8115e918054dfd53f1ad2e73d1123fc6579a2f9e7c0ee0a9a90fa691d7eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216189749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb845421c28082332c3a7eb6bca0a75eccfda734b2fc656cd7e3c219a63e7d3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:53:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:53:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:53:59 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:53:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:53:59 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:54:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:54:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:54:13 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:54:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:54:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:54:15 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:54:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7a406c716f76b77b181917991014d8797f9dfaf3f8c703c7f5fbfaa26eb6ff`  
		Last Modified: Fri, 14 Nov 2025 00:54:36 GMT  
		Size: 143.7 MB (143679910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845c44b05ea0d979d9151981093a0afad63544d3632c3905e3f50b0eb4d7f32b`  
		Last Modified: Fri, 14 Nov 2025 00:54:44 GMT  
		Size: 19.6 MB (19632214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4bedc322b5299131d91c59ac9e8638380f1d5c0504acb6b8de828f4a2cc4bc`  
		Last Modified: Fri, 14 Nov 2025 00:54:42 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a4adf3de8c910bd06fa9321ae12474f45c4fa63f7a0e3f4c73bf6e6910964e`  
		Last Modified: Fri, 14 Nov 2025 00:54:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:88667d009703b39ad08b8ed6f06528d61cf0bc2b8f801dcf2b634f307b76496b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4297940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e011e52cee050fd46a03738cea7345e473646dd8cf83c32f03d39968e0407a2c`

```dockerfile
```

-	Layers:
	-	`sha256:d953acfbf90e93955d17ec5714598fbd06c72210bc938c735136dc84ce11ade7`  
		Last Modified: Fri, 14 Nov 2025 04:37:26 GMT  
		Size: 4.3 MB (4279451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f968470e045b8d4ae6b2cebd7a179cf11593b3c930d763e0dcbfc44c63763344`  
		Last Modified: Fri, 14 Nov 2025 04:37:27 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:e4b89b4843f0cb2760ec2e9fa8c19ca4619994a7955cd2259c3d0dcffa01290f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221392367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04721a57866a0032ab7861486b889882d0a604bf9882c674c5cd69b02ed2fb97`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 06:59:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 06:59:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 06:59:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 06:59:12 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 06:59:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 06:59:12 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 06:59:39 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 06:59:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 06:59:39 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 06:59:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 06:59:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 06:59:42 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 06:59:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03721825e92ed5d3670f8aaad934e33c62dc316ab4d6db4103a5f455b6275fca`  
		Last Modified: Fri, 14 Nov 2025 07:00:25 GMT  
		Size: 144.5 MB (144525224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80a24ec9c1c021d8b6a02cff84baf2ca471e23ae641ad9161a9c577c145893e`  
		Last Modified: Fri, 14 Nov 2025 07:00:32 GMT  
		Size: 20.0 MB (20021715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43984172cb1ad06d9a616c7cc88ad9c833d0d3695d237c1c9bb94e5216d27c0f`  
		Last Modified: Fri, 14 Nov 2025 07:00:31 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ef483ef4a9c1faf6e278f539a5e9b21b9f52f19054e230f023fe4b67e22f81`  
		Last Modified: Fri, 14 Nov 2025 07:00:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1b1ae63a6c940991b0f2bdc93802f1955671743b52a125eae843a7452b9bcdc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f0f90003713fb4c8d5b03ac3514d940c70813ba7b896e49d835a9a15513207`

```dockerfile
```

-	Layers:
	-	`sha256:307df620af54ec482818e76f63693281cce64775b039a98c81bfe5fdc5113f1f`  
		Last Modified: Fri, 14 Nov 2025 07:37:13 GMT  
		Size: 4.3 MB (4281695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c68dfc1eaa58ed04b0779e6019b59b4b1219d9516a4dee82eddf2c30d64ae90f`  
		Last Modified: Fri, 14 Nov 2025 07:37:13 GMT  
		Size: 18.4 KB (18412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:6fa8a076582fe7c79a84a58fd05e9e21100960f60a4bb359dc3240af25a2b1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205976061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5843aa5512e87f7f3c15213dbf74f7b3d15d52823e0a0ff3256861b020f917a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:54:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:54:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:54:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:54:59 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:54:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:55:00 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:55:09 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:55:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:55:09 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:55:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:55:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:55:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:55:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9faef0ec95b30e3730f96a131ace05d8a92e63ac3db86dfbb78893f35b3e87e`  
		Last Modified: Fri, 14 Nov 2025 00:55:36 GMT  
		Size: 134.9 MB (134859061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecbc7993c384cb415958888b48b915afe9fbe5fbec567bf59a7f1177875e1b7`  
		Last Modified: Fri, 14 Nov 2025 00:55:44 GMT  
		Size: 19.5 MB (19460718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736da6b84203afba2eda8b7574a638cbf37b631da28b21ce2f80910bd33d462f`  
		Last Modified: Fri, 14 Nov 2025 00:55:41 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c9d1029d425d8e6b9b2976a9f97b5ac6f7875f487bd06fab5acb427e91cb22`  
		Last Modified: Fri, 14 Nov 2025 00:55:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9fbe000aba33bc783838425fa3c8f93faa925d4e1d4876df0b03398b3d75b26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4290018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b579633ee1104d0b932919ff2ed1b2fc3227c9d20aec6b351a86d35b05b96d2d`

```dockerfile
```

-	Layers:
	-	`sha256:be6f7116287cdc0aba2fa22d0584667acd46f3df5f3a78f030808874b6e6b6cf`  
		Last Modified: Fri, 14 Nov 2025 01:39:51 GMT  
		Size: 4.3 MB (4271650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7b777dd2e59d803f6eb3e030430c50d3a9d4526e327e2da7d3ba741be041894`  
		Last Modified: Fri, 14 Nov 2025 01:39:52 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json
