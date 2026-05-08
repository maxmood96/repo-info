## `clojure:temurin-17-lein-bullseye`

```console
$ docker pull clojure@sha256:762024b8580ad59b2c5afb15d14e347a668414073cd39eda6f0b4fbea57a2399
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:cc64eda243131401d89455d78dd198eb0a905afc45417938a653e2404172b51f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220816378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0c31ef832d60a425e3bc6302dab3cee6292b3b80f9ea77b1187e48f99ca15d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:07:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:07:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:07:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:07:10 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:07:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:07:10 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:07:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:07:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:07:23 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:07:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:07:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:07:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:07:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25fa090e5a723ad048576c600a747a1cfe745579ec63d396530f5434f877bc`  
		Last Modified: Fri, 08 May 2026 00:07:44 GMT  
		Size: 145.9 MB (145905487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce456285a12f7e19e37b4e2bc8e89b61d3599adec8d56027c66e98ef6cc980f7`  
		Last Modified: Fri, 08 May 2026 00:07:42 GMT  
		Size: 16.6 MB (16629550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e2856b60491bb38af058c924317414df0effafaefc9dbc82a918df0ebdcb31`  
		Last Modified: Fri, 08 May 2026 00:07:41 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af765273e270c759ae74bfd87e36e567fcaf4f69895dd5b3f630940551326aa2`  
		Last Modified: Fri, 08 May 2026 00:07:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:70f74d4a77a1799c4350d0614055b620af7c4e3f4640d52ffe8b3f9fcf7295a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4505010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec3ef3098e105323c44d5b7b0b60daa745e351252b98fd265e0b89e273e3c58`

```dockerfile
```

-	Layers:
	-	`sha256:4d82dfc02d81a360e61d22c0cd0ec5a7aaaa93d9c66cdaeb2e24e81dea6d2429`  
		Last Modified: Fri, 08 May 2026 00:07:41 GMT  
		Size: 4.5 MB (4486489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4e7b0e2c1bd05beaefd5c8a8d76021ed146c1d99d0137b3e4f7484f115b0e98`  
		Last Modified: Fri, 08 May 2026 00:07:41 GMT  
		Size: 18.5 KB (18521 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:24d77d6b45c3f5f6cc8416edef98cf03181d4633ca7fd59b8505e7ae8a64ccca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218111998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182ff733d34138683d140f590d4cb4bdff485d8519ca48f2484aba3f4493ad00`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:08:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:08:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:08:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:08:51 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:08:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:08:51 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:09:04 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:09:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:09:04 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:09:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:09:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:09:06 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:09:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650531e3648ee40ea90212a9e49051657d86424f2fde32afb4a93a01e87c0c56`  
		Last Modified: Fri, 08 May 2026 00:09:26 GMT  
		Size: 144.7 MB (144724305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a563be23f7222a05170a04a7e215f48fbbbc8e3643c542782e5bc1143955a31`  
		Last Modified: Fri, 08 May 2026 00:09:23 GMT  
		Size: 16.6 MB (16616505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431fe8e53ec46d054fcb8fe2d060a92569bfc3d6509308eedcafd080d7aa6f55`  
		Last Modified: Fri, 08 May 2026 00:09:23 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5093d1bfafb4783416749b1babc65ee6dce74dd789bcafb722bbe56856768e0`  
		Last Modified: Fri, 08 May 2026 00:09:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ea4139824558805b0a7fa4826e453208b39cf56d385cdf210f421ef8c7ffa8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4504106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1317967c0c6dbf86ea0ae50dc64b54622d9f62015577e07457869407dcc6c9`

```dockerfile
```

-	Layers:
	-	`sha256:7e872a4ec266808abba70850ea68f3e8b87835b0f63e7dc8c7120d3b29cccb79`  
		Last Modified: Fri, 08 May 2026 00:09:23 GMT  
		Size: 4.5 MB (4485463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efee80f4cb258769ac792ced30856dc3be26de345fc31a2129f98c6fb23feb59`  
		Last Modified: Fri, 08 May 2026 00:09:23 GMT  
		Size: 18.6 KB (18643 bytes)  
		MIME: application/vnd.in-toto+json
