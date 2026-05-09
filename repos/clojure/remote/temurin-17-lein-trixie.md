## `clojure:temurin-17-lein-trixie`

```console
$ docker pull clojure@sha256:3719973a9211c4d5efc34e25f8a943e4994f4331055de8975825ff8086b2c6da
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
$ docker pull clojure@sha256:caecbb09c900c9a3374d041dc1fef98a705fcd3299700914dcddf397613efa49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218311556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb0b495d6905617023a82583590a7560cb1397f72e42662b2caea01907bce30`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:16:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:16:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:16:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:16:56 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:16:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:16:56 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:17:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:17:11 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:17:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:17:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:17:12 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:17:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82221b23f6e537d5973db3bf22d54155383421572f261e6742cb38fa07285067`  
		Last Modified: Fri, 08 May 2026 20:17:30 GMT  
		Size: 145.9 MB (145905466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2d689a1c933b3e3c265683774359403fa28e2731466d2e9612ef882afc61dc`  
		Last Modified: Fri, 08 May 2026 20:17:28 GMT  
		Size: 18.6 MB (18585583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25462c67b08ac982847c0b9db8f969f0ef1a7578296a590e34afd9523235671f`  
		Last Modified: Fri, 08 May 2026 20:17:27 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d30b2df931fec55f9a7c48b4e8f2f672c87cb585b0f19e0333d9f6f4f3d791`  
		Last Modified: Fri, 08 May 2026 20:17:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8844fe6a63b6bd573da01f0d9a718c9df788483bd7fc7bfd1b5e65fdab939b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4189343d4e528f7058652a064a572a21bbeb1320b7dc3f0e1e90dbf606edda62`

```dockerfile
```

-	Layers:
	-	`sha256:087968a804141e02eb43a311b8ea6b5bde6e9137f4dd484d14e1dbb40fb7ffaf`  
		Last Modified: Fri, 08 May 2026 20:17:27 GMT  
		Size: 3.8 MB (3816154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d52776352797dc1f2113903781e122d082a3bf6d66cef2517e0be9f68ce8e9c6`  
		Last Modified: Fri, 08 May 2026 20:17:27 GMT  
		Size: 18.5 KB (18505 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8786a4b15cf6854080acfbd8b4c66cf94b72f82e3c7b36fe2d48f0c816109157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217457482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d920dbfb2a18f41e854fff3122d9bc9f923416813c47d2cba5226a60afbf8270`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:21:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:21:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:21:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:21:14 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:21:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:21:14 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:21:30 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:21:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:21:30 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:21:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:21:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:21:32 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:21:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64aefe75a8094a79c419218d1133f6361ff3f593b64890b994a808c5dc2bc6a6`  
		Last Modified: Fri, 08 May 2026 20:21:56 GMT  
		Size: 144.7 MB (144724334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a0d06bff4e974d8ce3006f02ae8785b19a058461d27a41b8a4ea681f6b64a1`  
		Last Modified: Fri, 08 May 2026 20:21:52 GMT  
		Size: 18.5 MB (18545526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd92f412cbbf76c6e2c017c1e5f2b247932dbcfde77d5f51db17fec7e7f479f`  
		Last Modified: Fri, 08 May 2026 20:21:51 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d7a29d5821cf3d086e8069974fdf60c901554c495131cc4c75c86b7c4784a1`  
		Last Modified: Fri, 08 May 2026 20:21:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c9cb7eec098fbb19793bd9f8cf211ce29c3083bad20f4f78de951aab85d446e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869ed6f168fda114f999159e85226827e3fe9a1687e776ed62d24d1777b06cd8`

```dockerfile
```

-	Layers:
	-	`sha256:1f5d7a7553aacbf250e3219403be87644d0181efdebb2c2c22add1b5974170a2`  
		Last Modified: Fri, 08 May 2026 20:21:51 GMT  
		Size: 3.8 MB (3817031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:049796ab00957f2a8fab2a6b6f002c17017446e6d26b69bfe756e2f3c75a9a79`  
		Last Modified: Fri, 08 May 2026 20:21:51 GMT  
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
$ docker pull clojure@sha256:1eccb35be5f6d37a993d4d8d33d7ca01ec6ba176fa9648ffa7371e67ddc11e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208427566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61ebc92ba4cfda8de9cf970a53368641c741f1c392cba3d74a6ae3f2a3a87cd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:15:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:15:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:15:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:15:32 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:15:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:15:32 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:15:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:15:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:15:44 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:15:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:15:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:15:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:15:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ed7aaeed1c65fcc4999767a473cf745af3bbd97738b57ccdb46296b8107390`  
		Last Modified: Fri, 08 May 2026 22:16:12 GMT  
		Size: 135.9 MB (135910435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b67b4d1bf1cdcc4bc074f91690af820aacd1d92be8ce95524baef3da385b7e0`  
		Last Modified: Fri, 08 May 2026 22:16:10 GMT  
		Size: 18.6 MB (18626657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a467150d645ee242bad7e982ffde2c6509bf34b1e899090ecb999caf97ecc8a3`  
		Last Modified: Fri, 08 May 2026 22:16:09 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259415ca3477d355c8d3de6e5e47a5db3cf938cd0c6e7b091a300e4839df1190`  
		Last Modified: Fri, 08 May 2026 22:16:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:43c15cff495057b96c6959848cb7f764e07799033a80aaf6c15fde4d6cb9ad9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894c6d85ad7798b211453c5db00b98e4f9809949242a87824d83d777aa739b80`

```dockerfile
```

-	Layers:
	-	`sha256:db47241f7cf47fbf591ba6f2896fa4fc819e204dcb45832d0faecc1dca46e1a7`  
		Last Modified: Fri, 08 May 2026 22:16:10 GMT  
		Size: 3.8 MB (3812581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6b191dee65a8c5133dfd9ad69673f7b4a7d2ee2f88953b8fff5e1f5618285c1`  
		Last Modified: Fri, 08 May 2026 22:16:09 GMT  
		Size: 18.5 KB (18506 bytes)  
		MIME: application/vnd.in-toto+json
