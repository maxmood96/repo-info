## `clojure:temurin-26-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:95e21f7f53a35cc38e1facbee5dd06c80a09ce09063784bee3a0713584a2c758
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

### `clojure:temurin-26-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:76676e5b32c80df553c78bd3eb67afaf697ad4305f4eade1d5b8d54f009733ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189405696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f18cbf106cae8603a0b2b27a73d0245c811bda0f532fb89e797ba690afe066c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:22:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:22:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:22:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:22:08 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:22:08 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:22:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:22:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:22:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:22:22 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:22:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85440b9bd76784273379c7c59331d3a5568d6a6036fb49ec7c00bfda8f52888`  
		Last Modified: Thu, 11 Jun 2026 01:22:43 GMT  
		Size: 94.5 MB (94524373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245ecec0bbb1b459fd20d1955499c93eb4e27ab9faacb61c37488d0114db8777`  
		Last Modified: Thu, 11 Jun 2026 01:22:43 GMT  
		Size: 66.6 MB (66642658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8733fe9255633e5ad290f09a8b2b21f19d0d58329bd7a238dcd2716c06cc52`  
		Last Modified: Thu, 11 Jun 2026 01:22:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef87c003b455a76851ebe5b4db7f00889ec4f02bc7953a07c6834aa01ed53b69`  
		Last Modified: Thu, 11 Jun 2026 01:22:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eef36f1bc0f467a8f19b89dfe27d81773366281b735c252fc2ba037fa6b16b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e16d4f2a49838d15224aad17e1390a236542f5c85393ff8ecc0eea17ba7f58b`

```dockerfile
```

-	Layers:
	-	`sha256:ba2da9d5ec5cf2d7c41445101bd270c823ff372e247e9ba274f07c92c2ba96d3`  
		Last Modified: Thu, 11 Jun 2026 01:22:40 GMT  
		Size: 5.1 MB (5078890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bdf00dfa64d02a7894e980d02162d9693d0409daee592b0d9936c0aba81e98e`  
		Last Modified: Thu, 11 Jun 2026 01:22:40 GMT  
		Size: 16.0 KB (15982 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:85fd8a4536dc4d8d0c2ccdf2bde6cf0ae4657b263dc75c24f06ee489dc08c8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188270989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae47925e8ac27b48c1b09ec09504883a4b954630ddf1ba6223a36f0c523db9e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:26:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:26:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:26:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:26:19 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:26:19 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:26:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:26:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:26:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:26:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:26:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750786772ca2ccb838203dfa2fd668ba3d06c4db633eeb0f0321d2e02e3d6feb`  
		Last Modified: Thu, 11 Jun 2026 01:26:55 GMT  
		Size: 93.5 MB (93504348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dd974794d004aa3f8a97212155bde5b43171ac255927788b19cba6630c711c`  
		Last Modified: Thu, 11 Jun 2026 01:26:54 GMT  
		Size: 66.6 MB (66643294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45832af340b14486a2eddb50a3c7db4500b5fe46255451c94a7cf484e0fefeb`  
		Last Modified: Thu, 11 Jun 2026 01:26:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e569d8b5186845dd75404321ae7107288dbcc1efcea3284abafb362babc51a5`  
		Last Modified: Thu, 11 Jun 2026 01:26:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d860f5f0f5cb00e08b8cb39d9f748db0bf1b2828194bcd3f28c26e42f4e6fdbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce0719ec060685410d38aea5a6987cde40e7a096cc08e907f4f0177d28aed2a`

```dockerfile
```

-	Layers:
	-	`sha256:768f94da16a01d6fc4696a9adb6e18545c5ea203bb0c0790cc99e443b6981207`  
		Last Modified: Thu, 11 Jun 2026 01:26:51 GMT  
		Size: 5.1 MB (5084648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a1c100f1ed3de5cf81c92e6e50d50280f05eea8f113fc3d0d628bfa9c73a6b9`  
		Last Modified: Thu, 11 Jun 2026 01:26:50 GMT  
		Size: 16.1 KB (16101 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:bfbc71b92580bdd2fb211f622efcbff5b55d65e0b4dc6430696853aeb4a69c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198461360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c78b7bc4ae0383c20e93545bd9b56d40d02c3af1ae0ddb62be26b0842ca4ef3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 09:50:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:50:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:50:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:50:03 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 09:50:03 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:53:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 09:53:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 09:53:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 09:53:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 09:53:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f46f239b276d689990cc6b2bd012c161df5f6f63e0a47f8e010857cf9c83c4`  
		Last Modified: Thu, 11 Jun 2026 09:51:11 GMT  
		Size: 93.9 MB (93902055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9951bffe8cb5aa886919cbb4b780028beb0af678bc148c023fd75b605f2be3`  
		Last Modified: Thu, 11 Jun 2026 09:54:08 GMT  
		Size: 72.5 MB (72476323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c443e1dcd033f5609e2615de6ea854fa1a2c639bc7fa72ac470348ee8c5268bb`  
		Last Modified: Thu, 11 Jun 2026 09:54:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f933e661d1a6990fe819a3f6ad16a82817de52e46ba367e4dcb386f9e13e95af`  
		Last Modified: Thu, 11 Jun 2026 09:54:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:651fa1560ebd9b6050fb74177a92595b60ae8a707cc5a57278a5aac950d9b431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6785435288340e5ce10737e186dae840008ba233bd6756f851b7fe6f1544a2a`

```dockerfile
```

-	Layers:
	-	`sha256:1f38aed1832b45bcb8aed363726a2294070c7d9657234503b1529fb4620f4098`  
		Last Modified: Thu, 11 Jun 2026 09:54:07 GMT  
		Size: 5.1 MB (5067984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a624ec9e8a22f4789ad91332c55152de756db565871da0a6ab6bfe5d23515c9`  
		Last Modified: Thu, 11 Jun 2026 09:54:06 GMT  
		Size: 16.0 KB (16030 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:94a048246661f68dae064c33b1120699eae0b8a45c3687e288999d7fd250f5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182883546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45dfbe10bf5b1fdde6db5e867fc8b331c80b3433885557e6d00a1bea3f2d49cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 03:15:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:15:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:15:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:15:32 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 03:15:32 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:16:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 03:16:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 03:16:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:16:41 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:16:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c95e0687f25470aace14b514fbf30caeca0dadb23874709d13232572d3ce19c`  
		Last Modified: Thu, 11 Jun 2026 03:16:09 GMT  
		Size: 90.5 MB (90536949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e5a4cafff70925fdf8be96a1b010ca389e256e800ef26e954120c8ea4ea78d`  
		Last Modified: Thu, 11 Jun 2026 03:17:03 GMT  
		Size: 65.5 MB (65452052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79ed7e6097a82031962f92574d3d0bc3969611893c780960f26ba8c3b50d757`  
		Last Modified: Thu, 11 Jun 2026 03:17:02 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee45dde04773a751027a7df5ed3fbb24f45de1e459a90096152718ea115d7e2f`  
		Last Modified: Thu, 11 Jun 2026 03:17:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:38ce9bf591ae48bf58587bec8fba81e509bbc1f0a0caac482d9e8cc02120f39d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52a64aab2e1ea9ef3d47c1ff3fe7016a4015e76102d5355f7cfda2649de891b`

```dockerfile
```

-	Layers:
	-	`sha256:5e69612ef0230b4caf87b0bf03e43a78dcbfb933aa734e739fc4b858fb7a09e5`  
		Last Modified: Thu, 11 Jun 2026 03:17:02 GMT  
		Size: 5.1 MB (5055397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77721b631dbb80f77ae8a0aab411a839c6870d0477d30519a0d671e55b787f2`  
		Last Modified: Thu, 11 Jun 2026 03:17:02 GMT  
		Size: 16.0 KB (15983 bytes)  
		MIME: application/vnd.in-toto+json
