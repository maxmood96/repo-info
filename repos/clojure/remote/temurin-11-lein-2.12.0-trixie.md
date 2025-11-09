## `clojure:temurin-11-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:baf274673e4907514d7798f63e59a31352a81e8faf68f96b64b8677f6a7cac7e
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

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:7ebcfc2700770bbefab7406995fbc1f5bc20c6591db78a80102621d6c00cdfda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217349152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b8c64484d73bacf10d241e71bb3049b62404eeb69c1ed7612bee8b72b3ec3b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:41:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:41:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:41:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:41:30 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:41:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:41:30 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:41:47 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:41:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:41:47 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:41:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:41:49 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ca2654ad3ee0951e5d9185f8adc67ee47e4a811e5d38d936dec1f6c3ebe5b7`  
		Last Modified: Sun, 09 Nov 2025 03:05:44 GMT  
		Size: 145.0 MB (144966518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3852b62b79800fad2bb720768b179250ae47c24f92cf1d6ee696d69fec60eadd`  
		Last Modified: Sat, 08 Nov 2025 18:42:24 GMT  
		Size: 18.6 MB (18579256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a5e6c6faced2c0535ff71f8b922e2bd36756f68235bb5a335d889cbe3dfbd3`  
		Last Modified: Sat, 08 Nov 2025 18:42:23 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:38ac266036c79ba0987780834d98c9d02f7bb1787a665886cf369b4b8e8188b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546b4e759837475d83a56e44928f17d3d0750ed4e78504e1c96cdeb0b6d5fefa`

```dockerfile
```

-	Layers:
	-	`sha256:d23ec2ef45f02b91ffba7ec008000a4a38c3305a7aae37ff7c0d323fa0281048`  
		Last Modified: Sat, 08 Nov 2025 22:38:29 GMT  
		Size: 3.8 MB (3833525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adfe19cacbb86affb3923e4817447f886e0c051a1a163874e629f26616f6a797`  
		Last Modified: Sat, 08 Nov 2025 22:38:30 GMT  
		Size: 16.4 KB (16363 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:410518501aa127ba910e81cf73ab319008b3e460358ad4ca1716c5e17c70ab0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214439829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c2cc1071ea7380c2e8753967ee7353a021cf1c68a7b85d40cb5b4a34dd8b91`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:40:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:40:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:40:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:40:47 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:40:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:40:47 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:41:04 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:41:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:41:04 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:41:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:41:06 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a87c1af45089a8c323fe175b657d7384fcaa3ba8123d6b1fd8621a74eac1809`  
		Last Modified: Sat, 08 Nov 2025 18:41:27 GMT  
		Size: 141.7 MB (141731667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4537ccb2a43de5e22957d1e81b05e0810dc425c60bcddf93470e423a05d761`  
		Last Modified: Sat, 08 Nov 2025 18:41:39 GMT  
		Size: 18.5 MB (18539977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dcbc59b8602393e8e132e76b0aeff53c2ac18eadeae6d31db5047b9bcc6944`  
		Last Modified: Sat, 08 Nov 2025 18:41:37 GMT  
		Size: 4.5 MB (4517723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ad0c12295ac3f7aac66792c1b67341eb56cfc7936d7b9c56b663117485b5b109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3851505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0822cd28829916c50df13783957480ebeae114cf097ac44d006423e0b7bd7d3f`

```dockerfile
```

-	Layers:
	-	`sha256:53e6a3d17fdf2ef3f8d0be5145db09805bde6d54d4743b55ada895209801c2fc`  
		Last Modified: Sat, 08 Nov 2025 22:38:34 GMT  
		Size: 3.8 MB (3835020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daf514a4cd3bde018bafd07ab683283d5bd89e0e5941c359dfa16dfa7ef49170`  
		Last Modified: Sat, 08 Nov 2025 22:38:35 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:20026ec8b61355d7e17cadb940efe397f84b63be6bc655299654b2801b8e1233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208344330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c7b6329945831d9e9092c67f2c34a83de737d1eb5107cbe1f946a788553574`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 19:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:28:28 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 19:28:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 19:28:28 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:28:58 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 19:28:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 19:28:58 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 19:29:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 19:29:02 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e8e3e02a4f5bce482ee6878197966e1ab6c51d874ce72ba1d61ebbe633711f`  
		Last Modified: Sat, 08 Nov 2025 19:29:39 GMT  
		Size: 132.1 MB (132079844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7427a87ed886b4acba4c4cb7bb857b2178efdd7dfd3cd193d0c2e209c76ca6f0`  
		Last Modified: Sat, 08 Nov 2025 19:29:47 GMT  
		Size: 18.6 MB (18636580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b06d5cf50c518d0633b5cb7d1935c451e1a81c00f3bfc80aa31708e3e1e4ca`  
		Last Modified: Sat, 08 Nov 2025 19:29:46 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:caa090c88f6ee21bd448baf92101ace3f249f8a853d63d3bde896b1223c0a20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e772efc5c8731ee0afcba474af811e8adafacec0dc0da34c02e20fe4e0e1f5bf`

```dockerfile
```

-	Layers:
	-	`sha256:adb70b5b99c121fcd250349c02b6d39d01187d5a6ea7ef95bf411b535e3ae50d`  
		Last Modified: Sat, 08 Nov 2025 22:38:38 GMT  
		Size: 3.8 MB (3833908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d36df548f83cc9bed0f73b838f02d2216add62b2f0da67b83dfd8b2a3e3e6c77`  
		Last Modified: Sat, 08 Nov 2025 22:38:39 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:cae2b6a2645e3433780295a6cede39fecaba351f94a45b141d3c439237eb0269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198184628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c056e09362a64bd74bf1680cbb676ea1468577c4c42ba54d300c3879fd77db3`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 19:27:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:27:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:27:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:27:44 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 19:27:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 19:27:44 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:27:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 19:27:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 19:27:59 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 19:28:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 19:28:01 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13576e2e4394f64e1066c692607d63be0dd492e012c5dd0b09da178823c04b8a`  
		Last Modified: Sat, 08 Nov 2025 19:28:44 GMT  
		Size: 125.7 MB (125694367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bf5a3bbe7523f87af90cac5ec47f1b7ad5339079d544c331c55df982beab8a`  
		Last Modified: Sat, 08 Nov 2025 19:28:37 GMT  
		Size: 18.6 MB (18620221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac64d24127300ca9976bcd1fb27b94213174c51d0fdf527f2fb74638ad140df`  
		Last Modified: Sat, 08 Nov 2025 19:28:36 GMT  
		Size: 4.5 MB (4517709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f32c383865650241a00b53e3f9c6926678ef9c4ac32d7803cf0592bd41bcb1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3846320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b43d5eef1c1205c4a824ed85fe3bfe576107d59eca11ba6abd97cdb49202be`

```dockerfile
```

-	Layers:
	-	`sha256:7e0f57a88e14eb00366fe4ccdf15a718ff795d2eea6e4a7eb44370dcf278d0a5`  
		Last Modified: Sat, 08 Nov 2025 22:38:43 GMT  
		Size: 3.8 MB (3829956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8876079cbc1dc3df67185684306fdfa36dee1f7c5f7b741905c729d0422d1da0`  
		Last Modified: Sat, 08 Nov 2025 22:38:43 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json
