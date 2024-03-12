## `clojure:temurin-8-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:443ad78cd1092159ad4eea9f7b41fb97714a56c3d505eb2ed1c8b8d8cdeeeff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c4720a9e0fcfbad38f53515d13714d0a74bb75d4fe8092b975018c3b2ccbd8b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (195034825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df6ddddbddde0aec90e749d5ec0573b8a1ea13fa9edf80ed1763db92350c01f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:11:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 06:11:46 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Tue, 12 Mar 2024 06:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 06:11:46 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 06:11:46 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 06:11:47 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 06:11:53 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 06:11:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 06:11:53 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 06:12:11 GMT
RUN boot
# Tue, 12 Mar 2024 06:12:12 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc526a18274cf01347cef30f1479f1386c5497903e9e5e6981c0654ecd3310b`  
		Last Modified: Tue, 12 Mar 2024 06:34:36 GMT  
		Size: 103.6 MB (103591911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70373079b52befe10510c74b73daf749a363705acc6c579af52c5dbb7f6c1a76`  
		Last Modified: Tue, 12 Mar 2024 06:34:28 GMT  
		Size: 3.5 MB (3498142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8375a42f9d0f8b9a7527624b42799290f94d261ace35fc419e39cc190e917e16`  
		Last Modified: Tue, 12 Mar 2024 06:34:31 GMT  
		Size: 58.8 MB (58820591 bytes)  
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
