## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:d5f2312ac5d49712573242d5bfc1804ec99e9183e71f827020647ece4e34d516
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
$ docker pull clojure@sha256:cfffb62794bb86780c26db6de3905ba4c4c657767b2434cfa9f9835f73b1716b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250325395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0467d55b371e61fa651e90850719ea63ae11049137c12e7f91114da767e4dc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 08:01:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 08:01:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 08:01:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 08:01:52 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 08:01:53 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 08:09:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 08:09:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 08:09:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 08:09:27 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 08:09:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0887e2dadb1bfb5e02baab4d6c0be869a68f477e138f696ef3347af998103de1`  
		Last Modified: Wed, 24 Jun 2026 08:05:10 GMT  
		Size: 145.8 MB (145766157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ed71c13fa5521a22704074422b173f7de5df43bb54ec1b222298ccf419c9fa`  
		Last Modified: Wed, 24 Jun 2026 08:10:01 GMT  
		Size: 72.5 MB (72476221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c69e066fdb4469e1f1e1d73b80de63f49a47b794e28b09ab836d53bd8aae7a6`  
		Last Modified: Wed, 24 Jun 2026 08:09:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5955f34e2ef3e4fde448781a617ee4086f842fb2c6a0620c7ed6c8997b800e9b`  
		Last Modified: Wed, 24 Jun 2026 08:09:59 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ffa85267a96e8cc59d95775eff44304a148c83c296bee0e8b5b313d453239fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f27b2afd5a35aa27e05b5fa9906ddee698e58d1862afde35ff2b4aa22dc06d`

```dockerfile
```

-	Layers:
	-	`sha256:28b6fcded51335359ae1161e546412d104fe36efbcd7aa689adcf7a192607f0e`  
		Last Modified: Wed, 24 Jun 2026 08:09:59 GMT  
		Size: 5.1 MB (5119157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1daa93ccac8d203a6dec17577f19389dbd5bb2b981d03b248acd95789881880`  
		Last Modified: Wed, 24 Jun 2026 08:09:59 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:fc1d102d09e2bf13f7354b5233f047ab0dabda038ade6cd12a17dd29a42a0979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228257283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc00b58b3e51d7ff3d9c4a7a61485d2fd7aa528a67a6d7f6ffa569760a3cda9e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:11:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:11:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:11:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:11:51 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 04:11:51 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:13:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 04:13:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 04:13:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:13:54 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:13:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb29b7db06616258b2d15f77b8d57ad53977da53f7b57a048a06f610786cd7e1`  
		Last Modified: Wed, 24 Jun 2026 04:13:16 GMT  
		Size: 135.9 MB (135910426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355870e3a1fd29f76abc0e707a20043291ebc36f66bf1d0d4472a6e77e459e46`  
		Last Modified: Wed, 24 Jun 2026 04:14:18 GMT  
		Size: 65.5 MB (65452231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e7c6b3c76f9fb3ff15b3aefee3560abf9222c06862b4fdda1430bdf3a0da65`  
		Last Modified: Wed, 24 Jun 2026 04:14:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9b3bf853d9b17a34484bd3744801480e4af53a020346efc0de4571a17f5ae7`  
		Last Modified: Wed, 24 Jun 2026 04:14:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6fca0e4dfde4fbea81e83528ac3fa0f8e29158e84b740c4c0692a5474b34ce74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a17eb18f9954cf4a6864811fa7ac6f8c59950d9a4c817449340493ee8f464a`

```dockerfile
```

-	Layers:
	-	`sha256:7a4b6c197b00ce1bdb5bbd666436f7281652143236186f7b728054c799e00d2a`  
		Last Modified: Wed, 24 Jun 2026 04:14:17 GMT  
		Size: 5.1 MB (5105320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfb16b911a6d1a902819d0c969bc7c63a21e8d7bd5e7245e966421b11e9f44d2`  
		Last Modified: Wed, 24 Jun 2026 04:14:17 GMT  
		Size: 15.0 KB (15035 bytes)  
		MIME: application/vnd.in-toto+json
