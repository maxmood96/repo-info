## `clojure:temurin-8-tools-deps-1.11.1.1224-bullseye`

```console
$ docker pull clojure@sha256:36def9b3a4ae90263228c3252a456c81ba2ee327779957353377450474633eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-1.11.1.1224-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ca63c47b2a1afa08675a13acd284e6f126110f3ec17c37dd5d6279e862ed00a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181560274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4b832c8d098e33f515483ef4891f8faa552aff1f735434ea332fee588ee164`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:40:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 07:40:43 GMT
COPY dir:bbb84183d7ea38d81d8401f01e29d08935ee4c8bf6f90c6527579a1554c3bde1 in /opt/java/openjdk 
# Wed, 01 Mar 2023 07:40:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 07:42:50 GMT
ENV CLOJURE_VERSION=1.11.1.1224
# Wed, 01 Mar 2023 07:42:50 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 07:43:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3bbab4d253eda43e3122fd5705014a69c44944a6dee8ea4d7d567afe157eb4ef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 01 Mar 2023 07:43:08 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 01 Mar 2023 07:43:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c09a39e83163f7497d4ee9341a8db18267bc11c708c7befcd6e06c90de109bf`  
		Last Modified: Wed, 01 Mar 2023 07:55:03 GMT  
		Size: 54.6 MB (54635557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b981886f0fb16de49db6f11eb248fd8cc49f65ed13cc14b05e68a1817d191c2`  
		Last Modified: Wed, 01 Mar 2023 07:55:59 GMT  
		Size: 71.9 MB (71878177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4e4f94b5b6fc94db3afc41ec24638a34780d934f2d34cd7f7ee0f649b3942e`  
		Last Modified: Wed, 01 Mar 2023 07:55:51 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-1.11.1.1224-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6445584831a6e7ee455b55a6162dd7b62ebc9c2b19a6e6c03e2f96ecad625cd6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179421690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff3d1fc6f1969cf6c15a39143ea60b21bf723145ea92bf16352a0966bef7946`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:01:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:01:16 GMT
COPY dir:b6d7e5613532d986930216de9e0fece0632e82564ce7a6a98baf63b4115f840d in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:01:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:03:18 GMT
ENV CLOJURE_VERSION=1.11.1.1224
# Wed, 01 Mar 2023 03:03:18 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:03:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3bbab4d253eda43e3122fd5705014a69c44944a6dee8ea4d7d567afe157eb4ef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 01 Mar 2023 03:03:35 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 01 Mar 2023 03:03:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b583ae59cedb3d06068194d612b2461bcf03fea5f1f8704c8a9987f693705b0a`  
		Last Modified: Wed, 01 Mar 2023 03:14:07 GMT  
		Size: 53.7 MB (53727940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec3536a31749f943adf55a09a8bea0a2b6b586042e120610eb1126af82ac563`  
		Last Modified: Wed, 01 Mar 2023 03:14:59 GMT  
		Size: 72.0 MB (71989918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2cb234876e9262f9e72889024a8eff06228fe5909bcac5a1dc2480653fdf096`  
		Last Modified: Wed, 01 Mar 2023 03:14:52 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
