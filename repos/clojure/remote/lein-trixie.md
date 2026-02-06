## `clojure:lein-trixie`

```console
$ docker pull clojure@sha256:aa9d39488782999575303dda37211c45da46c48708b4c217c6930e0c395ffef9
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

### `clojure:lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:718d8d27759c62326489874bb70ee316cc6937b6e638a677b04c6823376dec96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164647470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6a23c6bce24d9998e96555d511cd1e328097de9b9a1bd90e0a3f344d71a778`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:07:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:07:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:07:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:07:03 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:07:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:07:03 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:07:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:07:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:07:24 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:07:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:07:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:07:25 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:07:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ca7eb49b9a299cdbfbe0e4166ac0f7859f83e32d43a8a061388cf32873af1f`  
		Last Modified: Thu, 05 Feb 2026 23:07:46 GMT  
		Size: 92.3 MB (92256283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb20ca3aac51febdbfb5e9cf6cd0dab4dd725a3831e82cf354ad1817ce2d9512`  
		Last Modified: Thu, 05 Feb 2026 23:07:44 GMT  
		Size: 18.6 MB (18580091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1fd4220ecaa81071359907c9f1b7356153eec1d68073770d248a7b40683509`  
		Last Modified: Thu, 05 Feb 2026 23:07:43 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2738a8361857c6b6ebe7859f31ef201d8086309be83e8110d98f109c7c3d5fe`  
		Last Modified: Thu, 05 Feb 2026 23:07:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d335c5882e37d059d110e558ea84a0f26a36f6c088ff9361a980dfb40b9b4761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3802502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f740c4727d78aeb3111a4c32ccc6aa90e6ad6ad8bde69aceb6e8519023db53`

```dockerfile
```

-	Layers:
	-	`sha256:5fd2999589c3fed47d21943d6e4175197e61b031c350bd34e0b2b7e413040ee2`  
		Last Modified: Thu, 05 Feb 2026 23:07:43 GMT  
		Size: 3.8 MB (3783523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf399c8d8ae74c19da116e21c57c1c91df7bcc6cc1af22f2ec7c663ea879cbb4`  
		Last Modified: Thu, 05 Feb 2026 23:07:43 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:310fe5045810205ea380c2ba470b7cd74bf0cbb346df7a571ffbfa78d80461e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163999898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58218cde733e07c3cf652c519dd3bb4e24e969a3fe9517720516d0fcf77f8af7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:08:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:08:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:08:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:08:13 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:08:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:08:13 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:08:33 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:08:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:08:33 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:08:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:08:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:08:35 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:08:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32df255f7ebd2b13f1d14bd1d6469177649f7a396cd22159f862cda9245204b7`  
		Last Modified: Thu, 05 Feb 2026 23:08:54 GMT  
		Size: 91.3 MB (91288278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e24b140050589bc849239a6c89b8cd7494b9d35fed6e71a8cad9590c87f8de`  
		Last Modified: Thu, 05 Feb 2026 23:08:53 GMT  
		Size: 18.5 MB (18541435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7af540cb4c806303ec515d510e8fb2d361392815f0ffed322734638d8d4b6bf`  
		Last Modified: Thu, 05 Feb 2026 23:08:52 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3d3698ddf9bf3307612448aedfaee66251c72515e1663e56c881c71744fa7a`  
		Last Modified: Thu, 05 Feb 2026 23:08:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3456640061b77caad2bf056c8fd8604e42e52b3792056b520e254b418fd9bb09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77abdda130ffcb9ffd3de78ee960b4fe0f9083e42040626a29932a3a664fb106`

```dockerfile
```

-	Layers:
	-	`sha256:060cfad9d5e4e3b72857ff202305c0a49871cd132d155efc4cc8edcbe8b42b4a`  
		Last Modified: Thu, 05 Feb 2026 23:08:52 GMT  
		Size: 3.8 MB (3784421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ef3174810858defaaa0bd97f3cede1251171e0c822885d5e3ecdef0fb0b1551`  
		Last Modified: Thu, 05 Feb 2026 23:08:52 GMT  
		Size: 19.1 KB (19124 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:423d5df8a0b36277be506768055010b591ec9f05cfa21654a289b9da5c28e090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167900700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79acb1409382f4e9e8c2853db63119abfb3e217faaa1286e0c21c5b4db610f2d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:48:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:48:05 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 06 Feb 2026 00:48:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 06 Feb 2026 00:48:08 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:48:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 06 Feb 2026 00:48:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 06 Feb 2026 00:48:59 GMT
ENV LEIN_ROOT=1
# Fri, 06 Feb 2026 00:49:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Feb 2026 00:49:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:49:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:49:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3230ebb877a1444adbcad5521afaffb1c41773004c4324fe65c2c551a9cc1544`  
		Last Modified: Fri, 06 Feb 2026 00:50:07 GMT  
		Size: 91.6 MB (91632873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3592aef72592656244b79421c8d2881c7ab4347c4dae6ce8aa981feb882d243b`  
		Last Modified: Fri, 06 Feb 2026 00:50:05 GMT  
		Size: 18.6 MB (18637526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587ba20bb2ee02d46106a001def44a07dbb7cabaa6022d338c73fe3b855b3852`  
		Last Modified: Fri, 06 Feb 2026 00:50:05 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa996e2b368b508e8135f75a167c37d450e8907d36fd8f22e066feb03ed873a`  
		Last Modified: Fri, 06 Feb 2026 00:50:04 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fa663ae6c7b8111617f3fc38d85088b73a80fc9dd4dc8481dde94fa1107a3ea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db65d87d7b29baf82e1d36f5c8147a8712a6ca13ea76eea1cbb0e7e97e29a720`

```dockerfile
```

-	Layers:
	-	`sha256:9d751fca3119f593035e9256836355a2b9e9cafadc7b24d8e0ff8a8568767cd9`  
		Last Modified: Fri, 06 Feb 2026 00:50:05 GMT  
		Size: 3.8 MB (3767847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d14b4d9e02e8f36ae6119abd5a6cbf1b4968badefbbca9ee59f9849cd865b697`  
		Last Modified: Fri, 06 Feb 2026 00:50:04 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:111fc7a774005281848a2055be867b35aeac31e63b909c2855b0a8bb627d603a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161579753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181a44a4d2f904d3736a6edcc8396b5e8884d8b7f1457efc1a060910a9ebe042`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 21:12:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 21:12:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 21:12:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 21:12:22 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 21:12:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 21:12:22 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 21:14:01 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 21:14:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 21:14:01 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 21:14:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 21:14:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 21:14:18 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 21:14:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fe598f31566ea16873e9a3c5986699f1d21dbe097ec6c69f669dc2451a4a6d`  
		Last Modified: Thu, 05 Feb 2026 21:18:03 GMT  
		Size: 90.8 MB (90752897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2172e2fa7ff6ad8c232871a510c07372fd86987cdbddf7b23856c09ac1cf53`  
		Last Modified: Thu, 05 Feb 2026 21:17:51 GMT  
		Size: 18.5 MB (18531868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d68eb43f9d6d62a1775a8279aa541b9a8d04a16cf11f349cb28ba4ffa6f38fc`  
		Last Modified: Thu, 05 Feb 2026 21:17:48 GMT  
		Size: 4.5 MB (4517794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084ba41c146a70376b6687b33537806992327a158eff80a30d24a1db5d03d01e`  
		Last Modified: Thu, 05 Feb 2026 21:17:46 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d9c98eebacdeb369214e5208294079eed83809e78bc2ebeec13b53399fe66108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae637623e71c2b84165be8d74d8c025139e1376029aaf00b3b8e3418746d6ff`

```dockerfile
```

-	Layers:
	-	`sha256:eb46ded8ecbd4637d401b3433bb0d9c1a1568bc6397f9191a03d09ae24bc1e8a`  
		Last Modified: Thu, 05 Feb 2026 21:17:47 GMT  
		Size: 3.8 MB (3756021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0529034ed692eb70bd787169c305df4ab0c607629bac5eb85d3736b584a31961`  
		Last Modified: Thu, 05 Feb 2026 21:17:45 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:bfd0bf863f1a6e53104b6e59403e552204241aab4940f86800843b0476e2a773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160727371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22cf7764e6d30b8209619ba1df7b64042f7ac28486cc9080f244077664ac09d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:08:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:08:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:08:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:08:57 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:08:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:08:57 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:09:12 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:09:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:09:12 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:09:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:09:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:09:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:09:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d015902a7b24992ac0b8ff09bb1cfb5b5d66933fc6ff1b22b739b7f83f443214`  
		Last Modified: Thu, 05 Feb 2026 23:09:39 GMT  
		Size: 88.2 MB (88233820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddce5ce1e0e8ee1df1c23eb10e4115cd4f82d81fba2ec03530f84a65cb747460`  
		Last Modified: Thu, 05 Feb 2026 23:09:38 GMT  
		Size: 18.6 MB (18621012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a625f4d5e1370fbdea1e953e1825f23f563e04befd04c0584ab7b91e30c741`  
		Last Modified: Thu, 05 Feb 2026 23:09:38 GMT  
		Size: 4.5 MB (4517732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2177969ad2432cdc44535d6fc1cc7967fcab494967de37c7864c7c2ab04f705`  
		Last Modified: Thu, 05 Feb 2026 23:09:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3ef74579d714878df39fd9395610effe85ef3bc50d8419413589feec3052f8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6f1b953959f0c0ff7c190f25db12652f4ba0f4dd7d9330291c14964aac2dc3`

```dockerfile
```

-	Layers:
	-	`sha256:ac3715feeecb4458a69d947f001a0d060725b4d151bf1d4a9c14bf4090cba03e`  
		Last Modified: Thu, 05 Feb 2026 23:09:38 GMT  
		Size: 3.8 MB (3764512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30cac88d39e0071880868977e0e6da9a8c884261d9816fc4401d52548d7b3d30`  
		Last Modified: Thu, 05 Feb 2026 23:09:37 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json
