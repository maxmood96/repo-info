## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:891486027dfa279d2164fbcc78a78ad0f79870212049cd2a5336b00c190fd5f6
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

### `clojure:temurin-21-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:04394da23735d6163770f3a65c836f18aaaf37825772dd7f1ce8a95fa454a42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256134920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed8f1213ab678d250cca8b7cc62ad580526f35948e3c2107c62eafaf150278e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:35:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:45 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:45 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:00 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b1287dfd3cc2b19078e31b56cdbf919024fb7b29a7a27df5b2a49725841ad5`  
		Last Modified: Thu, 14 May 2026 23:36:22 GMT  
		Size: 158.2 MB (158166943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb112e8278d378692ee44ae8524d5c00e8ccd1d04409fb4f3199d861f8866be`  
		Last Modified: Thu, 14 May 2026 23:36:20 GMT  
		Size: 69.7 MB (69730653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfce13090dd6ddcbd3d44f698be6878e165b9c2c0dd80f93a277ea5d175cac2`  
		Last Modified: Thu, 14 May 2026 23:36:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eec20c27a69dd64fcb029134850930ad2c5dd0720668839af5d37395058bb32`  
		Last Modified: Thu, 14 May 2026 23:36:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:392acf431ef485ec39e24d7695223d4dbd62f2d60f2d717b378e62c8bc226c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1934d8913a317c6e4484f8aa216e15e0874daf999090164507836b0382bff8`

```dockerfile
```

-	Layers:
	-	`sha256:f005d9dbd376c93125117690864806690d2d9d570d81ec0716732c90f760ace6`  
		Last Modified: Thu, 14 May 2026 23:36:17 GMT  
		Size: 5.1 MB (5118644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:359a611b10f5da7602460fb71e05b6e8615cd7b247793e50b264b687b42b3381`  
		Last Modified: Thu, 14 May 2026 23:36:17 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1c1c91033ab3986fc5ac449970635f490745d84b90a91b802646e04b56132b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254300749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb41c7a21094d0ff6b07a5a719ffdcea3c0d6a6fe1b17c971946f3b943a4ab12`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:35:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:45 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:45 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:00 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb89ff3622d228d55fe912a07462c8dae7e70c24d00e35d859e7f43fd04e4b4`  
		Last Modified: Thu, 14 May 2026 23:36:28 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b98912aa83096abb2acb08a25f6b46769afd96254630037a8b5cf558517ea7`  
		Last Modified: Thu, 14 May 2026 23:36:25 GMT  
		Size: 69.7 MB (69722218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfce13090dd6ddcbd3d44f698be6878e165b9c2c0dd80f93a277ea5d175cac2`  
		Last Modified: Thu, 14 May 2026 23:36:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eec20c27a69dd64fcb029134850930ad2c5dd0720668839af5d37395058bb32`  
		Last Modified: Thu, 14 May 2026 23:36:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f779ec07c534599b686b4875ff066dd7411c435af9923076b40e3cb76eac0d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac8b6d555e6c5b837963247caedff3349eef97e79f7bfec37f1cecbdc55255b`

```dockerfile
```

-	Layers:
	-	`sha256:12e72bce6097ac8f93d5fc22d7cd344abc14cb7b71b6777fa03c2e8767567bf8`  
		Last Modified: Thu, 14 May 2026 23:36:20 GMT  
		Size: 5.1 MB (5124405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e9b3dcc0d208434343a098e200823da0a2e43a6c6cd0e56a76f3d71e695dc35`  
		Last Modified: Thu, 14 May 2026 23:36:19 GMT  
		Size: 16.1 KB (16107 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7c2f5d025315e5858696c76213a9145a39ffcdb12315cfde743c412edb2dfaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.0 MB (265988653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d002b0e4d17985a4fd9747cc222d914d65a85dfecc9595040c910982da7d615`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:36:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:36:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:36:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:36:33 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:36:33 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:47:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:47:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:47:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:47:55 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:47:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa7fc9485b4fb59cd58fcb71fcd4db3dba936648eb297bdcd72a79d669b2338`  
		Last Modified: Sat, 09 May 2026 02:37:42 GMT  
		Size: 158.3 MB (158343237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c44edd62757f17e29070d14d9634a5d38651aff102bf470c2eb98027101a8d`  
		Last Modified: Thu, 14 May 2026 23:48:37 GMT  
		Size: 75.6 MB (75565921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f7f7e2abfb7af5e2a09dfa8e005241bfa4a9056fd0d70c3848be3ccab169c2`  
		Last Modified: Thu, 14 May 2026 23:48:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227a2d90ae980d791179b0e1b78aeabce501cc3f466843cfd317b3c7f321f415`  
		Last Modified: Thu, 14 May 2026 23:48:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1d94d483ad37d398ed55e8aba06f60b90dab41af332575208a679562135d328f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2efebccac7148b257690db91476da18940df6184c1445d6482e08874941a83`

```dockerfile
```

-	Layers:
	-	`sha256:c4e02e94310ded4155ce34562a351f0735565779ba7742d98def4565bfe6e289`  
		Last Modified: Thu, 14 May 2026 23:48:35 GMT  
		Size: 5.1 MB (5123802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f70ea5211d2550e4e8e66ad949fd4bc168f365eaedb30d201f4b2d507ed40add`  
		Last Modified: Thu, 14 May 2026 23:48:35 GMT  
		Size: 15.1 KB (15083 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:79c72aad1ab33e6e89ee41bc1a036323a4da0c4a964775625a1eeaccef45da74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242825107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270c2d24179be38bd3aadc707c5578398471c550377b32bd9d1d34e307d3b4a2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:35:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:43 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:43 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:35:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:35:56 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:35:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0809ac89c26156735efc3efef86a8d96aae2e4f1b2e41c915b45551d2d163af2`  
		Last Modified: Thu, 14 May 2026 23:36:24 GMT  
		Size: 147.4 MB (147388338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c146b521829bd4bd4fcf95179bcfeaeaff0759158a77fe274495af9c4ad2b790`  
		Last Modified: Thu, 14 May 2026 23:36:23 GMT  
		Size: 68.5 MB (68544122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d9636c55380224fbd44fd3d2a83c728f2e61496f7a3b2058ee97177da436a6`  
		Last Modified: Thu, 14 May 2026 23:36:21 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80727b32365b7a03e91110f7426d0ece3751d3cbf0d0fbcfd222a8d086c8dc0e`  
		Last Modified: Thu, 14 May 2026 23:36:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:55fd99f4c2c780bf3bf1d484f7fb5fe960eb62ec08964dbb185e991b0929fe6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec081a386ec863db80b0f2ce96e1fc74c5f75dc61897ee4eaacef98cd46afdd`

```dockerfile
```

-	Layers:
	-	`sha256:99bd95b3bbb5b001e4d08e3f5e2306b04bb22a55b9aad944ad723887e8998e68`  
		Last Modified: Thu, 14 May 2026 23:36:21 GMT  
		Size: 5.1 MB (5109965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76b70a46a134c50a3714c6e39d03e0f9f7acd14f3b448f847d6bfa9a9b463e9d`  
		Last Modified: Thu, 14 May 2026 23:36:21 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
