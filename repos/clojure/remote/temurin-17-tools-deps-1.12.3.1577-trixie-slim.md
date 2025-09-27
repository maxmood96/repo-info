## `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim`

```console
$ docker pull clojure@sha256:442844b63546b6e8a18fc55ec3914a4fba5b3362f318f34b5b9a714364ee6cd8
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

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:31a7fb78765975a912fdbf3d57478432ffa60787584a3d74597113e446e6cb55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246463024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174feea5535a04252ced50614891bee256e2cc5b67c1e3702495b0133a0da389`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7c86dcb4ee141f6459116cc97941845bb4069009180725ead160a58c16c5f8`  
		Last Modified: Sat, 27 Sep 2025 01:21:11 GMT  
		Size: 144.7 MB (144693608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea0fbfd945f31d75964ff3c397f6847b9152c01a2ed6fc909d0ac828a08b4d6`  
		Last Modified: Fri, 26 Sep 2025 17:58:02 GMT  
		Size: 72.0 MB (71994881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06507df5b9e544a1eb6803a76773e45ed9f5e4d248e7eb54c4da11eec5cc08b0`  
		Last Modified: Fri, 26 Sep 2025 17:57:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb7efdfb1e7edd5e88950a84c1dcb8752e91eb97ff08b69857d7fca342643be`  
		Last Modified: Fri, 26 Sep 2025 17:57:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:63bae8b79e1e72e8f6658759ea2492070bfd47e9947d783d83b34d2ffabf0ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e17d731bfade1c196bc27331a410f053dbf84e3a79d40ae246e3232f358acc3`

```dockerfile
```

-	Layers:
	-	`sha256:16547cb5950002a431aff8813405f2cf86f55fd4aabebe64e5995fc760b20ffc`  
		Last Modified: Fri, 26 Sep 2025 18:40:19 GMT  
		Size: 5.3 MB (5256113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85bbf7613a8ef08ed23e5a937966e7c066adc48aa7f32eddfbd5c1ecc4adb01b`  
		Last Modified: Fri, 26 Sep 2025 18:40:19 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8f44aa378e4df2c18ccffe0484e0c23400133f4d86bffcda32f7d9bf6a38c060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245488232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38ce61c4f55faddea54dbd89d135424928bcdde7ce5a9a069b3e734d387a513`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ff9dbe67f8fb7f16bbd118a69ee0ef99bba88d6a84c7baa5b40aff7fb45640`  
		Last Modified: Fri, 26 Sep 2025 17:55:01 GMT  
		Size: 143.5 MB (143542130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2dd38200f4be020a6db8692ef588ffb248969b19b200fbb30317899302bd95a`  
		Last Modified: Fri, 26 Sep 2025 17:55:22 GMT  
		Size: 71.8 MB (71808428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbed1459abeceee1ef82d363406c819a45b2f1acfb80e5c382a1254f7bd7227e`  
		Last Modified: Fri, 26 Sep 2025 17:55:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e4be1d58b3da30e0bcad08431848efd019501a0a859d629409f352de2feeb5`  
		Last Modified: Fri, 26 Sep 2025 17:55:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bd9d91de1e753488bcf6a60426304e9c8685877cde65c9cb9b75d876643f0121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27f30ce9e192cfd96aebcc77fd4546643b6048f36825ab7f3962181f76b4fb3`

```dockerfile
```

-	Layers:
	-	`sha256:d41bef0df71d4e3a2b56d45069adf6afbe965db7df25297df419cc7768911b6e`  
		Last Modified: Fri, 26 Sep 2025 18:40:24 GMT  
		Size: 5.3 MB (5261882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b03e3c2da1a640e53c783846d95fe7b16db3854249b0e2382040982820cd35`  
		Last Modified: Fri, 26 Sep 2025 18:40:25 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:9b9692d02a42835c3cd0a9686ee3849015145bd14b6ac5dde005a632282f0e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255363954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61081ccbe3a20c90d7b60b9d3451b0c0e95ab9e599c99ce6811f29559ba3a834`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad50b32027f930ce266ed2ffa46f693b6d78881a7487f10923edb7f90a09b42e`  
		Last Modified: Fri, 26 Sep 2025 18:20:58 GMT  
		Size: 144.4 MB (144372861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea378ae8b89d3e2b12056a271f15c1ed257c2d0d5ed9726374ba3938fe832fc`  
		Last Modified: Fri, 26 Sep 2025 18:21:19 GMT  
		Size: 77.4 MB (77395697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c2c5739cf993d197041838efa9ecd2ab8c6f3db64faaba3dc3d2d3bea98e2f`  
		Last Modified: Fri, 26 Sep 2025 18:21:14 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fe6b086b62a29d0392e7075d0eeb4412a3ecde13023232bb9881404489bd4c`  
		Last Modified: Fri, 26 Sep 2025 18:21:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3cf2edfad8615d68b78bbfbca10e250b23ef2d1ca952fb7100f725cdd8af596f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c137b4b3bc014342553dc51763869b3b4f1a74e584bdbf7b7963bd9101d9695`

```dockerfile
```

-	Layers:
	-	`sha256:16a0cfbfdea4f7b51b311a09d7e0da23bda3c73dbd8273830c738b5fa2415460`  
		Last Modified: Fri, 26 Sep 2025 21:38:21 GMT  
		Size: 5.3 MB (5260484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe1c60770de9cef34330a5ef0ab2881ba0c065378d5d0fd30e9f58df4a22e1e2`  
		Last Modified: Fri, 26 Sep 2025 21:38:22 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:14e31a3baaa9c89047726fb514edbbcc22873d4fefb8005e44f195fab4767f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237512089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc89700f0acf3cd3ec5dc73dacaeb0fdf1eaee37e3d56bf57231e89440ff1d5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65924416454536dbbd82128b2d9bd35cab99bf268503d00ef3d8127edffe12a4`  
		Last Modified: Fri, 26 Sep 2025 20:10:44 GMT  
		Size: 134.7 MB (134724358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62f9cc9958d4de105c719c4ae3520419ed11cafbaf7bc97ebbf4d1b6e687b24`  
		Last Modified: Fri, 26 Sep 2025 19:22:16 GMT  
		Size: 73.0 MB (72953783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d586a8131adf540aad84e9a97025d220c83b96ae69475d5f4649088086f365d1`  
		Last Modified: Fri, 26 Sep 2025 19:22:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25509670864763f9435f3c3690e9a7929c3bda8415b16ebc61c8b5bdbd0251c9`  
		Last Modified: Fri, 26 Sep 2025 19:22:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5d5616fdd8af75aeff923ca98b77b1b496668d88cc4eae7d9a5d384aaea76c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed08a2c0f960d4a98603eca329a8b4700459512fea87ea4de040d7264b34b4de`

```dockerfile
```

-	Layers:
	-	`sha256:377636fdf4c83d384c0e5fac3d894aee82b44c4fc8fec90d83d02e02e6ee5f4f`  
		Last Modified: Fri, 26 Sep 2025 21:38:26 GMT  
		Size: 5.3 MB (5252037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e7341da86411eb7988d5111c02eca0989e9a413c51c6f4509482e92669aae7b`  
		Last Modified: Fri, 26 Sep 2025 21:38:27 GMT  
		Size: 15.9 KB (15854 bytes)  
		MIME: application/vnd.in-toto+json
