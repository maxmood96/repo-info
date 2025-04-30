## `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:50298dd93e8010f51854f60c3222119805ef78dcccd962d2efe14eb20812a6e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:49707f7530a343105eeca64dae31d85fcc5451118d96d0edb3f99d41eada91c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179200552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f219ad71e45305d3257f39a66fcd64ca0bd090d0b9c411b2ff7b0438b2c590`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3dd57d60a71208a73266502927bf5c5e6b1deee6c8c3d8e33f4b17f16fe326`  
		Last Modified: Mon, 28 Apr 2025 22:08:18 GMT  
		Size: 90.0 MB (89951979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92239c9aef96950f55e192ae61c3d1977fded49f6727f7500270a1e634d2e5a1`  
		Last Modified: Mon, 28 Apr 2025 22:08:17 GMT  
		Size: 59.0 MB (58992930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0642cf9bb04fc74d447f51ff0f1cc5553ce7f24c6309ddf140e95dcc536a5b`  
		Last Modified: Mon, 28 Apr 2025 22:08:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ef2e640d87c9a033228e5ff4abb0f4970dc2b9861614846fccd52d8474c690`  
		Last Modified: Mon, 28 Apr 2025 22:08:16 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2c4439bc1f5e5f5ecb14a0892c69ccd36552de5ed9abf7c8912cd94f25ccf2d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5085585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe10f15985037dff7e6656f61a381eb67aef2bb1cb0f9ef7f91a5cbba95ff80`

```dockerfile
```

-	Layers:
	-	`sha256:0304d41a220b49bfeb870670c45b93f64afae40f893e0bc347a9c8771103e0e7`  
		Last Modified: Mon, 28 Apr 2025 22:08:16 GMT  
		Size: 5.1 MB (5069713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70a36b72e8ef0118f3c6821515758232e63b39cdf2d39755085fc490b7df8d5`  
		Last Modified: Mon, 28 Apr 2025 22:08:16 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3f6b08b9138ccc110274733d8cd09c6e4799323be7455f2f3ca2819bba1dbcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176964167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa11c6880ac47fd07335ec702a6d018b6cc12d7afc9402693ceccafb60c6b918`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af99c2ce0ba7c28d6ec5d791ae9e290374a008adadaef9c91928b11cc64c6f5`  
		Last Modified: Wed, 30 Apr 2025 01:51:53 GMT  
		Size: 89.1 MB (89091225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6022624aad591eba77575fa23bc17ab36387243af07139829cb6d9bb5ee8b`  
		Last Modified: Wed, 30 Apr 2025 01:51:50 GMT  
		Size: 59.1 MB (59127260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7931681adf1e9d075252c07ad9a041ba0e4eef82d3380eab6989be43ff54fef`  
		Last Modified: Wed, 30 Apr 2025 01:51:48 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0337406b70a500aecdb660ed921c4a1eea7c8c3adee4ae9b36a0712c8bdabe3`  
		Last Modified: Wed, 30 Apr 2025 01:51:47 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0d906ecd4719befb1f720734399bd7934446b5fe8d15532848fcd2efcd3f76aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5091431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64772b76b4950a001d0582bb115f07723b45b3c0639373600ed1c3e25a54ef19`

```dockerfile
```

-	Layers:
	-	`sha256:632ffc0ed1d17472083a09fda367d02b4c3828a9717a1140e18f5af8c86f179f`  
		Last Modified: Wed, 30 Apr 2025 01:51:48 GMT  
		Size: 5.1 MB (5075442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cb0e5b65199d059e8ca341bd808c28758ca2a0dbb34a75314cc20c154b78fe9`  
		Last Modified: Wed, 30 Apr 2025 01:51:47 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json
