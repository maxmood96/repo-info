## `clojure:temurin-11-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:f0eeb40f039eb6da791c9dc0158b296fdef67161bff525800361f593ef15f003
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

### `clojure:temurin-11-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f3e69687ac61e73b20325de2af8f3774714f25033ef7e60f9a491bd9559c078c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229839954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5ed6706f7306396a6b8b5b4847edf38a5e3867e85eaf76dc0e3b82faa54f35`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f044ff11b698b4b12d0e165c63fcb15a20a22b32ce026f39dcc8108682113b`  
		Last Modified: Wed, 21 May 2025 23:32:15 GMT  
		Size: 145.6 MB (145635718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503cdcd79faee06e8c19e6fa5e2567c8e8b4814a2fb7ae01378915e850f2e5c1`  
		Last Modified: Wed, 21 May 2025 23:32:14 GMT  
		Size: 51.5 MB (51464662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9a3f1b996f600039ac317c103e99433df67660a16172410c65af4a6b9ca202`  
		Last Modified: Wed, 21 May 2025 23:32:13 GMT  
		Size: 4.5 MB (4514212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c6141ceb59c3353fb8d83d19658a9674d48c56ec4e65b2deb819ac72bc62da6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4403356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21f30b34ef19d663e571878aaf6502728862449545be7426182f3315f37e91f`

```dockerfile
```

-	Layers:
	-	`sha256:55f1be91978335f122e4427e1c26c1939fa56cf0e1de854fa0c06c01f1010cf6`  
		Last Modified: Wed, 21 May 2025 23:32:13 GMT  
		Size: 4.4 MB (4386894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b052225c71c1a4ec76d3548f89e5ae7876e11bbf42fce989086a0df0e5733fb`  
		Last Modified: Wed, 21 May 2025 23:32:12 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:168d9ef3b27814b60b82cfa412c96693273893ab9676f48b754c8953a46667bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226432263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66581583d1de324c6c6069c72eac6a9d9fb1c0424a374b930c7f8ad618ff1cbe`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_ROOT=1
# Mon, 28 Apr 2025 17:24:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b722f6de86e72fb07562d87346af6be7b90ba50431c937810c2662421c09c4b`  
		Last Modified: Tue, 06 May 2025 00:24:11 GMT  
		Size: 142.4 MB (142420712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f786f1d4f0c1f0f920d26b8e11f7b25f50641697d71a089c15d4a567e331af0`  
		Last Modified: Tue, 06 May 2025 00:24:09 GMT  
		Size: 51.4 MB (51430688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edaaeadac3339d390b764a58888484eb0ca52f5429fe93e0ce86d35b5cb2541`  
		Last Modified: Tue, 06 May 2025 00:24:08 GMT  
		Size: 4.5 MB (4514209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e47989e419a526c5aa287bfb274bb0c4c58ae5e304b637c591162bda10b8ae7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4364860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4c61b6532bccb62515542cc20792434b1a58af58824aab98d86bae282ef9cc`

```dockerfile
```

-	Layers:
	-	`sha256:c88fffd72cadd6b7d74098c8b788d1860a95ecee8792954f9a7f9d44114be8e5`  
		Last Modified: Tue, 06 May 2025 00:24:08 GMT  
		Size: 4.3 MB (4348276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bce7a6403bc9253866c0a3b54f6cf373476980e35916a9e78f9bbd920b13b8d9`  
		Last Modified: Tue, 06 May 2025 00:24:07 GMT  
		Size: 16.6 KB (16584 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d88e35fc54a03ba0b68cde25ed998b93e3ce18bf83e13b89b69fac76cd491cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226072795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf506ec3cf29d9c606cca84f3de03c8728d6c4696d2fd9f324549221a152b7b8`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
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
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072938722d633c364ba2ea6b70c7a07f710edd3b5fea7decbffa42f42997ea3e`  
		Last Modified: Tue, 13 May 2025 18:27:25 GMT  
		Size: 132.8 MB (132809833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163e180649d1ef65247d16a542f33e7c10e9b5d5f092c662ab85572af7571857`  
		Last Modified: Tue, 13 May 2025 18:27:23 GMT  
		Size: 56.7 MB (56680328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4a972545c46ed31683ff229affcb26a716b164247c8e33c63c4906ed9f2509`  
		Last Modified: Tue, 13 May 2025 18:27:21 GMT  
		Size: 4.5 MB (4514159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b31feb1abeab6f3a5e065d3e4e6e6ddb0eb39cfd19b754bcec416f23f1bc0791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4362538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751458239000a4fe544eef2f8d3e83af22ec331bbf55a10148c0b6c5d7b17b6d`

```dockerfile
```

-	Layers:
	-	`sha256:a08649d82964e4fd1da94a3c9d6d68228276a133854ad2f44c15a618bfc4ba14`  
		Last Modified: Tue, 13 May 2025 18:27:21 GMT  
		Size: 4.3 MB (4346032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c1a6e90371dc6c80061fff7c6e7a74d06bb1b1943249584054a018d3db5841e`  
		Last Modified: Tue, 13 May 2025 18:27:20 GMT  
		Size: 16.5 KB (16506 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:e82968b6e8315d1e5dc2625afcfdd8901fb25e05eab96f14fe5c06305ccaa98c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.5 MB (207455931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9684aa211511262c61a6c8d8ae7c9da91364c9704ec1acaf1efd991044c9c1c0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8320f723c77b813fa8f45308ad2223914b761653eab90015935672d843c1787`  
		Last Modified: Thu, 22 May 2025 03:39:39 GMT  
		Size: 125.6 MB (125585847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c94b7d586281007175f15564e1b21d229c0eaeaf74f7d429d0b05c800ed980`  
		Last Modified: Thu, 22 May 2025 03:39:38 GMT  
		Size: 50.5 MB (50473054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2f752a42c8b3b4ec69b7e7e270539b0f3f3bf0dad850b5887f5b193d8851cc`  
		Last Modified: Thu, 22 May 2025 03:39:37 GMT  
		Size: 4.5 MB (4514190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:77463ab17e42b5e4c95feae749a2aefa600d37877e96f4350af863d3b9fb49d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4397630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a321043130996080afe7f900c50e7227310b247a01982e9149005ca3f44dbe`

```dockerfile
```

-	Layers:
	-	`sha256:438c309eb5de8d869be0c0c611ffa93bfce4ce3b8c7b2b7999b86e860167e647`  
		Last Modified: Thu, 22 May 2025 03:39:36 GMT  
		Size: 4.4 MB (4381168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb2da92b970e55344a86ca9fd3326be9e73bd1028be858e6983ade723f8d685e`  
		Last Modified: Thu, 22 May 2025 03:39:36 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
