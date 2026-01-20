## `clojure:temurin-17-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:5d23c01ad71d41467582c5eabee7cbbb4f7d7a653cc98662897dc7ba96676961
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f1f9d7a3435e0b9d2c7db27aa3e5303d102e87c67719aafb376607d12c6e552a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (219991535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c9cd930c5d93fd0670b6189a39160f344cb52ea83d757a810329415c80afe6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 01:52:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:52:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:52:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:52:04 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:52:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:52:04 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:52:48 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:52:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:52:48 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:52:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:52:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:52:50 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:52:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:36 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b438b09694b598af3bb457c0a2e400e6a4427ffa095720292e627d78cf881f49`  
		Last Modified: Fri, 16 Jan 2026 01:53:38 GMT  
		Size: 144.8 MB (144847946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6ad366b5e75d119997890c47827f41e7dea68d8068fc63dfe0467cd6af1a9`  
		Last Modified: Fri, 16 Jan 2026 01:53:17 GMT  
		Size: 16.9 MB (16868955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a9d0406c46bcf70611f52fa18c8aef46caaeac496f7e51692da7eb8b72a6b0`  
		Last Modified: Fri, 16 Jan 2026 01:53:17 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b606c94e87a7319d0b94ce3b1c173c09721db8973ea6012e9bbd854659d1c6`  
		Last Modified: Fri, 16 Jan 2026 01:53:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c34e4371eedafd30fecac4b66bee8992539d899204d6de3f5272952d57045099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba55595b2d20ebee4818e0c5278d2b46a176152fd808fc0576757a3494429e7`

```dockerfile
```

-	Layers:
	-	`sha256:9ae8950d336fd6aa71cae59a33731901fe6c74a7766b98a4136281c233b3bee6`  
		Last Modified: Fri, 16 Jan 2026 04:42:14 GMT  
		Size: 4.5 MB (4476190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7c3d66591fd56ca38883b67e3fc780dff51fdff4d7d01c84196d8f0963ac530`  
		Last Modified: Fri, 16 Jan 2026 04:42:14 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:be909813d20847783b4a89dd07861bd44267e75b12319f0222a8c540af5ace6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217313178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77121945e41f6b26bfa0d18cdf27febb3fe324be4c1bc49005c2502168fa67b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 01:56:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:56:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:56:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:56:22 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:56:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:56:22 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:56:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:56:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:56:35 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:56:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:56:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:56:37 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:56:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7570bc4cbcbb0d0939d17ea76364760f5ba4a88c7d52dd417e07658664986905`  
		Last Modified: Fri, 16 Jan 2026 12:46:50 GMT  
		Size: 143.7 MB (143679931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3b5b50cd6bf99398cb9e88493544ac878ad496e41bed0c7479cefa4737ce96`  
		Last Modified: Fri, 16 Jan 2026 01:57:05 GMT  
		Size: 16.9 MB (16857296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2831cde0eec396ce2481fbdf362ff0ce28760ed712964dee9943a070727541`  
		Last Modified: Fri, 16 Jan 2026 01:57:06 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae29714c76942d1beb59c4050753cd3ae08b182a592f4d6d0084d69341d2f9c5`  
		Last Modified: Fri, 16 Jan 2026 01:57:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:dd785a947d609017915f8b6607b05cf52865c88ff6c8d2f62d5641843c33ab74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4493653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb36d9b360c0ca9b0b8b50bbe4f8499a06558d76bdeb1dcf8fd82aaedc06901`

```dockerfile
```

-	Layers:
	-	`sha256:11f25df5fa9c28d8b2361c6f9d27d68b617d63a976ee1bf32c190b346a9fc670`  
		Last Modified: Fri, 16 Jan 2026 04:42:19 GMT  
		Size: 4.5 MB (4475164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3113d558a3dbb5423d2aed4e8df903670e123b6eebcc3a6e93da44141f429da`  
		Last Modified: Fri, 16 Jan 2026 01:56:54 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json
