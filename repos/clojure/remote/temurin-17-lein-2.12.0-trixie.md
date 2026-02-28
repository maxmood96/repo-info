## `clojure:temurin-17-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:223753d9c852abb01afb2ca3b15db4cc9938eb1c009b8e070cf2ea2ad1da2317
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:72144f70c434d4421a086130143278ee28c7bca88caa3b1ea0e214f26fe8f629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.0 MB (218020085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96cf3ba6da264cd516f5a8d4df8d1e23c88f539197fd756b27fb2e668cbbca02`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:54:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:54:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:54:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:54:46 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:54:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:54:46 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:55:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:55:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:55:03 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:55:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:55:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:55:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:55:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189f0edef257c8c842b866cfc907940e04cd19ad7cf850494eb3e85f93d2987b`  
		Last Modified: Tue, 24 Feb 2026 19:55:24 GMT  
		Size: 145.6 MB (145628796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b911f199ab8eb8a9ae0bb5aac0e98419ffb772ba1c9aaabf1f4295d0a77d193`  
		Last Modified: Tue, 24 Feb 2026 19:55:21 GMT  
		Size: 18.6 MB (18580036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b91d4c0a89f49761f4c348c5e2e2458b225319a5deff23bad4fb1e838698dc`  
		Last Modified: Tue, 24 Feb 2026 19:55:21 GMT  
		Size: 4.5 MB (4517700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea9569c00ef5b60ed580940da297ddc62c7aaeeaf63d5bd3b0a8f0b5977ab86`  
		Last Modified: Tue, 24 Feb 2026 19:55:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:acb84732378083d797bedffc8cf9acbbd4c59be05ead395891b4be19336c6e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef984bea92b0a3add40a879d48dc7755bd58a9f535105236f28c0740b9092f49`

```dockerfile
```

-	Layers:
	-	`sha256:f48fa37ba3dda1358a35eeb01a2afda7e777faa4acbd3f6f5e28bebf67dced11`  
		Last Modified: Tue, 24 Feb 2026 19:55:21 GMT  
		Size: 3.8 MB (3815491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304f5cc96f46b9993bd091306d6ef2a4ceb271db6308c8249c1dd14488c5c47b`  
		Last Modified: Tue, 24 Feb 2026 19:55:20 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:252b4e48fd1cd0b3a026a45e00291ef236dda5a7058274b89b6c75f27defb648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.1 MB (217148009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f51330f0d349f60c6b748c91dcc4ffee4760ddfe2d86470a03b634d23b73bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:05:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:05:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:05:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:05:47 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:05:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:05:47 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:06:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:06:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:06:03 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:06:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:06:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:06:05 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:06:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47c2742c5137d1adc9a98d2d04fc2af2b324f40c2bb44d64cf745d7fc28fbae`  
		Last Modified: Tue, 24 Feb 2026 20:06:24 GMT  
		Size: 144.4 MB (144436198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dee45cef3262b7948c8da646e53cf28a278bdeac60cab7dc6424069de9dcfb7`  
		Last Modified: Tue, 24 Feb 2026 20:06:23 GMT  
		Size: 18.5 MB (18541452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d90ffd6ae13293757b4d4eb89d640ffa62c92afa1c18e2bf411a496f4c8dd77`  
		Last Modified: Tue, 24 Feb 2026 20:06:22 GMT  
		Size: 4.5 MB (4517763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7018f407f4e9adb724f16fa226c1e66a3ffb7a399f7a9af3e7d5575d3c231c48`  
		Last Modified: Tue, 24 Feb 2026 20:06:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5f7e7ac9c742169717b17a4daaddf130ff51f13e55199c930376308ffd296743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e136f15ba7190c1152659090f98b64c77ca04c40e62e7ea3e24d5a64690f9a`

```dockerfile
```

-	Layers:
	-	`sha256:10f60057bf6c2ef4eaecdbd0d645cfdf93b0186d6c6dac88c6dfbb7d58c1ceee`  
		Last Modified: Tue, 24 Feb 2026 20:06:23 GMT  
		Size: 3.8 MB (3816368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:720eb6450f84d59b32efcbf353e6409574a380d16c36e10f563dfe9939dfa628`  
		Last Modified: Tue, 24 Feb 2026 20:06:22 GMT  
		Size: 18.5 KB (18472 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:8c8d11250da1c7c02466b4ff9302b8a44fc969c11808b4006ed7b27117b0a398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221706240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e74748488b3877f4e3911dc266afd5aaeae69d49a1b0f62d055c7e1e61f92d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 01:59:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:59:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:59:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:59:46 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 01:59:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 01:59:47 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:00:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 02:00:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 02:00:53 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 02:00:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 02:00:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:00:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:00:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c93d40c272f62556f73a8f185bdb3534d9d5498e1326e609b9e0d6c7e31c711`  
		Last Modified: Wed, 25 Feb 2026 02:01:21 GMT  
		Size: 145.4 MB (145438250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04464e34beab301857bdd020dc9c2b6ac5465349a9594fe3e3d573b7a3a013cd`  
		Last Modified: Wed, 25 Feb 2026 02:01:34 GMT  
		Size: 18.6 MB (18637553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5282411832088b70956c7c9ebbb2bca70a21a9f6402be128c80ceff2a2ef492f`  
		Last Modified: Wed, 25 Feb 2026 02:01:34 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3105a3a4df4d12c96e473c9f3bdfb977fbe48b1c6d0cec0f5ead8c266f5dbd`  
		Last Modified: Wed, 25 Feb 2026 02:01:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8ed755e6d2b9db29e69baf483206a545bdd698b11af40d094b317589613e9c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82aea6a0a7bef0bd7e983cc9b3561c3748034bf0c2c9fadc1bb6426648b5297e`

```dockerfile
```

-	Layers:
	-	`sha256:5380f830dec5d0605adaae4cca5db57f205119be4097d7e538f02733a3968f79`  
		Last Modified: Wed, 25 Feb 2026 02:01:36 GMT  
		Size: 3.8 MB (3816491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b6000cc190feac922028a2013822cc92de1467f089ca4316312113381cc0668`  
		Last Modified: Wed, 25 Feb 2026 02:01:34 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:32383941fdd0159463ea662521a289e75ef4aedc128246f7d873fc03e265d9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213489947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab6cc4dcbad8ccb3043523062e39830b7a362ad95e7e834f8ac00ed26a277d0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Fri, 27 Feb 2026 21:20:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 27 Feb 2026 21:20:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 27 Feb 2026 21:20:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Feb 2026 21:20:56 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 27 Feb 2026 21:20:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 27 Feb 2026 21:20:56 GMT
WORKDIR /tmp
# Fri, 27 Feb 2026 21:22:30 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 27 Feb 2026 21:22:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 27 Feb 2026 21:22:30 GMT
ENV LEIN_ROOT=1
# Fri, 27 Feb 2026 21:22:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 27 Feb 2026 21:22:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 27 Feb 2026 21:22:47 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 27 Feb 2026 21:22:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3be247472b67578a1d05739722d8adeca41098796e5d6210800176db58046fa7`  
		Last Modified: Tue, 24 Feb 2026 18:57:42 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f27f4bf7ad939ca2936c66027f77feab15c20528c320fcb92eb833d88b76cc`  
		Last Modified: Fri, 27 Feb 2026 21:27:01 GMT  
		Size: 142.7 MB (142662998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64602cd14997054d669dc355e949c71f9d4d9afa6ae68086e8bfb3368f37535`  
		Last Modified: Fri, 27 Feb 2026 21:26:43 GMT  
		Size: 18.5 MB (18531794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529619e26cc23f446edd3f1d45c04bd37b0a40f6751be3d9a45d17f368679722`  
		Last Modified: Fri, 27 Feb 2026 21:26:40 GMT  
		Size: 4.5 MB (4517789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907a9680c8efafb07ca3ef2e5a4e8bc0c4b96f49ac365ace8e52b81a43c3da89`  
		Last Modified: Fri, 27 Feb 2026 21:26:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c82601fa8943c4e15e98d4168d73236a605b103d711433587011191efd91b632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3822445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92b91009f2e6f13a656b744c53795539a871cf6db15a1a942e2105e02c816c9`

```dockerfile
```

-	Layers:
	-	`sha256:b8db9d5d5ebe7c43f22e6f94a77658918950bb057af8a790dde7455e87db91c1`  
		Last Modified: Fri, 27 Feb 2026 21:26:39 GMT  
		Size: 3.8 MB (3804049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b66f3b29231630e90b62e5d33858b1c47bf5088851df3d5115dbd8acdaec4998`  
		Last Modified: Fri, 27 Feb 2026 21:26:37 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:3ac8e926ce352a99c668ab3a099ad033e46242091c28e9bb8c7ecb19fb9c94e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208121067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd661c145aee5eceb812249387a81acf85e4cb3a7a50c2daaa78584ea5a00412`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:16:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:16:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:16:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:16:39 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:16:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:16:40 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:17:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:17:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:17:15 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:17:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:17:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:17:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:17:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1be9b165f1f0dbdb0d3d0dcb750f4dbc95a320ac91bccfe873000c67e29774`  
		Last Modified: Tue, 24 Feb 2026 23:18:03 GMT  
		Size: 135.6 MB (135627117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7f765c6ab533a5b4da12e64a7e86dbe089aab970154f758ee57aa32e52a6a8`  
		Last Modified: Tue, 24 Feb 2026 23:18:00 GMT  
		Size: 18.6 MB (18621230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22267e0325f5eafddcf935b7f02026182cee414f5bfb0002ec08a5a7190654d`  
		Last Modified: Tue, 24 Feb 2026 23:18:00 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d4afabc9bc0705a9e9d26b09d811c6dd64eb42cb91ac65ca2a3338069a69e0`  
		Last Modified: Tue, 24 Feb 2026 23:18:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cab8a73d4060cbb3424dad9dfa6570d434badcefcf8556963181445b79eebe18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3830270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877f906e8bd40fd1afd36cb56725937b7ececa369ff193e98d1714be2b7a9327`

```dockerfile
```

-	Layers:
	-	`sha256:93051dfceca41a42cc9619d3b628d135a29ca468a1ec0b31a995290917abe49f`  
		Last Modified: Tue, 24 Feb 2026 23:18:00 GMT  
		Size: 3.8 MB (3811918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3feef6c0a0c22db3b2bd70f4b79f4d95cb674a8bcf6f480012aedaecd4ba77c`  
		Last Modified: Tue, 24 Feb 2026 23:17:59 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
