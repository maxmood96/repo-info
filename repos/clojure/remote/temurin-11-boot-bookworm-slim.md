## `clojure:temurin-11-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:89018b06cfef4b193168d331bb15cfa41e84844ff1654dfaec5963f4f9d1ee25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:71796fe444ed34701d4d89ee2bcd41ab13fd8c20950720a34de7203baccf7327
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236713763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feccb48d01da1e97a677388eadb33d3a17a28fa620975058e9e8a77b82a16994`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:11:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 06:17:30 GMT
COPY dir:9807503b62b5ec57f5790350ba2323b4402a31264d57970336b28a606d7a3a68 in /opt/java/openjdk 
# Tue, 12 Mar 2024 06:17:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 06:17:31 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 06:17:31 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 06:17:31 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 06:17:37 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 06:17:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 06:17:37 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 06:17:56 GMT
RUN boot
# Tue, 12 Mar 2024 06:17:56 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bd2ac3213922b6f0d900a8cbbfe1447fda071dc621133c9207761dcf773180`  
		Last Modified: Tue, 12 Mar 2024 06:37:41 GMT  
		Size: 145.3 MB (145271156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2f7ad5141080d6adaeb6a7aeb32ba8bcdd9627f3f38b038974e2dbe8e134fb`  
		Last Modified: Tue, 12 Mar 2024 06:37:30 GMT  
		Size: 3.5 MB (3498148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15723e81869cc8eb80ce2028789fecb9d3d6a92f94ef73819c9e74623f031d56`  
		Last Modified: Tue, 12 Mar 2024 06:37:33 GMT  
		Size: 58.8 MB (58820278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:639319686506266322470c596491d545f5bb124f1d2bc5e9b80e5269cf837d8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233307613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94255611d3d4fe154bb823d062dbac232c510649e1cdd916759755d96ada293`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:44:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 01:48:58 GMT
COPY dir:774c748cac67d918432726696917d770e1c557a90a62f56899a68f5b5861f304 in /opt/java/openjdk 
# Tue, 12 Mar 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 01:49:01 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 01:49:01 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 01:49:01 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 01:49:06 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 01:49:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 01:49:06 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 01:49:24 GMT
RUN boot
# Tue, 12 Mar 2024 01:49:24 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6040bd46f1e6585005f3d535c4dbe9fde45d2da23e3e11b657cf2ced2543d6c`  
		Last Modified: Tue, 12 Mar 2024 02:05:59 GMT  
		Size: 142.0 MB (142008486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2c080d25ffba1dd2859f2cd4673498e6fed1e78d4e341454d57a91b643ca8f`  
		Last Modified: Tue, 12 Mar 2024 02:05:51 GMT  
		Size: 3.3 MB (3322120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebc84a00bf12e70e69082c82a103fd4a4eb509af3a556f04dfe822b9197e1d1`  
		Last Modified: Tue, 12 Mar 2024 02:05:54 GMT  
		Size: 58.8 MB (58820573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
