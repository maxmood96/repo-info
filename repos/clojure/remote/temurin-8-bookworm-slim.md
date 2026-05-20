## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:9164842c43618c4a1582686512d10603f7dcd634936cf70aab323fb468c773e9
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
$ docker pull clojure@sha256:5366255e6d44fc28cb5b4a221db5fe238c64a1c897d7549c118d568a0fdac6b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160313639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be08f5bfa890e2c5182dc414e976330ac05d95f0c1eb6bc3ad63e25bff96f99a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 21:46:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:46:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:46:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:46:26 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 12 May 2026 21:46:26 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:14:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:14:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:14:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57a4137454cc0810d06042c272eb08276000e4b66a91f77145ef48d12c8463a`  
		Last Modified: Tue, 12 May 2026 21:47:32 GMT  
		Size: 52.7 MB (52669152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f196abc4fefe6f414e0100052dd8182945cf67cc7d015af36a673aa6fd6ae03a`  
		Last Modified: Fri, 15 May 2026 20:15:05 GMT  
		Size: 75.6 MB (75565387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa76b4e92f87697bbde2b3471a5b82e42e9638507b41cb52b8e8aa88b661c9be`  
		Last Modified: Fri, 15 May 2026 20:14:48 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:49938763c23e711b4b3bc275eeb667dcd627426958e459fc7c4061b93488125f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665f4eb3d7f84588c571bc56fa588c4b671b4eeeba1f09d8f1c0cb3e72d4cef4`

```dockerfile
```

-	Layers:
	-	`sha256:25fe345f72019470a7263258c9493a12066f8010b4d61a56db6e19f84d6c89c8`  
		Last Modified: Fri, 15 May 2026 20:15:03 GMT  
		Size: 5.2 MB (5242905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97f9339783c7a53719bb363682fc20cc2938023eba3b03dcd2d5eed2ca6da926`  
		Last Modified: Fri, 15 May 2026 20:15:03 GMT  
		Size: 14.4 KB (14449 bytes)  
		MIME: application/vnd.in-toto+json
