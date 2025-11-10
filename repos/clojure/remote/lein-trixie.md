## `clojure:lein-trixie`

```console
$ docker pull clojure@sha256:e90f01e9ac2d02761660f008949f1a1ceafafd179ed9de60f926d2eb09bdc938
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
$ docker pull clojure@sha256:12b2b1cffc1962b870c515e85f465bf7da93bf11eadf12d683ac593a4b21a7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164428266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce24d641653a6beab97a4d862369dcc09ae890786c3856946c57a0f000b43393`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:45:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:45:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:45:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:45:43 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:45:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:45:43 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:45:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:45:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:45:59 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:46:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:46:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:46:00 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:46:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53340e8244fb84dd3f11aac301690cdbb1bdf6097e1300a8023d41c48e09958d`  
		Last Modified: Sat, 08 Nov 2025 18:46:41 GMT  
		Size: 92.0 MB (92045315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c49885aba2fd2c5139d05a1d85cf9a44289b8f372da289babf33b019ce76ba5`  
		Last Modified: Sat, 08 Nov 2025 18:46:34 GMT  
		Size: 18.6 MB (18579198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b6930212b7a10d90c8e5223cfb5b8b476474eb77db1ba0fe283947a770d9f8`  
		Last Modified: Sat, 08 Nov 2025 18:46:34 GMT  
		Size: 4.5 MB (4517696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce37c339ff7fbed2589b24300314278b358298996966130bb69a72bfbdeab2a`  
		Last Modified: Sat, 08 Nov 2025 18:46:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c6ee14c18f407f3728a9af7078c9f02b5cda13a69ca7c6fd5e0be7445592e1e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4188b10efd88f1668bf21cba04e6f6607ea59a2034fdea59d421b624038c7c`

```dockerfile
```

-	Layers:
	-	`sha256:13a81d762936c4a9d49340131ae99ca124b93f5efaa31ec0af469f481a9b26d9`  
		Last Modified: Sat, 08 Nov 2025 22:35:33 GMT  
		Size: 3.8 MB (3764682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4f36ade4bcd38263b049cd92b9600cdfff56e4d02b7bf8b5846b6daaf2bf4da`  
		Last Modified: Sat, 08 Nov 2025 22:35:33 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:08d3c21ae487a9a41f42fe8c00ec92a0b9fae5448f4bae307a830b5ce91de392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163761039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f0af0a2a738264ef1f512642051094cfe354bea69ee9f7d4483cfc347f338e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:45:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:45:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:45:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:45:33 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:45:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:45:33 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:45:49 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:45:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:45:49 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:45:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:45:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:45:51 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:45:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8f77750ce026a739f37ae19904b5052d2f43b31149a8b99c21c67e1bc9d070`  
		Last Modified: Sat, 08 Nov 2025 19:44:32 GMT  
		Size: 91.1 MB (91052503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbad1e9120453786239e4e7b1804e6ee3afe852e9e72619c6e9c84b37187802`  
		Last Modified: Sat, 08 Nov 2025 19:44:19 GMT  
		Size: 18.5 MB (18539919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc61f9b5644f085fb1d9a7ddb91e570859fe6e7cfcc8d093a793f94bea3354fb`  
		Last Modified: Sat, 08 Nov 2025 19:44:18 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fbf47ff01a573ebb4e3a18c61be50ae3d7580d5233bc905ceba44c7f05697a`  
		Last Modified: Sat, 08 Nov 2025 18:56:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:657151bc7459919868170f80301eb79b909216d1b2b7ce5db69ee062a50e30ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491914c75de9084ee0e025cfce8bc8bb8861bb8485dfba87261e37b74bad68e1`

```dockerfile
```

-	Layers:
	-	`sha256:7c0adcfd77d7c8d429e4ab37eaf736995419724eec1bba72dc625f73a96e263f`  
		Last Modified: Sat, 08 Nov 2025 22:35:37 GMT  
		Size: 3.8 MB (3765580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eda66cb2b8194a2ea88cde8bb510f184c14ec6e75ebe32d4bc41a8ab37d20e99`  
		Last Modified: Sat, 08 Nov 2025 22:35:38 GMT  
		Size: 19.1 KB (19124 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:3729f99f35e9b4d5297df53b93b5d84dd9102b396ef6ace453f10084804e581c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167875653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd1869df34fb46c5f053d6762ffd2e7c5b58e71c53efc5ba47107b838034b06`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 21:49:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:49:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:49:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:49:21 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 21:49:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 21:49:22 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:49:54 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 21:49:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 21:49:54 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 21:49:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 21:49:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:49:58 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:49:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446565adb94c3c0ddf2d551f99efb1cdfcd6ea440c7b05bac7b6b03d99ddeddd`  
		Last Modified: Sat, 08 Nov 2025 21:50:56 GMT  
		Size: 91.6 MB (91610756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f049988664569670562ea25458cab29b2fd08a441aa8bdd03256b1e870e9f6`  
		Last Modified: Sat, 08 Nov 2025 21:50:48 GMT  
		Size: 18.6 MB (18636593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a327a5edef18e4e0ff5a1912ed31375b066773beedf695bde6ad41ef37b20ad`  
		Last Modified: Sat, 08 Nov 2025 21:50:49 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858dabcdd9b179239f53637e0f8dd6a801b060e126b13b54489f23d8f7f0e258`  
		Last Modified: Sat, 08 Nov 2025 21:50:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cc7ecc92af5c740a6a047cc91ff5bb27a048dfd17d2f3c248364dbab39692792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97237aaf13f5fe4d243dcfc0a10fabb8fa6863a3c3b7b0b5e8f9e36e54757748`

```dockerfile
```

-	Layers:
	-	`sha256:782d981c5d6cfd98f740e3f1b66059e36fb078c9a19665841d53f9861f367305`  
		Last Modified: Sat, 08 Nov 2025 22:35:42 GMT  
		Size: 3.8 MB (3766990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:045a8818fae35f1f48ed353697f43005d67cf4f1139a6e4e79aac1edc086a07b`  
		Last Modified: Sat, 08 Nov 2025 22:35:43 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:027275f6d42c91314ad939f53952200c4fc3f42f51a27368416efc753afdece3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161573055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ebc2ba5e19ec358b4218b61e77ce010d7130d174532b3f7da78bc82ce60eb2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Mon, 10 Nov 2025 04:31:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 04:31:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 10 Nov 2025 04:31:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 04:31:34 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 10 Nov 2025 04:31:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 10 Nov 2025 04:31:34 GMT
WORKDIR /tmp
# Mon, 10 Nov 2025 04:33:04 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 10 Nov 2025 04:33:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 10 Nov 2025 04:33:04 GMT
ENV LEIN_ROOT=1
# Mon, 10 Nov 2025 04:33:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 10 Nov 2025 04:33:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 10 Nov 2025 04:33:22 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 10 Nov 2025 04:33:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce920aff3ffeaa315b37b62cd44c0edec347fdf6332b121c2409c04bb3cf227`  
		Last Modified: Mon, 10 Nov 2025 04:37:22 GMT  
		Size: 90.8 MB (90752887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5beb5fe7a216aa5be4ebcad9c479a699c6888eeb5c09c3375f75bf6c3ffde77`  
		Last Modified: Mon, 10 Nov 2025 04:37:18 GMT  
		Size: 18.5 MB (18531024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e51ec7554a0ff142cd94a78480c0e1e01abeff0ded22a87c412640142b37920`  
		Last Modified: Mon, 10 Nov 2025 04:37:16 GMT  
		Size: 4.5 MB (4517790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9157e022271050e30d303b0b60114a23772829b4d40b47efda52c28f6f47248b`  
		Last Modified: Mon, 10 Nov 2025 04:37:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2c18eb93f6274d763d5c5c97c97358065a6ddc77276064c99f1955d3fe8ce3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d815053044562bd3bcd7840cf665b1c735d6a772e0c7b9b2feb31f22cbd293`

```dockerfile
```

-	Layers:
	-	`sha256:fe4c413d8a8fd6179da0502d136c4bfd46aa14e711f08cff5276e1834cbf99ac`  
		Last Modified: Mon, 10 Nov 2025 07:34:33 GMT  
		Size: 3.8 MB (3755166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4b4169a2a96b2c96a27b95fc8ca1cb37098357506a88921f8fc56cd949e7f7d`  
		Last Modified: Mon, 10 Nov 2025 07:34:34 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:84adc195f88b4cda5356191aab8bf7de289bfd892f7aba867564061307f654e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160701471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca42bccac7526d69b3ec5015cd0dd15ce2c713a8cf46db8530d61252eb55ccd7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 20:39:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 20:39:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 20:39:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 20:39:14 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 20:39:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 20:39:14 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 20:39:25 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 20:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 20:39:25 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 20:39:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 20:39:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 20:39:27 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 20:39:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b03eddb65d5a7688f7d8e1526982f728fe30afaeb85c4393004d80fa599ab55`  
		Last Modified: Sat, 08 Nov 2025 20:40:05 GMT  
		Size: 88.2 MB (88210741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea6b04290d27c16523ce6bd2793cea6997f5b2641bb10e6412264d347d3dfb5`  
		Last Modified: Sat, 08 Nov 2025 20:39:59 GMT  
		Size: 18.6 MB (18620243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2806c0f170aff0ad27e731f4211c14fa081581603ff11c3fbe63b986a8159ec`  
		Last Modified: Sat, 08 Nov 2025 20:39:58 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e24fec84ceb18b6cb9e9216efd411057cb7eacb31c4c2cf2b847281cc877d9`  
		Last Modified: Sat, 08 Nov 2025 20:39:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8e393a80c96f726160a670c1688a0036e46ec13363602b662eca4f5705568a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3782635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c1a2ce904b62553d35987146b26cf43492ba2cb8e31d8c9642100f98012c6c`

```dockerfile
```

-	Layers:
	-	`sha256:757a1d856c9f86fafcb2b1831a1aca46f6a758df5c7d1d7ae4e9b8853a7a4eb6`  
		Last Modified: Sat, 08 Nov 2025 22:35:49 GMT  
		Size: 3.8 MB (3763657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f02d1f5df07360f330a18f79b911573c07f3349513d3bfd37632de2d8ef83e9f`  
		Last Modified: Sat, 08 Nov 2025 22:35:50 GMT  
		Size: 19.0 KB (18978 bytes)  
		MIME: application/vnd.in-toto+json
