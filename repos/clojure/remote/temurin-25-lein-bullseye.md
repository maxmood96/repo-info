## `clojure:temurin-25-lein-bullseye`

```console
$ docker pull clojure@sha256:9faada4bba2d62b0640fe8e1536246375ad949ec6340db191a18879395be6119
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2c906c10cfdfb4ede24a4f9f1ea1ef597de212d8724063bdd7f80a6807c92de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167166854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f49395aed9b104c1fd5a403bd4386e2b9e5f39482bc7b5c3622a18b94124d91`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:06:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:06:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:06:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:06:15 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:06:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:06:15 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:06:29 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:06:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:06:29 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:06:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:06:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:06:30 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:06:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b056724f054b1b40182c93c9ae6dde88fbd988434e2f718fab964f6c6c81aaf7`  
		Last Modified: Wed, 15 Apr 2026 22:06:50 GMT  
		Size: 92.3 MB (92256332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3faf4349d2cc7274ef3a689390b3956cae9bbaf118eb0184272f3c3465f37c`  
		Last Modified: Wed, 15 Apr 2026 22:06:48 GMT  
		Size: 16.6 MB (16629587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de8d4994d721e3b147509e450f21b6728a4560f13b4b57624b7c1a8d4e10526`  
		Last Modified: Wed, 15 Apr 2026 22:06:48 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c637e448e95eb61ff6dadddfac58d4c2ae45091b9c460c34a301ce98b45a5d8`  
		Last Modified: Wed, 15 Apr 2026 22:06:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d1d868ba7c34c74ed49e51559c09ca099e7de3182dac928e39de2cf0b7b8ea15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4472905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60860bcaae04efe7138e8a810cf7db504ac0ab4b607b1cb33a1fea53f63611d2`

```dockerfile
```

-	Layers:
	-	`sha256:cd551835657bb1170d87d2590198d710b6d75e6afeaa68ac765534930fb0205d`  
		Last Modified: Wed, 15 Apr 2026 22:06:47 GMT  
		Size: 4.5 MB (4453902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:476151c0a2741a868208ee0d15f31b5c593ff0f4f59f55271a5e4944f404b2b2`  
		Last Modified: Wed, 15 Apr 2026 22:06:47 GMT  
		Size: 19.0 KB (19003 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0795a045bee9afa482c1f582f2b2109c57113a0a2c36c48451107843bfb8560a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164670424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dcd7553ebc77bce179edac59a2bb56ca766b7fe9e391faec9461b22018d6053`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:17:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:17:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:17:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:17:50 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:17:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:17:50 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:18:04 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:18:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:18:04 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:18:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:18:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:18:06 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:18:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ae9fd562707debc714f41d159708b040c7d56790e3d6105c4e2db61ca19e81`  
		Last Modified: Wed, 15 Apr 2026 22:18:57 GMT  
		Size: 91.3 MB (91288265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7294e9b313c006ac5f0ce315cb664235a6d0a99be8ca124d573862c2800d3bbb`  
		Last Modified: Wed, 15 Apr 2026 22:18:51 GMT  
		Size: 16.6 MB (16616365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd4af664f0c3d59e8a85e8c364731f0382e70bc8835f480ff996610c7b526ce`  
		Last Modified: Wed, 15 Apr 2026 22:18:48 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fcbedf981886bf179b048b5f25ecaaff0a670348d2726688dfe60a14cd2027`  
		Last Modified: Wed, 15 Apr 2026 22:18:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5ef024a284774e88ea699dc5c1300f5308db6342939cb8ee6d8571ba48b9086b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4472045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a426bd5bc1f4667c663f281f30ca16b3b42f4fb2a37abf80e696cdaef937b43c`

```dockerfile
```

-	Layers:
	-	`sha256:361fd3dbbe4453f899879f8164f35298f9bf0c6ece73f66fcc51134f09c854e1`  
		Last Modified: Wed, 15 Apr 2026 22:18:47 GMT  
		Size: 4.5 MB (4452897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11f20772da844fdd2991d965a3e3579cac5c0dbe0e0b20949799e48cd47de6bc`  
		Last Modified: Wed, 15 Apr 2026 22:18:43 GMT  
		Size: 19.1 KB (19148 bytes)  
		MIME: application/vnd.in-toto+json
