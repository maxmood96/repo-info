## `clojure:temurin-21-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:0073b1ec453eb9ab9397bfb30d85e22e1438a34adb64dc4ce5995bc3430e1e48
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

### `clojure:temurin-21-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3fe1cb05b67172767c99073769884d3472d9097906b3ce7ef29641e5747acc4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208330831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08d9d0b0ffb6205f5ba1606c67e5aa4965d45458cea37d78d0c3b72b1aeb7ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:53:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:53:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:53:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:53:55 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:53:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:53:55 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:54:08 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:54:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:54:08 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:54:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:54:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:54:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:54:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03cb4c502f7be8fd3e28ea83935d5dcd6a7e53dc49af4d9e845efcd5dad29a4`  
		Last Modified: Fri, 14 Nov 2025 08:50:28 GMT  
		Size: 157.8 MB (157825981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bac2263a91792ab243ef61cd1b7a9ab83900ca42f8d56eb9574a4342cf6720a`  
		Last Modified: Fri, 14 Nov 2025 00:54:38 GMT  
		Size: 17.8 MB (17758116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4da6e7928219fa0bbbaf477144e69c0c9f677a73bb2754aef77b5ab36cc2730`  
		Last Modified: Fri, 14 Nov 2025 00:54:37 GMT  
		Size: 4.5 MB (4517740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1675204b24b86043acaf259671f242f823b97402d2e91afc2a5daeb068b83a02`  
		Last Modified: Fri, 14 Nov 2025 00:54:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a93abad1aad0f9a552cfe2ceabb99246248a4d2bec183b73dd56d40889d590e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26e8cba1a3fc999725e27d01f52d2a1004bfdd2044f20634faf0946c9f339b7`

```dockerfile
```

-	Layers:
	-	`sha256:46614dd9a5ef0bc2a7d8ffe867b262b1928a2f3fa4951b20f8b47029ccdb7c00`  
		Last Modified: Fri, 14 Nov 2025 04:39:25 GMT  
		Size: 2.7 MB (2731890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d140249f5cc6b302e082ec95f8e989b451101b66b42aa223142dd4a3fd7fc0d`  
		Last Modified: Fri, 14 Nov 2025 04:39:25 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:546cd127dd79d2ebe9d4180768bf82c48e64fc0b4c7de86d3265535cf469a786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206319275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134182e5854d83f7f11d010b26c1a96d2968abd7f0b129afb6c71f2b93749629`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:55:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:55:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:55:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:55:57 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:55:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:55:57 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:56:15 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:56:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:56:15 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:56:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:56:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:56:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:56:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b02efe532d7270ab2cb86443c0a9be8e94e9371b6b075ad6f77182ffd6b8916`  
		Last Modified: Fri, 14 Nov 2025 00:56:40 GMT  
		Size: 156.1 MB (156107671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da51cc462c636fb4824ea20903f8d5e296402af3bc56abb3414600684005e1`  
		Last Modified: Fri, 14 Nov 2025 00:56:48 GMT  
		Size: 17.6 MB (17591080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b40ee267433b0c5adf26a6d89c4d9f0771c3483bc32228702966d680b3578c`  
		Last Modified: Fri, 14 Nov 2025 00:56:45 GMT  
		Size: 4.5 MB (4517719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fc8248d2eb7d60e5a0ec04e5bf08cee60a26f20514df2a23cd9108ad4ff91d`  
		Last Modified: Fri, 14 Nov 2025 00:56:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:341bdb40543114c3a7fcff1fcf0c896d6cebaf27cced19509d87709a3e5f4c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91900bebfe79cdcaa0b661309b24f404dcd36d3303c75c572b6dbf950aaaa8bb`

```dockerfile
```

-	Layers:
	-	`sha256:7282cdc207304e97bb5d8ddd49f55c288ef6d8efacdc17bac0a925545817f7ff`  
		Last Modified: Fri, 14 Nov 2025 04:39:29 GMT  
		Size: 2.7 MB (2731505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e3cb359fbcd0f6743ce944f1a4622295f9a0000e93a4a87f481d786d38fa6f`  
		Last Modified: Fri, 14 Nov 2025 04:39:30 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:518a10377f0646f0a896cebd35d29bac89945d9f079a0c843173c32de085e2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212489667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3e55d3bd0aa726ef422708074a7a8bf5a0c92ee7b88d7c5bc1c754f2912e32`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 07:19:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 07:19:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 07:19:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 07:19:03 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 07:19:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 07:19:04 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 07:19:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 07:19:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 07:19:31 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 07:19:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 07:19:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 07:19:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 07:19:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724967c85c6b3060d32217ac74afeeeb9733ac3265e5342756aa479d419ff33d`  
		Last Modified: Fri, 14 Nov 2025 11:03:50 GMT  
		Size: 157.9 MB (157942922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86c1ea71dacce985804236c9dcc0a1c3d81c1cfc2f13f677590ef53b4393c64`  
		Last Modified: Fri, 14 Nov 2025 07:20:32 GMT  
		Size: 18.0 MB (17959666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f17716bcf7973db8d4a4de83ab968aba5853ddef77dccf1a489143ee56160a`  
		Last Modified: Fri, 14 Nov 2025 07:20:31 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a838fd4ac338a4fb1fa8045d709b1de8e67ed9df0738132d0e0effe407bce2`  
		Last Modified: Fri, 14 Nov 2025 07:20:31 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cbd47e0d4aa60de43f1cc612518b28b85df3f53d873bc01b8476fabcd1d82821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054323edbc04075373869c6bd15290e357dcca4017a6077398102fa2416160b1`

```dockerfile
```

-	Layers:
	-	`sha256:d6b5d9c21c8cb66fb07e9ffcd6720e49025f05578c62883860b7892ca63f4d0c`  
		Last Modified: Fri, 14 Nov 2025 10:37:42 GMT  
		Size: 2.7 MB (2733723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c043b215f201eb0c978a48a0efc4108acf60d58ce3261f7dec968d031b23c62b`  
		Last Modified: Fri, 14 Nov 2025 10:37:42 GMT  
		Size: 18.4 KB (18446 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2c7add3c773cece820825cf4acd885674bd75e232642637f0ffd9ac8d317325b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195892408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7dd621aacdf3bb3be05e5f0365f6764389f4175ff002f5dee711cbcaa91ec0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:59:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:59:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:59:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:59:25 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:59:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:59:25 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:59:35 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:59:35 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:59:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:59:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:59:37 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:59:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001962ac540e5f4924816e58c77a53181ce9dd682f678ed1b57d3b8615d15054`  
		Last Modified: Fri, 14 Nov 2025 02:06:36 GMT  
		Size: 147.1 MB (147069871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab68c1e2cde2eb285e42933a13f55b0b4c4c5f66dff493019aaf58d8dfe82153`  
		Last Modified: Fri, 14 Nov 2025 01:00:19 GMT  
		Size: 17.4 MB (17419804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fd6892d69622fefdcf8c605bdb79272536fe08a451b35e6823f9112eed01db`  
		Last Modified: Fri, 14 Nov 2025 01:00:18 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729abc6b72ddc60a399778ba74733fc0112cf8a3258d4bd52edabae233fbc808`  
		Last Modified: Fri, 14 Nov 2025 01:00:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:11b535074c85b5f551c4aecc249751c79e3967c87e2c01a3b7399e43f99d2048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd60b5042b1dc807d377f54d652a811b4c84d0a4f8fcac254e8f351c72f2aaf`

```dockerfile
```

-	Layers:
	-	`sha256:c96b75000d730220847d96a9337589984c7f33ae5b5f28dfa08821a7ccea4335`  
		Last Modified: Fri, 14 Nov 2025 04:39:37 GMT  
		Size: 2.7 MB (2723704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e98bbc10a078acbbb8661e332d468c3a493d3749c75dacd8d306bba28ff0745e`  
		Last Modified: Fri, 14 Nov 2025 04:39:38 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json
