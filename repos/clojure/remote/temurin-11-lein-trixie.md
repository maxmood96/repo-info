## `clojure:temurin-11-lein-trixie`

```console
$ docker pull clojure@sha256:2f7798dc9e19ac3979d4b7c47da9375f2a80435d5ccc12c7f9bc05577e5d0e8f
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

### `clojure:temurin-11-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:0ed2b2c4bfe82aec6fa04f7ead8826136a8138dad2b9ebf305e89730d4dc16ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218207692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4908d8c22e29300b203728d4c34873e34f6bcccae63325ba2bd66698679b91e8`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:13:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:13:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:13:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:13:43 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:13:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:13:43 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:14:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:14:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:14:00 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:14:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:14:02 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9890a771c5b9d46c162af92bb87fdc994ad73fe6604b39383649855a6d1abfe7`  
		Last Modified: Tue, 07 Apr 2026 03:14:23 GMT  
		Size: 145.8 MB (145806914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c0d9df9030d22c7de4b384cca31e4d7a5c31a48a843b095cc304c872645b5b`  
		Last Modified: Tue, 07 Apr 2026 03:14:20 GMT  
		Size: 18.6 MB (18585171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d968ea6f09c54d3f4910c50d7d1055f65b2c102baef542989dcf2888c246079d`  
		Last Modified: Tue, 07 Apr 2026 03:14:20 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c52643e8761307132ead4c5a82ca7c71db1a26ce3ddac57b9280b9abc4a72909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62aa6b03cdbea4d5abf933066b2a5674db481844bfb0079d10913c18e3da4af9`

```dockerfile
```

-	Layers:
	-	`sha256:f0425f341c8247419e3cfb70c44313b3a85e48dd4c3c8f929c4afea467c51869`  
		Last Modified: Tue, 07 Apr 2026 03:14:19 GMT  
		Size: 3.8 MB (3835668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1546aa476b08b9f769220a0bd7e649592428b421aa4f0d8570eed292a55bb95`  
		Last Modified: Tue, 07 Apr 2026 03:14:19 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:895ce8ed7dbb54328be325163bb91d30e9a05d3494e5bb2e7351732ec20f75dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.2 MB (215227922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7dac9cc89db066954c3bff12ad0b064bd1718d217aebc49691bd331029690a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:24:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:24:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:24:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:24:18 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:24:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:24:18 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:24:36 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:24:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:24:36 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:24:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:24:37 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8657c16689b77fcb3dfebfa08bb214b5869ca0f587c0338919f27cfe4695e03`  
		Last Modified: Tue, 07 Apr 2026 03:24:58 GMT  
		Size: 142.5 MB (142500072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f685a8ff1c1e9e9280e4e6d11fe411e7ce6310dcab34fc4a4de480573ed246b7`  
		Last Modified: Tue, 07 Apr 2026 03:24:55 GMT  
		Size: 18.5 MB (18544844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921ce0168b8f1a7c50a73c335b3de9048fc51837b14b16bf64c1607b06fc65dd`  
		Last Modified: Tue, 07 Apr 2026 03:24:55 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:dfc6a7d99e03ee7d114799a3e3bf5154929c4357adadd015c762a4702c00b57a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43885a45a1930fd2d6e1db4fc9dde8b89e62047bd151c194de3f7e4b6b3c708`

```dockerfile
```

-	Layers:
	-	`sha256:80eb5e1f39366a9beda2b364acdc422d9b34975d6a6ef58c29575c1fd4fb13b3`  
		Last Modified: Tue, 07 Apr 2026 03:24:55 GMT  
		Size: 3.8 MB (3837163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5750314d050e948c1e81f101c985372c493b5b44b8ab8187dabc483aeb561481`  
		Last Modified: Tue, 07 Apr 2026 03:24:54 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:757cd36361d2c3d5d4df2ba8e521b518d291811bd43023349e5260171c21d852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.3 MB (209273604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96881bcf20a7a0e705923d1e5831f7618f9320fff5761816b3762abd81c61780`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:18:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:18:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:18:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:18:16 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 18:18:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 18:18:17 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:19:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:19:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:19:00 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:19:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:19:03 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6d8bc187d9d77c2b576c45cef2edbe313dca76b0d35a49ca751f0587487fda`  
		Last Modified: Tue, 17 Mar 2026 18:19:41 GMT  
		Size: 133.0 MB (132996714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469540854766193946c18f2c8f8fb3e55cf7ea2498e13313d42fcc59d723e24a`  
		Last Modified: Tue, 17 Mar 2026 18:19:39 GMT  
		Size: 18.6 MB (18640751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0eeb579bed4d6732616d2bf1324013ab943133b6df2e48aa23a58774566aa1`  
		Last Modified: Tue, 17 Mar 2026 18:19:38 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2088236c24a4a1e00a5d86b84e9e3c735ec8c7958ca205145d493cbb23570488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd2aeec24da9b8fd320925d0a098e07cffaa558e9e18a7115b91417b088bcbe`

```dockerfile
```

-	Layers:
	-	`sha256:cb8001734befe192460ff075153c74d8892de5cc95b83d8779c7facaec8852ba`  
		Last Modified: Tue, 17 Mar 2026 18:19:38 GMT  
		Size: 3.8 MB (3836053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4f0c3fed76c62a7bfe21439c2d25c6e664d02099a96f44bfafecd92714f8b0`  
		Last Modified: Tue, 17 Mar 2026 18:19:38 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:2bf79a6426fb8a48368001be4c2975c62c71d432eb22396c9b188a7e54ff2f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199071386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1e1c7ea4a1bd9ceea47e27f33e186a26d49276bb9d89572623a6f9be48a699`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:39:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:39:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:39:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:39:58 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:39:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:39:58 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:40:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:40:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:40:14 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:40:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:40:15 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a0f6af54b41978b4b00c1cf75bd9972713058d469f37803b6fe31ba2949998`  
		Last Modified: Tue, 07 Apr 2026 05:40:42 GMT  
		Size: 126.6 MB (126562219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966b00b54f541f2b1cebc9021034d726555986d98deed7f7aaf9917bcd009da8`  
		Last Modified: Tue, 07 Apr 2026 05:40:40 GMT  
		Size: 18.6 MB (18626311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af2cd9c475236055f22fe658eabf0062b5932c10f93fdad2951640b0afd38e`  
		Last Modified: Tue, 07 Apr 2026 05:40:40 GMT  
		Size: 4.5 MB (4517720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:268d7bff08303b8124b1fa9f7834c5fcd9848d5e3f505852e9e9edcd11984e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3848463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fa2513d59243be2746dc2e7a351cabdf326975a997ecd630314452df8c25a3`

```dockerfile
```

-	Layers:
	-	`sha256:7c4b0935d9d5d9528f5c0e8d10588c7763c5b2173e44ac6f0372d9c1aebf0767`  
		Last Modified: Tue, 07 Apr 2026 05:40:40 GMT  
		Size: 3.8 MB (3832099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0ea262f96640e7345cd327979e8fb14e86ea40ac6594e5a6cac7c5cfecec9f0`  
		Last Modified: Tue, 07 Apr 2026 05:40:39 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json
