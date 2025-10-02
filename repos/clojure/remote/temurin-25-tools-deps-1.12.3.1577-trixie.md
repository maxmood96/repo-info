## `clojure:temurin-25-tools-deps-1.12.3.1577-trixie`

```console
$ docker pull clojure@sha256:fd904e8b716c9c758bf8ebfaee385859616a0bee0337c8ee8c69b7b2630e51e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:4c669c84519c3220d279e4e9571e6a55c6e0e479fddce37fcf734fa4e00ba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229819930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68fe78864c23b2806f51d3927b016760c5a8fa1d05a6374d52ddaab512d62040`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0327c0d19787f0057ea8ce23dc2100ecd313f3ebdc93f7335614ef048938a48`  
		Last Modified: Thu, 02 Oct 2025 13:08:17 GMT  
		Size: 92.0 MB (92036036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0db4511e233681c7764d19259b84d59a23bf0ab17f4bb019886ccc0945d0eb2`  
		Last Modified: Thu, 02 Oct 2025 09:55:03 GMT  
		Size: 88.5 MB (88498228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9ba517f3546f5395ae123b0ccb2d05088c0f43412dba1c6283556901a508df`  
		Last Modified: Thu, 02 Oct 2025 09:09:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4109a72c822830729d6a8974920f0e18bfb191004ad9ecd7eb0476dbcca7370f`  
		Last Modified: Thu, 02 Oct 2025 09:09:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d51566796ee62aaaa54c92c1d82253f4061d7b47a19c1662154edb65ed019d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17a585445c0937e37e3864f6bb36aaf31f0d2b8ac880bd4b46268675d2528518`

```dockerfile
```

-	Layers:
	-	`sha256:716827cc420d742c50efe5c6394be51e26fd9aa168c39dd10256f903b6ff3a02`  
		Last Modified: Thu, 02 Oct 2025 12:45:39 GMT  
		Size: 7.4 MB (7418217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b300da7bd77bbf9292e789082516957617f0ff279f2ac3e8a34c1e5565f177d3`  
		Last Modified: Thu, 02 Oct 2025 12:45:40 GMT  
		Size: 16.5 KB (16457 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:50b392fb173c41ef295ea81177da7bf9fc6687e213217fa0860d4fe56e0f77db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229385823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6cd3b3f3c23d06c2056c4b948de6995ea4abac01a8d54f8ad0d2ace3e9c5335`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c028b2b2108cd8409d417e0eda1efcb2454ecae68896f94301dfee54401638`  
		Last Modified: Thu, 02 Oct 2025 02:48:20 GMT  
		Size: 91.0 MB (91045286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0913ac11daf6c95529e64022a7265defc32e471d918b0d340677c26e028e6e10`  
		Last Modified: Thu, 02 Oct 2025 02:48:02 GMT  
		Size: 88.7 MB (88690803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bd56accac022be28e8be903aaab5ae448eb73c4b23b90a9d7cf119598b61d0`  
		Last Modified: Thu, 02 Oct 2025 02:47:56 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8eedac3385e31a48d28e2192438a45a9a9eae32d637e2cd0ea1143c11ef9be`  
		Last Modified: Thu, 02 Oct 2025 02:47:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bad36f4cfaecd1d4794025ea3011e1c7abec6b0b3b08761dbf04723efa1e9e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac1ea46de22acae28374d4006d13f791f389962f5f48cf92c85d862c977cf75`

```dockerfile
```

-	Layers:
	-	`sha256:533a8094cb9ae1e02ffa0587e3064a44537548ffcd4acb9e9ae6e74df13c3863`  
		Last Modified: Thu, 02 Oct 2025 06:47:46 GMT  
		Size: 7.4 MB (7425268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b2bd08c85a8d3f490beef51f9982285e7674f73692a34912dff9399cbf6d83f`  
		Last Modified: Thu, 02 Oct 2025 06:47:47 GMT  
		Size: 16.6 KB (16600 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:06f5bf8dda2c51a4b8593d7a0bfb2dc952e0d8a00c27754e654a8fdf008a7a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238863625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3ce68bd452022f59a00a9a376c69ed07e5c27716537bea370d12a4ac109ba4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26068084d5c0d18ceb5891b6fd4231786726d8ad744810400957e5a91ddb77fc`  
		Last Modified: Thu, 02 Oct 2025 20:36:58 GMT  
		Size: 91.6 MB (91601758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71467a6d07245b31c0eb40aefee7298e6ca1b5ea78e44e930cf023736b74f667`  
		Last Modified: Thu, 02 Oct 2025 09:44:13 GMT  
		Size: 94.2 MB (94151608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03d394bad1b71a3d056ef5856b4c422ade53dc1f89ecb4101484a6a66942543`  
		Last Modified: Thu, 02 Oct 2025 09:44:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41025d47e309196346f935e1818fa741471b70a447e4371806e68a6f105f9c7`  
		Last Modified: Thu, 02 Oct 2025 09:44:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4355463c4ef0ba77751bc25176d3c8165c83b3e23438050fa6ea0b0b8a9318e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691ecb78eb58575e16ce7ff0cd310b39baeff8a771ce3632429a487569ddf3b9`

```dockerfile
```

-	Layers:
	-	`sha256:14f455343886a25851bc24c82cc1309bed21535596e114aa1eaa3fe516503367`  
		Last Modified: Thu, 02 Oct 2025 12:45:52 GMT  
		Size: 7.4 MB (7423946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f217cd2b50a670e6135a00ef4899d94c45ce91fc35943d0e987773f903aefc9c`  
		Last Modified: Thu, 02 Oct 2025 12:45:53 GMT  
		Size: 16.5 KB (16518 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:d5809dbdecd3dcaa2d1fda8a09bc3d745a1d1bc2232e646eb6d3db7c73047364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222945719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83dc1a36d45667145c5da13247b2551addabdff56ff2d48706ac128ca1d77b13`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8f913be5ecadf79e3ee9792194aaab366421c7e066487d572f285b293ff78a7a`  
		Last Modified: Tue, 09 Sep 2025 00:25:27 GMT  
		Size: 47.8 MB (47765447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d906c94ffd80ac5b5b080e8a6ba857d4ad76aa0160f09e49e866f4d2bc2962`  
		Last Modified: Sat, 27 Sep 2025 01:24:19 GMT  
		Size: 90.8 MB (90752393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2901c3a8e012ce31bbf7d9c98b5ae6f66ac8fab310ee6c87463906c9d95ab0`  
		Last Modified: Sat, 27 Sep 2025 01:24:13 GMT  
		Size: 84.4 MB (84426834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67fc3c7da6c97e20ac34bd2be62d18f79b8c1ee7710f92cbf623d5b906213e7`  
		Last Modified: Sat, 27 Sep 2025 01:24:03 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a187f4b5a7c132d00bab337e48ae052a43b235962cab6551976d0dda870fbb`  
		Last Modified: Sat, 27 Sep 2025 01:24:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f2f2702db5d4624353eb72521af76e4807ca7c665ad3b910904034bfe0a86119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9615eb108e42e4bca133583c064e79468f3d53273a342e473ac02f73f414960`

```dockerfile
```

-	Layers:
	-	`sha256:fddcea16304d2d08cf30cb9b1e0c8cf6568b9462c2fea1f95cf9e232e5894044`  
		Last Modified: Sat, 27 Sep 2025 03:38:02 GMT  
		Size: 7.4 MB (7406085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3294d422f87ed5b4a781dee441e5ec42b7c9d8ac6862226a6b2f5c8843b75e57`  
		Last Modified: Sat, 27 Sep 2025 03:38:03 GMT  
		Size: 16.5 KB (16517 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:279bc2dfdea3321d8a007ed5dc92e728b0a6b20cea733355911b35c224d4c751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226684407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd78963d8c7ddfba364eeee0bce80459ca8a27375d0afbe4da7f48e3e85b556`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:024d6c344f0b9dbb2baf07e95dfd2abbfadc5c8262ca381f39f6489670cbaff5`  
		Last Modified: Mon, 29 Sep 2025 23:41:06 GMT  
		Size: 49.4 MB (49351442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daa2639a0298f6857127b224fd64cd213fa2e6d60da8408ea6f993388788a1b`  
		Last Modified: Thu, 02 Oct 2025 04:57:03 GMT  
		Size: 88.2 MB (88206443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cd92ab84b93b12fe3d9c005d2f79a8bb378db428bf9638ef59651d5024cc55`  
		Last Modified: Thu, 02 Oct 2025 05:02:02 GMT  
		Size: 89.1 MB (89125479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b672554c78334f329ecf33edd282918cf2e18f48b469654e51aaba4e1116fc`  
		Last Modified: Thu, 02 Oct 2025 05:01:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87511cabf541670ab2cb823aff0b0469c173b3b49fa5c6e3255b312b2b10dfba`  
		Last Modified: Thu, 02 Oct 2025 05:01:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b9d5f8105d689f430268ee29415e36440dbc436a1335cb678d6cf227aa66b4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f9e9e0185ec0336d0000cf732016e0853c2bf7342a4b00b408d540daaf8a17`

```dockerfile
```

-	Layers:
	-	`sha256:d68a855e33f20673f5884c58e60122b9b80d6d86ebf0fe9d772550366fe14d47`  
		Last Modified: Thu, 02 Oct 2025 06:48:05 GMT  
		Size: 7.4 MB (7416687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8040c1fb1a921b8e93abf9891ef4251b333f9bea508e9e38e557003c6b0326f8`  
		Last Modified: Thu, 02 Oct 2025 06:48:07 GMT  
		Size: 16.5 KB (16458 bytes)  
		MIME: application/vnd.in-toto+json
