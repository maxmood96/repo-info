## `clojure:temurin-17-lein-trixie`

```console
$ docker pull clojure@sha256:e5660834ffacd2f728ecaf242637081be247f55d0f3bb6ffef0814d9ac040f35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:9be1a58378b2e3f5c2a14ad386f5ed100edbd17d06f621b70674117f28df21d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264822745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b338f052b270b8c3aada84177980719357cc1801827a36443b1f1cc8ef6e41`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f8c8542523ef5c08ca9bd5ab7d7265d12930a45ccc7c8364e909fde03c894479`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 49.2 MB (49248239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003e8018434ae51c02bceb8212498c273dab2e3fc802d9dc9a8e9518fa1f70b9`  
		Last Modified: Sat, 17 May 2025 13:45:24 GMT  
		Size: 144.6 MB (144634954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca10b966ea458cd86755d32ca49260ded7df418c76616d230f9babdb92b85578`  
		Last Modified: Sat, 17 May 2025 13:45:22 GMT  
		Size: 66.4 MB (66424986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe5cd2d44161515db71e77b1ad10cd37ca2103beb35553110bc37ee8d3051b8`  
		Last Modified: Sat, 17 May 2025 13:45:17 GMT  
		Size: 4.5 MB (4514136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38b5dfba672dadb9facc7e3bbf7f969215418491591f94d257d43769bd83c69`  
		Last Modified: Sat, 17 May 2025 13:45:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1342c40017b4c0400b5ea14718c3b52dfd7b2c742b37986e243f300c8539ad79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6303638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a632059f7b7818d7c0327ebcbfa4c0a9cda887f3a530febd6460018fcec179d6`

```dockerfile
```

-	Layers:
	-	`sha256:d068428e01186c9a657612db1dfa4c5a75b509f7e89c847bcea6fbe663b13441`  
		Last Modified: Tue, 13 May 2025 17:53:49 GMT  
		Size: 6.3 MB (6285236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb47f519219ef36a32e04d049f3d302a04c72d7af341108a02082e4726a87060`  
		Last Modified: Tue, 13 May 2025 17:53:48 GMT  
		Size: 18.4 KB (18402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:42d263ba0a08304c8957337bca8633e1492c24b3e01e3b1d8d30748b535b98f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.1 MB (264108726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5fb38b813d84464b0f7665d60d5aed1efa91e83720ec2b7dc8d9cbde8b8182`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:288a1cecb0ea762427d39b072c1ca965d193e927e04da652f7b21eb12e9b2acd`  
		Last Modified: Thu, 08 May 2025 17:11:50 GMT  
		Size: 49.6 MB (49624118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b282e0ac6bfae3681aa56a27479878cb17caec1c03eac0e2edb7ee5cb06808d`  
		Last Modified: Tue, 13 May 2025 18:00:41 GMT  
		Size: 143.5 MB (143512641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa4c415c6c3a58b7ccb4fa6ed8d830c03417447f3a12f03e840e330b9ba4653`  
		Last Modified: Tue, 13 May 2025 18:00:40 GMT  
		Size: 66.5 MB (66457329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f1b70ba51aa0b896f1010c6694e2d6cf4e3069222f59796ae541850ff9d01f`  
		Last Modified: Tue, 13 May 2025 18:00:38 GMT  
		Size: 4.5 MB (4514209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4264ad10d32feec4ecfa4af3f632244f49a0b9fd88a210ed9bcd8d195b8e7d`  
		Last Modified: Tue, 13 May 2025 18:00:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5b8a148f0be198f19514038e470e9c2013b4111ed0dd3167769f44306c283d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6310723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388ce0ed7361be8d9450400d44486b5a3abbcafb4942d537a0a977f824aa88f2`

```dockerfile
```

-	Layers:
	-	`sha256:3e6056340ef9d03996af48e108afb03ead77c2ede53d48ead25333e258699f06`  
		Last Modified: Tue, 13 May 2025 18:00:38 GMT  
		Size: 6.3 MB (6292199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:919532cd78a8931a0dbac31ee1ff870046824180221750212bd99c3f6d8da7f9`  
		Last Modified: Tue, 13 May 2025 18:00:38 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:fdaaca5c2376bde2732f047cb573609f00573f1401149f039584c7207bdc5291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273374216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e157a6f8a51c378e8c7d69f7a17671ab15f38a374898bb88fb09a547f617c221`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:03ebb30bb37cd398ea8ab1a268c301664089cf5a54d23466e4338782afb5f9cf`  
		Last Modified: Fri, 09 May 2025 00:28:48 GMT  
		Size: 53.1 MB (53072552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae552af9b4a5f2c0ec434558439412e3b3de2a024f98aa1612023e6c631f846`  
		Last Modified: Tue, 13 May 2025 18:57:26 GMT  
		Size: 144.3 MB (144280526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a5dbcf44d00c39e8899303af11331cd21f759189ad49bb46077bf6ccdfde2b`  
		Last Modified: Tue, 13 May 2025 18:57:25 GMT  
		Size: 71.5 MB (71506549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a126bee9d1a3d570c0a2f14507933739b0455b885a5eda136bafef9c62b7213`  
		Last Modified: Tue, 13 May 2025 18:57:22 GMT  
		Size: 4.5 MB (4514159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c698866d290553912ce8de4b378d202210a35b7f90a1becd85c43eec046a04`  
		Last Modified: Tue, 13 May 2025 18:57:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6e75b3376bd36db1b560440141de2729a041c29d93b1f2cdad7752aaf9b94208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6307635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1939609fd7db1b0f105c23567f9460fa935f92c2cb69ec4187af1fa2ac5996a`

```dockerfile
```

-	Layers:
	-	`sha256:9a0ae14779f8c5926a4fd2aa95809a73951996e5cb05458196b43c8a8fdec47a`  
		Last Modified: Tue, 13 May 2025 18:57:23 GMT  
		Size: 6.3 MB (6289190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58fa71894f05715928171a498e3d5aa556cbd5f1ba722b4d3eff39e4ac33771d`  
		Last Modified: Tue, 13 May 2025 18:57:21 GMT  
		Size: 18.4 KB (18445 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:0eba2b0385f8e4637624833896a2e15109b63ecdf32efd90948ea20cd64025c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256367408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5beb97744ead70a91af1de024a906645ae94381f63f5b9fee3f7b90dd6002a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3e87a3ef7201dacec1e06fe511cdfaa924c5bf89f4f022c082b59ff14eb11b6f`  
		Last Modified: Fri, 09 May 2025 00:14:52 GMT  
		Size: 47.7 MB (47740349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f9073eee7103f8b2bdcd4dfa76a64bae8444d17ffebad5b0bf5b4e6b8077f1`  
		Last Modified: Tue, 13 May 2025 18:07:06 GMT  
		Size: 138.5 MB (138492641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a85e32ba20d4b4e2ca605c3beff2f1582e4d0dad7ca0fbb0392af12846488`  
		Last Modified: Tue, 13 May 2025 18:06:57 GMT  
		Size: 65.6 MB (65619760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636600b757cb44b48e9fd6f3f0d3b545f9d7c5e74e4a434b9f7d7c6a1a37235f`  
		Last Modified: Tue, 13 May 2025 18:06:49 GMT  
		Size: 4.5 MB (4514229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da66c4b8b861f0580ba4c8a7994884469819f4acde921682dd5a6734d4a4fb49`  
		Last Modified: Tue, 13 May 2025 18:06:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9a1163743e3fe193aa4040b49d9304b7d548f93fa5d223577bfc200ea25d6a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6289710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c0422c8b01f2c28d0323d457c35331b88f845e481274bcd02c505ab3fc9a27`

```dockerfile
```

-	Layers:
	-	`sha256:e842383d97ed20d537b77cf3540019166ec249d174376cc43c3d0193e1547cfb`  
		Last Modified: Tue, 13 May 2025 18:06:49 GMT  
		Size: 6.3 MB (6271265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98835ca80ae4f898e8bb16a62d50ce2cb456314c1d017a039a333a930cb27ebd`  
		Last Modified: Tue, 13 May 2025 18:06:49 GMT  
		Size: 18.4 KB (18445 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:0a55d879c2562fa08808a80edd2ab27c79eb21fdded970514faf615ffa010703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.0 MB (256005744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05820c7b92a38c18c0736bd5252de89672994842613469fa7cd76055aa3eaa3d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e1ec3b1570f7d822c5a6aa013529484429ad99bde8495d827b56c3603992fd3c`  
		Last Modified: Mon, 28 Apr 2025 21:11:06 GMT  
		Size: 49.3 MB (49316646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ca100b33a26d036b967727026db8398303b1b8542c4f1f20bacfc893669267`  
		Last Modified: Tue, 13 May 2025 18:13:20 GMT  
		Size: 134.7 MB (134673562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4301c380bfcf08fa51cb8e55fab97f53e95312a94471ffcbdcb72d9ce1b06c0b`  
		Last Modified: Tue, 13 May 2025 18:13:18 GMT  
		Size: 67.5 MB (67500895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592235ada5be95803543b3088457d0209eeca8ed4006563c2497c6da90fa69af`  
		Last Modified: Tue, 13 May 2025 18:13:18 GMT  
		Size: 4.5 MB (4514213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db766693b6c3547d0119048d44501f57d293e27bd95dd2dbb50d9b25fcb3b458`  
		Last Modified: Tue, 13 May 2025 18:13:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0aa5db0d570485e28c8a27e6eec04f8433a5736656e90b4fa2e665a048eb81cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6299616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5b405fa2987f486cb30f562b1e015dc132e7f6618dc78ec9ff575b013bcf60`

```dockerfile
```

-	Layers:
	-	`sha256:f4d89c82cb7b8d0117eb66012c3b6d1ce1350c1b4a50b2e276974aae6cac0cf7`  
		Last Modified: Tue, 13 May 2025 18:13:17 GMT  
		Size: 6.3 MB (6281213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd297a1b8bc16c42d6b3ff2baeae663ba67912c831ebea066c18a16359488636`  
		Last Modified: Tue, 13 May 2025 18:13:16 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json
