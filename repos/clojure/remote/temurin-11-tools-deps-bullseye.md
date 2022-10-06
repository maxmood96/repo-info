## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:fd88823739d351f250453e52c24fd3a2b011116ad6b55e1e25beef6e0e97f96e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:adfe4867d0e8d63e70c684f190e35d18bca263dc89ae9cf36794a8e4288872b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300468526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127a397f7d81e7d5e9b484a3acc7f62af15739cb565d8791ac8b789ef108d040`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:30:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:50:38 GMT
COPY dir:e3c63d67b32fccda756dd62000a0cf47da966d18fe6f1f25cd1f37b60881f0ec in /opt/java/openjdk 
# Thu, 06 Oct 2022 03:50:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 03:54:31 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Thu, 06 Oct 2022 03:54:31 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 03:54:49 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 06 Oct 2022 03:54:49 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 06 Oct 2022 03:54:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3983f63d3e4b8776b5231e0bc9c49c468ccec1c53f32fc062195bdfef9cc693c`  
		Last Modified: Thu, 06 Oct 2022 04:08:30 GMT  
		Size: 198.1 MB (198125022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279c2707da25a1f81da9208ed1993ab5b0e7b7feb1fdab4fd51837cf69573b61`  
		Last Modified: Thu, 06 Oct 2022 04:10:33 GMT  
		Size: 47.3 MB (47296638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25dfe56c54c414c95169f036bda509e1385d6761aed85cfc41f562bb669a0bfb`  
		Last Modified: Thu, 06 Oct 2022 04:10:27 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b1a9eac7a8ab17e5741eae69c5a47d2eb9130b381f9a902f52be0e5fefdbd331
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295654461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2925bebb6dfc9f4214a33997a616c27660a525698303158eb0c1ea35cfcd9cd`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:31:52 GMT
COPY dir:0dc06d70d42a32ae203bdf41d3806f1204b90ca101c4efe4662ba862f2c76b8a in /opt/java/openjdk 
# Thu, 06 Oct 2022 02:31:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 02:36:39 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Thu, 06 Oct 2022 02:36:40 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 02:36:57 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 06 Oct 2022 02:36:58 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 06 Oct 2022 02:36:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2152e7f09463e6c7e89c91d7854a893cfa62910bf4ac2cd6ac8b299794427865`  
		Last Modified: Thu, 06 Oct 2022 02:57:06 GMT  
		Size: 194.9 MB (194866576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770130c3047111021b4d9c1b0c615f78da8235a45e6073720bdabffc808b9bd7`  
		Last Modified: Thu, 06 Oct 2022 02:59:25 GMT  
		Size: 47.1 MB (47086641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5445f30baaaf228c33008afad415d676e100a97d1af6df27b20803aca1245da3`  
		Last Modified: Thu, 06 Oct 2022 02:59:19 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
