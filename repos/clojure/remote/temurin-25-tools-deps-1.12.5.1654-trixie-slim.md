## `clojure:temurin-25-tools-deps-1.12.5.1654-trixie-slim`

```console
$ docker pull clojure@sha256:748fe10ad601a56d142d3ec9dab50c3c9cbc00ebc45bd9befb3f39b3cc455690
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

### `clojure:temurin-25-tools-deps-1.12.5.1654-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:97c63f384ba40bbac501bca780f82d025c158b811a2c974de0f44f0d0cfa44e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191312732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11630eba0300d7e42da44ef40b6c9a744ef87d169ba254034fde54d1e5d0554c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:13:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:13:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:13:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:13:21 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:20:57 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:21:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:21:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:21:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:21:13 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:21:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85725b1a35dd5e3f16336928c1a1047acb11646928c9c69ed9656422172ada7d`  
		Last Modified: Fri, 19 Jun 2026 02:14:07 GMT  
		Size: 92.6 MB (92574597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fa13791ce4cc0225d90eb6af83192de605cb9b1425389b52170e3fb0b1e434`  
		Last Modified: Fri, 19 Jun 2026 02:21:30 GMT  
		Size: 69.0 MB (68951685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5662531144351d7e9406104763cd60976b9a5de3b40019981951027df23083`  
		Last Modified: Fri, 19 Jun 2026 02:21:27 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e552d742f4ae2d1a7c4441b67c9e598f17f0d0cdb6008bb0bf9ae26bb9e172`  
		Last Modified: Fri, 19 Jun 2026 02:21:27 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fc66e6aadfd6a4c3c4b2bd499e6aef43da2cb1ac8bad58f1db41dc43b67f6736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5241970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2169420d7c6f16473c8193811bd52110dc0577e52dc4a11c2db98989de0e967b`

```dockerfile
```

-	Layers:
	-	`sha256:a50d3a25dd64cee653bbbbe19a9190621845a3e5caa2ec33f44c19a88b8919c2`  
		Last Modified: Fri, 19 Jun 2026 02:21:27 GMT  
		Size: 5.2 MB (5225324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fa549fe6c92d1c302d999fc0e911c14abd44ea3f449d3961a36b0c7c50527c1`  
		Last Modified: Fri, 19 Jun 2026 02:21:27 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1654-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6bb1f322b18eada449527cf15692d83c773fde9b37188fb24bd08b0a1c0d5d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190469187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50d6f5b901aff9f66cf5985f44ebf2c9d142edcd47d876f5135187e3e393530`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:21:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:04 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:21:04 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:21:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:21:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:21:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:21:21 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:21:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48b5d20952573913e2443a72434f1bae821b17cf19ae811f1ee1c3051d0fdca`  
		Last Modified: Fri, 19 Jun 2026 02:21:42 GMT  
		Size: 91.5 MB (91542250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e84d560c90a7c0987a757bf78581a62a877b6eb24b3b63d1e55fd66df468478`  
		Last Modified: Fri, 19 Jun 2026 02:21:42 GMT  
		Size: 68.8 MB (68777368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77f95fb378c6a95745d607a315b1343e944adc168214feeda60efdfb8f3de9d`  
		Last Modified: Fri, 19 Jun 2026 02:21:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177936d1a8265c52e313b0b7be521bc17c72d5e3a2a3604e1e199cfb67101c84`  
		Last Modified: Fri, 19 Jun 2026 02:21:39 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:80de2aae96dea008c1a3f839e0f3d5a45fb4f1f5dab6870a44df2a8a5e7bc8ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f609279ba714a490451878809d26145ad40a865dce67f72dba421ce83596955`

```dockerfile
```

-	Layers:
	-	`sha256:b1f543f262d37b9ad07c6bbad625f1d13f206e94e2b264720fd57c90e8200f62`  
		Last Modified: Fri, 19 Jun 2026 02:21:39 GMT  
		Size: 5.2 MB (5231106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d83f9626daa67dafada6ed8f5c332e668bcbac29ff4a213c3711fc6122919ae5`  
		Last Modified: Fri, 19 Jun 2026 02:21:38 GMT  
		Size: 16.8 KB (16789 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1654-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e65010f9b7e1563a7f326f8b99560f66b0f6206b29d1678d3ca5a95f47207c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.9 MB (199889777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f4699f458ff98bb0d7ea42b23ca11b7d737bda557a78d606851aacde2b3980`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 00:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:06:39 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 17 Jun 2026 00:06:40 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:57:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:57:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:57:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:57:31 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:57:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d2e9d705b633c31ee18ff0b56f7ec3ad425fb9e720182ee7a6e0f18d85842b`  
		Last Modified: Wed, 17 Jun 2026 00:10:02 GMT  
		Size: 91.9 MB (91914009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f7f8fc02103f298476a67fa95e4222c16a9a40bc5bd802e8e4b8f15b6b0f31`  
		Last Modified: Fri, 19 Jun 2026 02:58:08 GMT  
		Size: 74.4 MB (74368382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d112ee26803c2e58af945a0271c643cac43bc6a5bd16f063a81b9215cd8c9c1`  
		Last Modified: Fri, 19 Jun 2026 02:58:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b7447312cd70d5277882aa6225f9aba8af66b0a71e62ba4edd9137b87b7a08`  
		Last Modified: Fri, 19 Jun 2026 02:58:05 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3e97ee93efa00ecf6c11dc7fdf7af2161015d327188bef75969b83ce77fac099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3284749fe82632d3a624f9ed4762b86abce1f1a6043ae94b225d46daa3bb1c`

```dockerfile
```

-	Layers:
	-	`sha256:d5c240f36f7878be52109cdcf7191115783bb4109bc7df07c906dd245bfe4f88`  
		Last Modified: Fri, 19 Jun 2026 02:58:06 GMT  
		Size: 5.2 MB (5213019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1737f21c33197aa93a179668b32f04ac8c64e5a75fea7f84333ab7b43524699a`  
		Last Modified: Fri, 19 Jun 2026 02:58:05 GMT  
		Size: 16.7 KB (16707 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1654-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b9a520d67c77eba5aecc70ba24350c1278a14b53a4cfabe99d7a89f3ec136b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188205203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb507d9956cfc395a51ec0ed9b8b96cb0bd63e4b34dedc343b46106cf101f7b2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:41:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:41:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:41:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:41:05 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:41:05 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:23:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:23:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:23:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:23:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:23:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e141af4c3ca44d66006c21b5229d05180427e764c0a36b8e43c72eabd028a0d`  
		Last Modified: Tue, 16 Jun 2026 23:42:49 GMT  
		Size: 88.4 MB (88420336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c4513063d37f3b0074d42b00c42929e24a598a8c3909e143280aa33ab70474`  
		Last Modified: Fri, 19 Jun 2026 02:23:35 GMT  
		Size: 69.9 MB (69932471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745ed9a5f6d2326fa46784d7faf7bf57ef7aabec3403a304b4a509635b1e8ec1`  
		Last Modified: Fri, 19 Jun 2026 02:23:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984fd04c767808881663c4a02e0f7656c5c919535605278c13c6eff980165fd5`  
		Last Modified: Fri, 19 Jun 2026 02:23:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4159983de2c07d0ce9e6c7863d38e6a3a84fc9006dddfa19388e8e886adb1a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b690c5a7792383ce31d19227d2385d80fd511a6ef81d93050b37ff506c81a18c`

```dockerfile
```

-	Layers:
	-	`sha256:6255fbdcc3aedeceb11dd1c3349ebc084465034798aee30259b89c5fffcfb6af`  
		Last Modified: Fri, 19 Jun 2026 02:23:33 GMT  
		Size: 5.2 MB (5205810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf864d715d6cbdb528fa0d457921faa6d0ff63bd8af1f7a5eb922d7e65c4e20e`  
		Last Modified: Fri, 19 Jun 2026 02:23:33 GMT  
		Size: 16.6 KB (16647 bytes)  
		MIME: application/vnd.in-toto+json
