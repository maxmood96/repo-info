## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:aab6990328a59de256d9d4120de5185b82b4ee0d766d4f03700d9ab6cd1877a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a14d4d311791c1f8810495c19a34f12562ba53af7a998ff47ba0cf8cae410bc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196497711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f8e770e3948de4f7f4ec84acae86a632b17163e9ded948fe7d9c268c55dbd0`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:22:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Sep 2023 07:22:28 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Wed, 20 Sep 2023 07:22:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 07:24:24 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 20 Sep 2023 07:24:24 GMT
WORKDIR /tmp
# Wed, 20 Sep 2023 07:24:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 20 Sep 2023 07:24:42 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 20 Sep 2023 07:24:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d904e0e0acb14ab36621cdb61a83d87d553b53cafbe8016f9cc443e19e4ff9`  
		Last Modified: Wed, 20 Sep 2023 07:34:08 GMT  
		Size: 103.6 MB (103585017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4bb7ab43cf32720b3672dd5631d80ae79272d05876404f0486731d496ca1022`  
		Last Modified: Wed, 20 Sep 2023 07:35:10 GMT  
		Size: 61.5 MB (61494368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0db60a640e717ca1157366aecffa15ef0c5b75a2335d8536427249de21df1f6`  
		Last Modified: Wed, 20 Sep 2023 07:35:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e490f62ce566025bb38dc6698d34ef4a6cff8342d67e661e8d746b983fa1a0c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194365452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc9925f8ae0f307ad81d9b817f4bdf4ee8b1baf225efced90c3c7e99af4df94`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:46:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 09:04:32 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Thu, 07 Sep 2023 09:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:06:13 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 07 Sep 2023 09:06:13 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 09:06:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 07 Sep 2023 09:06:28 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 07 Sep 2023 09:06:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256b28be577c49d6f216cda63c69699c76582076b787ffcf77067af08f7f0490`  
		Last Modified: Thu, 07 Sep 2023 09:14:43 GMT  
		Size: 102.7 MB (102690458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb3a33a58e30da3508a2d7506b9d37cfeb39efc5830a85810a310cb44303a8d`  
		Last Modified: Thu, 07 Sep 2023 09:15:39 GMT  
		Size: 61.6 MB (61611473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0aba609b3327ef8e58f1274d14c17e67994c01058c8fb68165e1186b054532b`  
		Last Modified: Thu, 07 Sep 2023 09:15:33 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
