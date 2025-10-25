## `clojure:temurin-21-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:471fbf8fd04676725bb88e978b28ce8ef75cd7010fd95b4a05423c1751b4d0e2
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

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9391b216fd6e64ea572b2c5d8843f7875d921a8ef6060cfda34ea77cd79b656e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208309244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0d0afcd26cb2632f79fc24b4d6992a651477a010f9cf63ee2e6ae1f0f8e358`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378677bad3b37de91c3fcdd8f43e830fde663a4e4df097c3c71e0fb5932c37ef`  
		Last Modified: Tue, 21 Oct 2025 12:08:30 GMT  
		Size: 157.8 MB (157804769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c79ea26b5a6ee0d293f125e54bbe53fc8ce3cbf9d903087184b00d1a64f8cb`  
		Last Modified: Tue, 21 Oct 2025 02:22:42 GMT  
		Size: 17.8 MB (17758014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad288d5e2436736d46c38d742aa82662d506b5893fef46148ba9c6152217127e`  
		Last Modified: Tue, 21 Oct 2025 02:22:40 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd3d42257ba1189310d2902a6e3b51cce2968e8366655e4b2d90ae0413946ed`  
		Last Modified: Tue, 21 Oct 2025 02:22:39 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1dbf5f772287be9885b5ae4f673be4ef241522c899711e9d518197c3562a09f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6a2fb7ebf2b3f0cd9c5bf5514da63cc9231d93c95081b40121d6dd883800da`

```dockerfile
```

-	Layers:
	-	`sha256:a20e0cb8b6af6fc42d8dd6ac3b71672b44198cdb5f87d5f857193d9e454beaef`  
		Last Modified: Tue, 21 Oct 2025 09:41:53 GMT  
		Size: 2.7 MB (2731888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb8b50ba7fe496ad43e7e1fab43940a467eb1e1bed6e7a436640ba287fabdc16`  
		Last Modified: Tue, 21 Oct 2025 09:41:54 GMT  
		Size: 18.4 KB (18446 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5e0dee248f913fc4971c92e598d29d46fa4b6a049372f5d8e3afdf5fda8865df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206292684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e7313ce01d6a583cb762de3a15c542ab85c4aa2df3386cc67b78702aea01bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f31f258f38b9e1441357731b5d8e213c43ab1b55c520099d3ed1ad6ce6d858`  
		Last Modified: Tue, 21 Oct 2025 04:01:49 GMT  
		Size: 156.1 MB (156081275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e720257966cbe67b3cce12d7a24bcf65965ee321267b478e10bd7f413394d922`  
		Last Modified: Tue, 21 Oct 2025 02:28:31 GMT  
		Size: 17.6 MB (17591090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b8924a12a27a4114565330eb30070312feb08e6835c35ba96d66fc1c794e82`  
		Last Modified: Tue, 21 Oct 2025 02:28:29 GMT  
		Size: 4.5 MB (4517701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba02a5740e7f06dd29b1e142fa38d3ac599a3c1f6aec5c67a2bd28de05b49e6`  
		Last Modified: Tue, 21 Oct 2025 02:28:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2bed5e50eca8b1e26d83d2eb795831981ddb2ef333e58ecd3df73cf35ccc3fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b06e7ae50c753bebd011cc2d00605226b8d62920e678d11fc0a0f87357dbeb`

```dockerfile
```

-	Layers:
	-	`sha256:a3ae6838e6dcdede9f923de522f9ecbb6a7b472059b93247c0e1ea8d547bab46`  
		Last Modified: Tue, 21 Oct 2025 09:41:58 GMT  
		Size: 2.7 MB (2731503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd2339d8bc7ca4affc5bd8595d97f55cdb316bee3e2b1cf50e749962a6f8c502`  
		Last Modified: Tue, 21 Oct 2025 09:41:59 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:089dce1e2ae717be5da676f5185402f69d90e26f4ae1309c5abcf674eaced77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212510035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fdd55772942ca77673648258f74ac97a74e466c8eece1b088a1899bf12e88e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
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
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:5a28d569c39dc949a4743122d7b5ec2d2e0664f1276c801bf984a711d80f2a1d`  
		Last Modified: Tue, 21 Oct 2025 03:26:43 GMT  
		Size: 32.1 MB (32068780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4de39d3ceb05c0fff8b1118b58bf5502c7dbd9415c253b8957509f09667345`  
		Last Modified: Sat, 25 Oct 2025 01:34:32 GMT  
		Size: 158.0 MB (157963469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d90204784788df633cbfc0bb7affd045ff80f0bf718e29a3c3ec98288cb0575`  
		Last Modified: Tue, 21 Oct 2025 16:04:24 GMT  
		Size: 18.0 MB (17959599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f722b3a7c64f99c523ad6559aceb0b4827bb356224d45cef6255e5d4b2d0b8b9`  
		Last Modified: Tue, 21 Oct 2025 16:04:23 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbe4bc1594e926c2c7173c5769c4049334e90ee49e7420a29104b56042efbb2`  
		Last Modified: Tue, 21 Oct 2025 16:04:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a088733b5acc087147dc608f80b5aeb0e0b1c0cd2a71a59642497ca9217af8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a8ef316ebbef41e85d11980949bd66cf50ba69f02e67563fc70f202536671b`

```dockerfile
```

-	Layers:
	-	`sha256:bbe4f1eaf56b8a148363892d332196d1b94870c1119c807ccdd3cefb3ae55d12`  
		Last Modified: Tue, 21 Oct 2025 18:38:55 GMT  
		Size: 2.7 MB (2733721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f871bdb860f2b714d71718b02da4e16f0f4143d3336d848ba003267d2a3b64a`  
		Last Modified: Tue, 21 Oct 2025 18:38:56 GMT  
		Size: 18.5 KB (18490 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a536643c30ad11dffb588e8688184835bc843bbb51531e59edc025818eb10919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 MB (195849428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc1db7909f4be44f7d39b55f7c81ae79c80c4355ae93cf83af5caad074f7b4e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
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
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:43b0f588b497b17691a3547afa4ae41853829cffde6930e6425ddae4a3f89278`  
		Last Modified: Tue, 21 Oct 2025 00:21:28 GMT  
		Size: 26.9 MB (26884356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2050d29f18bc4af2bcce04cace956b592934350a910fd6a374fc66bd83c725a2`  
		Last Modified: Sat, 25 Oct 2025 01:35:12 GMT  
		Size: 147.0 MB (147026967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7fc06d23882a3e17494bd022c7835645b4ea69644738f27425136468af6c71`  
		Last Modified: Tue, 21 Oct 2025 22:27:39 GMT  
		Size: 17.4 MB (17419906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35427304a9e86d760443c5ff60000919324b69712a219faf8e5a21c8c51d045`  
		Last Modified: Tue, 21 Oct 2025 22:27:38 GMT  
		Size: 4.5 MB (4517770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c7d4e5f7ac47a6980242679a6eeb605c9e390880700151683006960d1775e5`  
		Last Modified: Tue, 21 Oct 2025 22:27:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6ea7d0a089b2c566d17aa120bc2b7d18730eba72084979fdb39bbdb54bfa2e14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f9757919c0dd7616d82d9603fc172e8cefdd1b93b40fcf6a6f9f8747c063c6`

```dockerfile
```

-	Layers:
	-	`sha256:bf07ed7ca0909dfae679baf9b59d9e6288229a31459d403388ce7a94254262dc`  
		Last Modified: Wed, 22 Oct 2025 00:38:49 GMT  
		Size: 2.7 MB (2723702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:378bda2446346328eaebb54eec94437f4fd646c856added75debdd68212329c8`  
		Last Modified: Wed, 22 Oct 2025 00:38:50 GMT  
		Size: 18.4 KB (18446 bytes)  
		MIME: application/vnd.in-toto+json
