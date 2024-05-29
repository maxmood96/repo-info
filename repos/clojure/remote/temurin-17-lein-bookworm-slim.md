## `clojure:temurin-17-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:dd092bcdd2c25b4eecf0bec4c24480382fb38f9113dc3802b953f8b298e53e64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ebd982bf751bf09acfb8814460c644c0d5bbea3145bc5f47b1855cdafa3510f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195936851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154cbeab0c515cee6c1ea1ace6c5d423db2ac62ceaf1e5aa10913ec4491843ec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3082342cc2e8573aaed93e867fb5e5362f9332a3983bdb223df833beb1e49f6`  
		Last Modified: Wed, 29 May 2024 19:57:04 GMT  
		Size: 145.1 MB (145094994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a462380f773970baf7707d93c124dc534df7355c1ee6ea4ccdb7a8207a073f50`  
		Last Modified: Wed, 29 May 2024 19:57:02 GMT  
		Size: 17.3 MB (17292962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a75cd3bc423bd1a0f05050b8c8b22bfef386445256772d019e11273f24917b`  
		Last Modified: Wed, 29 May 2024 19:57:01 GMT  
		Size: 4.4 MB (4398053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6488fd2692c5c7e56d7f469964a81acd92d6176904fd61667baec12e853272`  
		Last Modified: Wed, 29 May 2024 19:57:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f0d0316fecd55d4912e498aa310c0eaf9bf5b936ebfeb9dfdf84b3bedc5b4812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b754d8498a6159ce603ad987966b3b8e65627b8bdd0fd9e569f6f3e25072f6a3`

```dockerfile
```

-	Layers:
	-	`sha256:6c976ef7abeb2403287b4bf4af27d4f97af123c10d26827dfc7895ab1a94de5d`  
		Last Modified: Wed, 29 May 2024 19:57:01 GMT  
		Size: 2.4 MB (2398414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:280c870da8c9d84e11e8ad7d277107a960796983689af9cb883e6ada9f7ccf87`  
		Last Modified: Wed, 29 May 2024 19:57:01 GMT  
		Size: 18.0 KB (18030 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1393bf205dcd22b1233dd630fb46b8f2795821d8b8ad3295cd34a5a9c45a4337
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194781202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef3295a25dc2349b76931adda13b5aa51c2c7486fedd7b1b80fe28d06fe8b5c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:54:57 GMT
COPY dir:317487729b1812635c51c5f305bd9178bd957a141903eab756a1683874b5752b in /opt/java/openjdk 
# Tue, 28 May 2024 19:55:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 19:55:00 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 19:55:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 19:55:00 GMT
WORKDIR /tmp
# Tue, 28 May 2024 19:55:15 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 28 May 2024 19:55:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 19:55:15 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 19:55:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 28 May 2024 19:55:17 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 19:55:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 19:55:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72920bb393b41da798570e0a544fba4a0fc4aee2db82d333d8a4949661635df`  
		Last Modified: Tue, 28 May 2024 20:14:53 GMT  
		Size: 143.9 MB (143891839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8745c3ff136bc5df237a379dd27a34764347f0f8635511b9d06f9dfee2635b92`  
		Last Modified: Tue, 28 May 2024 20:14:45 GMT  
		Size: 17.3 MB (17311350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0fddc70a503fe162c32b85ece5084e4e6cfca7012708818635eceaae6397cb`  
		Last Modified: Tue, 28 May 2024 20:14:44 GMT  
		Size: 4.4 MB (4398110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576dcd8cdfdb465c1802730400ebc48536c9958b0df25a64a76b7f14d3f5836e`  
		Last Modified: Tue, 28 May 2024 20:14:44 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
