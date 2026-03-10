## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:9d6e3de28b7fe9c305ebf4b1b4ee977f8c7ba4bd877a38c879abd52996df6d43
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0ab1bf9b81f1829a12b2efdf67fa3e4eb508429bccbdfff579919b7a00da791f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235249410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662dca42e93e7b136eb3e8f77760630a0e766a232cd28fdddc9a3b23112e9ba3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 20:34:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:34:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:34:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:34:34 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:34:34 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4564d838c9f299200e8bc2f5e979f2f55032e5e644fda24982af6441f3c9eec9`  
		Last Modified: Mon, 09 Mar 2026 20:35:10 GMT  
		Size: 145.8 MB (145806697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e5f0864c30bcfc6ed48cabd6ba8aea657cf781a506e544c3a967de55d1ae2e`  
		Last Modified: Mon, 09 Mar 2026 20:35:08 GMT  
		Size: 59.2 MB (59183688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75f89f0af0e414d6bb8ec55acbd2e7fcfdc0ff04951f9ce39b30ae8f2897301`  
		Last Modified: Mon, 09 Mar 2026 20:35:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8b205acc9f2bf5d7e874a79dfe18f400e7e76b42a2a5853ae6598a580727193b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf1a180912fb8def22f6e4f0b4c6a9519ddff40f3b53bc78287db0871887f0b`

```dockerfile
```

-	Layers:
	-	`sha256:46321c3cff8fa5dea9c8c3eef1b4754f5b1718186c5c6db4e9697ebc0f6e4e29`  
		Last Modified: Mon, 09 Mar 2026 20:35:06 GMT  
		Size: 5.3 MB (5341818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee214b00ee8eeaefd24adc8285ea6823a6d20ab049f2518bb8810f493c59289`  
		Last Modified: Mon, 09 Mar 2026 20:35:06 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9d44345b0a959b2b1b1614aa31fcee20a82220352d68c09f6c004b160744e3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230570025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870c78d4a52f3e4fc0323d7de12fbabbaa0bc075d9acc12a919ffb9bb8cecbe5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 20:34:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:34:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:34:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:34:20 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:34:20 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687d5e7aec5ec88ed5013221039cedc831f5e4fcf7c2dd77bc9657f9bb40b3dc`  
		Last Modified: Mon, 09 Mar 2026 20:34:58 GMT  
		Size: 142.5 MB (142501446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877430678233055efb63d17bd8482083771276ebf2dec4d8665cfc1000438a83`  
		Last Modified: Mon, 09 Mar 2026 20:34:55 GMT  
		Size: 59.3 MB (59323463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876ecc1c3839e3f891fd107a11b4c10b6394a5ec51233961ec1b0e13c2e979d5`  
		Last Modified: Mon, 09 Mar 2026 20:34:51 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e980b336545f5ebedf8aae23f6b19a3505ccf6410afae81254906b3e013e3d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5362553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4473732242488a09a2de1244a8fd5c9da28743caf27005b82be1ba63aa21eac6`

```dockerfile
```

-	Layers:
	-	`sha256:19048f415ee82a604ede793ecd92931d3455f27d9a309888e201c3f44d6fcf5a`  
		Last Modified: Mon, 09 Mar 2026 20:34:51 GMT  
		Size: 5.3 MB (5348168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5154496661dc3f1c0eed91e65edfecb81be372e8420a86344763f814bf3a5b8`  
		Last Modified: Mon, 09 Mar 2026 20:34:51 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
