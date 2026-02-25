## `clojure:temurin-8-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:1d4e8dd362fbe83d4bf5ffbcbc7197e9171a22cbdcc11272b68c145cd4df7886
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5082c439e68a4594072b7556fe24f46ee48c419702198d8c9edb0a79a107e9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105913604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e61b4df4224b6890a2298ec777237cc8db4da8ad95ec862e88275b497316a7`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:52:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:52:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:52:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:52:33 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:52:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:52:33 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:52:49 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:52:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:52:49 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:52:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:52:50 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8362d916c99f3bb6ea102c595ddc32c0a7078d13606452e9b735932635b03336`  
		Last Modified: Tue, 24 Feb 2026 19:53:04 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bef2eac03edf5028f77e331a405754580a02234d2b6ca2b2864725de27d04fd`  
		Last Modified: Tue, 24 Feb 2026 19:53:03 GMT  
		Size: 16.4 MB (16447175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde621d4c58514de635bdd89347423bdecbfb01a949e0dd8d36d971250bb62a7`  
		Last Modified: Tue, 24 Feb 2026 19:53:02 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:491e7173e1e6f6dd298561b4b308827b2b0efe86ded79313ee2b12b7b9f7ff27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7bbe4ffa0fa92d74e3b83802a4b93fe55e60378e39e805bda4878e04e164fa`

```dockerfile
```

-	Layers:
	-	`sha256:6ee38ad6770dff1f99dadaf545dc0adbb12563d32ff59fd122440a4815abddd6`  
		Last Modified: Tue, 24 Feb 2026 19:53:02 GMT  
		Size: 2.5 MB (2485741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178536cf288d4d88c61eca709602d3087c6e2dce6b240bd6022bcf34147c0652`  
		Last Modified: Tue, 24 Feb 2026 19:53:02 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:18f5ddafe4b679c4e452d89104a0988072bab41c8c11f36f78f396c354c95414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105323008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf31f1efcb59c1614da35948d485bf295ff8257a520baf6fdc07024edd12291`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:03:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:03:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:03:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:03:10 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:03:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:03:10 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:03:25 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:03:25 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:03:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:03:27 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006ca2b977e55d31efb55913b42d1ecfd4043e6ab907fa440e4d74e7167cf8d8`  
		Last Modified: Tue, 24 Feb 2026 20:03:41 GMT  
		Size: 54.3 MB (54251612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee50edcbefbbd01a846011edf1376eb9ea1362a2e8357c98df9804d72252eca`  
		Last Modified: Tue, 24 Feb 2026 20:03:39 GMT  
		Size: 16.4 MB (16413561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d8106ba6cb86d7bfd6e85cd339c312639337663fbec71a8b063f5f2edb75b2`  
		Last Modified: Tue, 24 Feb 2026 20:03:39 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9a7002ae1aa0ff82b23e6554799d495800d9e555aba84df0989b7b046bf8a652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984d015ccfab7aab91756e61845c888c23c18efe7df5598bba6d1af246878f24`

```dockerfile
```

-	Layers:
	-	`sha256:2706e76e0e83ef52b5887d92032f4cc740f729e9ba4e0766e613a238a3aa9c10`  
		Last Modified: Tue, 24 Feb 2026 20:03:38 GMT  
		Size: 2.5 MB (2486059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da55ff21035a17874c7795abefd949a1a5352baa06fa2e148c5108d09e179003`  
		Last Modified: Tue, 24 Feb 2026 20:03:38 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a9f314811b230f017ed5a17f6099b80c1af7521d0d1a2eec0c6e6a02c8758804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107253279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b99586eeea023f973160ab135b29cf29c3b7ff2979857dc090bdc99e5a3fe9b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 01:44:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:44:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:44:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:44:01 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 01:44:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 01:44:02 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:44:47 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 01:44:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 01:44:47 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 01:44:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 01:44:52 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1d2b34408ac8afec8ecb73eda9c9a8f5b90be5df6cc2f490984d24c34e7003`  
		Last Modified: Wed, 25 Feb 2026 01:45:24 GMT  
		Size: 52.7 MB (52650417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b16a88ac9a01d098dc4f015b35d6b6a8349c2123bb8109ed1c030f2de7a069`  
		Last Modified: Wed, 25 Feb 2026 01:45:23 GMT  
		Size: 16.5 MB (16484879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35dd7e84a9e5a27ed766b593b70f3dc013fbf8f021c8d3795e8dc3d988dc161`  
		Last Modified: Wed, 25 Feb 2026 01:45:23 GMT  
		Size: 4.5 MB (4517735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a0d2932d9d131f688a0dd556a653fee047ed9913682cbb42e60baed81b6db64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a120393200b173cc209c9928cd229e3b3abfcb3be1ec9444a72c4885612b37`

```dockerfile
```

-	Layers:
	-	`sha256:a461fae55e27d0d062fbfca0b2d63e876c45b024b1b76ab75cb0bccf756e6cc2`  
		Last Modified: Wed, 25 Feb 2026 01:45:22 GMT  
		Size: 2.5 MB (2487316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c1284061d046af367b72c4245c2108209c6cd242ff6fe2794a42f25628e5be1`  
		Last Modified: Wed, 25 Feb 2026 01:45:22 GMT  
		Size: 16.4 KB (16426 bytes)  
		MIME: application/vnd.in-toto+json
