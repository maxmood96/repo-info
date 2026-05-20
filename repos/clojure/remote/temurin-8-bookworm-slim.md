## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:3dbc518918bc2a16726608c17eff25914c38822fbbf0ceed98e1894beebe678d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:65602697648613caa1a92181ab6484c3de86890fd11def07aa42e6286d73cfaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153170411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54355c432955aa424a052c6dbc5de0dfd4ee39390380fe66239c28faadcdea87`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:56:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:56:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:56:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:56:16 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:56:16 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:56:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:56:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:56:31 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f608e0f60894815ffdd38f97ac3b9eb178c2a5e741c5b9abf677144abe9211`  
		Last Modified: Tue, 19 May 2026 23:56:48 GMT  
		Size: 55.2 MB (55198723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e78f5ff5c4c34e12df9c449123e0c27490f8ba86c263de7899e63281e22698f`  
		Last Modified: Tue, 19 May 2026 23:56:49 GMT  
		Size: 69.7 MB (69737499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f106e69162fe5703a2f5dc051a43df7b00e62cc12a877b180721e880da35f1a8`  
		Last Modified: Tue, 19 May 2026 23:56:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5f2a9b70b40e677f123ba9872e8401546c9b90dfb2534e71ce8170d0d84a2dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d526e73921d6d1ee1df0688e7c3e941d88fee6d723631661176043f4b05e881c`

```dockerfile
```

-	Layers:
	-	`sha256:6ca267992e0933c204ebee852e93096cf7351c0e5443bfe5e2c30df3a2b8716b`  
		Last Modified: Tue, 19 May 2026 23:56:46 GMT  
		Size: 5.2 MB (5237174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:164330314cb3bfa6e1b5315478703889a19b8e1eeb5348183e46e37d5da83a36`  
		Last Modified: Tue, 19 May 2026 23:56:45 GMT  
		Size: 14.4 KB (14402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c3cad081657c408442d4dbbd83afc8f0b5d8368c95169b3db29cdbb5190f1a65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152120110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01980ab4b65f883a3db3673486b4b4e0bbd525ac4308a67418bfbc5f2e272dc0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:03:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:03:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:03:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:03:41 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:03:41 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:03:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:03:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:03:57 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c5bc76a88fef438313c3e302c0b6aafc604c3697662eb5fc6774928fab8280`  
		Last Modified: Wed, 20 May 2026 00:04:15 GMT  
		Size: 54.3 MB (54272927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84755eafc7ddd0d77853285b0e9e00189f933605b9cf7f9babf66479f6717080`  
		Last Modified: Wed, 20 May 2026 00:04:15 GMT  
		Size: 69.7 MB (69731495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932ba42874ac5da3c204dc64b835bd5776cab042b109b8b88d95d1123ff24d93`  
		Last Modified: Wed, 20 May 2026 00:04:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bdc76ea97274bd1cd74f7df6a2a0efd678a9a614ff87997381664c403701a497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1c9175d4f1ac7dd227c259ecbaa5ac69fb591681d698c0e32cb28e9198492e`

```dockerfile
```

-	Layers:
	-	`sha256:18dd46ddc2aa632c4b14bc9b21a7b66ce86a12d4ff75a9594abadaf84f9113ce`  
		Last Modified: Wed, 20 May 2026 00:04:13 GMT  
		Size: 5.2 MB (5243635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1c6fd0462c7ac5e1f12b3bd4b2caee011eb2b76df8a50ec1398c99fac15243`  
		Last Modified: Wed, 20 May 2026 00:04:12 GMT  
		Size: 14.5 KB (14520 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:11eb2292bd980496a897702b5e8090dec2b89586206753886a38405542c2299c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160317395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1a07816f13ed8ffa9a6dd858a2896327d695b78a302c7a6ebddf70b526dafd`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 05:43:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:43:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:43:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:43:16 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 05:43:17 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:46:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 05:46:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 05:46:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e7d2adee20295d3b262cdd2cfe943ade2d2c668cc3b4db782efb9526da7915`  
		Last Modified: Wed, 20 May 2026 05:44:13 GMT  
		Size: 52.7 MB (52669153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5443ff3ff57c34d01ff273cd101b5138f02c2a9c942b568971671e4da6f26e0d`  
		Last Modified: Wed, 20 May 2026 05:46:44 GMT  
		Size: 75.6 MB (75571855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3611e2ff1a7c3315e89aae8603d2aad4b0f1c1d907bd9965824db747b602eea8`  
		Last Modified: Wed, 20 May 2026 05:46:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8480c24244dffd78cb3029f1b4822e295b616a40033ba1f94d6f43ac790ce063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd78cb7b008c0da5850f934683f78a445ab81bbdc3b4960f488d261676db9c0`

```dockerfile
```

-	Layers:
	-	`sha256:b9c84cb459c93c1a666299899e5895584f34700e7196182333d565c2507bee3c`  
		Last Modified: Wed, 20 May 2026 05:46:41 GMT  
		Size: 5.2 MB (5242927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bbd47cef4ee7ef59473945dad63d134fba46309585b52383f387abca5bc7ea8`  
		Last Modified: Wed, 20 May 2026 05:46:40 GMT  
		Size: 14.4 KB (14449 bytes)  
		MIME: application/vnd.in-toto+json
