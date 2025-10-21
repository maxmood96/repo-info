## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:d618dc98999385c25a6ddf970536ef2571cbb2e8faa79254baa13b3b622d8246
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:682c9b2a3b3f4447bc5f8a2e8bdae830c115845a332054a0eb852969e81eeaaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152639787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2d3c404cb27a4264db1ad284fa2a1889acb2891534e28cce06133e164d2c55`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01f063824211661c0980be2f3025e7ba5abc389fd2f82b88fbe19877b26054c`  
		Last Modified: Tue, 21 Oct 2025 02:19:26 GMT  
		Size: 54.7 MB (54731351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5fc031b549ff14d0366b1b7ecd1746194b354108fa455d950327b7e51a4dcd`  
		Last Modified: Tue, 21 Oct 2025 02:19:25 GMT  
		Size: 69.7 MB (69679470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cc7dc9e86aa8fbdf50eb0e24d7584447562b10464677a3475e66450683ffd2`  
		Last Modified: Tue, 21 Oct 2025 02:19:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ab3cdb7117066e86185b303de9c3cfde177ff26f356a78838c7a66fec4c8cce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34f39d72268c184f4ceaed4783f82b6eccf3db67640b7e94a23819596a71156`

```dockerfile
```

-	Layers:
	-	`sha256:5bb2b202c0d495f97b3e4d943f8909a596b4a00286ad7cee76f493a13264ea7a`  
		Last Modified: Tue, 21 Oct 2025 09:46:13 GMT  
		Size: 5.2 MB (5234998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2f587525181ed0cab995724c23368f693e1afa6407a895589a02a60533c1e50`  
		Last Modified: Tue, 21 Oct 2025 09:46:14 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6a2d1ac97acbed9eb7d74141d8560ea35bdeb1c71238d6392124149fc8169a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151498872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c45f21ee14dcef7806583f17c73e3484ecbc295f44876c5538def5ac2f73a0`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b12bb59174b2fee7db245192ca74f5f9969fb384476f8acfb3c4ce59447ace`  
		Last Modified: Tue, 21 Oct 2025 02:24:32 GMT  
		Size: 53.8 MB (53835606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55096f4754a81bc4c433ae82ad5cf0dd6b77681954e63386b8b763e487ff730f`  
		Last Modified: Tue, 21 Oct 2025 02:24:55 GMT  
		Size: 69.6 MB (69560430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8912c69c1b8815882273787855b15b46a0153c57bc815fb5943d825609897cec`  
		Last Modified: Tue, 21 Oct 2025 02:24:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:caa54407152b437d5ab45459d932442dbb6461c67f6e5b12a88e31650561d20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ac8a98043c5a61c622249cd5efb4e791c4acb30550957342c834421025c56f`

```dockerfile
```

-	Layers:
	-	`sha256:7e250d58f7271738700179dc0d073e6ed032093bc7d6960368ec1218437a0978`  
		Last Modified: Tue, 21 Oct 2025 09:46:19 GMT  
		Size: 5.2 MB (5241457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e427f5e6aa26eacc81d43fdaec0d83ac1d172fd36e0befb00e553bbd077c3522`  
		Last Modified: Tue, 21 Oct 2025 09:46:20 GMT  
		Size: 13.6 KB (13609 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:22c3837338c95617ec1bc39cfb648924de17babcd30232e16eb561ff4f1e60af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159747432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c646621a43240d6d51e67fa481e7bc8842e438daeca45b4c45e77f84e63f8e5c`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
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
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4808b36faa8f51beaeed0fb85c1eb939ecd3b64b53ab9d96dd338710855719`  
		Last Modified: Fri, 10 Oct 2025 04:43:21 GMT  
		Size: 52.2 MB (52165456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d79c8b67448cd151c1713b590879b817aae9839797f59b343232e0897fe1085`  
		Last Modified: Fri, 10 Oct 2025 04:50:36 GMT  
		Size: 75.5 MB (75512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d64460c01bfcac62d6bb3dbfea275fc6344fde0665158e7fc26c7437a079f6`  
		Last Modified: Fri, 10 Oct 2025 04:50:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ecdc0394ff5cc6f958d10651ce2443f405c287f86dd3234c01dccbee44deea5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be05a028f2ccaf99ba7d11a531b927cb741147db0fd7e825d78615deb0780977`

```dockerfile
```

-	Layers:
	-	`sha256:387f93e3f63ce5ff22d871c6b9f8d46a01f80f20595fa099005139083709f230`  
		Last Modified: Fri, 10 Oct 2025 06:50:16 GMT  
		Size: 5.2 MB (5240749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a72bc6799b3d8002bec9c65dd0aa9e9e29562e133e47503f34e281e9020218a3`  
		Last Modified: Fri, 10 Oct 2025 06:50:17 GMT  
		Size: 14.3 KB (14338 bytes)  
		MIME: application/vnd.in-toto+json
