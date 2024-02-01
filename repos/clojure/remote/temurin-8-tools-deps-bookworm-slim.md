## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:b6683ce35fff09024218d8168dfea96d1149803f2e7c6b6240c6fa0ba6aec869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:65b6c9878434681d743f314de5b07af2ca44071ce5d43a34c8b7ee6e7dbfcb23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201808376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2cb07bf513b2599b33418c7700660659ad69dd46713a4d47581032da28528b`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:43:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:43:27 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:43:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:47:18 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 31 Jan 2024 23:47:18 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:47:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 31 Jan 2024 23:47:37 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 31 Jan 2024 23:47:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8737523e74fd9c99538de2ca50cca6b04391d8a935a352206bd85358725e987e`  
		Last Modified: Thu, 01 Feb 2024 00:05:28 GMT  
		Size: 103.6 MB (103591879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0488edf2dd6e8066638c5b39280fb5d0beeade3315bbcb4f3c6218a4048007d2`  
		Last Modified: Thu, 01 Feb 2024 00:07:29 GMT  
		Size: 69.1 MB (69065415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6469147651a52197c3291703a0d3d7b853518ccb3bac11b232bb66c5586f9cfa`  
		Last Modified: Thu, 01 Feb 2024 00:07:21 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:332aa0a1a19aacf2e4d1f95acd8bc6d84261b0db1dbb34ec2c1a998bd734c8be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200704357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9334b83214851baf57947b7cfa250f2ba864917d1a87047da3839fa54df8795`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:20:06 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:20:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:23:30 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 01 Feb 2024 06:23:30 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:23:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 01 Feb 2024 06:23:47 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 01 Feb 2024 06:23:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ff00c3057caf77824dec5403166b179825f63e8162fb481183e1ae304bfe83`  
		Last Modified: Thu, 01 Feb 2024 06:39:20 GMT  
		Size: 102.7 MB (102703030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de243c5192dcb04bb5a4fbcbef18dba455e906eb3fc42e1dd4dbdc7f079ece8`  
		Last Modified: Thu, 01 Feb 2024 06:41:17 GMT  
		Size: 68.8 MB (68819879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca49e4aa8a9de8d94ee9c7591e4daf130b1340f37bae7fc96649ebf5236a892e`  
		Last Modified: Thu, 01 Feb 2024 06:41:02 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
