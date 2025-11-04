## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:c143b8d571491631a5dc06749c0bd48b4713d70490d78f670b028833405c6d57
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

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:b1aba3c4faa6dac0b9a5fe1fa8a7b0d8e712cbfeb9c012d5f87a82a9958bb34d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275286312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc5558bd80cbda1736fa4136afde0e3e2bfbb54429f5f107993d50f37462923`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:54:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:54:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:54:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:54:18 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:54:18 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3812dc7bd6577a1356c0fb2e7d4144aadef1bebe4624d2f350847010ba1e45e`  
		Last Modified: Tue, 04 Nov 2025 00:54:56 GMT  
		Size: 145.7 MB (145658308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fc2e321027609f4c1122ab85039379b8188ddc4b15aa9644dde6e7513276fc`  
		Last Modified: Tue, 04 Nov 2025 00:55:10 GMT  
		Size: 81.1 MB (81146306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e558a01ffc589c8f5635651693c209a414f9b89b7020618d9e3b54c4965aae53`  
		Last Modified: Tue, 04 Nov 2025 00:55:01 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9139150985cc3b8cb40459cf64a2ecc92dec09f7109ddf1769dd8a7f54c9e018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2aa51e968884376f07ad445ca7d8c2a33ad55b8cb852de413efa5e5375f49a`

```dockerfile
```

-	Layers:
	-	`sha256:742516f6c1580515d3f7f3533d036dbb9bb927ea49cee5f997c6a8a5d5f61229`  
		Last Modified: Tue, 04 Nov 2025 10:36:05 GMT  
		Size: 7.4 MB (7395031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e027bc0892568e7b3eb3e99fbb0ac006c8c81b45bdf7c84e7256e97e79f78e37`  
		Last Modified: Tue, 04 Nov 2025 10:36:06 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bbac0d034a921a74deaf6fdffbb43e7dbfbed195a7e64c92d1b624393e9658e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271851503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e127472340e6ae03dfef6fb540b30da52d2bf3a10fcfa53b899234db0d36b13`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:54:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:54:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:54:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:54:49 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:54:49 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:55:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:55:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:55:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39ca20375766e48a6aa8f63cfbeb9eea64e5503ea5d7236532f1e0cc83a9c98`  
		Last Modified: Tue, 04 Nov 2025 00:55:27 GMT  
		Size: 142.5 MB (142460569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b7686d95f94388cc1b59845cbefee4c886f3e4cdc9905664f9c01c47d643c3`  
		Last Modified: Tue, 04 Nov 2025 00:55:41 GMT  
		Size: 81.0 MB (81030814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d59e66fb560746952d87f4bbd5db2e0664a2454f3b1214ba3ebb5ad9c8febc`  
		Last Modified: Tue, 04 Nov 2025 00:55:31 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c6178a818921b077e4fbb9b7c597d1fd8a2684bda3baab63a34899535b80ce16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7100720ad9cdf309c867a452b684295709f0b918c055f04903b7a0da331c25e`

```dockerfile
```

-	Layers:
	-	`sha256:606e1179edade030522bf7c5c8d16b9bf9738c636b84670332148ab1d88d8968`  
		Last Modified: Tue, 04 Nov 2025 10:38:00 GMT  
		Size: 7.4 MB (7401412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afef414ffd7c28eef5683604873cfa8cb1f5f955498ae12aadcabd83b6e14e88`  
		Last Modified: Tue, 04 Nov 2025 10:38:01 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:a6088ca8f1befcdf5e3a9d3dd5a22f9e4896f9ef5fdfe2bc3551b5884f8623e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272167176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e94521ed4495e740f1a12b8860995becf32ad9f024b736c8182a865a79c3dad`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:45:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:45:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:45:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:45:07 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:45:07 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:47:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:47:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:47:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752beae8309024b8cd32ca68c0c530c929561131d8591dd3246d3fecfb09c73c`  
		Last Modified: Tue, 04 Nov 2025 00:46:30 GMT  
		Size: 132.9 MB (132853185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38987b0ac55785dd9aacfd012e85af1491a5d62310105e522e782f5675cb7e5e`  
		Last Modified: Tue, 04 Nov 2025 00:48:49 GMT  
		Size: 87.0 MB (86986064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1254a1b8d7de60a2ad754f7bb0e4d34d0bd4c803314a1d19fa7a265dbad740a6`  
		Last Modified: Tue, 04 Nov 2025 00:48:40 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a3d0e70402a1c2cb2158338d129eac7f5824e4339c970c9364ea5825e88805be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb156e36a52a696eab90244d718379840c578bc16ff5f8adfaad4fca6c103bd0`

```dockerfile
```

-	Layers:
	-	`sha256:5d162e30f0461aa6017b722e89e5cb2329544a8e6b30b7e44da2e384e7a0b64e`  
		Last Modified: Tue, 04 Nov 2025 10:38:07 GMT  
		Size: 7.4 MB (7399630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e743ab4d7486d8eeffaab4766f407bc4932f29c51ef49063e343a0e172dc2078`  
		Last Modified: Tue, 04 Nov 2025 10:38:08 GMT  
		Size: 13.5 KB (13456 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:85d052adbfe974d19d4d5bdd21b36ff7c87c369057aebbb62960ac1a55dcc63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252717510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9008d0cfe792839cbd1348a5951e3fe2e16709f215301d259e1fac80934e732e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 06:18:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 06:18:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 06:18:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 06:18:31 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 06:18:31 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 06:22:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 06:22:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 06:22:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ecfa4c790ec4992e2fe9ce4c2639e46c2ce58b9f5a1669edf66bbac6c7a549`  
		Last Modified: Tue, 04 Nov 2025 06:20:04 GMT  
		Size: 125.6 MB (125622153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5ba988504b878c5a1e6cfcff428ab41c43dee981028e26ff0f6ed55de28646`  
		Last Modified: Tue, 04 Nov 2025 06:23:03 GMT  
		Size: 80.0 MB (79956618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf33ab9d32046ac5ac7b06270ee87d087ab05f09e77f646985b4f828da783a87`  
		Last Modified: Tue, 04 Nov 2025 06:22:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7f0e38c12910306a46273eeb1218331d3d695447d032b1891b397a8f52bc01a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd4626f1d304ee9fc2e1667775a627555b8bfb15ecc387760347af418a837b3`

```dockerfile
```

-	Layers:
	-	`sha256:3dfcd8d66d11832b398120bf80655c001120bf1fb1967de9bad5d9324259376d`  
		Last Modified: Tue, 04 Nov 2025 10:38:14 GMT  
		Size: 7.4 MB (7386354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f60eabfb322ea5168b9b449c0bdaa35403d3255b1ea4427330b4bb442702e669`  
		Last Modified: Tue, 04 Nov 2025 10:38:15 GMT  
		Size: 13.4 KB (13408 bytes)  
		MIME: application/vnd.in-toto+json
