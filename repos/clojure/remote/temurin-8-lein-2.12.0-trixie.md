## `clojure:temurin-8-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:7f9976bf9ea87f9d59464e9baed124a91665ea03d6ebbb5bd9f1a7f14cfa8909
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
$ docker pull clojure@sha256:feb0d86ed332f8181f79034aeaf3a740e2b1aea4c3d7168aba225bc2fb7957d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127107004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fb7c263772308ffca866d47f7ee0d59eb55d10bb5cf3242c7f51917045a918`
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
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb98cc33af6804c0763d94d10c7892aad09435d2e043d63c8c0f53ebddb7139`  
		Last Modified: Sat, 13 Sep 2025 00:03:50 GMT  
		Size: 54.7 MB (54731353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230eac1d55fe75d78e3518948a9c7e16e4da3157ca5d9e3bcd445c9b0032e20`  
		Last Modified: Sat, 13 Sep 2025 00:03:44 GMT  
		Size: 18.6 MB (18578383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ca1024ad99eb83c52bbfc7ee5a66ad8fd17b4d41d768c7bf6ef4c932392e5b`  
		Last Modified: Sat, 13 Sep 2025 00:03:43 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2cd0ce9a59137584db7e6be7ab51a5edc46005dc84108554474617e2d0d1a9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc76d1074ddfd5874c9f17d98909e207273e47375aaad06fbc76d2a962653b45`

```dockerfile
```

-	Layers:
	-	`sha256:a57a4291a3e1c99694688b275026d4879e7ef5c59cf38a33f2d9348eb50cface`  
		Last Modified: Sat, 13 Sep 2025 00:44:53 GMT  
		Size: 3.9 MB (3934942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3739137876db585bbd8a98e7013049f2532002f3bb8ffbb6a305903c19876a67`  
		Last Modified: Sat, 13 Sep 2025 00:44:54 GMT  
		Size: 16.4 KB (16395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5392ea6a4badbf01c2bffa8655ac5be970e86f357e6f718ee333d9c7ce464ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126536333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68fd5626d48c3fc3af42cc4b7d1acf920b82ffe42072d39618d49b11a5f90cea`
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
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632bb6a2eb73a17964ddeadb9ed8f5cb4a52dbbe4daeaeffc94a9be4d39fbb99`  
		Last Modified: Sat, 13 Sep 2025 00:14:44 GMT  
		Size: 53.8 MB (53835605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36da3d52038890c7b2806ea6b39a72341bcb73c952b1a79e06ac42b17e42be9`  
		Last Modified: Sat, 13 Sep 2025 00:14:36 GMT  
		Size: 18.5 MB (18539196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c88149bfebe65193b3e674c7828565f024817bc87079eed732b763df797a583`  
		Last Modified: Sat, 13 Sep 2025 00:14:36 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8070cabdbe5b2ef0417ffecb9cc583a2a7efae73b43b09366cb02e3c12ee3bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1770d27e61e617d277de33363c3de0391fc6df1786bd75fb33a83726ac348d9`

```dockerfile
```

-	Layers:
	-	`sha256:7b4a2fd24645bc7291292c9cf549093ea8c8512e63e66aa1cd7d1d77395ba974`  
		Last Modified: Sat, 13 Sep 2025 03:42:20 GMT  
		Size: 3.9 MB (3936517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:369fbef58e1103e3648e90ef3b61c34b6b7b1f9f0fb911fd91c6df3084fbb26a`  
		Last Modified: Sat, 13 Sep 2025 03:42:21 GMT  
		Size: 16.5 KB (16515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:9905cca49b1891d0d7df796d977deebc8abe588e378220f863e29ab4ecc48352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128423604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5279db0f7204b79a013a28698c9c1aeb99dcdf5beb6e7ad43365efaf125923ce`
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
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffc46708712e2739dd223f5a5084a3758b7e54dc9a68ef7ee76603b0b823ed7`  
		Last Modified: Fri, 12 Sep 2025 23:49:00 GMT  
		Size: 52.2 MB (52165393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a472792104da6be62314adf41a6a5238a217358585e5dc07a7223784c7262aef`  
		Last Modified: Sat, 13 Sep 2025 03:24:33 GMT  
		Size: 18.6 MB (18636037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89dacb6a5f4a0802a2df295ee50afe9f64c8e9c5ac78239e7651972d5861856`  
		Last Modified: Sat, 13 Sep 2025 03:24:32 GMT  
		Size: 4.5 MB (4517709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e00caf408cbac4a858aecc719a17600b65f6fa1366c47ecea481f756b7a8739e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4759e2d2072d50a90e7571e9a2d8c4584511706d538d5d42586918988329425d`

```dockerfile
```

-	Layers:
	-	`sha256:7320da72ecee3499937f0476a505f215050a0d7bd700f89acabbd251876adaa7`  
		Last Modified: Sat, 13 Sep 2025 06:41:30 GMT  
		Size: 3.9 MB (3936533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:778675cd4fd28ac831f6543774895859bc0568304eebbdbf8da2bf04c3c8e1b9`  
		Last Modified: Sat, 13 Sep 2025 06:41:30 GMT  
		Size: 16.4 KB (16439 bytes)  
		MIME: application/vnd.in-toto+json
