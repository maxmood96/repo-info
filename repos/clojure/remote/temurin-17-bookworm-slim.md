## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:fb9eab7b3d3b9c5b5e786ef5e3bea4ba4f02340b63d46e6da28b086b5b89b07c
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

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:37a2d59100305fe9d11a849acb87d12514e0fb965f97aafec85f2a57bceec065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240786799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d7d94fa42be4af0b0eea98f07bfe3b03e18ad4187f1b0ea422f192fb7691ee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:17:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:17:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:17:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:17:47 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:17:47 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:18:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:18:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:18:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:18:01 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:18:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835b86720fb069554fc782865a40b27d5029f59b1a172682a234ba4f834594d0`  
		Last Modified: Wed, 24 Jun 2026 02:18:25 GMT  
		Size: 145.9 MB (145905407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25fec7d3868b5691c8f214cadc76a5e6bc5b9d88ff99acd3985269835347ad5`  
		Last Modified: Wed, 24 Jun 2026 02:18:23 GMT  
		Size: 66.6 MB (66642713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8c6c5cf5704e773bf73b9d4a0d6f20c1608f429ef4f77120b8b8cf2c7a146b`  
		Last Modified: Wed, 24 Jun 2026 02:18:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c15199710e3293b9fd8127975c5a137fd9aa020e881cf39901213593e8ea537`  
		Last Modified: Wed, 24 Jun 2026 02:18:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8106385b48b47ee49661dc262fdfcc0cd386ad634842d7acbbcdf04b3c9d5ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b984e61525fdac8c7a9a1c22ad0460bf113777954a75964247c785bd785925c`

```dockerfile
```

-	Layers:
	-	`sha256:e45581e32c335446e68d5c697b9bb7bf6ad44e2a34063553bde548a943aaaef2`  
		Last Modified: Wed, 24 Jun 2026 02:18:20 GMT  
		Size: 5.1 MB (5113999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b6787a74db9103de460db751e06c167a58b7dfaa2efc2c607fe8e96eddfb3bc`  
		Last Modified: Wed, 24 Jun 2026 02:18:19 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e1d7d2def3e3d582fe270894f01a93a497444d4d37897fad08e631fa57ad7754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239491040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6c8e937e260c8d201d4521c3e4ea3df54209be6017cdc81292d2c31047c0ed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:24:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:24:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:24:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:24:22 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:24:22 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:24:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:24:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:24:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:24:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:24:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3756309079dd138d5098f7dc881a644b3351682e2a23624737e3e1a1952f493d`  
		Last Modified: Wed, 24 Jun 2026 02:24:58 GMT  
		Size: 144.7 MB (144724351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27534da9d4ff61020d2e6ba3a307693c6404f10ddb22634fd57464efd7e0b90`  
		Last Modified: Wed, 24 Jun 2026 02:24:57 GMT  
		Size: 66.6 MB (66643232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387564ac954dd434c7e23e6ce7b8156990a0e21f3b07654f125315d250718a95`  
		Last Modified: Wed, 24 Jun 2026 02:24:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c558c976eb2fddd89e6c576530369a348897fd685e3860bf4171ef2fc7f6591`  
		Last Modified: Wed, 24 Jun 2026 02:24:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f500ec4a2909eed4d6863b7a01c1080914874fdaf4afb4ea1064fb8c85ac5cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7338049fb17deb8abb3f86170fb4717e98693b954ed1a3a995eb43fc8865f8e9`

```dockerfile
```

-	Layers:
	-	`sha256:2541b34f8f90e808895e3faa1cf19bdd02e4206738af8e88e8b08600cf9d5dbd`  
		Last Modified: Wed, 24 Jun 2026 02:24:54 GMT  
		Size: 5.1 MB (5119760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20dc346fafd35e2714f45378be4e7d5ae5438cd200ec084944b186af57c70f6e`  
		Last Modified: Wed, 24 Jun 2026 02:24:54 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c7d994ba488380a414063a4657eab54034fd20e1f2b95497c418652efcda3950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250325569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6f5b15ce15fad3b0a75ee2fd75b3ada54d47ef629c8500a45825bce8296ed5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:36:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:36:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:36:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:36:44 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:36:44 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:46:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:46:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:46:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:46:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:46:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011a8b1fe08cbca6cfbf84dcf1035227586f8c0a013a520d08ca8f1bb6f1baa7`  
		Last Modified: Fri, 19 Jun 2026 02:40:33 GMT  
		Size: 145.8 MB (145766212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbf43af0d3048d5fa020f170a5962dd7a7f5cb9f8dab551a3f3d22e60a089c0`  
		Last Modified: Fri, 19 Jun 2026 02:46:43 GMT  
		Size: 72.5 MB (72476374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328d42e99eb0011073e9c9a750f5fa384f379a866b46e24a51f6f104549a3b16`  
		Last Modified: Fri, 19 Jun 2026 02:46:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03667bde63913e0892747b56d3a3abbac90e0821912011cd472c66471bc8857b`  
		Last Modified: Fri, 19 Jun 2026 02:46:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e1c25687f888fad8ce3543cb4cf7ab2cbb1fc1fe21317ecafeff88a82e200f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990ae71436877cca3ee0f7cd7c7d4b799620a2aaab93c4c368c08aabf5c9071b`

```dockerfile
```

-	Layers:
	-	`sha256:c614da0ca127923df8a30d3b594e9520cd91d0cfdbbbda9aa7277e27dd8b324e`  
		Last Modified: Fri, 19 Jun 2026 02:46:41 GMT  
		Size: 5.1 MB (5119157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13c74f5b9580d8ea1fb4cf7afb91faea5e495a5729de610f686a211409cc369d`  
		Last Modified: Fri, 19 Jun 2026 02:46:40 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:dda7f7b58491a92d916de05ebf9be15d5987ad4f3268741415f041efa9a48e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228256991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66322df27a7192a9e5f1e4d1c14fd9ccc4ca6cac805c64d87e4f1cf431702a00`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:16:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:16:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:16:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:16:40 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:16:40 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:18:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:18:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:18:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:34 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12de02280ae8885a4001fbd484dbfc1d6554fb904cc661889a6e6ecda0108b20`  
		Last Modified: Fri, 19 Jun 2026 02:18:03 GMT  
		Size: 135.9 MB (135910426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bb7cfed22cee602460bb74a125f636b3bc11e2534983e438dba605d02ab668`  
		Last Modified: Fri, 19 Jun 2026 02:18:57 GMT  
		Size: 65.5 MB (65452018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d8ca75eb62d275af2ba849834ce38d598c1f6f5a543bd0d778696142079705`  
		Last Modified: Fri, 19 Jun 2026 02:18:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b0891787dfee78652702f88b3ad022a32bdb69a32c64ae8424f88bc81a1fd9`  
		Last Modified: Fri, 19 Jun 2026 02:18:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:35fd9322a3f98de15fb6ee6c63c762082470d51e515f9396df75236a408c4cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5121309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ba1f4e0c319862dc16689befe4bb519843bae82ff70419f8381e889aa0e18c`

```dockerfile
```

-	Layers:
	-	`sha256:780c5948f114eaf4410f7d48c2d4ac523b10e15c628700264cda0e4776de38d6`  
		Last Modified: Fri, 19 Jun 2026 02:18:56 GMT  
		Size: 5.1 MB (5105320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99edab377c85f002a9233cabf68954de415eddb3be07a6a9d7fb1c997e62f1f0`  
		Last Modified: Fri, 19 Jun 2026 02:18:55 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json
