## `clojure:temurin-11-tools-deps-1.11.1.1435-bullseye`

```console
$ docker pull clojure@sha256:e841c36d7487c6ee266eb51ffcf4e4f25c8a92e95b1b93bc8f1fdf39315e2eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1435-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1e51e98e8c1e18b77dcc50c51d2386ad75276247edffd8c56d1ebfe6b38952e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269621454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1c860d8edc728e0bbb904dd6e7704ce5ec1b576a2c7533af704e2b53bd67ea`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:20:10 GMT
COPY dir:27feef64ab9493a1c978ebf5ca0dc5d8ce2aa9d0441a77081243d3ab0f99637d in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:22:37 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:22:37 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:22:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 21:22:54 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:22:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb84145e720ef12c948dfb02c9cce9a91b0f285a5139c63fb5df70da7603db33`  
		Last Modified: Wed, 24 Apr 2024 21:44:35 GMT  
		Size: 145.5 MB (145504683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32190255ad6981f2e298ac59ba6bc5b1fe526b3b3a9308e8b24a9e6e86285ab`  
		Last Modified: Wed, 24 Apr 2024 21:46:27 GMT  
		Size: 69.0 MB (69017285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c6777cc995e83245e9d3a8705dcf2665bb7727ba66314f1c685ffdc1a86f20`  
		Last Modified: Wed, 24 Apr 2024 21:46:19 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1435-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:300ae0c063d45794455c6bdb6acff539cd35930eb73eebe0cea734ad786b2ce6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265186950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c725ac364638d4e922bd29b37a43ba284c0770e7e3fd73f460f2a0625e7cb7f0`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:05:23 GMT
COPY dir:ed1d7b3eb6412a67cc5fb5f9ef1702ecc8bb34e5c226d446c2bffff7a9d8d2bc in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:05:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:07:28 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 19:07:28 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:07:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 19:07:44 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 19:07:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c103559d9a51b5c973652ab0b7b7056114129f4061944495b13f05cd0ed1ec`  
		Last Modified: Wed, 24 Apr 2024 19:25:24 GMT  
		Size: 142.3 MB (142304379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a838a9762414f3e4b467bd2762ac966f91d509f58d3892c28dfb2b89fde0de`  
		Last Modified: Wed, 24 Apr 2024 19:27:01 GMT  
		Size: 69.1 MB (69141996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13b84a6d5749a7febee89896ca8c7d8eb42a0431def2cfd3ee9572b0f83ff20`  
		Last Modified: Wed, 24 Apr 2024 19:26:53 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
