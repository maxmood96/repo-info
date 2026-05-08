## `clojure:temurin-17-lein-trixie`

```console
$ docker pull clojure@sha256:a3b1f599415049343db79c876de6d68663372ad7dddcbbbad3d8d80713bd6e35
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

### `clojure:temurin-17-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:f72fb682e5fd7cb148a65b2371dcfabe1b4bc64a78b0c1f479da66b216a25410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218311269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26fc17c76bf6e3eb8ca6f3c1fcc55fb955fa8fbc24a86562bc53cf2e9927fc98`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:07:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:07:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:07:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:07:28 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:07:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:07:28 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:07:42 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:07:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:07:42 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:07:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:07:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:07:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:07:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f531ab35d0b751562a6ca12fc0b48a5cdbeabbaf470c8b51d2256b4c3a30e1`  
		Last Modified: Fri, 08 May 2026 00:08:05 GMT  
		Size: 145.9 MB (145905473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14567075eff6540fa700a1dfff8bae5d69e3a2fd1d6b173c743573e0a83aaa6c`  
		Last Modified: Fri, 08 May 2026 00:07:59 GMT  
		Size: 18.6 MB (18585521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85850652e981e1c8a214ad4fc98646a443cec3645e283b56aacbb4a43810af23`  
		Last Modified: Fri, 08 May 2026 00:07:58 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f115f4c0c2547010e36fcdf383e078465e10c38c51890af8759c30b024a5f62`  
		Last Modified: Fri, 08 May 2026 00:07:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7eae3e7ba5901f1707361305367407596c4d870c5bff3a61433a89a9d4bda393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3795cecf7b9f2cacbb875c3f94773db22b502b3546985b6530e9a4c8a30d0c`

```dockerfile
```

-	Layers:
	-	`sha256:08fa097092a81646c1f936384125cf0767cab66840e5372a80d1ae90cebd7497`  
		Last Modified: Fri, 08 May 2026 00:07:58 GMT  
		Size: 3.8 MB (3816154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2012230f90a08dd35a4910187c037ad19def0758b9f95ecc506bb1719aad7db9`  
		Last Modified: Fri, 08 May 2026 00:07:58 GMT  
		Size: 18.5 KB (18504 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3418232e1fdd3c9d665e8c518f13457a27bcdc80db1f67351a6af53612128146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217457221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f841e478d5a129a997de15cbdf1dbd9882b82ff2d312d482170e68c78157a8b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:09:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:09:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:09:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:09:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:09:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:09:18 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:09:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:09:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:09:35 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:09:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:09:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:09:37 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:09:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef281072183023145dbf9944bad137f5588c85495d7642d1c0ab0aec0b265e87`  
		Last Modified: Fri, 08 May 2026 00:09:57 GMT  
		Size: 144.7 MB (144724334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0fe23ba8b26c8cdd0ac865fe6a8f25e1c565cf80cf2ce67dbeb4724156462e`  
		Last Modified: Fri, 08 May 2026 00:09:56 GMT  
		Size: 18.5 MB (18545454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d40a34084db7e6479e5d74c18346005c10e1cfce1d8365582513b74e2504a8`  
		Last Modified: Fri, 08 May 2026 00:09:54 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deb9895353e75f3228faea73daec461d8f8e35187306294c0726a9671efcdbe`  
		Last Modified: Fri, 08 May 2026 00:09:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2c10a1e983d8202f4f12ea6969f95a12e51616536a25cab15aed4605ffd35304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b54d36c651a1a9f35fd73c983d1daaf176ae65600f9e91e897865df4c18494`

```dockerfile
```

-	Layers:
	-	`sha256:bd59779f1a7633e23b9f2d4b84865833077dd7d8052297ed5ead6ddf94bf4d56`  
		Last Modified: Fri, 08 May 2026 00:09:54 GMT  
		Size: 3.8 MB (3817031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef61446f3e2a8fa0191464e15f1e4c10460efdebab3ed1a662b57def1f7b3e58`  
		Last Modified: Fri, 08 May 2026 00:09:53 GMT  
		Size: 18.6 KB (18627 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:128003818378d64c6dc4b9bca4bc65843e6d033b4550abec7bf50f7bbf8de604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (222048437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb04235020a7447443fd43c8bef11e5cea50e58c5eaf32e85ea9fb655a4b3d7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:45:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:45:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:45:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:45:58 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:45:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:45:59 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:46:32 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:46:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:46:32 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:46:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:46:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:46:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:46:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937b7eb5aea1a56bc2fcf2ec92c34b7b899cf187331f6afa218be284e921541e`  
		Last Modified: Fri, 08 May 2026 00:47:15 GMT  
		Size: 145.8 MB (145766229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f971726d9672d25d9b6041d65ce5b96e8607466371acef858c72c4df38e14f`  
		Last Modified: Fri, 08 May 2026 00:47:12 GMT  
		Size: 18.6 MB (18641039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80af6239652ac025556480de1018ac56b7f334bae21630514fa177a10826f54`  
		Last Modified: Fri, 08 May 2026 00:47:11 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e402ca0a7ebfaa69739b879ffb332c1364d04707a2fcb788a1ea51368fe3f16`  
		Last Modified: Fri, 08 May 2026 00:47:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3722d4724e2af2ed9028dbf14b9c907f92ca8393087f74de3813681cee12efb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c199e5db6120441460280ed0fd47d6009916a530201f70af765e9c7abd201f2`

```dockerfile
```

-	Layers:
	-	`sha256:8b5073c50f115c4ee886e50ed64c27c8d99693f8f0b3826c89a98b2c682a333f`  
		Last Modified: Fri, 08 May 2026 00:47:11 GMT  
		Size: 3.8 MB (3817154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e5792acb00a4d23bcc6fb414c6f9cafb00d37510f83ab1b0882240047598ef3`  
		Last Modified: Fri, 08 May 2026 00:47:11 GMT  
		Size: 18.5 KB (18549 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:26a74be83a457fa66e498b4da97fbc571092053074f96e11a315a2327952f0e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213517493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023a7e0e4cf28e39ec45bfbf384f39ee1b7bb312c53cf76dcf3e5f132b3bd119`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 17:41:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Apr 2026 17:41:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 24 Apr 2026 17:41:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 17:41:31 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 24 Apr 2026 17:41:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 24 Apr 2026 17:41:32 GMT
WORKDIR /tmp
# Fri, 24 Apr 2026 17:43:06 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 24 Apr 2026 17:43:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 24 Apr 2026 17:43:06 GMT
ENV LEIN_ROOT=1
# Fri, 24 Apr 2026 17:43:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 24 Apr 2026 17:43:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 24 Apr 2026 17:43:23 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 24 Apr 2026 17:43:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca059398ab85ec46154b4adc01fde7c5c787818bd1a043bdd89c080ecbd2e3db`  
		Last Modified: Fri, 24 Apr 2026 17:47:36 GMT  
		Size: 142.7 MB (142662892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3521f548075742b9621c6ffbc5187c729e30e044a6574e659dee29ecc2aa13`  
		Last Modified: Fri, 24 Apr 2026 17:47:17 GMT  
		Size: 18.5 MB (18538167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5914f0065faeca3d050d5335162a6d13230737573dee0a5438f5aae391052b61`  
		Last Modified: Fri, 24 Apr 2026 17:47:14 GMT  
		Size: 4.5 MB (4517788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32abd50ec5da449cf656be6cfca21c1e42837f40f599723c2c95b44e08cad4a8`  
		Last Modified: Fri, 24 Apr 2026 17:47:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e874d25e23587e37a44040b1a712ba52447ce482063753e85f9c87757c487b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3822480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31532fe3a88ab62a82c914c3a6a0161652aee4d8f36374bf49468cf878e5eb12`

```dockerfile
```

-	Layers:
	-	`sha256:a9372520cccfa94f06083a84603ca32183c15a019d6a44b9fb55ab83486df534`  
		Last Modified: Fri, 24 Apr 2026 17:47:13 GMT  
		Size: 3.8 MB (3804085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85f80f411fb5126e0f58202087dfcd11ae54bdd2d113fcce869e54a8a4e86f7a`  
		Last Modified: Fri, 24 Apr 2026 17:47:11 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:e71f3c2190602b0030af984508fc7778c167a8c1346e6071d6ebc1ca1912c849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208143887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70d3939a9ffbc6f7568987d3482b96d1273dfeb1986617fe3ff3f54fc05eabd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 04:00:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:00:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:00:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:00:59 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 04:00:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 04:00:59 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:01:12 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 04:01:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 04:01:12 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 04:01:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 04:01:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:01:14 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:01:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e16fe85adae75453b23e1a85eff2f2415cfe3e7b615e2876f8d9cf1fb833b9`  
		Last Modified: Wed, 22 Apr 2026 04:01:42 GMT  
		Size: 135.6 MB (135626975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8e6b191f8a53a4745ad7a3e245b65486c24c9819e1fda5ba98e5a45c24ec23`  
		Last Modified: Wed, 22 Apr 2026 04:01:39 GMT  
		Size: 18.6 MB (18626627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450c22a55fbace1a5f9f5276a208aabc1f5fb53547f154388bff32c5c087461e`  
		Last Modified: Wed, 22 Apr 2026 04:01:38 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641b3ce94b4e8a1b5d2e76d3208c9568d1089354e8ad8208aa2ae128505e95ad`  
		Last Modified: Wed, 22 Apr 2026 04:01:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e6344381f708b6e0f11c66f2f6ffb40742da6390b1c5fb0b37bb6cd8f67c946e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3830306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a539cee8b725ff5d994b922c7874fef2f957e57b4fdbbb2f025ea9548d5fe9`

```dockerfile
```

-	Layers:
	-	`sha256:a0e601dc6fea85c9806098e2a3fcf2ae8947f5a550dd3aef0e769e84db6ef0f5`  
		Last Modified: Wed, 22 Apr 2026 04:01:38 GMT  
		Size: 3.8 MB (3811954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39435cf2f72a3ca11ad749c95550a6f553df1736efa73ce0811af6000c65ccd8`  
		Last Modified: Wed, 22 Apr 2026 04:01:37 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
