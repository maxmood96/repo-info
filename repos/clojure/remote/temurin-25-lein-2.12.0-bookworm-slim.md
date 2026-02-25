## `clojure:temurin-25-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:1ccfffffecd613b4f1088d35a23c152e875d4166950dde329bd43e786b980f4e
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

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f66adaf3b50d84f29af981843c98afb194ae1eb62727ad8542492ad7e027fbd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142769529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102dfc12cf86f57f001195119cde76d10961539b748c507ae878bc53bf22abc7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:56:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:56:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:56:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:56:38 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:56:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:56:38 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:56:52 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:56:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:56:52 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:56:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:56:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:56:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:56:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd096e7c40988423f6c77bc0fc7f410f4d75089c5730da8b282832fbd83a174`  
		Last Modified: Tue, 24 Feb 2026 19:57:13 GMT  
		Size: 92.3 MB (92256297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e934cfd30da56d5ed12ab4530a9393240499684f7fc5c0ce3b514e437734b099`  
		Last Modified: Tue, 24 Feb 2026 19:57:11 GMT  
		Size: 17.8 MB (17758775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54895648eb324a5f55df197c3f72d41b4bbfc2cbf90aabe11cacb4a831a7917c`  
		Last Modified: Tue, 24 Feb 2026 19:57:10 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c8041a8e5b69fab7d8d7bd3076d0516811875d5f0b915949c65ec80121f5b9`  
		Last Modified: Tue, 24 Feb 2026 19:57:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9d95642e011ce68cc6955e3e9183b84e06d8acee3961588fb395d7f2ccad8ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3fc7e71dfe64f8a13772c3984d12b1c8ad2df342f81e747fb35f6ae1d3e1d1`

```dockerfile
```

-	Layers:
	-	`sha256:37dcb050074b46fe6485f2e0a52f80a3647a77e8531dc3f0d93d6a3728ef6440`  
		Last Modified: Tue, 24 Feb 2026 19:57:10 GMT  
		Size: 2.7 MB (2698110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f7675e1d901d93d718ebc0126f72541ada9e55506a646d7c592f4991d11a733`  
		Last Modified: Tue, 24 Feb 2026 19:57:10 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2961831a9808bac8008b4f34c0977855f19600d4cf184a0d64bd609137611a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141514243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37a41e322eecd75a2543bdafd72efe2232376c033db596f189725d5cb58ccba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:07:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:07:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:07:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:07:31 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:07:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:07:31 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:07:44 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:07:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:07:44 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:07:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:07:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf7db0639b9604757615e38919ccec56b3ea72873f074df0bef51269a953f2e`  
		Last Modified: Tue, 24 Feb 2026 20:08:04 GMT  
		Size: 91.3 MB (91288270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72e673f29323766dfcda9f6c2c900637a6236e67928304f97a94a3f4a9c0077`  
		Last Modified: Tue, 24 Feb 2026 20:08:02 GMT  
		Size: 17.6 MB (17591724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3e155630a62d000262351734859ed533624d0e2c777f1159f067752c7e71cf`  
		Last Modified: Tue, 24 Feb 2026 20:08:01 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f757ea383e47edf2f5c0a7a12626c60df72add6fb3ad74a379a13bf60387ab2a`  
		Last Modified: Tue, 24 Feb 2026 20:08:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:252d17d3c8b50fe7ff1cffb86588c4f16ddbc7df43398f6bdde1b98becf6dc86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2716949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81d6591b6ada693b1c61ef13c7d1c9d36ab40ea6d5948c94deca86708891f95`

```dockerfile
```

-	Layers:
	-	`sha256:6ba09ce3963301c706e2a7eff437dc83aa83692a451b7bc590fecee5f31b44ad`  
		Last Modified: Tue, 24 Feb 2026 20:08:01 GMT  
		Size: 2.7 MB (2697746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:133782fb2b1df75d2d02e3f15d79ec46e73059b5b5db3929866ffcb98d4d635a`  
		Last Modified: Tue, 24 Feb 2026 20:08:01 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a5d0b41f175876b61ca27f2672e464ec35f3379533c8238e166f22686819afaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146180905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbef26292639dba3f00ae2607d943fd495c8a6566f9db2f37615c9f1ef11464b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Fri, 06 Feb 2026 00:46:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:46:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:46:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:46:09 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 06 Feb 2026 00:46:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 06 Feb 2026 00:46:10 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:46:55 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 06 Feb 2026 00:46:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 06 Feb 2026 00:46:55 GMT
ENV LEIN_ROOT=1
# Fri, 06 Feb 2026 00:46:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Feb 2026 00:46:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:46:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:46:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91cb234547828975d01511eb3f1e2f07f4c3226976323dbaf0a3fe8832f8431`  
		Last Modified: Fri, 06 Feb 2026 00:47:43 GMT  
		Size: 91.6 MB (91632917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171b4156b02e7968173386d2ba03194ae24075715430b85f25bf221e71a61a92`  
		Last Modified: Fri, 06 Feb 2026 00:47:41 GMT  
		Size: 18.0 MB (17961096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda48d5d7550131f3d6aa85fc87b15b2d2bc9579a8b8436436612637e687c922`  
		Last Modified: Fri, 06 Feb 2026 00:47:41 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6106f317c5d6e3abca94c14ba7805b0aca21887384cda4bfcac8fe96a8a6348f`  
		Last Modified: Fri, 06 Feb 2026 00:47:40 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d1d8ca32829239be9a8fe9fee1434f1b4d8d0a98aa78806ae79de484f879eb4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2702381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2ad8abf935d7b1b1f5218f31954cfc482fd8a0f7b31891604b3813a99bc261`

```dockerfile
```

-	Layers:
	-	`sha256:4801988d5886e13e6deef6498b5775a26075164028c63db3cf8ea94c0818519a`  
		Last Modified: Wed, 18 Feb 2026 00:03:45 GMT  
		Size: 2.7 MB (2683267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a3f9371e9e651c5b73669984cf336cfc5204e35f4a3e43dc69194087f8ecf8a`  
		Last Modified: Wed, 18 Feb 2026 00:03:45 GMT  
		Size: 19.1 KB (19114 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:23985aa37fa252826a802933ba7011d935fb2e857f06e4e74c774c1e486cef65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137064744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3244c7c53562c1424c589dc6b6eee787bcb14d4549b33c8b6fd1ec77e7823b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:22:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:22:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:22:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:22:55 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:22:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:22:55 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:23:28 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:23:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:23:28 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:23:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:23:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:23:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:23:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a2c7f155ba43475a58ce53d7548c5de702bcc0cc952b4fe414a2ed67d07e94`  
		Last Modified: Tue, 24 Feb 2026 23:24:09 GMT  
		Size: 88.2 MB (88233846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9a3f30508869f9674f86fa6de14e5ded30afcc5aeb9f827dbf24b2c0313e43`  
		Last Modified: Tue, 24 Feb 2026 23:24:08 GMT  
		Size: 17.4 MB (17421191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c6e810204baa620baeb52774b91c5e38691aedbd19f36fab8f0e4e8e5fcb6a`  
		Last Modified: Tue, 24 Feb 2026 23:24:08 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dbac5009380a7762bdc2ad39a9a9cc9599a48379ac6c3df8a3cbdc911f861c`  
		Last Modified: Tue, 24 Feb 2026 23:24:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ef13fcdc1c6d5d08592ffea58ca065c28e8ea0c3f3613c06c653f154ff7fd99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7412a4c005e2313b06e2b90593511f80eeeb9c686fe52776c27915af59aa03`

```dockerfile
```

-	Layers:
	-	`sha256:1e1973a84a2b39d451a7d8823d8a3311f57c17bfc588c82d6863fb74115ce2d4`  
		Last Modified: Tue, 24 Feb 2026 23:24:08 GMT  
		Size: 2.7 MB (2674486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3996807e0e2970505df650c5b7a6b663c17ade60da99b3966ceac352ed9644de`  
		Last Modified: Tue, 24 Feb 2026 23:24:07 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json
