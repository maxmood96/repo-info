## `clojure:temurin-11-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:cd267ebb9fb2de134ec986cb82d51d78c1378d8c923af7c4336c6412ef9615cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cf1810e43851011355ccf48a772b555e9f0d723124808832e59a7a4b90b5940e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196196138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c1cf4c4ebbef33aa97dc7810bcdbfce957ee002343547df4013f70403e9aeb`
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
	-	`sha256:0051e37ea87f46ec9a23ca18770dc1145a5bc3b7c4162bca01ec3cd4bd4a31ce`  
		Last Modified: Wed, 29 May 2024 19:57:07 GMT  
		Size: 145.5 MB (145504827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b113c200ed30cff36894fb09a48d588ef8dbc44390458a37df0601f0688866`  
		Last Modified: Wed, 29 May 2024 19:57:03 GMT  
		Size: 14.9 MB (14859295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a75cd3bc423bd1a0f05050b8c8b22bfef386445256772d019e11273f24917b`  
		Last Modified: Wed, 29 May 2024 19:57:01 GMT  
		Size: 4.4 MB (4398053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:54a64caf95baebfea7b9782bfbf4136ac4e0abe76acbf2e428bd2b90516f72b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2708534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c0c1b80ee392ac3e2c435e4faadda475853d62604b005ae30edf8b06ad2fff`

```dockerfile
```

-	Layers:
	-	`sha256:525610c370c3630b52b5600b78cf304b7de08780ae8abfebca4b5ba8010f5621`  
		Last Modified: Wed, 29 May 2024 19:57:03 GMT  
		Size: 2.7 MB (2692501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea0fe3feb86e7718afcbbaa33a769fc4fd2a5536e0de5afcc36664dbab56f5a`  
		Last Modified: Wed, 29 May 2024 19:57:02 GMT  
		Size: 16.0 KB (16033 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1f6b0e85cfd7b31b891f05d811a90352e1a8cac3ba34ebb9598a3de37940c6bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191636164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71336c3cc6a6490c386f307f61c145b4f4853897acd160e8c2891a64788f43aa`
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
	-	`sha256:6d2c65d67dde4128718a343ddd96ca8084f61812e9a2fd2f2c143f0dc6bbbba9`  
		Last Modified: Wed, 29 May 2024 20:38:19 GMT  
		Size: 142.3 MB (142304134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f951d187b7bab3e9c80a04d6144d1c702e7687ba35806932ecb309c0b9058e43`  
		Last Modified: Wed, 29 May 2024 20:38:16 GMT  
		Size: 14.8 MB (14847059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4855cbe54675af6b8129e0aa262b6cfefc744f44023d55aeacf567e2547e15f`  
		Last Modified: Wed, 29 May 2024 20:38:15 GMT  
		Size: 4.4 MB (4398031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:211b40f2087a9b51b7d52b7cb1b8221987db0c74e623991cc8c129b2270b4efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bbf55a76db90755e4ebadbca4ab8962b1a666ca119d3aca65fe169fdf5fc4e`

```dockerfile
```

-	Layers:
	-	`sha256:5d3b625e7c88af6d48a461bb9bf1d0954e95676440bc44acd89b68436426ee71`  
		Last Modified: Wed, 29 May 2024 20:38:15 GMT  
		Size: 2.7 MB (2692727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99883bf21a8883bacb858f576fc939146035cc232208b33fd940e7cc88127d01`  
		Last Modified: Wed, 29 May 2024 20:38:15 GMT  
		Size: 16.6 KB (16562 bytes)  
		MIME: application/vnd.in-toto+json
