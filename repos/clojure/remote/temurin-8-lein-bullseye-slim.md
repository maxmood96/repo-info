## `clojure:temurin-8-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:fac66fbfc6e3ef4941b946c25eb308b4f9b00bc5cc56bc114327bb01dbb65746
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7d70416a6bd7a65e2f79d9e45078dcdfd5ce34edb165e145ed41e0a05c5e4ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154291515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de853ee7d69ed4d4def058d12055b6ed3eaf2b92d86d807d9a4a43b34f737c8f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 15:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec0e951c193d01a3301d79f7828a833f89869c36e05bef7e029badef5730a3c`  
		Last Modified: Wed, 29 May 2024 19:56:57 GMT  
		Size: 103.6 MB (103600229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6e1ce728898f47b5768a1f8ef552c85669d40cc4fb6c9d5180c1c1b6b7c1a9`  
		Last Modified: Wed, 29 May 2024 19:56:55 GMT  
		Size: 14.9 MB (14859247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7805c375ffea7207de950fc5c38d160e211990a63b02cd51d61928a5622e8d`  
		Last Modified: Wed, 29 May 2024 19:56:55 GMT  
		Size: 4.4 MB (4398076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9d92b67748b3326373504a5398cbc5f15e4311fdf67597db69ce708820ba8ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2731014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3e734e4c87582210203d0c216640b9038889b580cd18912d07f9712794cc74`

```dockerfile
```

-	Layers:
	-	`sha256:b09eefb4d0facce8c705e8cab64ac308b27700494d2c965deeb611f08b748205`  
		Last Modified: Wed, 29 May 2024 19:56:54 GMT  
		Size: 2.7 MB (2714991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1f952e362fca6c3ac539011c3f8e10467d0565a47d5367b927c338d7d162b39`  
		Last Modified: Wed, 29 May 2024 19:56:54 GMT  
		Size: 16.0 KB (16023 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4bbb3fa003a40bea41ea487d079fb319a8400f8c5c5d7c6eec369324d6eb330d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (152032467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9db5acbc9170524297a1a6634875a827e393257176b036e597d3c5930132480`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 15:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96413e5e1bc47e07d164012b8a21fa2146eaf62aa0cf9162f8bba4071fc67e6`  
		Last Modified: Wed, 29 May 2024 20:27:29 GMT  
		Size: 102.7 MB (102700442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a01aa8ed7498738a3c9292db77627fedfbd57d58a880384de081c72e54f5c4a`  
		Last Modified: Wed, 29 May 2024 20:27:27 GMT  
		Size: 14.8 MB (14847046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248af0af32a6eec5222fc58ae9dfaf4144d3504e2a7f4ad9b5f4f4eafc2185f4`  
		Last Modified: Wed, 29 May 2024 20:27:26 GMT  
		Size: 4.4 MB (4398039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2871c794f427203ba8981020d244ebac8c586fa6d97e5c6e2971c70da989b011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2731778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6808ae7cb69cf4f98a09ab8a647a9493ffed39d36b71b484023765eef71485f2`

```dockerfile
```

-	Layers:
	-	`sha256:a52f82154d37500deecfb8a3b33584f48d5f2a2e658a69e50b97d5043338fcf7`  
		Last Modified: Wed, 29 May 2024 20:27:27 GMT  
		Size: 2.7 MB (2715227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b76c7b85ed7733ad6ac0a6bb7839bbcdaaa92b334a5e7f854b1b0f7ff4c20fd`  
		Last Modified: Wed, 29 May 2024 20:27:26 GMT  
		Size: 16.6 KB (16551 bytes)  
		MIME: application/vnd.in-toto+json
