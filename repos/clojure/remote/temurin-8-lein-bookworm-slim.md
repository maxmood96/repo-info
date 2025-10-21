## `clojure:temurin-8-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:c93154df0c7cc7cb260529bca3bfa57951a8f123479fca12054dd2988be97edb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:270bffcf216e6da9a95207ad11cdfcfd1493ff2dee42ddb437cb0ba408a2ca37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105235453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b05c2e5eeb361b3020ff9d1cad56e69a72e6909097b7e67d17d118f7338d7d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c3f6adb0f74d5bd84d535b6093218f274eb93e816be6f5d5d792f6081146bd`  
		Last Modified: Tue, 21 Oct 2025 02:18:26 GMT  
		Size: 54.7 MB (54731351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f47b84678c023910175a87ae041ee1e2e670498cb3f1b3d2fe9a3a29b252c3`  
		Last Modified: Tue, 21 Oct 2025 02:18:20 GMT  
		Size: 17.8 MB (17758044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac0f9c0274edfd5d80be5d686fc124b2c4c67133d7fe4858a89de50b9f5e579`  
		Last Modified: Tue, 21 Oct 2025 02:18:19 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6328f2425c2144ed31c9938e94444bbf81d5f29583a64b9a737145dd1675636b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e33d05023e53292e293658e1d30afe7f401b02c9d254dcfc282f000ee8cde00`

```dockerfile
```

-	Layers:
	-	`sha256:1cefdd1c40cdc395aad29320c787fe774e47ce26da746be12f536d3cfd16596b`  
		Last Modified: Tue, 21 Oct 2025 09:46:47 GMT  
		Size: 2.9 MB (2850398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:feba0f6d9accbc46f0c455d4f5535ad7485855d96b6083bf8ea404a9229a6499`  
		Last Modified: Tue, 21 Oct 2025 09:46:48 GMT  
		Size: 16.4 KB (16443 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3396a17dcab5721b9f49b9b7852327708be76474214c7a36801a252a062ffd50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (104046670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab0e4eace10e29654faf8379b41c813dfee6eb9a87afbc4d10c49ebe8d7c90b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b12bb59174b2fee7db245192ca74f5f9969fb384476f8acfb3c4ce59447ace`  
		Last Modified: Tue, 21 Oct 2025 02:24:32 GMT  
		Size: 53.8 MB (53835606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e02b2710e6556ba2eb0a1d5faf72f6617bd5fc596f1510d01394cb7a0e507f7`  
		Last Modified: Tue, 21 Oct 2025 02:24:25 GMT  
		Size: 17.6 MB (17591125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c793adc419986a368e34805dbf41e94547a1934eaf42e422714c97458afe791`  
		Last Modified: Tue, 21 Oct 2025 02:24:25 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5d51f7b4936532a99c43bc2058b54be1c5e8e420bd27b5c36bd4c39eaeb7ba4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d115774de9eeefcb5cdcf9b21b7814bc9d05cebf21be391ab4dfe3e4c4ff775`

```dockerfile
```

-	Layers:
	-	`sha256:5b99445073d849b05774f423af613d8c6efed8058d860ac283796aab0135f944`  
		Last Modified: Tue, 21 Oct 2025 09:46:53 GMT  
		Size: 2.9 MB (2850711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:379ed5d2902f1aead85c10bcf00d3d553016b3dd565c507326a7c4c6930de385`  
		Last Modified: Tue, 21 Oct 2025 09:46:54 GMT  
		Size: 16.6 KB (16564 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1b702d0f8705911d13e97cc78e687b36dcc804e7aeecfd07d9bae51f17dd2dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106711465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd0dfd5961d5cca432f87f6716a5e4c0c4564d00ebd0a8255df2ef04507afc7`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4808b36faa8f51beaeed0fb85c1eb939ecd3b64b53ab9d96dd338710855719`  
		Last Modified: Fri, 10 Oct 2025 04:43:21 GMT  
		Size: 52.2 MB (52165456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fec11f5bdb036489889980f9db4f3d87837812d20153a8152110127d818c1bc`  
		Last Modified: Fri, 10 Oct 2025 04:43:19 GMT  
		Size: 18.0 MB (17959555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77056ecf93e40d8e6a2dcdc3fec08dd2ec52d5372cf0f3eb36d38e4df3a2200e`  
		Last Modified: Fri, 10 Oct 2025 04:43:19 GMT  
		Size: 4.5 MB (4517725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bffe33c34cf84a1a6be8e84f9e318cd5bf56215bc850afcce92c5f6ccf7449ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3040e2542df5d3724620b4f334455f320747f802fd36be26ce6510fd541c49`

```dockerfile
```

-	Layers:
	-	`sha256:f2d932f0b8b0162f324d8d13b920d1077c655c58554c45961e334f28d369434c`  
		Last Modified: Fri, 10 Oct 2025 06:51:10 GMT  
		Size: 2.9 MB (2852824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c72011d9124b5beb4dc4c36268176652893ee1365548a553ed7b99ab3e156fbe`  
		Last Modified: Fri, 10 Oct 2025 06:51:11 GMT  
		Size: 16.5 KB (16487 bytes)  
		MIME: application/vnd.in-toto+json
