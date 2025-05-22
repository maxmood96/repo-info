## `clojure:temurin-21-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:40741214022247acfa3e9ae4d509651816bca19c96ec008db3250a4c28709428
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:71ca5789e989ab3fdbbcb215dd6665811dca0ddabb8ca792e13b95973b662d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235684817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1cb83c233cce1dbd6770f0b979cf3e6cfae2638fa5833d78875c0adc63e500`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8514c63c16694f915b06f9be4fe78291541a594c23459054be955a12f6e1d6`  
		Last Modified: Wed, 21 May 2025 23:33:17 GMT  
		Size: 157.6 MB (157634485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d6d141339bbdf82cf17d680e98ce14521d7531ecec12839588a61eba2bda19`  
		Last Modified: Wed, 21 May 2025 23:33:16 GMT  
		Size: 43.3 MB (43279765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291dd8f68610d7fa71f8eef6f59c7d7f78bc8304554f664abc221defff0bad19`  
		Last Modified: Wed, 21 May 2025 23:33:15 GMT  
		Size: 4.5 MB (4514199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd5bce1cf52f806aa1e07b564ff56dfdb59b7717ba883b89e07951ad5d55fb3`  
		Last Modified: Wed, 21 May 2025 23:33:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fe7067b00c80b168c68f4333b936855d7f2b3a51d7dc52e11f44e07c2a7370c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4638838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb51953d2d10d00e0c3e92f10b09419389ff30d11ff1bf738d17d3d481d1b00`

```dockerfile
```

-	Layers:
	-	`sha256:77809489cdb784e6c3e10102142c21f1cbd94a337c02221c9efe313f7df94085`  
		Last Modified: Wed, 21 May 2025 23:33:15 GMT  
		Size: 4.6 MB (4619718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6c4efd6e1895f0c5e6748058ebf098c37e59e064a03308c807889069f32d873`  
		Last Modified: Wed, 21 May 2025 23:33:15 GMT  
		Size: 19.1 KB (19120 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8e7e5fda778c9ec666fff22e4dbc68bc866ee6cf5c399fbd5dc3a9334fc096f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232502221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e17c3fe05752135058ca8527e90c74b61d139bd5badc017e5f2115afa388bc0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb91d4429e152a4ef12cdda1f1c22c8aa83ef90eec350facd6ba0b74134ad97f`  
		Last Modified: Wed, 30 Apr 2025 01:47:24 GMT  
		Size: 155.9 MB (155928805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5991ae6f75af6017bd57020f5a1bd421fe71aad9f473bbb3d1a68e98a4d6b8`  
		Last Modified: Wed, 30 Apr 2025 04:49:17 GMT  
		Size: 43.3 MB (43314202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406b99687a11d3065a3b7a407ce05d2fd6e6f7ebaabb3f7f1445c47dde60b644`  
		Last Modified: Wed, 30 Apr 2025 04:49:16 GMT  
		Size: 4.5 MB (4514140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefc80613e97d93c56311677a15af0897bb02b05ff6036d86e2375664214a1ad`  
		Last Modified: Wed, 30 Apr 2025 04:49:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:27694b99cad207738e17f94f25c963074e5d0f01ded98b5481406d2ab77ecb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4598886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a84cb895463c4421a609f1af30c9094b0a916922411e6caa0ea043a508d635`

```dockerfile
```

-	Layers:
	-	`sha256:41b38f06ecc6312d0a2435d9bab693c3678c428149616c49abe980482d1ea7c8`  
		Last Modified: Tue, 06 May 2025 00:41:57 GMT  
		Size: 4.6 MB (4579621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48cb41d30e0e3662440bd7c2badff70b0c0da52dc5fadb631a50aa8b765ead62`  
		Last Modified: Tue, 06 May 2025 00:41:57 GMT  
		Size: 19.3 KB (19265 bytes)  
		MIME: application/vnd.in-toto+json
