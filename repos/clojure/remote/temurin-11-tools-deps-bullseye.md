## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:2a6ea1811f1f1b7940df50b540db29092947ac0846bcb93b5c39684442be4aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:43132e6dd85fb0341abe3fc948c12865b912b2dd124fd37d452e8bb16d8617f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325398542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc1094fa78cda2cf2ec1e5147f7b9f18a0948580047e3356435c8239241353c`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:40:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 08:55:04 GMT
COPY dir:00b91555b346efd0ed206d19de82e3af67e3591603a223e1eef0aee2c231a058 in /opt/java/openjdk 
# Thu, 02 Mar 2023 08:55:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Mar 2023 19:23:27 GMT
ENV CLOJURE_VERSION=1.11.1.1252
# Tue, 07 Mar 2023 19:23:27 GMT
WORKDIR /tmp
# Tue, 07 Mar 2023 19:23:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "11a5997124d7469578a78f145e68fad6eccd32bf7086979f6abbf19739c85930 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 07 Mar 2023 19:23:47 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 07 Mar 2023 19:23:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5820d2bbbd2970cc90facbdcbef131608a5ed716d56ff1bba2614ecda317ebb4`  
		Last Modified: Thu, 02 Mar 2023 09:12:31 GMT  
		Size: 198.5 MB (198475399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c5eee2776aa05873c99a67808259b9cfde613c757410ac00676d06a81b4cb2`  
		Last Modified: Tue, 07 Mar 2023 19:34:07 GMT  
		Size: 71.9 MB (71876602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948d0f5aa5569df5c52ea29c1b684a3a3f0a14df4990d48db6064f95c701510f`  
		Last Modified: Tue, 07 Mar 2023 19:33:58 GMT  
		Size: 619.0 B  
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
