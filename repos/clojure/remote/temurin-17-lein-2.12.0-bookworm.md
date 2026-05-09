## `clojure:temurin-17-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:e95e74e42e506d8a8be334280b8d94be59307dc824c17431848ccbd250570235
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

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9da6b2ff67134662fec0665820bbf56c63484772024105a96c5e2c860eb3a7d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218718886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e03aa925fab2a21979db612c79f51270cd154f432ab199f13d6f163c7258a8c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:16:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:16:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:16:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:16:40 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:16:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:16:40 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:16:55 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:16:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:16:55 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:16:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:16:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:16:56 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:16:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e8ecfc385c67ded6769ce9a7a837faf019a10d8baf3cdfc210e07581521cc4`  
		Last Modified: Fri, 08 May 2026 20:17:18 GMT  
		Size: 145.9 MB (145905487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ce91d9d96a8eb0848ca02b929522ae4dd602e2be2321bbf21536a1df795011`  
		Last Modified: Fri, 08 May 2026 20:17:14 GMT  
		Size: 19.8 MB (19806553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6796e5e206470cb6f8ac70b408ae7caa6433fc2063cfe1fb053af3f0e49c9656`  
		Last Modified: Fri, 08 May 2026 20:17:13 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f6adbc6761da2468507b2c0242efb49193c275242a2bb097d3f8b14d2d92be`  
		Last Modified: Fri, 08 May 2026 20:17:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:28127388e445b1310f51c4ba8f9e2903c88c8db9de0053e969ecc2d7c27443b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc12a12faf00669483b2b8b79ae20fd17ad081b84182df9f959af14b45eb0c6`

```dockerfile
```

-	Layers:
	-	`sha256:5da16c50b3d69a62ae8a59fd5e7311639c7c48dad2a944c2014525797c6949a0`  
		Last Modified: Fri, 08 May 2026 20:17:13 GMT  
		Size: 4.3 MB (4282358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e7aa429988c955b93c4a6e01f01947637e6e4ada8f47bb51077f5ad16e90cb6`  
		Last Modified: Fri, 08 May 2026 20:17:13 GMT  
		Size: 18.5 KB (18522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:84e6e27baa48066a16cc31b37359971396a106a0623a1e4051c785a1d4a17f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217252739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a13e03e861b3231819ddcdc1152c2b4087367bd2048a74291d057b982bf1eb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:20:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:46 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:20:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:20:46 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:21:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:21:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:21:00 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:21:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:21:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:21:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:21:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389583e3e640c603011c92cca4d441999b5e7c806bc8872bf46f680f6260c5e5`  
		Last Modified: Fri, 08 May 2026 20:21:23 GMT  
		Size: 144.7 MB (144724355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ba24d15de6ab691c6ca6be05147df3d1c855eb87831d1402030d769ffda01d`  
		Last Modified: Fri, 08 May 2026 20:21:20 GMT  
		Size: 19.6 MB (19637042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdf6b8b14c493f7eb5fbac59dafb73bf6237c4184023a5a19f18a2899ec68d7`  
		Last Modified: Fri, 08 May 2026 20:21:19 GMT  
		Size: 4.5 MB (4517763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9085e7546addcb8f3181b42d2517df8f76d3987b5111203b79e6653970dc578`  
		Last Modified: Fri, 08 May 2026 20:21:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:99b6381b65e3c2990f3a9da192e1de565a97574e67e0d16dc066432d88e5fb1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd939d4cea992df9704cc21a3a3182eb8b248dc1ef09187764a9bf8864c25ce`

```dockerfile
```

-	Layers:
	-	`sha256:32eb6c31c2d08ddeea265970422a9c728c77b75e0fa74c054470399943482f1f`  
		Last Modified: Fri, 08 May 2026 20:21:19 GMT  
		Size: 4.3 MB (4281973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e54d1c99055962ca95815e03b7f6da11907fb8c5a66b63b71e0b652dfe03ee50`  
		Last Modified: Fri, 08 May 2026 20:21:19 GMT  
		Size: 18.6 KB (18642 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:9a943b4e3cbd17409647fc61e2b029b3f71f812a9c397f5746e64736c696b48c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.7 MB (222651666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9deb79d9c24d2ace3307969056a1ddd804d75d2974caa1728c7c27bc939603`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:43:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:43:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:43:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:43:06 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:43:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:43:06 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:43:47 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:43:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:43:47 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:43:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:43:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:43:51 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:43:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1a630844f3ca330b4aeb3cf62ea83634554dfbe591d28cdf3d1bbe7c2c4aa2`  
		Last Modified: Fri, 08 May 2026 00:44:30 GMT  
		Size: 145.8 MB (145766245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419e191c7ec4b8ec3cb4ebf0d56a17bdad44e0f536b66424b1152ae26f2de926`  
		Last Modified: Fri, 08 May 2026 00:44:28 GMT  
		Size: 20.0 MB (20030506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a883e733f7ed5810bed9ad730543ab1e9fa9dcf21f414b765bae147c277196d0`  
		Last Modified: Fri, 08 May 2026 00:44:27 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4868052b9600bafefaae8a0a1ec28b16a4ec94dd4727eab9ee656adccac2719`  
		Last Modified: Fri, 08 May 2026 00:44:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5a43a0e686d129dd5a06b985f1786f788ffb9ae25e390db9c9e39a5f1d498220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfe995cc87badbfa918db774caf2549e49d7f6b9b1eaa8aa5ab1c46a20cb209`

```dockerfile
```

-	Layers:
	-	`sha256:4b96d5e5ec89d694389ed472c7e1eb33cf0316e20483a29885f654a83607d42d`  
		Last Modified: Fri, 08 May 2026 00:44:27 GMT  
		Size: 4.3 MB (4284219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3df0ebc9e962434ac2e531db4a1ba520486ac84785ac4fdcc2f917e8eb141476`  
		Last Modified: Fri, 08 May 2026 00:44:26 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:fff2d47d5f8227fd25c1691fba64fa0b0cca849d28f8d33cc089a555dfaa4379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 MB (207043356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5840000154d21f751f995ea1bb5b8b00b892b2c5538142e51960b730603e192c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:14:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:14:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:14:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:14:57 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:14:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:14:57 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:15:09 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:15:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:15:09 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:15:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:15:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:15:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:15:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c10a6897782f771d3606e3e80b8e1017d240690fd955802892aea8e434131f`  
		Last Modified: Fri, 08 May 2026 22:15:37 GMT  
		Size: 135.9 MB (135910446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d064fec90ebc8e6b60bf79e2f590f8d9e6916788af9a14266be6e4e2e57a96`  
		Last Modified: Fri, 08 May 2026 22:15:37 GMT  
		Size: 19.5 MB (19466704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b703deb27f43c9b29d501c1ed1ae8ba1a06032dae9d6dd805e2361aa4ee4b8`  
		Last Modified: Fri, 08 May 2026 22:15:36 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93da3ebcb74fb38095769b032c732cca80ecb2032c3e7859fe7d8b367058143`  
		Last Modified: Fri, 08 May 2026 22:15:34 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1f857863aa5d0468850f63844b37995e089e59539eff3fedfe7d4ab804786afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4292694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c271d580e80994c74e1f2e260f421095db75f6f3c02de8a56814c34defef82`

```dockerfile
```

-	Layers:
	-	`sha256:766bed963688ee7530af0d46ef224c844dc23deef99ffba45d789a368bd6c87c`  
		Last Modified: Fri, 08 May 2026 22:15:37 GMT  
		Size: 4.3 MB (4274172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea23169be06d826079151172471bdfa4a2aa01f4e09740bd00a3dbb6c4fd082f`  
		Last Modified: Fri, 08 May 2026 22:15:37 GMT  
		Size: 18.5 KB (18522 bytes)  
		MIME: application/vnd.in-toto+json
