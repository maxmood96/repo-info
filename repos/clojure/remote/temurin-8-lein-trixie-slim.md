## `clojure:temurin-8-lein-trixie-slim`

```console
$ docker pull clojure@sha256:70489546346e879ffb5aefcf51349012bec20c8fcfe565c186268f79ad721b63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b8ec7349869adfaab2ed0eac9cf6bc643baa49af98059ebe360b6980444f4d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105469940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9aa94a85bb624a943652ae694324604b6ad31998e26e4d47e768a287a79ba0e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69b2774a080c472777c47ff168f7a37f5fcbf754fd7c2cbfe7286e6f5c80d78`  
		Last Modified: Sat, 13 Sep 2025 00:03:52 GMT  
		Size: 54.7 MB (54731285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9c3f1bc89875af7e64def21c72459d72094ed8435197cc7622d114be85e6cc`  
		Last Modified: Sat, 13 Sep 2025 00:03:44 GMT  
		Size: 16.4 MB (16447368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdcd626f4fd51ba7c741e0012f5a09c2e2d3e9146483891f248d580c994ac25`  
		Last Modified: Sat, 13 Sep 2025 00:03:43 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d289c702da7d77af79806b38112c20225f74f34a630e8aa89907bec152c3a536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde9993c41a6e631fbc1f2041cd195e53ffe34bfafb65995d7b73d04c15bdbbd`

```dockerfile
```

-	Layers:
	-	`sha256:53b022d9cd277ad85746e39426cb0179d7cb06a914692df798e0a94af43768c1`  
		Last Modified: Sat, 13 Sep 2025 00:45:02 GMT  
		Size: 2.5 MB (2485000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8a04ba5264e5c41f7bbde1e2a468aaf652d3ac7da40ad70feb1e8cf584d1d05`  
		Last Modified: Sat, 13 Sep 2025 00:45:03 GMT  
		Size: 16.4 KB (16425 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c093183f040a7f6906e9a3ca095099f9ead4da61bccb67e3aa39a0c4e7bc3a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104903543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612130e7bf28bb357618f99d8ad37b267765442a1d0538e052bee2d2d809c83d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181a3570bc4b6aa9d3073920a72c002ae12f14978f22b5e7fe60a9c3e13a9347`  
		Last Modified: Sat, 13 Sep 2025 00:14:41 GMT  
		Size: 53.8 MB (53835607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d5911ec170a552fac2e47efe7d30aafb0a4b793d1b4134f65b4860d6269781`  
		Last Modified: Sat, 13 Sep 2025 00:14:36 GMT  
		Size: 16.4 MB (16413567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85644cc5dff58c767a92074a60891dbc284304cc2536a5f6be1483113dc93661`  
		Last Modified: Sat, 13 Sep 2025 00:14:35 GMT  
		Size: 4.5 MB (4517706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:71e748cde239c7e7ed583d34b97c688acf33c844809fd1bc57aa241eaf5021e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6b2c7c0eb6bcbb03214687c54e290adb8b5ccdbc2818b1c8c71f6dee58d9ba`

```dockerfile
```

-	Layers:
	-	`sha256:7a7b8066cff3b5f3c66ff46cb0865deb10934a317813e6feccc879c5f4642b57`  
		Last Modified: Sat, 13 Sep 2025 03:42:24 GMT  
		Size: 2.5 MB (2485316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfff46da4731e95daa781e88f1a40dd28bcf6472b183e80390f4ee1dba65e9ca`  
		Last Modified: Sat, 13 Sep 2025 03:42:25 GMT  
		Size: 16.5 KB (16546 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c76c8f1688e6aeecd9b52edd3fdff8dc9690ea298c0a94637661fa558024e898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106763891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd09af1b39623dbf287b1bc94cfe54a8be23442f1e9bf0fb86fb95d0606ee68`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9594a17f6d492bd2de8476aeede85d31ea493e730654abd0387d1bd172577f`  
		Last Modified: Fri, 12 Sep 2025 23:50:56 GMT  
		Size: 52.2 MB (52165369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453289b5257a7307c076ee20cb1dd1c418d0a15ea492f4a81e24dcf5153e0057`  
		Last Modified: Sat, 13 Sep 2025 03:25:41 GMT  
		Size: 16.5 MB (16486410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc16a334111b39ddb67f19218d2e4c328340cd779a6200bfa1edbced38c68dc4`  
		Last Modified: Sat, 13 Sep 2025 03:25:40 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2d4a9f37f0be4d2bc8da0fe29962847d18d0fdb1caa3b6d29c31f6778f80a746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32b1a1f31ce169d36b5b12da6c849a72af5e15bff1035e278d99b5d2970c5cb`

```dockerfile
```

-	Layers:
	-	`sha256:2d7e3e992f8adcbea1c24eebdd7339e5a890c98dedf1b434853863781a41212f`  
		Last Modified: Sat, 13 Sep 2025 06:41:29 GMT  
		Size: 2.5 MB (2486573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75399d5329d698bcaa584853bb4fab5a5642fe7f2135120f5d8c1ae245f9c925`  
		Last Modified: Sat, 13 Sep 2025 06:41:30 GMT  
		Size: 16.5 KB (16468 bytes)  
		MIME: application/vnd.in-toto+json
