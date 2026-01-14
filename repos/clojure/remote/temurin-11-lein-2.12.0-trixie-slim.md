## `clojure:temurin-11-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:2a1396d6d4413e944392ec9f94b89c02b78fc18c8b80244a298269e958d701c6
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
$ docker pull clojure@sha256:a0cc581f56967012fdf061eb021eaec9fe988534eb3bca3e152111a32d2e631c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195705253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06149fa7d8016e5442c0434945b63846d50ff3c5c007cd4250bf06dc7c8acafa`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:25:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:25:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:25:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:25:48 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:25:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:25:48 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:26:05 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:26:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:26:05 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:26:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:26:06 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7370f67f51117d25cec6d70cc7143cd651679c1f70aa1fcb9d8e218d9103d50`  
		Last Modified: Wed, 14 Jan 2026 11:25:38 GMT  
		Size: 145.0 MB (144966600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a78c50abf8c43a3c569cc5413c190034fdcf4bebcf779305a415d6b13ab151a`  
		Last Modified: Tue, 13 Jan 2026 03:26:34 GMT  
		Size: 16.4 MB (16447234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873e5704cafc02df5f5692684760ad7a3c0f6c8396e21c94059b63daf97e5e98`  
		Last Modified: Tue, 13 Jan 2026 03:26:32 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f062bee42e9d0754f5b7c3e88fbf916dd24b377604314d07d19be56a4aef83c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71055ce0674c53f328172262e5005ee8f7dceef3c8306c5b906bee4cedb98559`

```dockerfile
```

-	Layers:
	-	`sha256:653a09b44f8a07dccacb46a013f648ce13334ce9bdd050cbc4adeee070aa3f69`  
		Last Modified: Tue, 13 Jan 2026 07:38:26 GMT  
		Size: 2.4 MB (2383639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a03ebc89470fbf60a55fccc8306f79b6870a1c517b6aaa62e9bd2ec797c5677b`  
		Last Modified: Tue, 13 Jan 2026 07:38:26 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c018a1acac082a9069953a0c7e2432a0dab843adeca6f5c0bdd3d9c65695b4bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192797280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b0d35888549cdb7e678544e9800ecaedc52a275e0be5da0f014708ff54fda70`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:30:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:30:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:30:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:30:47 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:30:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:30:47 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:31:04 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:31:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:31:04 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:31:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:31:05 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9d0c086f1caa4638e2672941b0aa2ab7cc341ecfb2687aafd89d4031383569`  
		Last Modified: Wed, 14 Jan 2026 11:26:14 GMT  
		Size: 141.7 MB (141731577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a95f33a0d7fb02ee5b4d421b3292af4ca5dcaa32ba38d187f380f47edde517c`  
		Last Modified: Tue, 13 Jan 2026 03:31:34 GMT  
		Size: 16.4 MB (16413925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694588ae33484079ddc8c00296e8c20543dc8b03e34ee2526ea956a117711a60`  
		Last Modified: Tue, 13 Jan 2026 03:31:32 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:943d5db6513def2181a600eaff7dd10756069e22afa4cf96a8e96f24fc6cf2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c3fbedf20ca24ae50992dcdb3898e911a2efea24b12ca877c4c6b512b10ee7`

```dockerfile
```

-	Layers:
	-	`sha256:bd01c7b7e0c316803d5582cbd48fdcc409d27025aacde5f4acfd72d2601f3805`  
		Last Modified: Tue, 13 Jan 2026 07:38:30 GMT  
		Size: 2.4 MB (2383875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69fbba1fa618fa6ed8f4e37e11a08d65e91f2010787dd46015969978df6e5875`  
		Last Modified: Tue, 13 Jan 2026 07:38:31 GMT  
		Size: 16.5 KB (16515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e4e2de85aa11304f5f72adf2e3f58f84de488b25d192114694d6b93fb70982ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186680823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2879cfbecad4838ca20003af02643ee5688e06ebc65364284cbd65eed9b404`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 05:38:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 05:38:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 05:38:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:38:08 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 05:38:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 05:38:09 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 05:39:01 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 05:39:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 05:39:01 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 05:39:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 05:39:05 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e67d402cdd431289d747055012c60263964e508ffd51c9c226729bf26f2231`  
		Last Modified: Tue, 13 Jan 2026 05:47:27 GMT  
		Size: 132.1 MB (132081973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a76897fe6ea4681cddf15d014770e2be773bc50f86818096c9a295cdbf1bbe`  
		Last Modified: Tue, 13 Jan 2026 05:40:00 GMT  
		Size: 16.5 MB (16485457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d411a547a509b4d52fc6dd8767a3069684659b21c9d021a8f6527255c60724b7`  
		Last Modified: Tue, 13 Jan 2026 05:40:02 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:862d5b488573ce08b11e8141c4d8f7d6b5214bdc1fc9cb7c85a3275079bad7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f3d407722bcdfc87d6022c099d40fbad77ed55059fb1603c932e93c1da5e21`

```dockerfile
```

-	Layers:
	-	`sha256:8c1b432a61693b33d06f93f65d266c141450943478a3ab8665ca93e2454fe839`  
		Last Modified: Tue, 13 Jan 2026 07:38:35 GMT  
		Size: 2.4 MB (2384004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebe494eb200dfe6e4ed9e20e6a449ba3cc5c6a81ed5806ccee60e70095347b01`  
		Last Modified: Tue, 13 Jan 2026 07:38:36 GMT  
		Size: 16.4 KB (16438 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:eb09a530b2bf8f02645b0d9d0c476bdbc72ec6e9887a477acf436aa1bf1f11dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176528640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b450def418f39b2b1fe8d1f9e9b2b1d80a5492b19b76d985415415a9f2e084d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 15:36:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 15:36:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 15:36:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 15:36:37 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 15:36:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 15:36:37 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 15:36:50 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 15:36:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 15:36:50 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 15:36:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 15:36:52 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43a8cdde4ec741a5a298d924bab15f641b5de6c3d621d845ea2be1bf1c2ebfb`  
		Last Modified: Tue, 13 Jan 2026 15:37:40 GMT  
		Size: 125.7 MB (125694401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9cbd8e950c77abb5b4acfc164f0cd301ccf4f5931ba39b652180b56612d814`  
		Last Modified: Tue, 13 Jan 2026 15:37:28 GMT  
		Size: 16.5 MB (16483037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938b213731b00f4154ffbd4345ab1f8b00025d11ba4d9ffde8e262e794774e64`  
		Last Modified: Tue, 13 Jan 2026 15:37:24 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ced43cbed1bac46725d5ad7f2a2a04cc20dc856270477b937a11d3d84583bf80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2396464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e44c776db98f85a9106bf6de27217357927f447015adae457ac66cb78db309`

```dockerfile
```

-	Layers:
	-	`sha256:e089d6e363ccaece189fe1c10fe5fc75db0173f64a242ee43eb224f1f0ff87d5`  
		Last Modified: Tue, 13 Jan 2026 16:34:58 GMT  
		Size: 2.4 MB (2380070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2976527fa05d6304b88120188928584c334b1b5b34e8dc828fd057ec69aa49b4`  
		Last Modified: Tue, 13 Jan 2026 16:34:59 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json
