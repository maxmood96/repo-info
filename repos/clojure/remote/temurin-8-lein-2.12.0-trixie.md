## `clojure:temurin-8-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:8c9c62414fb5dc0826b123387983943ec4c8f5c38572263339b16d129815b89e
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
$ docker pull clojure@sha256:33d9b34b3d1cd019ae847920eadd2a7ee0df46db7c0579cef824b42f44c93c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127570826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee8753712ec9b24576d6cb4dceef1d57b1bd94e8d90f0e3797014c72968cb65`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:12:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:12:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:12:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:12:25 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:12:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:12:25 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:12:41 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:12:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:12:41 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:12:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:12:43 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7f2575998825ec48f0cb843f86cba21ef9ebf8bdc7d6f852ccb9b6b1f3aabc`  
		Last Modified: Tue, 07 Apr 2026 03:12:59 GMT  
		Size: 55.2 MB (55170117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d34d4769c4f89a77d4126a70b7ec1d77b404d05c1382a4eaf0647c177f3ef6`  
		Last Modified: Tue, 07 Apr 2026 03:12:58 GMT  
		Size: 18.6 MB (18585102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ea67d24131f0381920fa6cd13ec9cb3cf99b2fd5893cb8960056387c02fac3`  
		Last Modified: Tue, 07 Apr 2026 03:12:57 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:dd27410c556b224c8b25a58bc3496db68db03f9cdd73af4d4d4d27b3afdb0fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51b7152e499c1558d2863308d7673859369035537fbd6efb89232ecdfec5359`

```dockerfile
```

-	Layers:
	-	`sha256:093c461a0cabe361d34e64a1b2bd4293298fda9cf2e1e2d5587e8cbf1bf6cfcb`  
		Last Modified: Tue, 07 Apr 2026 03:12:57 GMT  
		Size: 3.9 MB (3936516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8b8132786b22ee8fb6c986686b2ba0ca1d6938fd2d3f5dca34ee1d28a77f758`  
		Last Modified: Tue, 07 Apr 2026 03:12:57 GMT  
		Size: 16.4 KB (16352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5115a39964b1e441ba200e00d18e8e3dd89090f6037d56f88f8de1f946cb8424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (126979405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d281718daba86f03a0ae4bfd3778ed4870cbd5e2addf66bfd3aca34c969aaf3`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:23:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:23:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:23:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:23:01 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:23:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:23:01 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:23:17 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:23:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:23:17 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:23:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:23:19 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b54288de21d56a26b38c1a565c93186bf5534ef40b36ca04404d5eeecdb7a6c`  
		Last Modified: Tue, 07 Apr 2026 03:23:37 GMT  
		Size: 54.3 MB (54251612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18925c9334e8cb5edf902fd4e05e6ea7742f5790a7677231b41439dc28475630`  
		Last Modified: Tue, 07 Apr 2026 03:23:36 GMT  
		Size: 18.5 MB (18544789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30c0a601fd7ead0c74050f2ca772665edcce1cd53cc973de7fa85895d8e7415`  
		Last Modified: Tue, 07 Apr 2026 03:23:35 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cd73a549ab247ab88449b3023a768c5d91639e8b8047f3e8ab7cdec84a933c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d020c614623946f95a906a5cefe193475fc69bd8e47971ffd22c74c541b66b2c`

```dockerfile
```

-	Layers:
	-	`sha256:cb0e65c1acc1f4e1518603faf8601632670a729d13515af76ec1486e37f5a315`  
		Last Modified: Tue, 07 Apr 2026 03:23:35 GMT  
		Size: 3.9 MB (3938093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c8588685c4b76c9a4f0290efd459e2d716e6d829a621b27aa6ebc406bfb4ec2`  
		Last Modified: Tue, 07 Apr 2026 03:23:35 GMT  
		Size: 16.5 KB (16473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:bfa4d20e4fc7ce20a7c9be2562113e0f16adc6a86a0945601af630a4fb3bdcf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128927274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b99d1fbdd9fed749904d4d428733b1c560acb386fa7b2026063676c663ccfd`
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
# Tue, 17 Mar 2026 18:09:33 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:09:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:09:33 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:09:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:09:37 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf4e66022f0a54019718e5fb82aff975c8ae1279a587e803dd7d8da942e46b2`  
		Last Modified: Tue, 17 Mar 2026 18:10:01 GMT  
		Size: 52.7 MB (52650377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86d9f0b5c0ad1ef84be42cce5423ebdce3964b851d74c68f26c1907f623b9e3`  
		Last Modified: Tue, 17 Mar 2026 18:10:01 GMT  
		Size: 18.6 MB (18640751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f210a512ad8660759d87ab2bbea4f45ff471b124442b9c7e626d290cba2156da`  
		Last Modified: Tue, 17 Mar 2026 18:10:00 GMT  
		Size: 4.5 MB (4517764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:08d824d2c7de946bcf2b3d8b5916704d7c9190ee99cf22bea54a0d483b683254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e02c4223956a9c24b0cd1cbbba1d0cdc028477adf53e45b4f0c90ee411f334b`

```dockerfile
```

-	Layers:
	-	`sha256:6ff0d23f0d6cdf16feb4ab0598d100787f53d6cb8c1914c2fd89050358ed8017`  
		Last Modified: Tue, 17 Mar 2026 18:10:00 GMT  
		Size: 3.9 MB (3938111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26de3c3148b6318c965179d01fc388734619eff32aeb0e2c515720621f49adc2`  
		Last Modified: Tue, 17 Mar 2026 18:10:00 GMT  
		Size: 16.4 KB (16396 bytes)  
		MIME: application/vnd.in-toto+json
