## `clojure:temurin-21-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:d2a1aa74689aefa0acd7dcd0ac378b0611fbfa4f0e6dcd5ae23dbbc283c69637
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f62f8e2886bab00e51f00aa33c9bd8897fae70160798a725d90e39468461423c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208281796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14443381ef44ad8d9396b06d6d340299c215b2cbc658ad09d9a12d8e00d7ebcb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:26:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:26:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:26:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:26:30 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:26:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:26:31 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:26:45 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:26:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:26:45 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:26:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:26:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:26:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:26:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ded9f5c74f9a4abc356e8bd87d40939324a0ec3c8d42f5df58639c1c39c307d`  
		Last Modified: Fri, 08 May 2026 00:27:09 GMT  
		Size: 158.2 MB (158166935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f643e3158826ee231905f05ab8d633a96882a37463cfaa4a935cf14d3deed37`  
		Last Modified: Fri, 08 May 2026 00:27:06 GMT  
		Size: 15.3 MB (15338783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc572e250852992afd6c64e27e872df6efb4e4c82c047582674d8b77bc3a882`  
		Last Modified: Fri, 08 May 2026 00:27:06 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b8c5f6a98918fa83b488b1fbe086e83cd8fd552e46f38c99062f4b274944c`  
		Last Modified: Fri, 08 May 2026 00:27:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c94eff2bb476b76623cc898ab166c54b5e04e9343895c6febb7df59d7509db9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3048618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e955ce1e407e5e4da19e94adb4a8af9b9c450b6cd8ba23ebfded552c2c85590`

```dockerfile
```

-	Layers:
	-	`sha256:5eed99acaffad1a4f8b6b4451d454584ca53080fbb9b9fb5a2a1b2d962bc4352`  
		Last Modified: Fri, 08 May 2026 00:27:06 GMT  
		Size: 3.0 MB (3030061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b884d8d1cf5ed9f4aee76c9effec367c8780c191221bcdc29a27bcfb6ddef58`  
		Last Modified: Fri, 08 May 2026 00:27:06 GMT  
		Size: 18.6 KB (18557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d65d43922e685d00e9f6792789eee842c5a6e72b5a5a323c12fff765f56f8798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (205049061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b36ea2ad1b26349eaa2d5d544584e4ef20379d2e307b2b9a9900c6c9541b11`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:25:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:25:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:25:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:25:57 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:25:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:25:58 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:26:11 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:26:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:26:11 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:26:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:26:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:26:12 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:26:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11be66d2d63427821d5d983a59308fddd8fccea02d98012836524f5f6c67b078`  
		Last Modified: Fri, 08 May 2026 00:26:35 GMT  
		Size: 156.5 MB (156461225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe99a7b29cc8ac091a176ca73df6a1ae85eeef9e20aa4c446af4f7651c55a52`  
		Last Modified: Fri, 08 May 2026 00:26:31 GMT  
		Size: 15.3 MB (15327183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d3f7eb7cd56533b2a7f7b200d194610a9643fd72aa692a7cc47e95c7933d0d`  
		Last Modified: Fri, 08 May 2026 00:26:31 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77573f2339f97c042281ac26697d2ecebe3e45ea83ffd63096e9eff7771028d4`  
		Last Modified: Fri, 08 May 2026 00:26:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec7536d1f3123e64c3a7e9021a006ba6d465d986f7bc82f233e77528414be18d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3048348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:848baca51148b0bb1b31fe550f2f5c77303aad8c12e9b1a6cc3e7aabbd8129da`

```dockerfile
```

-	Layers:
	-	`sha256:ae6d785eb569be616a970889357208079615b3b4f0defb49c763b39372d2586d`  
		Last Modified: Fri, 08 May 2026 00:26:30 GMT  
		Size: 3.0 MB (3029670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486d38a2168faf1368332b2611f64c8293938469f34ae2a2a2bf76fd47ee4961`  
		Last Modified: Fri, 08 May 2026 00:26:30 GMT  
		Size: 18.7 KB (18678 bytes)  
		MIME: application/vnd.in-toto+json
