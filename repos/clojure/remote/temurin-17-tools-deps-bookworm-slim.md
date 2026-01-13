## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:874e234303ef91b0561db8a0a82f641e3e14f5e38a7117b8af61450c6b598709
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

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4c374e6943824e02a9788f8bf15fb6e6dfafc12b39c663ef1c6a2efca438e7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242754530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85e87c4d8256f7e2b3642575a3ed3a60b1f9d509b2777aaa86591ca99e43f27`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:31:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:31:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:31:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:31:59 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:31:59 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:32:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:32:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:32:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:32:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:32:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224b381186bb323cf85cf51cc38ce4abf495a739b7b4c9ef4e3b5ce33a706c68`  
		Last Modified: Tue, 13 Jan 2026 03:32:35 GMT  
		Size: 144.8 MB (144847947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa382fee461de5796041d0f745dec649ef84b8ea5860459e0cf6449b6cd6c80`  
		Last Modified: Tue, 13 Jan 2026 03:32:49 GMT  
		Size: 69.7 MB (69676972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3d193d54f89d24a4eaf8afb20fd360d087ca76369759eda4a8d515d308d604`  
		Last Modified: Tue, 13 Jan 2026 03:32:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ee0761e6579cf9c2f5f88fe7e6cd88dd9278f2e0b6cea7b58bfd2373d33d97`  
		Last Modified: Tue, 13 Jan 2026 03:32:42 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c00c47733d11b6a2cacfbc360c264d48face3094af1d818dc1658ffaa0c6b433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9725e3361304a5a9d32011164c0eeef5d89ed44754673abba27f9af12d38f25f`

```dockerfile
```

-	Layers:
	-	`sha256:a243cd514291b883867e141cb0006322f7b667ca53ae8e4f333f3164e5f2bf0f`  
		Last Modified: Tue, 13 Jan 2026 07:39:27 GMT  
		Size: 5.1 MB (5113400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2a4c286b93aed4ecb26c154eeee3ae50bb7b9225198f83738d07cd9c5495bbb`  
		Last Modified: Tue, 13 Jan 2026 07:39:28 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6c690039395ae4648dd7f6d259f34ba7b017581495a397c474a7810f1a3ed4f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241461426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de060c07b0734a7fe8f5fa411f40df39d71dad90230d5332f279e41255bdd86c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:35:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:35:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:35:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:35:30 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:35:30 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:35:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:35:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:35:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:35:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:35:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e0e00caff936c90d25452dfb35ffae7a2a199cc703a3313374c5de48cc11a2`  
		Last Modified: Tue, 13 Jan 2026 03:36:08 GMT  
		Size: 143.7 MB (143679910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb5798fe57f029859e5beec30a416d97db429703badffd7cdfedfa3ec32babe`  
		Last Modified: Tue, 13 Jan 2026 03:36:21 GMT  
		Size: 69.7 MB (69672590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6549903da259c56365927f481605c38deace1f433513e1e0dbd6313bc5e4ffa`  
		Last Modified: Tue, 13 Jan 2026 03:36:15 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d892691c9f751b7dee30b41d57b5c4b022fa7d3bc387deb43f098e9d34b6432a`  
		Last Modified: Tue, 13 Jan 2026 03:36:15 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7ff241835c1483e45d58ca2c4f0c593f1f7f357618157e09e9612f1e72cdff43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439e4482db5fad79f0f33df510b0eb0d3d1f403d01e59ea4c373da154ecb6b8d`

```dockerfile
```

-	Layers:
	-	`sha256:33a478804e51dc234b2a5f76faac2d31787e13624804bf3273f191523f014a27`  
		Last Modified: Tue, 13 Jan 2026 07:39:34 GMT  
		Size: 5.1 MB (5119161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47d1961eba8aa77cd3e46d80739d9e9efa0861f177e44a1dc532625db03266ce`  
		Last Modified: Tue, 13 Jan 2026 07:39:35 GMT  
		Size: 16.0 KB (15953 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c17cab168fce5408036c249a648c58e93c0c5e0a9048cd6d22a3fa570146e589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252105247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194640bcbd04bc1e5fd26b7d1494684cef168385fcd6ba7ec126333f1f2dd7a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 05:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:17:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:17:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:17:49 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 05:17:50 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:20:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 05:20:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 05:20:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 05:20:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 05:20:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c662a1580b47c492cf3baff3cc57fac4e48d81084d9a9ed82cf007a60ca93b2`  
		Last Modified: Wed, 31 Dec 2025 02:31:09 GMT  
		Size: 144.5 MB (144525257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff4709ba829cd9c55a21fe3f91d66db8013aa45695d961458945599cf081333`  
		Last Modified: Tue, 30 Dec 2025 05:21:09 GMT  
		Size: 75.5 MB (75510105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ea468b25f0839bd9228f493169609a5a0ce91beb643748f72ad42c5375c8c5`  
		Last Modified: Tue, 30 Dec 2025 05:21:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658ee058d9ff05f302d8a06534f6465075e70696cf24a32268ee41e925f7adc3`  
		Last Modified: Tue, 30 Dec 2025 05:21:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1cc4b63652e80e7277813ba4a2beff1460aafe383108cec114370f3b0f06d05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8014d5077e725ca061a647218a298f8c7f71590fb749c3f32145e42b56175e31`

```dockerfile
```

-	Layers:
	-	`sha256:cb72cb025f892153ea19523a08e045e039b589b9d7a4dacd747333f753f3c4a1`  
		Last Modified: Tue, 30 Dec 2025 07:36:14 GMT  
		Size: 5.1 MB (5118548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c03296bcf7a4581b9424a3fffa082e42277f42113784191b394c5a2bbbcf093`  
		Last Modified: Tue, 30 Dec 2025 07:36:15 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b7027fe9c0e54d5874158bd29a5a09c52327db8f9ec64eb61e4eb28e3c471c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230233230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf1f760b3df842459bf5c15fead51a700d8306f5540df1fe8bf14a428512f9d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:03:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:03:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:03:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:03:40 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:03:40 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:03:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:03:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:03:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:03:53 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:03:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fd087cd33abb835a3d928d9f2e0a964896748847afaf3e2058ca1eb9f5d830`  
		Last Modified: Tue, 13 Jan 2026 03:04:37 GMT  
		Size: 134.9 MB (134859046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a29aee86722544fdf5681abf808d7d02aa3481de0b558ba15faf181135eaf1`  
		Last Modified: Tue, 13 Jan 2026 03:04:32 GMT  
		Size: 68.5 MB (68488731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91f73e993590a91d2bcc5943ffdc45d326d22a75f6f982a5baa9d933fd3c62c`  
		Last Modified: Tue, 13 Jan 2026 03:04:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91dbbe09d9d972b333767d4dbb4c40dd50747dfb57bedff4b9b56ccb19255cad`  
		Last Modified: Tue, 13 Jan 2026 03:04:27 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a04c792746cb72118209cc0b2ccb2648b26af5e68c321dcd5d086326ae920b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea0d209fb097705fff52eabcdb55cb7a6629697b910dd7bb840909d49f01604`

```dockerfile
```

-	Layers:
	-	`sha256:c252ed99d76af9c2a61eb497e24af51f3d53b767a0e3784e89426384c34e5dc0`  
		Last Modified: Tue, 13 Jan 2026 04:37:18 GMT  
		Size: 5.1 MB (5104721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446fec8a31943df7bab4e480ca4dd0315c1e1b1a2520213f34b420463b1c2b98`  
		Last Modified: Tue, 13 Jan 2026 04:37:19 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
