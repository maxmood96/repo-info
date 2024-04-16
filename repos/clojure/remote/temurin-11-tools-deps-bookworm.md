## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:a484fd27e0fd4711b67b167d47e74f94ba32caeaba0c67b6f33f8985633af066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f9642642db720e0c00714d32981c54be947aae8f863c176d82421953afd9c674
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275322659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97d97ea2bcee7c53a57d5534ee0152f5715a080389e3762c1675a66fabc2c3c`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:16:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:22:41 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:22:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:26:42 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 06:26:42 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 20:26:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -sLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 10 Apr 2024 20:26:26 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 20:26:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a514947677172b8fc44890310625cf6cc5b905b6756bd6f81147c12bf9d8653f`  
		Last Modified: Wed, 10 Apr 2024 06:42:18 GMT  
		Size: 145.3 MB (145271226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcadfc0cf8e6b401f83f0d705786502a18c833246ea579a6ece0418380c6f61`  
		Last Modified: Wed, 10 Apr 2024 20:43:50 GMT  
		Size: 80.5 MB (80490456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d150021a3bd955e39a449c022bba53c95b24f733ed7060a5c3e47253d3d85550`  
		Last Modified: Wed, 10 Apr 2024 20:43:38 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b8cb40e0ff5e154c4130001b4d1e9072612d0a0f103b4fdf561c0f34e2a2bc43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271858894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2e15f44344445b26fe8da55ab81c5afeca5743235a42d62033299b96064099`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:37:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 06:32:39 GMT
COPY dir:337eb37873e2fe424b3d62c18ff2640cf50898156a884981e9e10924759441c3 in /opt/java/openjdk 
# Tue, 16 Apr 2024 06:32:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 06:37:55 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 16 Apr 2024 06:37:55 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 06:38:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -sLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 16 Apr 2024 06:38:15 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 16 Apr 2024 06:38:15 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc51715a24a46140347f8e42a20868b5d5df2b6fc903958ad67dda303c34ee6`  
		Last Modified: Tue, 16 Apr 2024 06:52:13 GMT  
		Size: 142.0 MB (142006321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfcd2680f55df0a38e05c664a9668cd399429baaac31b6285599576b038a067`  
		Last Modified: Tue, 16 Apr 2024 06:54:46 GMT  
		Size: 80.3 MB (80255691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f090ca5fcd4c2119ef2bde09fd2e6f1495e185ca5f2aedc0b153d71ae462e570`  
		Last Modified: Tue, 16 Apr 2024 06:54:38 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
