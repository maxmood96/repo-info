## `clojure:temurin-17-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:53f2de32279e3e8d268b1130d8e842a3f604abcf4e471fd1c5701e04afcc6a29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dee1470baef3c7bad9c1d3b7f6e105a8deaa26aac4492f252a36f16ab69ab5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 MB (195786711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f6a602a05a1b72587cef944181b1b4e369f7a097d46d0ed67e11fcd93c99fa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c7745bea9f9ced5cbc5f2704569661e10283e705bc3f66e9a4d1640c737669`  
		Last Modified: Wed, 29 May 2024 19:57:04 GMT  
		Size: 145.1 MB (145095043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ee3faf84a93046f83fd8ef484fc19556b3a11557bbc2bc2854da20744701a7`  
		Last Modified: Wed, 29 May 2024 19:57:02 GMT  
		Size: 14.9 MB (14859264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9f3d07e6d5745f52acdcc3c1d5d0fc34a47c96b2813ad0647d9b3e03bbec03`  
		Last Modified: Wed, 29 May 2024 19:57:02 GMT  
		Size: 4.4 MB (4398043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd206c686c5a4b6f6bf303afd2e951dcf87283d8847db107ae3c0e8dd497eff`  
		Last Modified: Wed, 29 May 2024 19:57:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7f24bacb2634b6af1e533cb19ae15ec28557418143ff9bf2dff33d07e4dd84fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2710530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30491826462098588231288c5cc51215be154472a4e4d1fd614275299a50ac36`

```dockerfile
```

-	Layers:
	-	`sha256:ae126d3a9cbdfe1d06bc51957a73bb574730a24af76e0876460c0a88789b8696`  
		Last Modified: Wed, 29 May 2024 19:57:02 GMT  
		Size: 2.7 MB (2692501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3737f31112bdab31810472b2b0fa684dddeed5888a033b02bc281ed06e76facb`  
		Last Modified: Wed, 29 May 2024 19:57:02 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d9a43d8a6aa873685d67159aba449d63d234629043f1d7b90aa5d053c38b37b8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193429924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54816c6aefb4655fa4a6cc3523011b04304f45df2bc1924bb510d16f8c61960b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:45:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:55:44 GMT
COPY dir:317487729b1812635c51c5f305bd9178bd957a141903eab756a1683874b5752b in /opt/java/openjdk 
# Tue, 28 May 2024 19:55:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 19:55:48 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 19:55:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 19:55:48 GMT
WORKDIR /tmp
# Tue, 28 May 2024 19:56:02 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 28 May 2024 19:56:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 19:56:02 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 19:56:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 28 May 2024 19:56:04 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 19:56:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 19:56:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf072d6312eeb8d6d05dc50f44eccfa94ca9ae5a08d2b299b845776b87f175a`  
		Last Modified: Tue, 28 May 2024 20:15:28 GMT  
		Size: 143.9 MB (143891870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd16b78d82b29ebf8fde1c94f3d41d6b0d372046bb7f6413f5fbe8bbe20798ef`  
		Last Modified: Tue, 28 May 2024 20:15:20 GMT  
		Size: 15.1 MB (15052587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031edbbddf1a5df7f268c8805b30acdeacec39035273c299b5ecf814a0b5aae3`  
		Last Modified: Tue, 28 May 2024 20:15:20 GMT  
		Size: 4.4 MB (4398158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7a2bbb39c5203cd7bcd7527d123befc36b6db40ea291a890ab1d3d8a3899ab`  
		Last Modified: Tue, 28 May 2024 20:15:19 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
