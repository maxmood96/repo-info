## `clojure:lein-2.11.2-bullseye-slim`

```console
$ docker pull clojure@sha256:7c3c76717d82c3d37973d7a06025c7aeab0c81bbf563361c0a40dfa039c62e21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:lein-2.11.2-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b20bd132ce80c3c384baa0404bd783fb153985b512a45bdf3c11f2efdfc2a13b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.2 MB (209189601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a8138e44f9034883b11a67b9580a2b668f36cb36ba43efdf334ff2d3791f83`
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
	-	`sha256:13d7155ee56667d230f2a69a83266f563256e1e77ccc1c073ab333d757cbed98`  
		Last Modified: Wed, 29 May 2024 19:58:15 GMT  
		Size: 158.5 MB (158497942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3ef9bd3d6474ee6bb176485b12fca58bd2a9917a36f072d6050094209e3712`  
		Last Modified: Wed, 29 May 2024 19:58:11 GMT  
		Size: 14.9 MB (14859264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bffa577883560eb0584df06e935bbe72dc628fe90c5bb837cdfc9c57e08b7a6`  
		Last Modified: Wed, 29 May 2024 19:58:10 GMT  
		Size: 4.4 MB (4398032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d18389370f3140c7fcc18f37f49c8be51565b84ae923b4bd7bb6def95a8426e`  
		Last Modified: Wed, 29 May 2024 19:58:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7df53e1d11b33a3ef64ebee8e70c8467c9706dcf069a84075f5b8e15e66c3e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2711865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2222976d4e01d1f68eae6fd2812cf8f2d35c59c2bb09e38809044048514397be`

```dockerfile
```

-	Layers:
	-	`sha256:02f2fe9c153de543b0d7d557f2283f5425c673b8996d981cc84c49f08b87839c`  
		Last Modified: Wed, 29 May 2024 19:58:11 GMT  
		Size: 2.7 MB (2693173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:964584ca6f589015423cd28df78727daaf1737b3cf6eb94c45533fa0f1e2e6fb`  
		Last Modified: Wed, 29 May 2024 19:58:10 GMT  
		Size: 18.7 KB (18692 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.11.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:706d9026dd579df3fc8206bfe694f24abd02523a6ad8253249a08c893832c5b7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.2 MB (206203518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ae9fdb19640f8b3387a83735b24e080bbbfea7759da1ee53db65a23a25fab4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:45:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:59:30 GMT
COPY dir:96a90c8e1c03defb238a6d560d8927dc81a1a58af3fce1471cbce5249ed27f38 in /opt/java/openjdk 
# Tue, 28 May 2024 19:59:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 19:59:34 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 19:59:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 19:59:35 GMT
WORKDIR /tmp
# Tue, 28 May 2024 19:59:48 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 28 May 2024 19:59:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 19:59:48 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 19:59:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 28 May 2024 19:59:50 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 19:59:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 19:59:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed2bea0b9b9544adc08ee8bd3f3e7847626f72fc9c4ff496bf41857e66608cc`  
		Last Modified: Tue, 28 May 2024 20:19:15 GMT  
		Size: 156.7 MB (156665547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4583bd3ead65aeb9eb2b788f0ad6af5a4810fa9a51a50d8b03d73a52bdca07`  
		Last Modified: Tue, 28 May 2024 20:19:05 GMT  
		Size: 15.1 MB (15052556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c92126eaadd9a48cbfca5b3ac07f1f79457a6917772f0d679375298606f7e70`  
		Last Modified: Tue, 28 May 2024 20:19:04 GMT  
		Size: 4.4 MB (4398107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d7be060917075e8076d1a15e50e26ced5c31184e971afd075830a512d37f6b`  
		Last Modified: Tue, 28 May 2024 20:19:04 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
