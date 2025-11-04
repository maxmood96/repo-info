## `clojure:temurin-8-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:a85da6ef24d991766914c64fc4078ad0761533ce5a79f150dfbc916968f8919d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:37a1abf43b40906f1f94e04a3b520e7d792bd16d5ec92debc6a09b4513a790d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127113835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df6beb594d02131a1bb606b114ace5c79ffe9def8fd50b49e09f977297c9dfe`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:29:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 04:29:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 04:29:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:29:43 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 04:29:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 04:29:43 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 04:30:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 04:30:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 04:30:00 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 04:30:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 04:30:01 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875dbfa89fb97aa13f3f4ea32a07e5d148a8adc3519e6e1a3806f8af06bef292`  
		Last Modified: Tue, 04 Nov 2025 04:30:33 GMT  
		Size: 54.7 MB (54731291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adddef70b394777ccafae67e30b7e9ac78c271a694b749161795567bbf53be9`  
		Last Modified: Tue, 04 Nov 2025 04:30:30 GMT  
		Size: 18.6 MB (18579159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f3e8604a372c7af27792be713dc1ac441f9aacd6c5524a81964a283ef6312d`  
		Last Modified: Tue, 04 Nov 2025 04:30:28 GMT  
		Size: 4.5 MB (4517725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8982546adfd1a01c9b76622d4917023ab3564ce20f3f5268bb5f863a786eb3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2eaf9eb989e1cc7c4cd68e64becc44254b4cc4fd436bc087b79adaf1dab940e`

```dockerfile
```

-	Layers:
	-	`sha256:3370ff4bf5eba8ad84ce7d68fc1197b9b431a2c881fa0e1cc26004408f592978`  
		Last Modified: Tue, 04 Nov 2025 10:48:45 GMT  
		Size: 3.9 MB (3934996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b50c501197379b0002207c9969267cc847fb5ce42febd5f09b9e5c7c337bc430`  
		Last Modified: Tue, 04 Nov 2025 10:48:46 GMT  
		Size: 16.4 KB (16350 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:479b5fd7d4575c379e5f9c8d7fa26b1800405e1eaef849378a18e909a387af5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126543634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dabbe8457fa07e56b5224fd87f66b770ea140e44b2c7a077b594d15c1fc9a354`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:43:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 01:43:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 01:43:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:43:25 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 01:43:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 01:43:25 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 01:43:41 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 01:43:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 01:43:41 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 01:43:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 01:43:43 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5bdb42897e2f1abfb792d3b20785cf855ea952a6b15e94f225eda38967036e`  
		Last Modified: Tue, 04 Nov 2025 01:44:05 GMT  
		Size: 53.8 MB (53835577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cf9c7fbeb13309f71c802d9d4105ef650e5ff675a147ad7a04fd557aa2c88f`  
		Last Modified: Tue, 04 Nov 2025 01:44:03 GMT  
		Size: 18.5 MB (18539891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e805c529eea09bffcb09f2d5acbe103ee9a055aa4c788275fd4d6f0d871397c`  
		Last Modified: Tue, 04 Nov 2025 01:44:01 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:96e60155dbd977da447afada41f51d2441248ced16e8a49559f4cd608b8b0564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2162ccabd11cbd4329e573fd84392dca030b9166481edcae75f08216538c9c75`

```dockerfile
```

-	Layers:
	-	`sha256:9131237d8194d88e79e529bb4817b6464837772e3b4a0d5677a5b5947fc46db1`  
		Last Modified: Tue, 04 Nov 2025 10:48:51 GMT  
		Size: 3.9 MB (3936571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa5178b964f7b2f2a21f141826303052d2090808317c3832873b83ec9bf891c2`  
		Last Modified: Tue, 04 Nov 2025 10:48:51 GMT  
		Size: 16.5 KB (16471 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:752f703f8cef0b4259dc9b4ccd4fb3990958feaaad28f5ee611d232e1b09640b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128429883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da951da16aa9a64bb9a2ca9e236e58ab703a4e15ea32304cae7481d1305bd86`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 13:02:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:02:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:02:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:02:15 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 13:02:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 13:02:16 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:02:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 13:02:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 13:02:56 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 13:03:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 13:03:00 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431f20163584da71198702546386fbb961546d955c4c1930a7d523c1e219f1cd`  
		Last Modified: Tue, 04 Nov 2025 13:03:55 GMT  
		Size: 52.2 MB (52165358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f62a8e1da95e16d73bc62af5d708ed7ca005611b2f335f9a53b70daaf86217c`  
		Last Modified: Tue, 04 Nov 2025 13:03:46 GMT  
		Size: 18.6 MB (18636597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b923d65f9d533b526be18caaca290b8c5e91d871382f6298b55bc3c72ea6f7e6`  
		Last Modified: Tue, 04 Nov 2025 13:03:43 GMT  
		Size: 4.5 MB (4517769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4659e2f5e675c3ad136f6d2c3bb8fc96345d27135e9bc10b680a352695ad0ac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d4736bcaffb2fbbfd622a99e4550154a5334c0fa51334c29ef4f98daab0f3e`

```dockerfile
```

-	Layers:
	-	`sha256:7b713cc3bbd2c9a1ed0f10cf8ec03cc060f9c315ba66f789cae9d7620d91b560`  
		Last Modified: Tue, 04 Nov 2025 13:38:43 GMT  
		Size: 3.9 MB (3936587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090222cf7464f3c748d2661b1153606ab0ee3ec6bd277fc59f8524cf3a5adedf`  
		Last Modified: Tue, 04 Nov 2025 13:38:44 GMT  
		Size: 16.4 KB (16396 bytes)  
		MIME: application/vnd.in-toto+json
