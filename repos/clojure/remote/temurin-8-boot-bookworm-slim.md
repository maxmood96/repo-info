## `clojure:temurin-8-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:d75e4c04b61c6530d5ef552a0e80c71f0ef8618a9e7d3b225b5f4caa3b036699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c0e33a9885684d74bc8b310cfe0fcc0bba2943cced44e501139676b31836541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (195034682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7de0ce63d4c6987e0810f55a861452a8460b1ce08a6d4404051a847117e81f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:47:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:47:31 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:47:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:47:32 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 01:47:32 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 01:47:32 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:47:39 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 01:47:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 01:47:39 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 01:47:58 GMT
RUN boot
# Tue, 13 Feb 2024 01:47:58 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e1a9cbed5cc87e9380774cdf6c1211d2a3f6e261065440396d798b85e10c29`  
		Last Modified: Tue, 13 Feb 2024 02:09:40 GMT  
		Size: 103.6 MB (103591878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b8eba3750f982d6d856041374a351b737ba23e3867910aab409121368ca618`  
		Last Modified: Tue, 13 Feb 2024 02:09:33 GMT  
		Size: 3.5 MB (3498212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48995acffabb7d26d475d8e83aaad26fb0922fe4689bd4ad9c69fb2993bfa4c8`  
		Last Modified: Tue, 13 Feb 2024 02:09:35 GMT  
		Size: 58.8 MB (58820501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:995c2911cb127b6cd45ff5f1e0c23e4043378647d9da532580cc531aefb74bc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (194002150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8962b55e1288f6ae1f608154e0cb997deb29c4efdf33d5fee17c8b7f94a746`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:44:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 01:44:05 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Tue, 12 Mar 2024 01:44:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 01:44:08 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 01:44:08 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 01:44:08 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 01:44:13 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 01:44:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 01:44:13 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 01:44:32 GMT
RUN boot
# Tue, 12 Mar 2024 01:44:33 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1478a95520d8443b9ba68ce987b2b8e96b7506c41725158097bcb6d619dad9b8`  
		Last Modified: Tue, 12 Mar 2024 02:02:57 GMT  
		Size: 102.7 MB (102703056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1963a22ae94a777ee8b16e4da10e142d51b04ecb8e72201bbd42a9ed2509a4d5`  
		Last Modified: Tue, 12 Mar 2024 02:02:51 GMT  
		Size: 3.3 MB (3322128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d430ecf5ad724f56a1f709fd786a3f25d7ef8e672f836ae720a0c20aecbd760`  
		Last Modified: Tue, 12 Mar 2024 02:02:53 GMT  
		Size: 58.8 MB (58820532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
