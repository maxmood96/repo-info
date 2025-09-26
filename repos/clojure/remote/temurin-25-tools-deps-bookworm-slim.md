## `clojure:temurin-25-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:a45c91ab7cb25c9bf0444c6a08e03dc07c94807b870278ecaaf3ed6945ed8370
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

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3e035086cae8e5daff2270d195a51a53f8d74d29750834ef7bbd3f5095d8e93b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189945189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead03589f989424dbd5c11b0a6555739ba3cc492ef4819da8fd03b220ffed63b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d246c6ecba7e7b17904ff55b3aad6afe00355ee6dd20eb082a08c4765744e08`  
		Last Modified: Fri, 26 Sep 2025 17:58:38 GMT  
		Size: 92.0 MB (92036050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e38004bec71fcdb8aea9e9e9748206bb481d4429d01fcfbd022e1b5f839118`  
		Last Modified: Fri, 26 Sep 2025 17:59:14 GMT  
		Size: 69.7 MB (69679750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68290439035a7d4a1827b337315f9235cbdea432398f64df82e90d4c567ec7ef`  
		Last Modified: Fri, 26 Sep 2025 17:59:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d8c60a706ac8cca251b49e229b896c72ddf5906c37259920f622e351dc2fa2`  
		Last Modified: Fri, 26 Sep 2025 17:59:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1d86fe0690861c10cf312ab2a469cd63413eb8d6c9ee9ce973da05bb9ce933d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5081302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2f0eb56b130dae709571dd8fb3135410d6bd7ff35cd009b542e7d83ea5b78f`

```dockerfile
```

-	Layers:
	-	`sha256:cbddf580e875048c40cdc66b7e5425ac8b05ef347ceecd6d686e9fea4d8c9901`  
		Last Modified: Fri, 26 Sep 2025 18:43:51 GMT  
		Size: 5.1 MB (5064734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3630fc39d18118ccd5dd4041d04b8a10004274938a4d0a2bfa7f346bbe48bae2`  
		Last Modified: Fri, 26 Sep 2025 18:43:53 GMT  
		Size: 16.6 KB (16568 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8d440ebc7800603ad79a2f184b183abcf339ef943bdb9c92b3ce7d876b360147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188708740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51faed191f894862b9cbb53d387a0cecbb133ca131977a3840d12588fc7bf18`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff83642fc0e39cb2de1d8d00c18c68ec53df130ceb328fa420606579a0c4ab9`  
		Last Modified: Fri, 26 Sep 2025 17:57:14 GMT  
		Size: 91.0 MB (91045211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccc699e022ffa9dc4336f5ae314b346ffb0a2cda729918ab54bda6641ec2c36`  
		Last Modified: Fri, 26 Sep 2025 17:57:11 GMT  
		Size: 69.6 MB (69560389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed39e2b63e55cec6df901d81dca0ed77dbe3d85a315c02b92d62fcea09e08b5`  
		Last Modified: Fri, 26 Sep 2025 17:56:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7940f9ab0c6a8f30491247ecdf9a64f13cfd03ffcba3c0f5ebeb8010e854b5fc`  
		Last Modified: Fri, 26 Sep 2025 17:56:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:342800039f238b40ab95359f451b9e7d790548bdf7293af0012b41716b6d3277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eca09fa84026dd1767e68a408283a0a15b8f5aa28255a24df9d2ccac19b3638`

```dockerfile
```

-	Layers:
	-	`sha256:1dd7860307f63ac68f4dd21a3a6ac8ccef02c1a43f9fc4d461baa9a6c370c31a`  
		Last Modified: Fri, 26 Sep 2025 18:43:57 GMT  
		Size: 5.1 MB (5070516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a1fea63fbe386680c6b4613627de185cfaa6b8fa028db6b7429f129eec77133`  
		Last Modified: Fri, 26 Sep 2025 18:43:58 GMT  
		Size: 16.7 KB (16710 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4c1444369b5e5025e4580425c71c73bd026f40672fb0e09c4ba4df063ceb2fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199184591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855457bd30bbeae793e2b9d836732682fdaaf9382757363319940ee8805f1319`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
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
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b83e47ae3b30aa3093df4f180985fd1630fec818fba2e1374e2543b60a51eb6`  
		Last Modified: Fri, 26 Sep 2025 18:32:26 GMT  
		Size: 91.6 MB (91601769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e9eca38787315f3d8cb687bc0b480e2136d627194ff8ec2f57f4da22075c06`  
		Last Modified: Fri, 26 Sep 2025 18:39:26 GMT  
		Size: 75.5 MB (75513017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb78a70778d7473b55d0626588c8a4f7d3c8f678c019a6f0fba42a50f9b7b63`  
		Last Modified: Fri, 26 Sep 2025 19:27:01 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f42de89f5f1108eab67262eef2783b5ada1f46cc4ef8a977e4b1cd67a41dcf5`  
		Last Modified: Fri, 26 Sep 2025 19:27:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:589f86a47037b510c91b0c950f3fd451cf3ba862ee583cf40fe671cad819193b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b3133e8908ebaf9661cad95f18779e4f31b4410eeeff5f243cc334dd15301d`

```dockerfile
```

-	Layers:
	-	`sha256:f821f7937ba972c5c74a4f026e680c9b1b3e506a591233e2bd5a2984b97f8a6a`  
		Last Modified: Fri, 26 Sep 2025 21:41:01 GMT  
		Size: 5.1 MB (5071202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fd2d34596215635c853e1ace9355ada5164c249a8ac887d57340ce5b8587042`  
		Last Modified: Fri, 26 Sep 2025 21:41:02 GMT  
		Size: 16.6 KB (16628 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c3de06b1dc4b555dfc6056ddcbe0d232d2b3a530ae78afde042493d07cb24cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183582678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0448cb3f47bbc22ab3ed206d89b140ee462627df8c1edd6ced6ccecc0335320e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4c7e89dfc58d6fc774dcdb3927087c39099f262dac15887ad857932541ea64`  
		Last Modified: Fri, 26 Sep 2025 19:32:11 GMT  
		Size: 88.2 MB (88206458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ff8397e8a9aa5590fc0b1fb469c490dacbfc72d97dd27d94f1e1645d4a9bda`  
		Last Modified: Fri, 26 Sep 2025 19:39:08 GMT  
		Size: 68.5 MB (68490881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faac05d3bd2a16cf8e91447ce1dcb0217352f565a5be14d7d98809e0910fe5cb`  
		Last Modified: Fri, 26 Sep 2025 19:39:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa1060fffb9abda9c835d24bc641f1ceeea0d9d06c9a701b89d13316c36f5e6`  
		Last Modified: Fri, 26 Sep 2025 19:39:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:51dfd2c53dad9f96c71c525a00e6f934e6a3e91d61f0d685ce2fcd49c7b248ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5075171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675e8d19e3f37e30a92a604237e5fe783876bb00df9c48c10276bf7a9faf672e`

```dockerfile
```

-	Layers:
	-	`sha256:ac99a267935a4a58e492a1590aada418c18b9699ff84351592aacb1a54d93321`  
		Last Modified: Fri, 26 Sep 2025 21:41:07 GMT  
		Size: 5.1 MB (5058603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da25b3360dacb5f2fb489816cfb401e15c0242f947ee527a7e0c6682058dd860`  
		Last Modified: Fri, 26 Sep 2025 21:41:07 GMT  
		Size: 16.6 KB (16568 bytes)  
		MIME: application/vnd.in-toto+json
