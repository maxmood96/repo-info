## `clojure:temurin-24-bullseye-slim`

```console
$ docker pull clojure@sha256:48ebf2aa16dadfe85cb049eae8dd4a9d681571f946cb3761813d7919afbf612e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-bullseye-slim` - linux; amd64

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

### `clojure:temurin-24-bullseye-slim` - unknown; unknown

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

### `clojure:temurin-24-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:27b2fb0a297a1385b218f12ec07706abc22000e0f1878559665b096d7ae29d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176969195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b372b83705cb58c4adeae3abc59310b782bf60724101a622b5ba4473776ee18c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae42a3f31dc9c598d7e1fc0cd9fe47899c924fb3f0b223d2f40875923c684595`  
		Last Modified: Wed, 23 Apr 2025 20:05:20 GMT  
		Size: 89.1 MB (89091273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a924e91792b0ed404105bd1b470a373bde4dea6d944a0a4cdf16dc4b64d2d26`  
		Last Modified: Wed, 23 Apr 2025 20:08:55 GMT  
		Size: 59.1 MB (59127376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8182f99db5662500163f4c02da14d6361ac588ab37a916e88475d466b64d23ef`  
		Last Modified: Wed, 23 Apr 2025 20:08:53 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48717f565f972a4468f3654bd3cefb15edff88303f45d5894989064f7edb20b7`  
		Last Modified: Wed, 23 Apr 2025 20:08:53 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ef199ca6896d55dfb5de45821a82e195a5f29b02e782d7cf4bd390381c0309b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5091378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338601f973403b0f42a46f33d9f8eae44f6f9d4301fdf45dee08488b62cce8e1`

```dockerfile
```

-	Layers:
	-	`sha256:8691fb81cef1edaf30933db65ad405b13d7583ef04ea39ef455de32b607b1db1`  
		Last Modified: Wed, 23 Apr 2025 20:08:53 GMT  
		Size: 5.1 MB (5075388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a8284c5282dcf9d847c0c0c095b37378e60c8e13e3f3faa12f470b0611d650`  
		Last Modified: Wed, 23 Apr 2025 20:08:53 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
