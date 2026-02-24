## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:2fc827967c49e3fa17b77d1155e95b65b1c8797239052431b24e08c7681a1f15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2d26ae6c84e3d378241b4763cc4dd07309cc18eba3428d5e05715dad0f8abfac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144592439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4ec5a239e5ee42309c2a4a96e98d6638208583af34e90f96b56124f95df4ac`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:52:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:52:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:52:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:52:23 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:52:23 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:53:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:53:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:53:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b748e78e7b88335045a7938572d023d71fe0f01480d555a0534a19c0f0ba5b`  
		Last Modified: Tue, 24 Feb 2026 19:52:53 GMT  
		Size: 55.2 MB (55170068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836563929cd8049d62f2da4af6e8e3c50f1490259e9cab28ce571f84c1c1dfc9`  
		Last Modified: Tue, 24 Feb 2026 19:53:27 GMT  
		Size: 59.2 MB (59163348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1710ee35494e6b5a1177b22acc5c27f4b0e0d249fccc3e1fe5b16a78e7be7dd3`  
		Last Modified: Tue, 24 Feb 2026 19:53:25 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6ad5aa0b9c52d6ce4f6989c5ed94d4893963b20096ed46b85f35303292922fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a95eeccb561e1703925efc0f758718e430612418961e02488835cf32c2f5d8`

```dockerfile
```

-	Layers:
	-	`sha256:a8fd7b239d3f10569fb3d3e21fb144a4e4de80ac661d77bbb3b31c8a2ae0f8c8`  
		Last Modified: Tue, 24 Feb 2026 19:53:26 GMT  
		Size: 5.4 MB (5441151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f801a2bb4c638eea814d36ff3407d33bcc5634e6575aa3372588dc054132448f`  
		Last Modified: Tue, 24 Feb 2026 19:53:25 GMT  
		Size: 13.4 KB (13448 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ec92f64e9c714685c6723c84333601ce6d3ec3672410eac2e914dfc8a54f0560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142300077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec7f8f5b2bd45c470209305f28c9dc272c8db0392213d9115cc2736dd24c5b7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:03:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:03:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:03:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:03:31 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:03:31 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:03:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:03:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:03:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe67424060a40349b961269969bd062b5394d4d81765195c0d812a7f3a6dad46`  
		Last Modified: Tue, 24 Feb 2026 20:04:03 GMT  
		Size: 54.3 MB (54251619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986fbf80d3dda26fe9d4c603d5b8fb0a831a00198e89abfde048b4636c2f933d`  
		Last Modified: Tue, 24 Feb 2026 20:04:02 GMT  
		Size: 59.3 MB (59303345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c6d882637d9530db9528ce68fb4198ecee8b366d1569c101f314c061af9135`  
		Last Modified: Tue, 24 Feb 2026 20:04:00 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5a307f64b164cb4431586008b0da54e65bb3aff5f57f8e9a8105f49f73853395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5461949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beef978f45c177aea189f8b331e09ac6f7f4c6fde7d90136fd4897fc0e5256ee`

```dockerfile
```

-	Layers:
	-	`sha256:6b01f3afc5fe23ff818058fa4dcb3bd6d89b7dae556e3b25c359ed58a9b8a4f8`  
		Last Modified: Tue, 24 Feb 2026 20:04:00 GMT  
		Size: 5.4 MB (5447583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0648a67159a62e2bc62cde9a52c6ed072aa6395d57edf6de49d9be9eb9024c8b`  
		Last Modified: Tue, 24 Feb 2026 20:04:00 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json
