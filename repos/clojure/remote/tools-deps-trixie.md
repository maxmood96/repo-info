## `clojure:tools-deps-trixie`

```console
$ docker pull clojure@sha256:30636d1bcf8e177f15a9391f4e2fa80d4f85841aadac551b2b5a5b884664e58b
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

### `clojure:tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:4dff565d5cdbd9433bd52ec4a33f17f515231a5eea84f720b80ca2c98a669b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227493781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8578b76b239fe661876eb6a95c477de144101ccf0521c679cf3ff8b8cc914be7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:01:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:01:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:01:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:01:42 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:01:42 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:01:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:01:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:02:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:02:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:02:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b8ea5147a5ada10c1e36dce6d8a3e665d639f45dfa06782da4a48f8e6a9d9e`  
		Last Modified: Wed, 20 May 2026 00:02:23 GMT  
		Size: 92.6 MB (92574574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12acce1c40840ebc1b65fec797cdc776981552e04677e3dbae6be44e60f5f01e`  
		Last Modified: Wed, 20 May 2026 00:02:23 GMT  
		Size: 85.6 MB (85607542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd6b53c58fa866c3620a8e725e6bed328578e76102ec2eafc9e9e49e4dac46d`  
		Last Modified: Wed, 20 May 2026 00:02:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf84b8bb7ceb1e74a9abb2f89e278e76c8819407894601e8afe010306ebea5ad`  
		Last Modified: Wed, 20 May 2026 00:02:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6608d2e7fc79932909ea4476107b72435bae3f9e51ef051dfea91c5ddfa35f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7456127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e609bb96e708853bb77cc0477fcbe48142dcfa7172f36bf41d14b1adff19d633`

```dockerfile
```

-	Layers:
	-	`sha256:6d64610521ecbf92e7904d344f89f5864ee4ad57ec20b00bb3ab8cfa3e00de57`  
		Last Modified: Wed, 20 May 2026 00:02:20 GMT  
		Size: 7.4 MB (7439558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2089f57638ac3da13e459d56d85d61a58c8bc6d643bec5cc80d1551e630e1c3c`  
		Last Modified: Wed, 20 May 2026 00:02:20 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3a2a2c3d8cda91c207635ff563d8287eba469509dc30c614997394126fcfdb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226647338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb122b61eba2a7f8febf9a83e365600be743e179de72d4ee5f563be36409370`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:08:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:08:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:08:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:08:25 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:08:25 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:08:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:08:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:08:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:08:43 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:08:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ce3dd0057a2a2ec4a603eb373e747d6b9d1b79507268496f43627a5f7d237e`  
		Last Modified: Wed, 20 May 2026 00:08:58 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e52aa0ca6820ccd789b45aadfc7a68500f4768f048b341115caf9580d2a6402`  
		Last Modified: Wed, 20 May 2026 00:09:05 GMT  
		Size: 85.4 MB (85431819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39caff6453bbf9e0b6eadecc9995040ea3ec8f2e58ca7d681d562a052262fe31`  
		Last Modified: Wed, 20 May 2026 00:09:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b79c585a1ac46cd2873f9f44fcd1c427e343243a201393e7f9701269661e81f`  
		Last Modified: Wed, 20 May 2026 00:09:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2a90a7161e06c42e617edb1f14f6d09e4807e2c678407da696c18abe4a861b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7462683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff132a935d8c0b9578630813e7688aee3bb9b0bf40c833c87bcac6fda0aa0b8`

```dockerfile
```

-	Layers:
	-	`sha256:d9e68802e20f92c2b208559ace9bbe890f6373a5d980c1066995641b7b422b25`  
		Last Modified: Wed, 20 May 2026 00:09:03 GMT  
		Size: 7.4 MB (7445972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f2664f958173aad1e5d74c22ebc0e4cfeaab26c644fb94934785e87274c743`  
		Last Modified: Wed, 20 May 2026 00:09:03 GMT  
		Size: 16.7 KB (16711 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:08a0695799b395a768ddbc748511274d8264a8c0f4e5f0a24f9421b1bcc7c8fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236045826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4003875a2d5854371d03842ad3117567208ff69e8341744536b3da60c6c9d08c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:42:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:42:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:42:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:42:40 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:42:40 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:33:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:33:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:33:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:33:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:33:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2325345b811e94f6ff3ccd6a646a97c3cc4365dd97daee1fdfcb79b03cec8cfc`  
		Last Modified: Sat, 09 May 2026 02:43:51 GMT  
		Size: 91.9 MB (91914029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9883aef0bc85acd55be92f3be8d783a164545c8b39a214d255c516dc194c0214`  
		Last Modified: Fri, 15 May 2026 20:34:30 GMT  
		Size: 91.0 MB (91007585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5471725dcc8234aba5a0046f06d6ff2617c22849010ff89228bd5870caf867`  
		Last Modified: Fri, 15 May 2026 20:34:27 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40576b25892aec4cf9a8a5f85de9be6fdaf3701cb0e8504ea535d9a3508720c8`  
		Last Modified: Fri, 15 May 2026 20:34:27 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:258b9e5d7df25663f85cfd99f920a113a30c8ce4fbd7b3ab4e69e684d4e51d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c15a3a0d78e771e9decc5baf1e1fa47c6f063ed21a2bdc39f3ca7d89f11184`

```dockerfile
```

-	Layers:
	-	`sha256:0ad9849b65f58c43ab8ae4a4435c10f16faa51910d1f66583f308de5eb46b0ac`  
		Last Modified: Fri, 15 May 2026 20:34:27 GMT  
		Size: 7.4 MB (7427189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18476ac61778607fc2da3bad89670b6ea9320272c552d8e8a510d9b446d2fa4f`  
		Last Modified: Fri, 15 May 2026 20:34:27 GMT  
		Size: 15.7 KB (15674 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:b63e06a120709b4dbf2590f29b7fca821de551802dcb15abc4b077051661b883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224360131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b0d461501c5025b66f7e69bd8613c50a7cbe92df3ccac4c91b93c770d55ef2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:34:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:34:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:34:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:34:58 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:34:59 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:37:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:37:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:37:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:37:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:37:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a92a76ae7b655491f20639c1a27895a4fe7338273ae814b1de259101697f0c`  
		Last Modified: Fri, 15 May 2026 20:38:16 GMT  
		Size: 88.4 MB (88420336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291de378db9c19667d00b6f891370a8c84be230b97e3589f787d6241f62b2d6e`  
		Last Modified: Fri, 15 May 2026 20:38:15 GMT  
		Size: 86.6 MB (86566445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63597033dfd787e9ef0392df547a1abf1a5ee472ab426cac41d5951259c063b5`  
		Last Modified: Fri, 15 May 2026 20:38:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5857ed32944d53d5be9f432168f2c9d6c92ef34db0dd94e7fc44fe86c7d96e93`  
		Last Modified: Fri, 15 May 2026 20:38:10 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:edfd80599b15b9caeed2945ddade79a33895bb9ec4eb44557fd5f0e3c01d3f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7436497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cedab147490d65c65fc906d8b9059b5839f410fc8d942f249413efdd4a8fdf8`

```dockerfile
```

-	Layers:
	-	`sha256:9fe23aeecc6c6a2659d6d45b0776d80287c576fcf8e2ad04528cb74d027b9ef3`  
		Last Modified: Fri, 15 May 2026 20:38:11 GMT  
		Size: 7.4 MB (7419928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a666fdb1043f4ad254f58d5ecc1e371db9f3ba7128d5aa76ab04405b673340e`  
		Last Modified: Fri, 15 May 2026 20:38:11 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json
