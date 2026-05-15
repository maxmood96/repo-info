## `clojure:temurin-25-tools-deps-1.12.5.1645-bookworm-slim`

```console
$ docker pull clojure@sha256:b51845782ad1468985a218e79ea117e0cf742b550699f996ed8856778fead4d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.5.1645-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:47c939691cf989fbc94b8696f488917c340c495780b0563b9c17894546badbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190541774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e18ca0485912aa8bb46d9479fb738b8c9e6d02d083fee5d659511dcb9f8805b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:16:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:16:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:16:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:16:01 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:16:01 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:16:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:16:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:16:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:16:15 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:16:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb8432142ed7ace244c972b3a446d138c296b3199043980585163e45f59ac93`  
		Last Modified: Fri, 15 May 2026 20:16:36 GMT  
		Size: 92.6 MB (92574564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fedf62e709e2e5dec00989826008ee2d941f186872df1f16004962e2bdff6793`  
		Last Modified: Fri, 15 May 2026 20:16:36 GMT  
		Size: 69.7 MB (69729881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b357a329c0116312c376db9fc4f7901b5d707103ac24af78bcb63f0c4349cc1a`  
		Last Modified: Fri, 15 May 2026 20:16:33 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b8522ccc0f553cfe64044c47839bcb35a592ce6849908bb790dd5a3ab278b6`  
		Last Modified: Fri, 15 May 2026 20:16:33 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cc545418aa7f31949311e81e04610b857633209d3fb262a15aa804a33b78c916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5101561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e0f73c470c52499c8e656015c1562988710ef0b4d14d5d51259d4d717f8171`

```dockerfile
```

-	Layers:
	-	`sha256:8c86eb0f4926b2a1bdebe1ef6b77bf476b1ef71adfcfe1d1b9d94ad9e9bf3d04`  
		Last Modified: Fri, 15 May 2026 20:16:33 GMT  
		Size: 5.1 MB (5084882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee62ba8ca989e218da1957eaa88e0731a6626c5e66777bd2a567c125ce2d527d`  
		Last Modified: Fri, 15 May 2026 20:16:33 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1645-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:964de8e3a91838a41832dad9802daa8ec8a20e55b4470309e6a2b89a848b4cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189382269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9135c494ec9b02ea335e2ca743bed726849e5814bd2406d5730c90d9ba45ebe6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:16:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:16:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:16:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:16:03 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:16:03 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:16:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:16:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:16:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:16:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:16:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5a26e993f76775201b377e26c191181283038c24e57624c9158b8ec2dbf3a1`  
		Last Modified: Fri, 15 May 2026 20:16:39 GMT  
		Size: 91.5 MB (91542270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c271be1998dc190b6198b4e404ca287b55075efee0633da62225baef1be0c5`  
		Last Modified: Fri, 15 May 2026 20:16:39 GMT  
		Size: 69.7 MB (69722787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9632c345d42f8154b89320f094be4ac2626017ecc777bf30f4af5bda7df26f2d`  
		Last Modified: Fri, 15 May 2026 20:16:36 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fab3550e7390abab7bee0377509c59736d436bea0f7367433ea3da3d590f376`  
		Last Modified: Fri, 15 May 2026 20:16:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2d5a8eb58ffd5626ca91cfa2771ef0fc87e433da1d9061a2711e5a1aaead6e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5107485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6f117d6ea1ba84614b52415d11e2ebcbbf6afc6e5b43c649865184c4fd6f4b`

```dockerfile
```

-	Layers:
	-	`sha256:3c28f63a5dd4477aaf158fa18655d590e739e6392f6f982c76a3f5ba17e66ea4`  
		Last Modified: Fri, 15 May 2026 20:16:36 GMT  
		Size: 5.1 MB (5090664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f44bd2dd0940cda608eda4c6bb96ce5446690bf466caeecc299df3ffaace84c`  
		Last Modified: Fri, 15 May 2026 20:16:36 GMT  
		Size: 16.8 KB (16821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1645-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:cbb4b7daadfa0c462fc14cba0ddbfba5ecba6b1e8b66e09fd4669db3d629c44e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.6 MB (199558906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfa012dfd5fc8edcbaa198dfc20e83569c578525208d34e02e65cc766f96d54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:42:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:42:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:42:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:42:17 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:42:17 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:32:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:32:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:32:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:32:14 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:32:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2d1c7548cf004fea430b1528d91b72c7b0058d926919d1835a7b351081faec`  
		Last Modified: Sat, 09 May 2026 02:43:20 GMT  
		Size: 91.9 MB (91914029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef322e3a9c290183413fea60e33cc4a1da4745a950e58c8a325c55ec7434a724`  
		Last Modified: Fri, 15 May 2026 20:32:49 GMT  
		Size: 75.6 MB (75565378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ef33cbb31e1ac133c3fc1d1df7262907e43b66870dc2b1a74b77ef1c451547`  
		Last Modified: Fri, 15 May 2026 20:32:47 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cad7a6a304705352e1e244d6f39b14759681c631d122931f2129abc462ccd1`  
		Last Modified: Fri, 15 May 2026 20:32:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a89e656e9989aff1486b9f0081931662820da9385a6177cafed0509a2c6871b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5089149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36914c959b1e9b82efcb5629bc62d1b6999cc9e78d3c4a86cef88429280216d8`

```dockerfile
```

-	Layers:
	-	`sha256:0e30984ac041721ba8ce2b83e257233426909dcd9d83f48d16838ae84d6d878f`  
		Last Modified: Fri, 15 May 2026 20:32:47 GMT  
		Size: 5.1 MB (5073364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8616656158ad103b09e9b3a8246aeba60f470c0953f3b5fbbefb1a8805e1034f`  
		Last Modified: Fri, 15 May 2026 20:32:47 GMT  
		Size: 15.8 KB (15785 bytes)  
		MIME: application/vnd.in-toto+json
