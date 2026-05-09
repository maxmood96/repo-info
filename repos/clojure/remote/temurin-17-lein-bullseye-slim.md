## `clojure:temurin-17-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:e7e1878619505473f033f4b10dd080e76db32967f3dfc3e79dbf1d496aa411bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4bed4f1b4044de256d489557d53faacdc607fdc8660ebe2043670ae67d4543f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196020447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c5b48064e5f0ba9c2aa17f759fa6c02802b5468f382bd61359f78e1de4d44e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:16:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:16:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:16:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:16:59 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:16:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:16:59 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:17:13 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:17:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:17:13 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:17:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:17:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:17:15 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:17:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5502651b6bb976b3f5ce6cc8b971af19b5047b55c13b753689bde07eb91599d2`  
		Last Modified: Fri, 08 May 2026 20:17:35 GMT  
		Size: 145.9 MB (145905478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9863f0e79294e5b81e5e18c1b0a8e39940eeab31881161e3c3f4b7ae915398d5`  
		Last Modified: Fri, 08 May 2026 20:17:32 GMT  
		Size: 15.3 MB (15338831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c7eebb4747d9fe301ec1b0e43b5197b0b4f3c678e5c3d799616d35e2f90bb3`  
		Last Modified: Fri, 08 May 2026 20:17:31 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e770e3774d517aec06c18e5f922522e77cce6181feb15fe8d2036a13cc328868`  
		Last Modified: Fri, 08 May 2026 20:17:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:93747cbd067b23070960ec8a9b11a41aa2f1191198290de61f05654d5a0d7a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe5913b7a3825cbd9796617bc0ab7dab7ea8de6428258b1a955506a1d069afc`

```dockerfile
```

-	Layers:
	-	`sha256:04c64f1cbcc6d85e18b9d00a34d925f82869f5a2339cea38fad04d9ef7eb72ad`  
		Last Modified: Fri, 08 May 2026 20:17:31 GMT  
		Size: 3.0 MB (3028209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:698454fd40d88ebd04409a7ec1fd17bc1da4e2ee41b7be772c2c76db90e32c5b`  
		Last Modified: Fri, 08 May 2026 20:17:31 GMT  
		Size: 18.6 KB (18557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9c195151cd60c552f962154944c7d363cb5937fc51bd982d4dfc4df8f7fb9426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193312313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6713ff4143f5f3da8dfa8fdb7a406507b5582160cc51d63bf4b32e3ee3e9d7f9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:21:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:21:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:21:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:21:22 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:21:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:21:22 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:21:36 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:21:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:21:36 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:21:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:21:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:21:37 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:21:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc08641ac30ce339861689ceb854131a5c2582544cf0d940738dead902812db`  
		Last Modified: Fri, 08 May 2026 20:21:59 GMT  
		Size: 144.7 MB (144724334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6734638a242db6cb562257547294a813726d7e26612198dedb5ed7b683006a09`  
		Last Modified: Fri, 08 May 2026 20:21:55 GMT  
		Size: 15.3 MB (15327240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8639b222785aa2af4a4f7e48634c58ee908934a5a1d9ff43beff7e862bff92d`  
		Last Modified: Fri, 08 May 2026 20:21:54 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7cc56b7dc6d131b2966fd53d343fdb58f56e055d81d8669fc4ce1d8834d415`  
		Last Modified: Fri, 08 May 2026 20:21:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e64d52393f7351d266796c47d6bda9a1a73b3afa3a08f8f55f5aa4a1cb9d4b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9640f0b45230cd143084567b4f9b96842508f18782165e1db619480793a7df`

```dockerfile
```

-	Layers:
	-	`sha256:1af932a9159d283f91255be0be65f1a23258bb2da75d0072ca1e38f4f795e032`  
		Last Modified: Fri, 08 May 2026 20:21:54 GMT  
		Size: 3.0 MB (3027818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74dc268b7e2c15dbdb1c8bd6e18907b3c6b5f3007282634a3b0237fdc7f73e2d`  
		Last Modified: Fri, 08 May 2026 20:21:54 GMT  
		Size: 18.7 KB (18678 bytes)  
		MIME: application/vnd.in-toto+json
