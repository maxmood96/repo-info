## `clojure:temurin-8-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:7cf81b711dc8f5677b9099a0ac8dc7e7119723fb1bbcf7caeab4e33324b37b82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b31850d45130e76b3666883fdc2fe5c4a56491270d361afb3e5bf3819b86c527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156504747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b043db3420b415444dffc0d364c3e47fd2a798fe555c823e690d7c056bf376f5`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7213e46b58c31f8ee244733821fe2452a7348f8b16bc0f72c9a570c20cec45`  
		Last Modified: Tue, 30 Sep 2025 00:51:18 GMT  
		Size: 54.7 MB (54731348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e871c6a5c80bbdf207901c822706dbe13f5fc96ac880eb24b7bec67b281afc30`  
		Last Modified: Tue, 30 Sep 2025 00:51:19 GMT  
		Size: 72.0 MB (71994989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99ba25f2f50a8b50dc29af0ea90f8631dba845a65db9fddc3c3125b939231ae`  
		Last Modified: Tue, 30 Sep 2025 01:37:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cfbd1ffa678a6d7a05b9aa101d633d55dd7157708f7868387b636e8abcdaf4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfc1f4fe996962385ab4cdad1526fc712049c1b5c8e1ec4a519a277e171f273`

```dockerfile
```

-	Layers:
	-	`sha256:9be943523709957dd8b57055eea5593daac04bbf3d5b53840de565fa98bb5073`  
		Last Modified: Wed, 01 Oct 2025 15:45:02 GMT  
		Size: 5.4 MB (5377723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c78dda26c278c99c37d2d0a495b71419fa8c5866a026020bda36c5588762664c`  
		Last Modified: Wed, 01 Oct 2025 15:45:03 GMT  
		Size: 14.3 KB (14271 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; arm64 variant v8

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

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; ppc64le

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

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

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
