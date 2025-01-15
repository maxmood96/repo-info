## `clojure:temurin-8-lein-2.11.2-bullseye`

```console
$ docker pull clojure@sha256:1a907c9e84e933d7a482d9fb356570a9e2f4846b7ba6053220c3953fac999fd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-2.11.2-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:80c720429c64b9754b55b4de97dd2e348f82d061cdbf3a636443a7ec4dc074da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214466072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e165cc2d938a355c32292617aeb22cb49aefb9c298526a24795769ef5dd030`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_ROOT=1
# Mon, 06 Jan 2025 23:07:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db54dddfcf1b694c458c5b325dcbd05b12129211794212a811606578007e94a`  
		Last Modified: Tue, 14 Jan 2025 02:43:20 GMT  
		Size: 103.6 MB (103633930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d5c07f157dd0ee6f33cfef02a75b0a6e780c5d3bbeda20aecb5c103036015a`  
		Last Modified: Tue, 14 Jan 2025 02:43:19 GMT  
		Size: 52.6 MB (52578736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f31dfc467a3c28479323772c354d120a12e3010bb37b4c07047b85153ac975`  
		Last Modified: Tue, 14 Jan 2025 02:43:18 GMT  
		Size: 4.5 MB (4514210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1758c72edb824d40ded074e42bbdbd6f32929cd3d43f4f47d53e8260e93de753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6758404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5bb6a5ae9488b84aeeec916d5e3fea14566e7432ac1e27d9a2d499cdf31cf9`

```dockerfile
```

-	Layers:
	-	`sha256:2a8383e072ccb7017a7dfae3e324ee0a95279c69aa25e4806c794f9a65fa8431`  
		Last Modified: Tue, 14 Jan 2025 02:43:18 GMT  
		Size: 6.7 MB (6741978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b60aebbab01a7cc4be0b225e7d03d052ad2b5a35571189e58c1258494167bcf`  
		Last Modified: Tue, 14 Jan 2025 02:43:18 GMT  
		Size: 16.4 KB (16426 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ad4fab7d08b44f10de7bca78ce2f811f535ce33253946bde89d1d7bf8f2dd5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212132661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10b53eaf0e85f86bde91b2b550f7b4cf3c0c48546f995eb0cbb874a6c0c5205`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_ROOT=1
# Mon, 06 Jan 2025 23:07:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 20:36:01 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f468498da49c43dd921b0f405aeeb87eb714221124b311e09a623dcaca2d6c`  
		Last Modified: Tue, 14 Jan 2025 22:03:36 GMT  
		Size: 102.7 MB (102747715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a827f023bc8e243f6ca98cf9ab19d85f6caa1c0867ce3438d3dec4e7811ab22`  
		Last Modified: Tue, 14 Jan 2025 12:15:13 GMT  
		Size: 52.6 MB (52624637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9240282dd3b755e760d22f3f81886de4d489df69d58b30ca2e884a3053446f4d`  
		Last Modified: Tue, 14 Jan 2025 22:03:31 GMT  
		Size: 4.5 MB (4514217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5c9e731e37b5e1e02de51db0c7f7ff8980b000399b30d9dafee266db0a0e6b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6764254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5685045126fea0e93365cb9e985633ccd8e1aaf9b95def2f9483f2186519b700`

```dockerfile
```

-	Layers:
	-	`sha256:47a0107df83a5ff7144995d59f4f5074863d674dc38187862694d0d554759a1a`  
		Last Modified: Tue, 14 Jan 2025 12:15:11 GMT  
		Size: 6.7 MB (6747707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef962356a9e8e342cbe3f80fbfb5d45038a78afaa6f4bdf0e07ebf80e3437b61`  
		Last Modified: Tue, 14 Jan 2025 12:15:10 GMT  
		Size: 16.5 KB (16547 bytes)  
		MIME: application/vnd.in-toto+json
