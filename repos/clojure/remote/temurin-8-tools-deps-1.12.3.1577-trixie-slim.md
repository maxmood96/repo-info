## `clojure:temurin-8-tools-deps-1.12.3.1577-trixie-slim`

```console
$ docker pull clojure@sha256:62512f00a790222431cacc268b21375e9f4280eb784fbab5b6fe4eb11636271f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b4de929ed9b9d35db341999e83bc02c25501bf178288d1d569f70ef14a57e3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156500300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a3fe1cfcd8979d5b756075beb33942a9b78d4c64fce4236e174b1b58cc9dea`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ef26f8f37d30d8f5872327cb77125ef593604ff3cb7e6ccf0824c7bb6b1e89`  
		Last Modified: Fri, 26 Sep 2025 20:04:00 GMT  
		Size: 54.7 MB (54731292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd34c68c74cf88ceb48a68c80ddf15a91fa1dadeb3a3a347b3a833f0f391c31`  
		Last Modified: Fri, 26 Sep 2025 20:04:14 GMT  
		Size: 72.0 MB (71994868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf6260dc30387239691a8883453e6b7be4739e06aed93b8e48e716b53afc390`  
		Last Modified: Fri, 26 Sep 2025 18:44:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7c3ffdeac57673e56c34e69a570c3f8fa49b09ee6a8b18c15b74aa8deb6b69aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa96bd75f1c3a6b65bcdc53679e450d6135bb2ef358a629d52eace46e39e49d`

```dockerfile
```

-	Layers:
	-	`sha256:c233e81b5c9287931a17a2bca841c1b3409bb64dc71b96a5d7e46bdbd920d191`  
		Last Modified: Fri, 26 Sep 2025 18:48:09 GMT  
		Size: 5.4 MB (5377723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ab42399ec0a0e281fa99518a7f72cf3e913006a6ad88859ebc9a80dc919a0e8`  
		Last Modified: Fri, 26 Sep 2025 18:48:10 GMT  
		Size: 14.3 KB (14271 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:42888541d96d7e3127d313268608b12ba2f1609ef3ccda0623e3e39639975d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155781203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ce3251dd99cde27505dde53f040ca0141fd9d39687cde3bd658a164f0c7adb`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab8ae5703d0f794e6ee6047842a513c27486bc496feb3f085fd20606c0f2bb2`  
		Last Modified: Fri, 26 Sep 2025 20:03:54 GMT  
		Size: 53.8 MB (53835608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7a9b6760697f00563d169605c850feb394d4895f055c9da2cf555aa4c675bc`  
		Last Modified: Sat, 27 Sep 2025 00:22:47 GMT  
		Size: 71.8 MB (71808318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62c47bdbf53569bf0fe5502e1237af88512fd94fa0ba44863058f10876c8cab`  
		Last Modified: Fri, 26 Sep 2025 18:42:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b5981b13fe71836c2e511db23d27e7c9d6477a72ad4991de3df85b909e46c93e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba836088cb755a00997c7222d0223ed9e25fc9625515531d034a0ab7355a1275`

```dockerfile
```

-	Layers:
	-	`sha256:fc990cdd93e2fcff0dcb3206d949b7cac175599f11d4aca48b12f14f3d6ee803`  
		Last Modified: Fri, 26 Sep 2025 18:48:15 GMT  
		Size: 5.4 MB (5384190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b518894e5eba701fb8d29e6195d61250dabf637bfbb714c111f98aa2151f1d07`  
		Last Modified: Fri, 26 Sep 2025 18:48:15 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6319b31f6c510cd1e726b9b5ca3333b05189c70a34ccf2b21c4fbb5cbd0e5ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163156053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78187552b93c4de800bf785e761154baf976390aa80554718f479764386c7c06`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8eee8bce99a76d210e5226d05f1f223011095df9ceba3078d13e6a47ffdc8a`  
		Last Modified: Fri, 26 Sep 2025 18:02:34 GMT  
		Size: 52.2 MB (52165414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b6cdea36f88efffd44402d9e52dc2f8f885a4464932a8b9df7d85b71b69698`  
		Last Modified: Fri, 26 Sep 2025 18:02:37 GMT  
		Size: 77.4 MB (77395642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d20def3c9e1edeabde38cd8001b891f172314e43f72251b95b0a844bf79b127`  
		Last Modified: Fri, 26 Sep 2025 18:02:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:86faaa8bc7827dabffd17cee259f8a90b819344af0302dd968baa1942f01dcb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6bc66b1bee817376602de4eaa88c0a525e3737c6d520da87c1d84680e0f571b`

```dockerfile
```

-	Layers:
	-	`sha256:39fd155a082296beb5dac77d8f5e4e65de788c47df4c1771a395b06d16aaa998`  
		Last Modified: Fri, 26 Sep 2025 18:48:22 GMT  
		Size: 5.4 MB (5382687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70a41093ade855b56d84b4b0566d5627da16338abc396fecbe3da9f1c07ccad3`  
		Last Modified: Fri, 26 Sep 2025 18:48:23 GMT  
		Size: 14.3 KB (14319 bytes)  
		MIME: application/vnd.in-toto+json
