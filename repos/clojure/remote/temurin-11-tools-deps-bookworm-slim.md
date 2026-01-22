## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:bc637ed436a105aa2f0457ef9303ee6b5ae91ee390a5c41cbe948d44f85ae90d
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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3e8ede65a553aa679ed7db3b1f8bbbe60b61576955b0056c33832fbe3ef1c884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242872530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a5936c15279b119373cb6f9a438ab8bacd2c4dcf0cc7e5f0bfbf2b83081465`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:48:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:48:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:48:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:48:58 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:48:58 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:49:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:49:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:49:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4306e15446e003068d0753b998d75f76e28c28044de2eacd7a293adca5bc4504`  
		Last Modified: Fri, 16 Jan 2026 01:49:35 GMT  
		Size: 145.0 MB (144966614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5106d5efb9eba76d3b0496ab80adf7f0bd7d689160907ed6899d6358c67e8b`  
		Last Modified: Fri, 16 Jan 2026 01:49:34 GMT  
		Size: 69.7 MB (69676702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9da35d6b5e6f09bb6d3a939d5261e365715a673970258765fb3a774ed9e3b4`  
		Last Modified: Fri, 16 Jan 2026 01:49:31 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3ab6fcd9fad4d1487b810d8c917bb46789745b81d3f574b3b8eb886034ec3b49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b731cc3142453adecbf49802491d1dd6a1ce452f5598d88047d9f99d25ba95b6`

```dockerfile
```

-	Layers:
	-	`sha256:74e2fcd65f0f6cdd43472918d07d58f15e1268bbb1057bb349965d9942a6aa00`  
		Last Modified: Fri, 16 Jan 2026 01:49:31 GMT  
		Size: 5.1 MB (5133539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32470d8b6ca4933fe061bd6efe8a84240f3b7137e7d9affdfdfc6b34cd12678`  
		Last Modified: Fri, 16 Jan 2026 01:49:31 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9c746e2af9da69b793e6d5b5431f8408160f287999117d1531945b8b11d4c183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239510985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfd818c486e061ac8e1e47a028bdfbab78807d408654b735493c46a1b1cda8a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:49:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:49:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:49:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:49:56 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:49:56 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:53:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:53:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:53:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4310d5c299f93b8b4bfe0617d4d41bcb16d50a54761a167feee4b4968de5027b`  
		Last Modified: Fri, 16 Jan 2026 01:50:30 GMT  
		Size: 141.7 MB (141729867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3373d0f23c9880b230793ad6795a07261b37a131a59dd8ff8bb6efbe3a89b894`  
		Last Modified: Fri, 16 Jan 2026 01:53:25 GMT  
		Size: 69.7 MB (69672584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58691315f4ab96ee51a354b3f10dd4201c1009c259ad7dd48bed3bc0769219a3`  
		Last Modified: Fri, 16 Jan 2026 01:53:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dad34d2f30c6a1cfa7b2dc85900461eb87dcc468a5a68b2bacd851f91b3a96a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606fccda319bc79f1fcaf3ea24a868ffea73cc0d69e82ff10dba39aae01f0175`

```dockerfile
```

-	Layers:
	-	`sha256:6704dc95f3f7b1efeb4a24258c337dc17e83e0b9a7bed9c0e969a1134e4b040b`  
		Last Modified: Fri, 16 Jan 2026 01:53:23 GMT  
		Size: 5.1 MB (5139918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ffb499e455875a66a5f9eef737e44e0fc749d2a1c66e3e346edd53d126bf366`  
		Last Modified: Fri, 16 Jan 2026 01:53:23 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ae3161f01a476d290d426b02bef35ff4beb362d3f3a28dd262a9d5af9bec5de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239661768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0ba640f563d2e8f3c54bb97cd65b610922fe44dd7a357acda5aa7c6efa5cd1`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 02:57:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:57:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:57:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:57:41 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:57:42 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:05:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 03:05:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 03:05:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:03 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68470ec8404f299576dbb308d66a6189dbad0deedfff83c1babcebaadce578a`  
		Last Modified: Fri, 16 Jan 2026 02:59:18 GMT  
		Size: 132.1 MB (132079791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32752da1d663412fb5d4afe17cd7e970896ed86418eca58d1124b2687480e374`  
		Last Modified: Fri, 16 Jan 2026 03:06:27 GMT  
		Size: 75.5 MB (75512623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2363957817e0bbdbfa0b2ca814dc24138907dfbba8e2707052c73f72728ad2d0`  
		Last Modified: Fri, 16 Jan 2026 03:06:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:21d993dbc3ac6d1ce69e2d5f68b5f1ae7286d58a5393983cb7608d18531df0cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f27d8b0d2e7f65d62a74dedcd28434399fdd317126b092b7340dd9465083b2`

```dockerfile
```

-	Layers:
	-	`sha256:9fb81238e6b104728f6d739b24a0610e044231f07ee5ad8ad3ec05149366bc7a`  
		Last Modified: Fri, 16 Jan 2026 03:06:22 GMT  
		Size: 5.1 MB (5138082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f4c5d3a755062691a3922e776c744845cfdbd8f636262a8a6df838dcf470efe`  
		Last Modified: Fri, 16 Jan 2026 03:06:21 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:eb8f0f99a19da4c5fbd4f80839c47bd43e25bc1f543d8f6271df6a8f14e0a633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221068585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52ba7ce02cea319c8c488d4eb1269c56ff1d42cde4f61a105c9dbe643276395`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:10:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:10:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:10:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:10:27 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 15 Jan 2026 23:10:27 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:11:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 15 Jan 2026 23:11:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 15 Jan 2026 23:11:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:08 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6afc4974fb908d05b5af46341b93ddf48b979f8e96d01fa55d603a755a876a2`  
		Last Modified: Thu, 15 Jan 2026 23:11:07 GMT  
		Size: 125.7 MB (125694860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8051939983e78f2064a7b2fef293405c7c6dda06e7053e6562460b1835cb9c13`  
		Last Modified: Thu, 15 Jan 2026 23:12:18 GMT  
		Size: 68.5 MB (68488667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf950b6049fd301f72a53e7d3e05258236e3ef6ed08ba4d71915b10e9e87a8c`  
		Last Modified: Thu, 15 Jan 2026 23:12:16 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:29094a33a7ddd9de33c8aa36f05e6903225dd47ddc2dd2e3789ac61e9d22fd4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e421cd4925bb44368ea65a6347c95b71253f35c8c07c789948aacc7f09ab3c`

```dockerfile
```

-	Layers:
	-	`sha256:2582d1e5a6c27b9f585af4f54e0f3a9dce7f8dac70efec552fbe44fc914ca924`  
		Last Modified: Thu, 15 Jan 2026 23:12:17 GMT  
		Size: 5.1 MB (5124864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc4ee0621fe64c29f316fc15c07d79e90e8bdb4357fa2f9a6956b6bf7f563eae`  
		Last Modified: Thu, 15 Jan 2026 23:12:16 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json
