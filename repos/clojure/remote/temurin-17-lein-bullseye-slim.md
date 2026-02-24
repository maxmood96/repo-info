## `clojure:temurin-17-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:0e0c2e82824c746e5a9ee048293cbe1ddafcd3929c70e1184b349637352fa867
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4b7abbccdc2d9db92a99b0b73ae0dbb76849bb843c0f54d883a2b8d783a0786e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195744088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c71bff7c79abe9f03677a897851d2877f129e9808523f109554eac8f0c360ee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:25:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:25:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:25:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:25:58 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:25:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:54:33 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:54:46 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:54:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:54:46 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:54:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:54:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:54:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:54:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24208c22c76b0f2308e76a96140d5c4512aa3133159ab42853b59733a0efbd5`  
		Last Modified: Tue, 24 Feb 2026 19:26:56 GMT  
		Size: 145.6 MB (145628714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c294a2aa83a95b4e56de220c774ada483bc2bca00dc94f32ab6ac853e25462a`  
		Last Modified: Tue, 24 Feb 2026 19:54:55 GMT  
		Size: 15.3 MB (15338861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fec3201883e9d7cb2dd328f8f384f8d43ebfe7cb75104e599484a964f23c50`  
		Last Modified: Tue, 24 Feb 2026 19:54:54 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf72cf0ddd3818e8b59a709a3e86476802f39cee7083c40a6fadec256ff3015`  
		Last Modified: Tue, 24 Feb 2026 19:54:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a745ba7e2efa0cf5035775a703e0aa24f92a898dc134bff0c73b6f5ebb157626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad082f3f6e0449ce6997bc0ccdd521bce7e1702b4bc2cdd54406c611fa66d539`

```dockerfile
```

-	Layers:
	-	`sha256:7236c1999fb1337dccda8ae1c0ca3ecd58cd31db3038fd4891842b1cc758e776`  
		Last Modified: Tue, 24 Feb 2026 19:54:54 GMT  
		Size: 3.0 MB (3029206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:842e39b5091b78ad66d690dc85baf55b4c4912f8df6ebcbcaf55a03621da195c`  
		Last Modified: Tue, 24 Feb 2026 19:54:54 GMT  
		Size: 17.6 KB (17602 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:89324c6c0cc0b9ccc5b4d859a77dba40bca4c1a0bf50e2b57a1c9886ebfad240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (193026072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230a24118b4c63625b1b6dbbd0aa84b8a41f94104588ece4e55b5110657d7187`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:05:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:05:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:05:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:05:40 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:05:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:05:41 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:05:54 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:05:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:05:54 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:05:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:05:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:05:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:05:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbf8b0f02ac76978eb31a13a676b86796c0184fcf4ac327317df21d1d1e9341`  
		Last Modified: Tue, 24 Feb 2026 20:06:16 GMT  
		Size: 144.4 MB (144436218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7726e8492aa54e494bcce7a5ccab3cf31bf831505678e145b626d6d4ce273300`  
		Last Modified: Tue, 24 Feb 2026 20:06:13 GMT  
		Size: 15.3 MB (15327233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334ac1203d1a109b3c592c3afa0872839857c614486ffe9cac5425605f3f6f7`  
		Last Modified: Tue, 24 Feb 2026 20:06:12 GMT  
		Size: 4.5 MB (4517722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85ac76c26a3054d20a226c1e54f8f734b2de55c43ce774eb3775ec316497ef7`  
		Last Modified: Tue, 24 Feb 2026 20:06:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f227a718abe081cd771bc4bcd9a10f2e08d6202d35958c7620570d4f3a9cf022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bc92f86d9404d5dd86eb25a34e7c29919ace736d3b113c326a70fe8d34404d`

```dockerfile
```

-	Layers:
	-	`sha256:9fb461830b207a6f974fab3459bf79618188058105ecdb2229fa4b46064dfc70`  
		Last Modified: Tue, 24 Feb 2026 20:06:12 GMT  
		Size: 3.0 MB (3028815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e61d207ba520f45385dada12b280e7b50a797c99b726f2e2f504743e0ea3b8c1`  
		Last Modified: Tue, 24 Feb 2026 20:06:12 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json
