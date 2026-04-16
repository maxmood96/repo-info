## `clojure:temurin-21-lein-2.12.0`

```console
$ docker pull clojure@sha256:bc69c1e4117121420e9d6d48ad8b241214c31c57464b27cf82dd799bc97de87f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-lein-2.12.0` - linux; amd64

```console
$ docker pull clojure@sha256:1a11db9fe2946cc414891fa8013883fe54bcb8ac5b0368ba8aa98b63a3a0850e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230670662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cef29da2bc080b4b0be12954699676a03ea875ee17d35c9704584b3a635ad31`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:04:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:04:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:04:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:04:59 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:04:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:04:59 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:05:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:05:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:05:14 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:05:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:05:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:05:16 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:05:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bc26f6be5a89699368d444aa4bd45c9c742c022984eb7fd6dee5bbe16a0347`  
		Last Modified: Wed, 15 Apr 2026 22:05:37 GMT  
		Size: 157.9 MB (157857054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb850f59219844f538d1e5199487865a695dbc36573cac1eb15b3f3dbab60e6`  
		Last Modified: Wed, 15 Apr 2026 22:05:34 GMT  
		Size: 19.8 MB (19806602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf662e754d59f5c1005b64492707e3738189060df6ed97c0bfd339d3d22cf53`  
		Last Modified: Wed, 15 Apr 2026 22:05:34 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ccfd0e618ca2d81fec22f118dfe4c90b3c75be08a95a57c67820f02427e9aa`  
		Last Modified: Wed, 15 Apr 2026 22:05:34 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:e654e2fc0d7403488b68dd4d7cb5b6afd984026cb8b9cb39fbedeb5e13eb8280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bcdfa93c400d76cdf861ba7b6e6127b149c18b1a1b0080653a36191f54a14c`

```dockerfile
```

-	Layers:
	-	`sha256:a1d3db04b433a0e5b3e6c5839e3bc7c777dcf0fc592ca8b03bb5d07860da0ef8`  
		Last Modified: Wed, 15 Apr 2026 22:05:33 GMT  
		Size: 4.3 MB (4284233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53392f40044ba20d75a0000bdfade09dbd2e85ea7cb90505bda88a5d6fae3046`  
		Last Modified: Wed, 15 Apr 2026 22:05:33 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3b093efd3f92c0d0b1ccc24a74bc2171b747c9aea0507a1ec36da38089229dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228661438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ba19f64e83e05a711474b88343cbefdbf37da0335c4ddc29ca0b9979ff6f8e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:16:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:16:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:16:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:16:19 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:16:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:16:19 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:16:34 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:16:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:16:34 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:16:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:16:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:16:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:16:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b50cd48475473801946c6cdd3e81d11af7fd1c00bae76354c9e4914e15f60a8`  
		Last Modified: Wed, 15 Apr 2026 22:16:58 GMT  
		Size: 156.1 MB (156133027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3da1c1d13521c1c51001817ef89fb34126cb89c652abe281c14195b9fd0b07`  
		Last Modified: Wed, 15 Apr 2026 22:16:55 GMT  
		Size: 19.6 MB (19636985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e982b5c19e59c00646aaf92eb31c2119c3d2a46ea1fc4a4a33637dd305c34dd`  
		Last Modified: Wed, 15 Apr 2026 22:16:55 GMT  
		Size: 4.5 MB (4517735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bc12f240d601c36d491e9be7354b7912f43f4e3f59c1590d5f931957b8c20c`  
		Last Modified: Wed, 15 Apr 2026 22:16:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:4e479a30a8883d9f0168cd36609c0663a7dabc2ba9e4fb25c11eb9a48fe1d896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8065da4132600519559e2bf93544e50e4b583a9ab10eda61a31e9b683840d47b`

```dockerfile
```

-	Layers:
	-	`sha256:a6e192ae01053a026294011df4c4dffaecf1fafcd008c1b92929935b9f4c571c`  
		Last Modified: Wed, 15 Apr 2026 22:16:55 GMT  
		Size: 4.3 MB (4283872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc01095ae87f920cf983dcab518f50e539d8be2903330dcee7beaab8dc9ef29e`  
		Last Modified: Wed, 15 Apr 2026 22:16:54 GMT  
		Size: 19.2 KB (19163 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0` - linux; ppc64le

```console
$ docker pull clojure@sha256:9adaaace429efd2df94164e849e9817b915fe454093ae72942642a57dd7d7fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234856562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394726213dd936e7c31ceb406f5e939bc23201afefc2c04c209a814e28c4802b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 14:45:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:45:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:45:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:45:11 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:45:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:45:11 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:45:48 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:45:48 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:45:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:45:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:45:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:45:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e3fef080cc35cf9b72cdc460d1508c5e1620da32f827f1d747773b4bb79804`  
		Last Modified: Tue, 07 Apr 2026 14:46:39 GMT  
		Size: 158.0 MB (157977496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f8688a56fe29aeae35d60b4898f69dcf38a8409a3511cd09291bbd74e564ad`  
		Last Modified: Tue, 07 Apr 2026 14:46:36 GMT  
		Size: 20.0 MB (20023935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea77695a55b07ce08195df7a8ebdbb3b8fe1aad7b7c8fa1e55edd3d038591898`  
		Last Modified: Tue, 07 Apr 2026 14:46:36 GMT  
		Size: 4.5 MB (4517764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619aa5e751a83825ebe32fb72e2d266fc873eab17cd541a9fccaa95a21b8b3b4`  
		Last Modified: Tue, 07 Apr 2026 14:46:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:ca8670496a2dd55dad50071122f7a919b2818ab29bbb923673c43595829e2187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef43c5bdbaef605ce96ff140b4b555858885fa9eb5f4c105c695a9d37df6b9d6`

```dockerfile
```

-	Layers:
	-	`sha256:bff6256d0d21883bff6d15dffc0c0cf633f0315386817a56a0440f2584fdd846`  
		Last Modified: Tue, 07 Apr 2026 14:46:36 GMT  
		Size: 4.3 MB (4286106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98477d37de7cb3120db875a428b15470e4a6bb6b4da9a8d92ebbe63d0a0d2e4d`  
		Last Modified: Tue, 07 Apr 2026 14:46:35 GMT  
		Size: 19.1 KB (19073 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0` - linux; s390x

```console
$ docker pull clojure@sha256:219142295a0a6834de0cb041e337e2f024aab677f2441f370b1b481e5526e9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218238176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99ffa3cba4b357e47412cc37c3f9018379a13c09dd60e9c8045704fdfe57efc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:40:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:40:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:40:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:40:45 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 00:40:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 00:40:45 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:40:57 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:40:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:40:57 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:40:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:40:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:40:58 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:40:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec1519275620c74494ba6b32f0dd3424a982665925199511df236a83adab50a`  
		Last Modified: Thu, 16 Apr 2026 00:41:28 GMT  
		Size: 147.1 MB (147105233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0200b2572ff73b5cccb58b52881206cf8c0338d61683f6a38dc8632c04daea`  
		Last Modified: Thu, 16 Apr 2026 00:41:26 GMT  
		Size: 19.5 MB (19466725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d4fa187b5072600f6097b20ea41ca1bfe2854341fac689eb4622c5c769aa0c`  
		Last Modified: Thu, 16 Apr 2026 00:41:25 GMT  
		Size: 4.5 MB (4517706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a6a92c5d425a4be5ab995fce3b17d14cec09c9bb97b5ea302ca04aecf1c0df`  
		Last Modified: Thu, 16 Apr 2026 00:41:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:33592f6610759d66e4099f220f700522957296a53baaa16323de77b57855980c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4295065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c22ed53bcb96c4a6ab9257702a5844401a099bba5f4354a11a97167e6f61fc5`

```dockerfile
```

-	Layers:
	-	`sha256:fa7c6d46ce3fcf8fa23f68674471625b589c7d852159d3b0997e6194da51cf30`  
		Last Modified: Thu, 16 Apr 2026 00:41:25 GMT  
		Size: 4.3 MB (4276047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c04f8dd9f77c84f91ad17795b2d9eebf8aebb2d7c78dda1a5fce35215b0de058`  
		Last Modified: Thu, 16 Apr 2026 00:41:25 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json
