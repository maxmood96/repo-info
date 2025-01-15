## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:c67ad4ce148dca338800cb212955ad6c9525f3cf87bfa674db4b56ccad09cdc0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:86d411b591ef5368752da69b8becc20894db5ab58a73efd8d4e9bdd3928df914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256433649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92b6ac2eec7124321a3c7f36c488001e713dff9e4e893b2825aabfc0546c12c`
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
	-	`sha256:51c852fbc1da31d29d8895d771ac0e2c28fd0a033a4ad9940f167d9568de43fe`  
		Last Modified: Tue, 14 Jan 2025 02:43:37 GMT  
		Size: 145.6 MB (145601500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd2cc38d3d8ff82cb72b644033af79cc1e05daa91451902db37b8cd11aa463a`  
		Last Modified: Tue, 14 Jan 2025 02:43:37 GMT  
		Size: 52.6 MB (52578811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f6a823fabd56c3156f928d62c443e9581d26195ddfa7993640c54be792f95d`  
		Last Modified: Tue, 14 Jan 2025 02:43:36 GMT  
		Size: 4.5 MB (4514142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:656da49d1dd0a586369e0805a06ce08c71658fc5bcc27e47a93e5e5791964394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159e45444c791082ef5008ff6a68aa2725f32e1dff2c4bd3ebcdc8d50d29f65a`

```dockerfile
```

-	Layers:
	-	`sha256:8bc368da20c70286294f35fa359123ab80b0c2f57e48864cd8a492f4978ce7b7`  
		Last Modified: Tue, 14 Jan 2025 02:43:36 GMT  
		Size: 6.6 MB (6639897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ccc6473b150442b9eefdf59083febbf7d8e97f8f155d82418c3bfdea65a2af8`  
		Last Modified: Tue, 14 Jan 2025 02:43:36 GMT  
		Size: 16.4 KB (16433 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e13b802a0d9ce9d96b00844c8bbd6bc8b5444495671220903ca079efedad1ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.8 MB (251773902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa9417f77714d33a23f62223dbeb044a95d7f0c067a13fa5aec81d7a147d918`
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
	-	`sha256:35e780c45b36bd873816073e4e93fe81cb349e604ae86992d9131497c0598ea2`  
		Last Modified: Tue, 14 Jan 2025 12:22:08 GMT  
		Size: 142.4 MB (142389012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddcc0dbeb8500cac6f88265f56ec5d1b3842290c3c92b1d9e96d804a17829c7`  
		Last Modified: Tue, 14 Jan 2025 12:22:08 GMT  
		Size: 52.6 MB (52624655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c4fa7d6e29d335dba13e16450039ddc0162db3c7eca7ca09c8d90cea0268a2`  
		Last Modified: Tue, 14 Jan 2025 12:22:06 GMT  
		Size: 4.5 MB (4514143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1e94daf0e4c841ee9fb1bfed653ed97e71436ab35b6be1e54f5d164640e84f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6644bea7e37bda54bab7dab25253df1e012380f659159179dd9715ed2f14e663`

```dockerfile
```

-	Layers:
	-	`sha256:bd98de709b8baca9c0797db8d057d757599f542c08e9f817af9a3ad09c7c3a98`  
		Last Modified: Tue, 14 Jan 2025 12:22:05 GMT  
		Size: 6.6 MB (6645546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed4a91b1734375da3e6b2818fc005bb5b1b5d19865fdb9bdef1a307d0c2eee17`  
		Last Modified: Tue, 14 Jan 2025 12:22:05 GMT  
		Size: 16.6 KB (16554 bytes)  
		MIME: application/vnd.in-toto+json
