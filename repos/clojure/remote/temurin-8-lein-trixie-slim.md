## `clojure:temurin-8-lein-trixie-slim`

```console
$ docker pull clojure@sha256:88ddd32e2ca586330499e7cfdd794bc959b3d8dfebabbf21ff7b43958eeedf72
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
$ docker pull clojure@sha256:a546ace81f37dcf50427a9a28a2e661084f6dbe0e9893ffc32e668c2f58f2b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105911570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0d5ee11e2c1acd711716b39bb5c498f76ecaa24d251c05cd45e234a390500b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:12:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:12:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:12:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:12:40 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:12:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:12:40 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:12:56 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:12:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:12:56 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:12:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:12:58 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a6e59470f04d832c5a947630e75d733730bfaf63836a68556cb78c1936d9f9`  
		Last Modified: Tue, 07 Apr 2026 03:13:11 GMT  
		Size: 55.2 MB (55170118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08150a242bb4d83244195e6a126eae19131c26f1356650caca00d45427d85b5d`  
		Last Modified: Tue, 07 Apr 2026 03:13:10 GMT  
		Size: 16.4 MB (16448022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f83a40c65fe426320b5796c488fb4db52934f38d01f76beb0df917db1b150ca`  
		Last Modified: Tue, 07 Apr 2026 03:13:10 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7439cf7eed5224c89a4c74d887f281a77e3d7d7520fc03cc5b625f337c34176b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66eafb4297faf1873a2f9106878ddaf8c32530581a6c4da2ee6951213407883a`

```dockerfile
```

-	Layers:
	-	`sha256:8b2088ac6ac0cff7347e2ae3d9602878d255473602115690e7a658f769534265`  
		Last Modified: Tue, 07 Apr 2026 03:13:09 GMT  
		Size: 2.5 MB (2485777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25c03e6cecd5d32f5a7cd9864c51b4ed5205327501b8e6891ce80a1493266b09`  
		Last Modified: Tue, 07 Apr 2026 03:13:09 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ad16c1f2b7c45ef6de1bad9b33644759af721c7a1dc869a24301fae781a5302e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105321953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470ed6a35ff12afdf7b9b4976697b6fe933028af50a357e05d69fd0c6f270cfc`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:23:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:23:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:23:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:23:33 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:23:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:23:33 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:23:49 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:23:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:23:49 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:23:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:23:51 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7a39f6059ad01ad7388b97679d70af6e9aae3e00491d074be2ed0c2ecaf390`  
		Last Modified: Tue, 07 Apr 2026 03:24:05 GMT  
		Size: 54.3 MB (54251622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026cefc7f7a8e722322dc8941a8eaaee5536d6a8cfc240cd6b86a6bbdf550477`  
		Last Modified: Tue, 07 Apr 2026 03:24:04 GMT  
		Size: 16.4 MB (16414016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965a0ba64d747e88f2471ecf00e54ab00d25e77a7c9e859679971a6ba2611ccc`  
		Last Modified: Tue, 07 Apr 2026 03:24:03 GMT  
		Size: 4.5 MB (4517732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dd2927fbe223c654d373c2352e97427b9142ec82a840237d86de7893bc649dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d8e4e7e07cf174958dfd219eafc17bcc157099c7932ab2e884a9b21ae38337`

```dockerfile
```

-	Layers:
	-	`sha256:be7788b33b77465038c46e5ffbde7d6701daff392b22681575dd201a0498f6f0`  
		Last Modified: Tue, 07 Apr 2026 03:24:03 GMT  
		Size: 2.5 MB (2486095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58380456392146fe944b8b5ac87ccdf2e3943854e88ff4064e91efd029e4af57`  
		Last Modified: Tue, 07 Apr 2026 03:24:03 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b7d1d76364a00dd7e60989427f0b8d859269ca103e7a7f1cd3da3a3a4936e313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107246530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c18aed980d710d648ce03cae649300bd7f79345519f9d55e03cb62a4734c299`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:08:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:08:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:08:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:08:40 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 18:08:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 18:08:41 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:09:29 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:09:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:09:29 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:09:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:09:34 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf4e66022f0a54019718e5fb82aff975c8ae1279a587e803dd7d8da942e46b2`  
		Last Modified: Tue, 17 Mar 2026 18:10:01 GMT  
		Size: 52.7 MB (52650377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ccceb106778461836d6f6c1403b2b9e6392061f8129ba94413024d07f8bd6`  
		Last Modified: Tue, 17 Mar 2026 18:09:59 GMT  
		Size: 16.5 MB (16485519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f3468d5ce70ec6d043ac11ef0e252a6d9aec46f8ff067bf292c694ce3aa29c`  
		Last Modified: Tue, 17 Mar 2026 18:09:59 GMT  
		Size: 4.5 MB (4517768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b8b593e56ac3ccb246bbe50030fdc4c04a29234ffb3d6c6e1c7e273edb969622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ebcf17e935688a3b2551c7672dc19f34445495c70fa5d65e0518e8d448f232`

```dockerfile
```

-	Layers:
	-	`sha256:dd48717eba321128ff91055e682ca0d4ff3474a27e48a191c843002ee8c4bf66`  
		Last Modified: Tue, 17 Mar 2026 18:09:59 GMT  
		Size: 2.5 MB (2487352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cae03f0fe29102eea80381b213b151cbf35eadbd4e43d7476058bd88fe87978`  
		Last Modified: Tue, 17 Mar 2026 18:09:58 GMT  
		Size: 16.4 KB (16426 bytes)  
		MIME: application/vnd.in-toto+json
