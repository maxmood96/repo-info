## `clojure:temurin-11-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:2a2f99bd7933efe52482c9d35278128bd630e330c2cc0ecfdcaf152036a71931
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

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:eaaeecc650f62d2817018249ac7b5eef268ddee0cf3f56dbf53d4c52b478cfd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195708103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4a78533794e4ef7d2f485d7481f82ddc7ab89f017801c923c44b4b7f2c147b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:55:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:55:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:55:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:55:15 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 00:55:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:55:15 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:55:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 00:55:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 00:55:32 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 00:55:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 00:55:33 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e322c43c95531fcf58008dd1b162b446869a807a77ede69728bb565029d0269`  
		Last Modified: Tue, 30 Dec 2025 00:56:20 GMT  
		Size: 145.0 MB (144966652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bc4dc2f8fd52cdbf2d5c0ab44771cdfab152abf3bba0051b7391dc38da9515`  
		Last Modified: Tue, 30 Dec 2025 00:56:00 GMT  
		Size: 16.4 MB (16447169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d131ee9eae19a04879fedbf759050ed28d27d731020022aa36c4afd28e10526`  
		Last Modified: Tue, 30 Dec 2025 00:55:59 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ef8bababf1d30f1084e456eb9dabaec596c0708b8fb12b74559f0445f29863d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a099f5f156706f2d230aa32b3cf6a2554ad5379639dc4380f511da663e536da`

```dockerfile
```

-	Layers:
	-	`sha256:6caf23b5381048805c32d369f11a3ad12f7f1deb65796a98c7e5ac2bcbddef8b`  
		Last Modified: Tue, 30 Dec 2025 04:37:56 GMT  
		Size: 2.4 MB (2383577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:657eb1ba2662f6464183328c445a432a278a9bb0e22325d771893134259f0bb2`  
		Last Modified: Tue, 30 Dec 2025 04:37:56 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:336e8be2a2775c4a4035827cd5ad2b120804c15d694081cc54a5834e602d57e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192801836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dee1ef9417b2b83d7fe1defcade1a37c0830b03d3b00d9aeb4bb27f36e9a5bb`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:56:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:56:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:56:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:56:35 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 00:56:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:56:35 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:56:51 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 00:56:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 00:56:51 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 00:56:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 00:56:53 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fb26c3fd4471bd4bbb27e524bd96bb89890333d14ed5f022d507b47550ce7b`  
		Last Modified: Tue, 30 Dec 2025 00:57:25 GMT  
		Size: 141.7 MB (141731574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba27fe04a390605dc98c84e2dee2fb45d3c02a4f1eb9b22808ec5a6504e24f0d`  
		Last Modified: Tue, 30 Dec 2025 00:57:18 GMT  
		Size: 16.4 MB (16413840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4720d00ff97d3d9979f7058bdf7201f3dc91b94355479565d490735de4b71da5`  
		Last Modified: Tue, 30 Dec 2025 00:57:17 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1a6baf47538389c4854a231d2e947655e9f927729ab21d2cc1a976a1b3553f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b1b4713d5796ddfd67adbe4c699410ce0797ef49cfff7966735e9f78c6f8e6`

```dockerfile
```

-	Layers:
	-	`sha256:edcbe2f9c9871c139572bdbcb60744001431fc0e76d596ca4bc776bc59b98981`  
		Last Modified: Tue, 30 Dec 2025 04:38:00 GMT  
		Size: 2.4 MB (2383813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f76d4244803930aed3bd30f951634aed10966c0e45e1f7865d2bffad65ae78f5`  
		Last Modified: Tue, 30 Dec 2025 04:38:01 GMT  
		Size: 16.5 KB (16515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f7fa8fa61d71f995031613ba69584e1e3634dcf34abc0ea94926b65574160621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186681941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b831bb646fa35c87b54cfbe6d4a8b97070df16c734330607075cc7a4f99826`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 19:07:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 19:07:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 19:07:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 19:07:54 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 19:07:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 19:07:55 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 19:08:41 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 19:08:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 19:08:41 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 19:08:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 19:08:44 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cf28f764c2e28a5292338b5c0ca4db8c991fe900f886b5b721adc6ce62ec4b`  
		Last Modified: Tue, 30 Dec 2025 19:09:47 GMT  
		Size: 132.1 MB (132081972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76aa3ff84f430e77f6ac8235cd204257e32ed8afc5fde32affbff262b1d5a3fb`  
		Last Modified: Tue, 30 Dec 2025 19:09:31 GMT  
		Size: 16.5 MB (16485291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3321dda51f06ae49c66f9a17ca877e197f45626c81fc6d758b6374e04420e5`  
		Last Modified: Tue, 30 Dec 2025 19:09:30 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c89894968c9e60a5671463730f4f8175c840e5498e79ad029974966f2454cd67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07781120af215a2e055c9c30ea8e3866fedf90e091f4c87e97a75dfb40b9d534`

```dockerfile
```

-	Layers:
	-	`sha256:543bfd942f9a2ffdfc2d4c5df888d258c225a2c2d3111e45e543d6a441059784`  
		Last Modified: Tue, 30 Dec 2025 22:34:53 GMT  
		Size: 2.4 MB (2383942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:452861fc10cacbceb7736cdaed231a885e8de693017d9bc6178bfef1f1516baf`  
		Last Modified: Tue, 30 Dec 2025 22:34:54 GMT  
		Size: 16.4 KB (16438 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:607f0cef3996b4442cfc2e2e1595f07a38a35e49c2581b03777dda6d8b2be07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176529586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d39034075f439025da8af3dd433640ce2d5cb349a65b41e82cd5687841a884`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 02:00:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 02:00:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 02:00:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:00:48 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 02:00:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 02:00:48 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 02:01:25 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 02:01:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 02:01:25 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 02:01:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 02:01:27 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2229b218e921c120f98aba19421a93b00de9976ceb5c36fb717d0f777015f1e5`  
		Last Modified: Tue, 30 Dec 2025 02:01:48 GMT  
		Size: 125.7 MB (125694401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f09729e51d36c826785fa803eb2618c8f8e3b42037b55445229927d6b739d6`  
		Last Modified: Tue, 30 Dec 2025 02:01:53 GMT  
		Size: 16.5 MB (16482979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cd2c37af3df08854e83f4145d0ae8b08929632ce2d1a826b5c13356df755ff`  
		Last Modified: Tue, 30 Dec 2025 02:01:53 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:415155a8312e8bf5b250b6ed9bb43aeb4f432dbfd8223e348cca5f6e1050c3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2396401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5d202160b03732f65a8cdb93364f33ab94f790e7e19feb3457e623e1b11e6c`

```dockerfile
```

-	Layers:
	-	`sha256:718e5a7f568a6c0d7aba189872b17709e2434ad768bfadc51c0ec0c70d260634`  
		Last Modified: Tue, 30 Dec 2025 04:38:07 GMT  
		Size: 2.4 MB (2380008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e291a5298a9d71095519e84c3d3f29fa10929cd7508d0ef797297f1bc674bef`  
		Last Modified: Tue, 30 Dec 2025 04:38:08 GMT  
		Size: 16.4 KB (16393 bytes)  
		MIME: application/vnd.in-toto+json
