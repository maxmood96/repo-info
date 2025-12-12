## `clojure:temurin-21-tools-deps`

```console
$ docker pull clojure@sha256:a01bb28f732ea4371075c5ecad731f8bb02a5043371bbc0563d00887259cffce
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

### `clojure:temurin-21-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:ff429f8b02dd3eaa4125005b70abbd7f89a58eaafd2cbcced9463d4a501fa53f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287454644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956456411416c6d0fdf0628d2fb14c7942f4c561402b08ab5c1eae04acdcfeb8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:39:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:39:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:39:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:39:35 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:39:35 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:39:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:39:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:39:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:39:49 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:39:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1673ffe1dcaf56a22da976014ac180d9f164f693f8b1ff277e5a1de9f0e864`  
		Last Modified: Fri, 12 Dec 2025 02:05:33 GMT  
		Size: 157.8 MB (157825957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05980fa5a40c025d0c84f66dbfc61dcf723c5942aae2e793adc8ae2976bfff38`  
		Last Modified: Thu, 11 Dec 2025 22:40:28 GMT  
		Size: 81.1 MB (81146909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b115b101e250c234510b643e8f8e08aab7b71ea0f6e01a6d4a680744fe5cab4`  
		Last Modified: Thu, 11 Dec 2025 22:40:18 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3f646383e65d19f2b8fe68bce3bf2d1f695a2c4f74db18135b218e289f1c2f`  
		Last Modified: Thu, 11 Dec 2025 22:40:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:b6cc100214edf45d379e6583a067761d673c5dd37ae39cbefb232c1065d7018d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f035069bbcd1d408013605ef53e716befac6cba91522f3039c60f5e59c2852`

```dockerfile
```

-	Layers:
	-	`sha256:3eb698ef0e3dbef3915c0b0d5409fe6b7d476a9013557fe62f8a068e395e64f1`  
		Last Modified: Fri, 12 Dec 2025 01:41:27 GMT  
		Size: 7.4 MB (7378678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfe8a4660b0eac944102a0a5bf35f39c1866dc22ec9ca094494ac915a772ac27`  
		Last Modified: Fri, 12 Dec 2025 01:41:28 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2762e69af12ee9d83a605076bde4f7eeab2f2ba15ab7656dee1eb3bf9d1a4661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285493707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8190ceb0fd03631cbcd4d38787eb6c04a6b5a2b20744afe0da55824a13d97140`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:40:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:40:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:40:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:40:03 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:40:03 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:40:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:40:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:40:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:40:18 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:40:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349e501c256220bce4716fbaec52d9fd62f645c39af638fbe0bf1c516c23f04d`  
		Last Modified: Fri, 12 Dec 2025 02:06:45 GMT  
		Size: 156.1 MB (156107650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2e5290593902b5a99e8e03ad51225ea2550d025e735fcaddaf7ec16c290070`  
		Last Modified: Thu, 11 Dec 2025 22:40:59 GMT  
		Size: 81.0 MB (81025948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc09abc9130af6104b2672ced74eb7f49b07f2d10125e5e74204cbfad78be0`  
		Last Modified: Thu, 11 Dec 2025 22:40:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dda9828d37a3df133d9f9b9d6ca7b62c79434fef98ece760ba8bacb49947c8`  
		Last Modified: Thu, 11 Dec 2025 22:40:53 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:dc9f1b46080273295710feec75066bdca02eedcfe68149dab6a3a0e48b6587d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96417a097dcc06c2a8fbf22c0294d0d2ff3e34b75f5cb923804844535686538`

```dockerfile
```

-	Layers:
	-	`sha256:01d772acda7249d38266cd414dd38280921d2d7b816fe5e0963592fcb55ebed3`  
		Last Modified: Fri, 12 Dec 2025 01:41:35 GMT  
		Size: 7.4 MB (7384465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42cbc6afbe75393c34359acea20b68399fc10328894a2e19ebe3d5f189139cfd`  
		Last Modified: Fri, 12 Dec 2025 01:41:36 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:dd7a5483d7b5853640f8edd1273143405c2b8ed6479edd1fbf0bf5630eba32e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297253563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b23957d0e85fca4cb8100ad4dccb3dbced7b582a0cc3f3fc2bef9f77ee2e40`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:44:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 22:44:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 22:44:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:44:05 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Mon, 08 Dec 2025 22:44:05 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:59:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:59:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:59:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:59:10 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:59:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84193563598712b437e18d1f55a29d0760b80aa62c9cc1125eb6b86822607f7b`  
		Last Modified: Mon, 08 Dec 2025 22:49:33 GMT  
		Size: 157.9 MB (157942939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f96b8a6b51eb5e6a1b9838be666286dd4276855ddce5a72b58f4b27669d4d29`  
		Last Modified: Thu, 11 Dec 2025 23:00:29 GMT  
		Size: 87.0 MB (86982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a43eee5d662572932565e766710c955aa8a164d81dae6173eea3df426a386f3`  
		Last Modified: Thu, 11 Dec 2025 23:00:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da90e3ce86da1e4af55a0fd16294cfa66f67890d7bfc2e1fe4727f493794323`  
		Last Modified: Thu, 11 Dec 2025 23:00:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:0a627622fbbe55c238fff5e1a3203f1fe7aa4261622b304c1205be1b69aba41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0180947cbdeaa7036f975540f49626df50d3c4bbc61acbeb3e8fffbe98b5579e`

```dockerfile
```

-	Layers:
	-	`sha256:ac064db00940dc0e7e5ad2471313095f566c327db7c931d318033f488da87fa2`  
		Last Modified: Fri, 12 Dec 2025 01:41:43 GMT  
		Size: 7.4 MB (7383904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:130f9808d7f8732fd0ed68f5c650af5653036cefd4e0e8fbd77df79e08669738`  
		Last Modified: Fri, 12 Dec 2025 01:41:44 GMT  
		Size: 16.5 KB (16522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:ed256ee57ca79a5747228069db5c72ed69c457a07841084795b38e37da84286a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274163697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba21cd03109bd828b0b0b9ea4888070b0f742c2e06fa3cb4ef297ba581115cb7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:35:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:35:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:35:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:35:27 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:35:27 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:35:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:35:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:35:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:35:40 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:35:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f1896ba83f603ad81e0d8cb48b496e763b4b781a68efe11f1b6de9da929514ea`  
		Last Modified: Mon, 08 Dec 2025 22:15:09 GMT  
		Size: 47.1 MB (47137665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5647dac97a4f99e1a7e68a7662bb89a5ca15fcbeb8411b76c378b33eef28a222`  
		Last Modified: Thu, 11 Dec 2025 22:36:27 GMT  
		Size: 147.1 MB (147069848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d50e5dadd361b96279dc25e7d28bad8dee93cecab9a840e17c673e9af22b2e`  
		Last Modified: Thu, 11 Dec 2025 22:36:23 GMT  
		Size: 80.0 MB (79955142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cb4d101cd01fa86fc4a21fe3c39fc40d001698c44296bb6d768e28bbdb9d51`  
		Last Modified: Thu, 11 Dec 2025 22:36:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d152ed4a98c0402c4010c27f0d6e347f5d89d6d1a051547c14620aac154c693`  
		Last Modified: Thu, 11 Dec 2025 22:36:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:23d74a846684ad2157cf1a5bed12daf1adb83045d4f52b2082c9a8bfa791984f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758ddb8ae5fff669804d213ead916b00dcaddc7e5ea349088eeebe94d869e9be`

```dockerfile
```

-	Layers:
	-	`sha256:127446d9ed5f3a3215c549b1bf637e8278d0e5914027d32303cfe2a7f53e8755`  
		Last Modified: Fri, 12 Dec 2025 01:41:50 GMT  
		Size: 7.4 MB (7369997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:824c525b76f63af67d85165088e4c6b4a67aa09f1ab13ee202375e078b39263e`  
		Last Modified: Fri, 12 Dec 2025 01:41:51 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
