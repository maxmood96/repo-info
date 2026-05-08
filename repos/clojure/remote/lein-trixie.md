## `clojure:lein-trixie`

```console
$ docker pull clojure@sha256:bced427c3f2f45eaaad71d987d607c3217a67e695083c986936dcae49912d1f2
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
$ docker pull clojure@sha256:d492456328bc5c0d7510d655bdbeb3ad3ab473fe259bd2dc25e6e0bf3cab20b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164980308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bb8366f5debadbf3ae39ce68c14f5fe4c1b8bd989f88e5243bd7fdc3e97a8b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:27:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:27:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:27:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:27:54 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:27:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:27:54 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:28:10 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:28:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:28:10 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:28:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:28:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:28:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:28:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864683f7c3a4309b884c17c19c79e6b026c3ae3103f73c278a7ddb00270c3a8`  
		Last Modified: Fri, 08 May 2026 00:28:29 GMT  
		Size: 92.6 MB (92574597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232dee2f5fc5fc18a2a8a71dd70349160cef3a98580406b9cf7950add75ec35e`  
		Last Modified: Fri, 08 May 2026 00:28:28 GMT  
		Size: 18.6 MB (18585481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2e78a624e6258ec13e70893416b59817d93f9d38295b3db5288067b7ed9cbe`  
		Last Modified: Fri, 08 May 2026 00:28:27 GMT  
		Size: 4.5 MB (4517701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb5b32f43a6f03365a89cf7295ed17a1843dc23fa1cb8cb34a25cdb065cb077`  
		Last Modified: Fri, 08 May 2026 00:28:27 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ccc4fb630cd2ae15e6f3ec9fa36f9807849c01dbbf9bcd602214f5ee32f218ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36e0016ef394f1cbb70f41c400ba9d50289caa7464cfed8dba3bae841b65757`

```dockerfile
```

-	Layers:
	-	`sha256:7c562175720847905a855a619b864b5c5073bb63a4fa5a18f9eff712cdc13620`  
		Last Modified: Fri, 08 May 2026 00:28:27 GMT  
		Size: 3.8 MB (3784182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1bacbdf79edb5eebf5a5866f469a8cfc8ee75db8c4cf86c4755715d1853ee3`  
		Last Modified: Fri, 08 May 2026 00:28:27 GMT  
		Size: 19.1 KB (19133 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:944d814ee819942a2e11ea151fa4145be1223218473999b39b3e3fea864cdbcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164275106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fda1b220d120f9978c40d050d4ceb32ebca662e74fc0041c109d003535a40f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:27:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:27:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:27:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:27:31 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:27:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:27:31 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:47 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:27:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:27:47 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:27:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:27:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:48 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f363d2c4bb036c5a1453cd8f5a94606998566d08c8ec327fef225e6161f72ed9`  
		Last Modified: Fri, 08 May 2026 00:28:11 GMT  
		Size: 91.5 MB (91542278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b11045208a19b78410a5ed1a30ef89cdf72caa07424774421d3e9634aa19e2`  
		Last Modified: Fri, 08 May 2026 00:28:08 GMT  
		Size: 18.5 MB (18545451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24e0c10344fa1b394d9f8246f06fb7693e66e5925af19e63edc24d4410ee089`  
		Last Modified: Fri, 08 May 2026 00:28:06 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8ff0b59830d6b6b7f6a042c5892be423059c9960da420fc215065609d2dc58`  
		Last Modified: Fri, 08 May 2026 00:28:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5f9bf8f7416e75c006f1f33fbcf3d59b5d14eabed7ac8a41aaade793c3c265db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3804356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980c035a45d1bf33ce524a57220c39294e5b73fc37e41143bda783b85560f43a`

```dockerfile
```

-	Layers:
	-	`sha256:b5aec1e3812940dd69420e00926865b70a3f7747e7cbe0597c01c6e09429f300`  
		Last Modified: Fri, 08 May 2026 00:28:06 GMT  
		Size: 3.8 MB (3785080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f27a4816e8d07d228ba4f2c1e55708739eada6c4408f35273f84f6bfb0cc7e37`  
		Last Modified: Fri, 08 May 2026 00:28:05 GMT  
		Size: 19.3 KB (19276 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:039f60b428a2fe3c6b0ea23e59ab1581e87c6c2ae5350653d56044166479bf4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.2 MB (168196074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413940f7e4058d3c2e2fd7482e7c9a1a04d6b270b8af410ecd0eec5f38ca484f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 01:44:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:44:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:44:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:44:02 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 01:44:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 01:44:03 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:44:43 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 01:44:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 01:44:43 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 01:44:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 01:44:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:44:47 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:44:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c0840b059b135fa7f7f221d2f316e4eeea1c12b50461d42b38e0a6be805d85`  
		Last Modified: Fri, 08 May 2026 01:45:19 GMT  
		Size: 91.9 MB (91914028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c1530abd084ee5a7b315c7464400391a6124ceb3235ab2fd5f2cb021f1f01f`  
		Last Modified: Fri, 08 May 2026 01:45:18 GMT  
		Size: 18.6 MB (18640926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f00e0e86f30fcbcdaa8d14655158c7bf11b6696f6608e6946a1b5ce3f16ab0`  
		Last Modified: Fri, 08 May 2026 01:45:22 GMT  
		Size: 4.5 MB (4517706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2d2a525640c6abaf7d84e6fe1eac5f015183c9ed4f954e28f2a15e54ba5960`  
		Last Modified: Fri, 08 May 2026 01:45:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:51441c10e69381dd45fe5a623cca6ca667920d06b68c9a47afc94300dcf9d12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3787695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdfc9b1ce7f8d0df92791d69234e0c85e4bb5651421913264aab52e6532ae875`

```dockerfile
```

-	Layers:
	-	`sha256:943a95e779fb0d7fe127b8a1c0d1f44a0813cd902bbf3ee9eeca813e45f6a48a`  
		Last Modified: Fri, 08 May 2026 01:45:17 GMT  
		Size: 3.8 MB (3768506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b349b45ec816a8ae8ea2c15cc3ee9c7f43dadcbab90d7d59a6f66fdbb6a8699`  
		Last Modified: Fri, 08 May 2026 01:45:17 GMT  
		Size: 19.2 KB (19189 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:652b07943ca0027030613ef5fca1438e50bb1741d94317b0b07d50b3dff6c6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161869572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6254f2e8d49e0cccd59ac963edd77ae649374fa17e1c3296e6d5c60176fd8907`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 01 May 2026 01:11:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 May 2026 01:11:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 01 May 2026 01:11:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 01:11:16 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 01 May 2026 01:11:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 01 May 2026 01:11:16 GMT
WORKDIR /tmp
# Fri, 01 May 2026 01:12:50 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 01 May 2026 01:12:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 01 May 2026 01:12:50 GMT
ENV LEIN_ROOT=1
# Fri, 01 May 2026 01:13:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 01 May 2026 01:13:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 01 May 2026 01:13:06 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 01 May 2026 01:13:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af697d12e7ce2f4ea84af1fb9a0a596fbf93eb7670e91abadfbefd74c762bc67`  
		Last Modified: Fri, 01 May 2026 01:16:52 GMT  
		Size: 91.0 MB (91014936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9647da42d45465834ca9d726dd6ba8ab7154229324a906125aa4f54ed182068a`  
		Last Modified: Fri, 01 May 2026 01:16:42 GMT  
		Size: 18.5 MB (18538216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea677db7cda1fc11a1df54732e5c0a35b177d6fea9dd5b9fada24b296b0c912`  
		Last Modified: Fri, 01 May 2026 01:16:38 GMT  
		Size: 4.5 MB (4517773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c5993422fd9895d407148ca9d44146ad1138892aa640404299ccf263d81b5e`  
		Last Modified: Fri, 01 May 2026 01:16:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9f6e25d1b01cc0e7e93bcb1474083c896239daa5e3049d6b69f98e2c7a413a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b64e4ddcf916f155ad45057af1f2377f1c7a46f30b4e3c74427a952e035f81e`

```dockerfile
```

-	Layers:
	-	`sha256:7ef6ce2ac8ccf2db60d0fa69cba6ed091477d82acf938c822bc39d97d9b90b33`  
		Last Modified: Fri, 01 May 2026 01:16:37 GMT  
		Size: 3.8 MB (3756682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1af6d1abe7c4b12bbe52c6c840923bd739f49c1d412e3329b135def5fb5630a`  
		Last Modified: Fri, 01 May 2026 01:16:35 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:f5409a3be19a450e210b988d4db48018d2aee4cc906edd2283ef14fd00113e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160937270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef51d96c60012d2e9ebee2a62642fdb4e99e37799442282b3b9a23a1b4ca898`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Thu, 30 Apr 2026 23:50:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:50:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:50:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:50:51 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:50:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:50:51 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:51:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:51:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:51:14 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:51:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 30 Apr 2026 23:51:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:51:16 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:51:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ee46c033b5990060b9acaa5985a11a008290bfbbb27b32d546e2487a9a5e65`  
		Last Modified: Thu, 30 Apr 2026 23:51:37 GMT  
		Size: 88.4 MB (88420341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036aba4cd2f1bfc6185738b104fac521ee625e68f7a0f033a27d86d71c54b556`  
		Last Modified: Thu, 30 Apr 2026 23:51:43 GMT  
		Size: 18.6 MB (18626693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7969b6187c6556ea2d12b19793fb918d01dbbc2469c584fb909e5e702b4c41e2`  
		Last Modified: Thu, 30 Apr 2026 23:51:42 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4839e5acb38a045fe58a88bfe15a4abca491e2196c9ae20b82652e7ea42e896`  
		Last Modified: Thu, 30 Apr 2026 23:51:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a50275d35b109ab6dcaad30ffe20913387580f61d8381bc5755bd136c665ef96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18515fe3e7c1e1d5fe7ea78079e8a244da0dafffb1e9995be3f9d1b28cf27a6e`

```dockerfile
```

-	Layers:
	-	`sha256:2a7c18415c23c7073323a4381925f488404c9f4e315aee0a57e4596601805f30`  
		Last Modified: Fri, 08 May 2026 00:40:45 GMT  
		Size: 3.8 MB (3765171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afb3046dceb1d0eb7390193723841db37d86c2737a9e39fb3589edf4115e3853`  
		Last Modified: Fri, 08 May 2026 00:40:45 GMT  
		Size: 19.1 KB (19133 bytes)  
		MIME: application/vnd.in-toto+json
