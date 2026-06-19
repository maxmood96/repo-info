## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:1f2842835e4b5b5864eafc6b3ad4dac9318202de863859a1ab8faf7f3cbcddfa
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

### `clojure:temurin-21-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:6eba884df90d96b09d8fb4c5503b49b012d53f26aafe90f9f7774d50fedd9b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290004043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2c3bebf52028bc30d3eb32977b38da1e73d6a4f5d14f81f80944b2e88ef890`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:19:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:19:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:19:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:19:20 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:19:20 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:19:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:19:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:36 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36140704f6118dd487b331d51e6cdee0e4005e9f7e474bc7588f4b1185551eb0`  
		Last Modified: Fri, 19 Jun 2026 02:19:58 GMT  
		Size: 158.2 MB (158166919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7fcd271fb4ab5833476cafd4faf39dbc27a972e159955583081cdf187a56a2`  
		Last Modified: Fri, 19 Jun 2026 02:19:57 GMT  
		Size: 82.5 MB (82518964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4446eca6228b80a14601fc43b6964f8012744c7f5a6869d646772511b48e1719`  
		Last Modified: Fri, 19 Jun 2026 02:19:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01b3a4d8d2c0a1101a7f6f7b7c3b05593a59bc07c11b4d69a2aa765595c0a6d`  
		Last Modified: Fri, 19 Jun 2026 02:19:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3d4d2465a9132c80f44abc80c9f5fc5a275b6326b8e9f94f8d15754d70a4d471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05225ff9c219b2d6569abfcd4a04bbb95d317400d3f1ee712d0f83f1b251fd2`

```dockerfile
```

-	Layers:
	-	`sha256:ed8ea6973f437b8fe303508fdfcba35d6914e6d99e19108e1f9180d4bd40e48d`  
		Last Modified: Fri, 19 Jun 2026 02:19:54 GMT  
		Size: 7.5 MB (7470623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af328edf4c28463648ce39860bfbb153556d112ace1c87548f1ccd0a5a6fbef5`  
		Last Modified: Fri, 19 Jun 2026 02:19:54 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d2eba69c563d3d304d8a5a2dd814a84d6bfda7bb1b04bb49a172ee4a04cdb21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288478897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2a72e7020eefcdfcd3d32c2be4a6a12c134295ed3dc101b37de58554c7f6d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:19:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:19:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:19:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:19:55 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:19:55 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:20:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:20:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:20:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:12 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67e43a1e14d9e3c0ef9f4f0ee02cd052b9ebbd1076b3fd26ab93c18f864ca84`  
		Last Modified: Fri, 19 Jun 2026 02:20:38 GMT  
		Size: 156.5 MB (156461275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66f02de2e288e90cc79ab842a1de3c8d682064143764d1ce7607dbf12e6cfd2`  
		Last Modified: Fri, 19 Jun 2026 02:20:36 GMT  
		Size: 82.3 MB (82338413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffda8b3cd5ebf6289bf7e13f37f3cfd9e1ba536bc295360e090d983d0c3fee1`  
		Last Modified: Fri, 19 Jun 2026 02:20:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874f940bdfce3e27038d646f64bcb4057280a1e1e3d45b50561fb09b3d8a1f62`  
		Last Modified: Fri, 19 Jun 2026 02:20:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f5ee83c1dfea0e15de3d87ea16405c2a5daee6ea311542d3c14fb371c006da58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef31dff3cce97a40a65e8398403ddc620bd8e45dbf26512f0a288ca0ff165594`

```dockerfile
```

-	Layers:
	-	`sha256:7401921ee3e6a5bf91cc9277e109231a52f4ab0a2dd365eec17b393b1a31dbb7`  
		Last Modified: Fri, 19 Jun 2026 02:20:33 GMT  
		Size: 7.5 MB (7477016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b240135add6be73445cb719da06a9d85c5b25439ef8bca116f9ae9c4e995e23d`  
		Last Modified: Fri, 19 Jun 2026 02:20:33 GMT  
		Size: 16.0 KB (16024 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:b965aaf60c1a0e5bf5ad011a45ca72a7c9e85cac56c93a195264f26b6bed2b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299420806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be82ec9920098a67359cb225ce4735fb1a330ca59b82a85a3cb36d136463992d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:58:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:58:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:58:45 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:58:45 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:52:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:52:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:52:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:52:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:52:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb31c7f870ef8ec8aee6455f55c7a957b94017aabba051fbeec8aa80bef9255`  
		Last Modified: Wed, 17 Jun 2026 00:02:33 GMT  
		Size: 158.3 MB (158343224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d5d0235fd16d40608b3186087d69ce25cc2cbbb480e5865b7a5f1882ffdd64`  
		Last Modified: Fri, 19 Jun 2026 02:53:31 GMT  
		Size: 87.9 MB (87938605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92ce4ebae61ccd63ed9b2c04de007b9fd395fc289557d9c182123b9ce73d413`  
		Last Modified: Fri, 19 Jun 2026 02:53:29 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492a9fae25a8080a352035d00d315acb56c2eca86e98ab94e5dc659472c2c44e`  
		Last Modified: Fri, 19 Jun 2026 02:53:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:de6285dc3fa1bfe085462f69451707d7687a096d723f7def4a0925ca31f54c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735696cbbb6b63f6d55f55510d7a9c64602a3d5b4bf065148c4aadd466db6eaa`

```dockerfile
```

-	Layers:
	-	`sha256:83dbc31bb9bc2c127ec197d6936b24d9aea5377da90168e30f05743090229d69`  
		Last Modified: Fri, 19 Jun 2026 02:53:29 GMT  
		Size: 7.5 MB (7475044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1524369aed5658e95d33eb9a3726b3d9c1c2693d2938595405b368b7c31af379`  
		Last Modified: Fri, 19 Jun 2026 02:53:28 GMT  
		Size: 16.0 KB (15956 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:8198d8beab89323d42362f2f9ed19b6ed387a693731c7d8a8bddf5323cd8eacd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 MB (280277559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec49c50d778b982790e3d56b4003852a3f2e342070045117aa53a6930ca7102a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:38:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:38:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:38:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:38:00 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:38:00 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:20:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:20:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:20:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:32 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c55ae26073105dbb12b878ce93ae33f8d0835ba25a28114c5d1f6b6e4fbfe51`  
		Last Modified: Tue, 16 Jun 2026 23:39:40 GMT  
		Size: 147.4 MB (147388349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a365f16057f8f0104e425b38decce4c8868b6eb0ad39712a690895e1432ce5c8`  
		Last Modified: Fri, 19 Jun 2026 02:20:57 GMT  
		Size: 83.5 MB (83502275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a21b1a4208cece9079f3bb95cd2de6e00a4a9dd0298d8d9f8981fa718609a6`  
		Last Modified: Fri, 19 Jun 2026 02:20:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961efa857c9c03a081ad890cabb2dc65d062e97555ab14358cba6555879536a4`  
		Last Modified: Fri, 19 Jun 2026 02:20:56 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f065951a1f821a66a0d6f527e2329a6cfaea8d12ecb02c927820225bb4ce38d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fb13d0492f09902fcc13c92af4a42b90d86183436d1b073f4d6d21ec133ebb`

```dockerfile
```

-	Layers:
	-	`sha256:c8709b358ce9100c286796a158163c424e141cc205a342c5c3720d73d281f2fc`  
		Last Modified: Fri, 19 Jun 2026 02:20:56 GMT  
		Size: 7.5 MB (7466545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c0992c91d8646f8a220765f1e142ae0b095541856a6ad0a2a76901fe31ed5b2`  
		Last Modified: Fri, 19 Jun 2026 02:20:56 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json
