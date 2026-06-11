## `clojure:temurin-17-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:5feaefdd0a1e7dce5148da1677b12ddd064160d20d39cb4eb4b3661cf63ac237
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

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1197df06f3bbf57000d70d63f8885c458fa9cced3da558d9d01782e2385cf76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244643373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d009b03f2a1f070fd2ec84dc17032f1a2640b7409fdc91d1e4b02a4b1f7daf0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:19:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:19:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:19:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:19:05 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:19:05 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:19:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:19:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:19:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:19:21 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:19:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc159ea5850a8698486296d4c386aa9d2beff3d923de2e0df961791c05767925`  
		Last Modified: Thu, 11 Jun 2026 01:19:42 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cadf953937dd92b8719e0901e3fb6224d0d686810281c9834654dbfe236c57a`  
		Last Modified: Thu, 11 Jun 2026 01:19:40 GMT  
		Size: 69.0 MB (68951463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07880afeea7bd2a60e1a431f3bec3dc695a1183f36e15d89f4bde26689df05a6`  
		Last Modified: Thu, 11 Jun 2026 01:19:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441b177d813efb7a8ec3d09db21340aa6ce6e42799ef40935ba0ce6389ef7ca9`  
		Last Modified: Thu, 11 Jun 2026 01:19:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3526fa15537fda527c4629c51b4fb681a8cb602885270cdbf3e5b59fd35a9593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d87c0a3f6064e31429385c51abd6c77eab3b3e562ad20fe0954bc6bf5553dc`

```dockerfile
```

-	Layers:
	-	`sha256:dcece64d3c812e733ca9174396953b5bfe2476b38e53536c07b2c38a7ff42e03`  
		Last Modified: Thu, 11 Jun 2026 01:19:38 GMT  
		Size: 5.3 MB (5257242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea5d2fb95142824541dd6ed89449858db01aa06712121ee187efd7312286127b`  
		Last Modified: Thu, 11 Jun 2026 01:19:37 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1dd9a34212e746d12c5caf3eadf1aa8e596ddb1ae178373f55e3fbfd36a5561a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243651328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac5639685f8954e2aef7e01133cdad519e03ae4ea13292bd1c63e97fdfc4856`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:23:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:23:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:23:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:23:21 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:23:21 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:23:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:23:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:23:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:23:37 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:23:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9435d75879704f2f895af71d406335ae4b4b9f3c6a095ba818dc617936775a`  
		Last Modified: Thu, 11 Jun 2026 01:23:59 GMT  
		Size: 144.7 MB (144724360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60a2787a9b16aa00ca7ac8e10c91aaab12e849cf9c99c5f723d1d218c4fafb7`  
		Last Modified: Thu, 11 Jun 2026 01:23:58 GMT  
		Size: 68.8 MB (68777394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5de03bfca00e9f7a1509065d11830f1222dcd22447570cf7374475e527998`  
		Last Modified: Thu, 11 Jun 2026 01:23:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a8e9447964c7c9db66fd820dc4d3d38ea24ac883fe8dd06e2e2dd39190169c`  
		Last Modified: Thu, 11 Jun 2026 01:23:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:33bb92a3d912e54c74ed5e3dc5279f05073c9accf1c5529938b7afed2630eca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363c822c95c61cb217a08c42baf9d54005e3ce4de8573ffe8f45657f059f7944`

```dockerfile
```

-	Layers:
	-	`sha256:766dc3f8e7dbd36e2655620cb40866727b474ab05ae288e3bd8bc33d5fa71e5d`  
		Last Modified: Thu, 11 Jun 2026 01:23:56 GMT  
		Size: 5.3 MB (5263003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a97885b544cec0acc927bc7dbedb653facedc6182a11497a5dd8ddc10d2e91d6`  
		Last Modified: Thu, 11 Jun 2026 01:23:55 GMT  
		Size: 16.1 KB (16083 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:bdf5bfa3cf79a469537ef88227d372efad162afbeb1c5694eeeb25f7e6b20d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253736692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ecbc7eeeff02ca7232ec784e50c6f690d8e7d4f1b5bdc1cfde8d5aa3def2a0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:56:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:56:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:56:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:56:03 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:56:04 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:57:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:57:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:57:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:57:01 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:57:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00b56959c90c5f0fe14cf07141a8ccbb5fba2b1e9b43bac05ab20bc6c254eda`  
		Last Modified: Thu, 04 Jun 2026 17:57:46 GMT  
		Size: 145.8 MB (145766113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fce969075dad3f8234f1b38d92b693985c08aa5da5a3d9c2bf1df9338e3b006`  
		Last Modified: Thu, 04 Jun 2026 17:57:45 GMT  
		Size: 74.4 MB (74369083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fec052117ea57934c22cd72ec755fb81c95ad4b7e7a0a188a63f6096b3d5ed`  
		Last Modified: Thu, 04 Jun 2026 17:57:41 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f523d8e1a558a75fbdf09ee5876900417a47255842c5a5585cd78696aa53e04`  
		Last Modified: Thu, 04 Jun 2026 17:57:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eec43f905b9174fdfb3b97bad417ca1372fdfd4a2ab6ec29496331c7ed312123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ded7ea8818a2115c0a602d5cc4a439358007d122035d2bb9ff618065f20146`

```dockerfile
```

-	Layers:
	-	`sha256:15b0a9eab191f93cd912c57f29a3227a134159644788aec896c8b20926304f94`  
		Last Modified: Thu, 04 Jun 2026 17:57:41 GMT  
		Size: 5.3 MB (5261613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb5dc171f1a5579fe1f444d0ba8f75a0e597394e655c8cbcf6d0fd12bc4d114c`  
		Last Modified: Thu, 04 Jun 2026 17:57:41 GMT  
		Size: 16.0 KB (16013 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9a25dff25fb36800879aa5927d286a76ff43a23c13d3b81a7fbe06f5bcb72ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235695326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946f154447b08f9cce886ae73ecf992ef396787c69302a0ad37a2d9bd54659fb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:11:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:11:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:11:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:11:00 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 03:11:00 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:11:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 03:11:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 03:11:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:11:16 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:11:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c16ff26feeea60ea62c804efec48b3f427e98fe5a6b9c7d66d46c4cadae16c`  
		Last Modified: Thu, 11 Jun 2026 03:11:48 GMT  
		Size: 135.9 MB (135910407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fefbef163883a87067dbba8bfd92fa53a34f1dc30cf8c024baa71470715db4e`  
		Last Modified: Thu, 11 Jun 2026 03:11:46 GMT  
		Size: 69.9 MB (69932523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08593d0884571fec38cc6c793ba054f889921008d2d47bf1951195434dc73a76`  
		Last Modified: Thu, 11 Jun 2026 03:11:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1b423090375d80ddc90f5c6fa9aa5aef2e7a560df63663dbd2b310a0b3cf15`  
		Last Modified: Thu, 11 Jun 2026 03:11:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:541e9df1c70777faf30f2f4a2b1f5ebaa96c7cae96cd953dc293afacbb90defb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31fe4ec88cb601cf94241dc6a0ba118810c5c56a697fb136e1b73e286504b4ca`

```dockerfile
```

-	Layers:
	-	`sha256:17a2dba81edcbcb683b6a74e18f2d70474d0cee0d84e6e25ecf57c778a5d7cd1`  
		Last Modified: Thu, 11 Jun 2026 03:11:44 GMT  
		Size: 5.3 MB (5253166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f58477115d3a15971070177e49cf894ff4dd84266cf7cfb6b26b9a49da9582a`  
		Last Modified: Thu, 11 Jun 2026 03:11:44 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json
