## `clojure:temurin-17-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:5ff10409eb2d497326d7d0eb3979211fb9c22fe9924885c8694cb498c9ae272e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ac230ce531fabf2fcbe4abe195225909480fba779866716af44e5d67066b7f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194787755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a8d539ad97ddb9eb59eaa1396c25aabb131900e98ec65774764a1c34465004d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbab0c1df679ea7d6208804c8086ca613cf9b525341034111090a0ea41810663`  
		Last Modified: Sat, 13 Sep 2025 06:37:39 GMT  
		Size: 144.7 MB (144693284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9629d6be205c65917f91f53b30822e88afd7ab62dd68014d6af1b355407823c`  
		Last Modified: Sat, 13 Sep 2025 00:03:46 GMT  
		Size: 15.3 MB (15320216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04165c85933150641d12dce797c7fe596f75f3f6f745bc7cb5286dfd0fa56eed`  
		Last Modified: Sat, 13 Sep 2025 00:03:45 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a2dc0360894c0e901644d30cefdd2233e9c5dfb52777fb16dab8c8301b1a8a`  
		Last Modified: Sat, 13 Sep 2025 00:03:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bd8bde376c604263c3be5b5972466ea028c161d7b7d7314f4d627fe0ce362ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3327f5a69d056da20e525a0f200abe673180d5905498d67e4ae5e6f5d8e9e424`

```dockerfile
```

-	Layers:
	-	`sha256:97dc6eb44faa61ca0e7dc0537dc5388f2e8f483271e45cf6105562b30c6215e3`  
		Last Modified: Sat, 13 Sep 2025 00:38:53 GMT  
		Size: 3.0 MB (3017908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b0425a972fa1ed3460e22c44e33fee321aefcb71dad0ef2df0f19a0ea7b315`  
		Last Modified: Sat, 13 Sep 2025 00:38:54 GMT  
		Size: 18.4 KB (18446 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eb84bf9ac36e37e8e0571137936deec4f320e4c2df27f27f4bb59699e2e0a74e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192118369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0dc596d70ca5fccf2ac99295d63e31f5f9c6800f4ecbb0c39b9e501170b2f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28990eb6631dbee88fab859b46c91a2e09cedb23723e647576126a96295f885`  
		Last Modified: Sat, 13 Sep 2025 00:15:23 GMT  
		Size: 143.5 MB (143542207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d6d3114c2d3e9f4f2b9fed6c5046e80e568138d050c6b1c20d479f9b7582ff`  
		Last Modified: Sat, 13 Sep 2025 00:15:36 GMT  
		Size: 15.3 MB (15307529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bd69195dacfa91c4bb42ceda952865d4bc858f1aeaa7bac554d0410c7bd421`  
		Last Modified: Sat, 13 Sep 2025 00:15:36 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7040358e7bafc06efe8b4056e7b1f324a8d31e75e04f596ed7f8070bac358a02`  
		Last Modified: Sat, 13 Sep 2025 00:15:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:221b4fbe8cda67893f09b39b01030c1b0b5fdf69753c23025c406277bfb6be37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f0fe8e2d3accbfba4939be4b31a901577b6ad704c85e13bf6e410c5adce261`

```dockerfile
```

-	Layers:
	-	`sha256:33f8adf7d62ad7d2c185a61252db2bcf1176d23014cf41b7dd0cc7af1bd35128`  
		Last Modified: Sat, 13 Sep 2025 03:37:39 GMT  
		Size: 3.0 MB (3017517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13db222b5604083fccc995406aa8fde8e7dd7d782745b998ea792690216c4bb5`  
		Last Modified: Sat, 13 Sep 2025 03:37:40 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json
