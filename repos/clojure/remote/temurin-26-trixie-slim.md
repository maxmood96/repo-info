## `clojure:temurin-26-trixie-slim`

```console
$ docker pull clojure@sha256:3064689c2f10138fd941ffd9e05c2d178ea7cb238454f2f9d83454bc8e852fe7
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

### `clojure:temurin-26-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dce4aabf21c4bc2b19798653883c8bfa5480947c26bbf290689c4d1952fd317a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193263383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30fe9d343950370aa8e329eef0632682888f8611d4bc53572bfd6e8402739c51`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:23:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:23:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:23:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:23:46 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:23:46 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:24:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:24:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:24:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:24:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:24:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7020f1ec83328676282492fa84979425fe5045628f627c3f2f17c7839eea59f1`  
		Last Modified: Wed, 24 Jun 2026 02:24:26 GMT  
		Size: 94.5 MB (94524362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85550bb1adfb95728d7219f6f95ab166a1217b96df5da75d710bd6065cea65f`  
		Last Modified: Wed, 24 Jun 2026 02:24:27 GMT  
		Size: 69.0 MB (68952559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7845a6e22af616b4efc45535c3283acfc84fe310550abd13189473c36040d12a`  
		Last Modified: Wed, 24 Jun 2026 02:24:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dda96327abd34b339cdf7eaf74020e6795c1c95e3c6610072f63bd30bb7e140`  
		Last Modified: Wed, 24 Jun 2026 02:24:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4019fe17fcb37e56ef6a042b7be54db593a073af00394e761eccce0fc8e69fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5238091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d10753ecbbb2f93e3b1821b4de93d91b3e9b0b36fbcd97b72ed068020b4ed3`

```dockerfile
```

-	Layers:
	-	`sha256:9d563f3e073e5a555213187d24ba559231409e4dbc1639ba397cb2f2a0d21b11`  
		Last Modified: Wed, 24 Jun 2026 02:24:23 GMT  
		Size: 5.2 MB (5222133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad6b7dad5ed744ddbe0825ddc00ad810968a53f83d59a5319e3ede7897b4e5c6`  
		Last Modified: Wed, 24 Jun 2026 02:24:22 GMT  
		Size: 16.0 KB (15958 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e5e914d3fb43988ad938e2c7a78a6f0019bc362f362eb95390b02f54c3a0dc38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192431194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3636ceadb47a25c32c756fe86c88dc622775854fee620b8a6f2409fb93f61b1b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:30:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:30:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:30:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:30:23 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:30:23 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:30:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:30:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:30:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:30:40 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:30:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e986244b4624a7bc15984b4cb76b25c96a1b45c9b6890477f413f5898bbe4d`  
		Last Modified: Wed, 24 Jun 2026 02:31:02 GMT  
		Size: 93.5 MB (93504323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22865c46f9e4197e746b90b8af4ff016b07b2cd38cf5a42c7ce478d96bfa81d5`  
		Last Modified: Wed, 24 Jun 2026 02:31:02 GMT  
		Size: 68.8 MB (68777280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2d724cb011cb450a9705f287ab53cde77c632605e4ff1c14d9ca7ef2769edd`  
		Last Modified: Wed, 24 Jun 2026 02:30:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe526643930a8b1de60eda30fc226f1425d1f5f311e559cf61d226e4daf42ce`  
		Last Modified: Wed, 24 Jun 2026 02:30:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e3a30e369520c89944393c65fda3874d82d306db0863f4e306bda8e5d84c3fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e6fc7d2e1fec72d23e13e59b0de7e51641e47561dff59f3a3829bccb515243`

```dockerfile
```

-	Layers:
	-	`sha256:92128200593754a3944966eaf544fe1301b9442a571b1b8cc7c80ae2024f02c4`  
		Last Modified: Wed, 24 Jun 2026 02:30:59 GMT  
		Size: 5.2 MB (5227891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54d225d3b593ecf1a4d713e2c2465d8dc143830a807e0aa2e108d18088a6168a`  
		Last Modified: Wed, 24 Jun 2026 02:30:58 GMT  
		Size: 16.1 KB (16075 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:711416d6d5e22465d205acc4bdfd8c685cf4918b4c267eeac1e6b5f3b3049437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 MB (201878710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a469f8ee7d772d9a3a22c56c06421e68d3ffc2944d5d3cf3441208a5bcf7b675`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 08:34:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 08:34:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 08:34:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 08:34:39 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 08:34:41 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 08:40:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 08:40:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 08:40:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 08:40:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 08:40:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb8abfa12b6427363309b1547420d955191530c07a3fd257bfff14f6647ed36`  
		Last Modified: Wed, 24 Jun 2026 08:38:02 GMT  
		Size: 93.9 MB (93902053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb26d74bf672e2d2b15f4d9d36e0a2f307327614061cbec8e21fbb8f2f5db0b`  
		Last Modified: Wed, 24 Jun 2026 08:40:49 GMT  
		Size: 74.4 MB (74369231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f1a05e8f0b7b7c9d5f1d75a0dde9ccb1e6906317350d8b62aa39b50264d8c1`  
		Last Modified: Wed, 24 Jun 2026 08:40:47 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c575c193ddf304aafc5fa8f2a12b6964e40bb4b256a8afbbbb6c33e00d4fd8ad`  
		Last Modified: Wed, 24 Jun 2026 08:40:47 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ab1c5675a000100c2acade36d130f0b4f751a0777180619099aa877baf0e1a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5226447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e9171bf9d9fd4bb05110fe80fae1f5179171645100bad1d41aece0b0b31876`

```dockerfile
```

-	Layers:
	-	`sha256:220c42a3f37bf408c4e308bc9f8ce7df4de53ab2a3934bd2adca9bf1f2d4e569`  
		Last Modified: Wed, 24 Jun 2026 08:40:47 GMT  
		Size: 5.2 MB (5210440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b841409c7aea82439763c9e80ad299872ac7ca9df48f2b2b46c20662b626bfd2`  
		Last Modified: Wed, 24 Jun 2026 08:40:47 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:67b505c59208b853bbfbf544ad8eff1b4870d2667b150923042b21e7c4d581f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190321357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad36dabae2f54ce10eed7d64ceec65602cb654d920dd86a2988eb2b5eed721b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 04:22:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:22:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:22:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:22:18 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 04:22:18 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:22:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 04:22:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 04:22:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:22:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:22:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ed18b3a4d85a66c1965e8c0e5e750300010d018b10e87fee4a72e22d4f1ff3`  
		Last Modified: Wed, 24 Jun 2026 04:23:02 GMT  
		Size: 90.5 MB (90536945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594f487fff352474b5c2d46f1cde777f3f27b72bfb12a852d8a301f5106f0344`  
		Last Modified: Wed, 24 Jun 2026 04:23:02 GMT  
		Size: 69.9 MB (69931991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8b96734f9bd9de158421e3969b3f9add95fbbc6b0ede4c9a17e71660705666`  
		Last Modified: Wed, 24 Jun 2026 04:23:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac6c54dd194bd2fcdb35066df2ca3e29bcf060177231afb639be2680dfa598a`  
		Last Modified: Wed, 24 Jun 2026 04:23:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c84bfdb3e7e6880440e3bf6478f63fd495cf89343c13fe21667911e639dfb8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e79bf40b592a34d1f48119dc11cc42e50f0dfad4c1d8aa739ae611e1da03b6`

```dockerfile
```

-	Layers:
	-	`sha256:e1957d25faabf39917a42b5e0bfdcf4d05ae38adf15b218f272c041dc6252b1b`  
		Last Modified: Wed, 24 Jun 2026 04:23:00 GMT  
		Size: 5.2 MB (5203243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5cbde770dcddf0d8383542b60407840a2037574556a0c86084caed135c37dda`  
		Last Modified: Wed, 24 Jun 2026 04:23:00 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json
