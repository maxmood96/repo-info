## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:6f3a7873ddb57f04a3041aa80601a2a4f59446590adfe0181edb671dead61d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3eab501b2043b50377ae9a9cef72280639c1d73731155e216b8a12e487d4a967
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325399012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c38eda3ccb2333da23eb697aedbe41301d376c05995280c46b685740bc3a097`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:40:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:33:47 GMT
COPY dir:e649a995635d4b28f1458e8ccc09f5f71440b52479cfda5ea11e99ab14d0ce82 in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:37:23 GMT
ENV CLOJURE_VERSION=1.11.1.1252
# Thu, 16 Mar 2023 07:37:23 GMT
WORKDIR /tmp
# Thu, 16 Mar 2023 07:37:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "11a5997124d7469578a78f145e68fad6eccd32bf7086979f6abbf19739c85930 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 16 Mar 2023 07:37:46 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 16 Mar 2023 07:37:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2dcd1e2bf77431590203ffdf654085ce8aca2e30f82f7499367035ec790dab`  
		Last Modified: Thu, 16 Mar 2023 07:50:28 GMT  
		Size: 198.5 MB (198476007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53cf3e46588b86519cd55a7c793735a41a53f41b4c05de8949c823e3968737a`  
		Last Modified: Thu, 16 Mar 2023 07:52:11 GMT  
		Size: 71.9 MB (71876463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05858a6af89c2b97b20461ff294bc735a00258971ed91105c1b2059033f1ab97`  
		Last Modified: Thu, 16 Mar 2023 07:52:03 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7ec5198526609f30caa2c91d8027fde3c6fee8c25d58d674234ee6e34aa45f71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320934109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09dafca66a1b27512792a01c6ba46dbfa87529bd8d3a4b16b75243d2af3467d8`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:01:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:49:40 GMT
COPY dir:d446509417048b798354227404c222c2c6031477a91cb1b64eded33f5e598adf in /opt/java/openjdk 
# Thu, 16 Mar 2023 04:49:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 04:52:49 GMT
ENV CLOJURE_VERSION=1.11.1.1252
# Thu, 16 Mar 2023 04:52:49 GMT
WORKDIR /tmp
# Thu, 16 Mar 2023 04:53:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "11a5997124d7469578a78f145e68fad6eccd32bf7086979f6abbf19739c85930 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 16 Mar 2023 04:53:10 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 16 Mar 2023 04:53:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78a05cee032288c91b44a6ea7c2e0389feb35b08ef573e2bd5677647987ef0b`  
		Last Modified: Thu, 16 Mar 2023 05:04:28 GMT  
		Size: 195.2 MB (195242536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e12146b177bc9e22e750438602ea54368d4f09dba7dfa98a23aa6644dfc7c4e`  
		Last Modified: Thu, 16 Mar 2023 05:06:29 GMT  
		Size: 72.0 MB (71987739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ff0ef8b117ddbe05bd07c34ac4cfb7fba97c6d405cadb701d1656429fa907a`  
		Last Modified: Thu, 16 Mar 2023 05:06:23 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
