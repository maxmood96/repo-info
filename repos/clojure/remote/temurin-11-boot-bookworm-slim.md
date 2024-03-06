## `clojure:temurin-11-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:d230b2013a29c77aa1fe1c439297b0e3e3667aacb4976e47b9ad2e1235d58296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:adffb98c73dd88a7fffff0a837852333ed6a747671cb930abcc1a1da8c3071df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236713963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe5096587c56dda0b4a595696e8db6646e694f658783ce8ed69e65fafbe2201`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:47:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 14:02:05 GMT
COPY dir:9807503b62b5ec57f5790350ba2323b4402a31264d57970336b28a606d7a3a68 in /opt/java/openjdk 
# Wed, 06 Mar 2024 14:02:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:02:07 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 06 Mar 2024 14:02:07 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 14:02:07 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 14:02:14 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 06 Mar 2024 14:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 14:02:14 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 06 Mar 2024 14:02:33 GMT
RUN boot
# Wed, 06 Mar 2024 14:02:33 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d001d8a2900abfa74e3eea1ab01d3a896c3ba25736082483c2e900b34e2ad16`  
		Last Modified: Wed, 06 Mar 2024 14:23:15 GMT  
		Size: 145.3 MB (145271156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ab27a4ba672f08246e529dec5f73e6007a79e790a9b7520c1f02d04be3de8d`  
		Last Modified: Wed, 06 Mar 2024 14:23:04 GMT  
		Size: 3.5 MB (3498213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d799e0b5074df0c794b82894437b152f641eb167b0656a7bf473943b7d7527`  
		Last Modified: Wed, 06 Mar 2024 14:23:07 GMT  
		Size: 58.8 MB (58820503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ec94b5acfd0f07af3450c5bd128f5fb0d10a5c643f75698b2ce2d013e4595a7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233307366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e1fe4745103c8d0df910fe48ca21643ffc552e17f472835c8c222cc24e021c1`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 13:16:12 GMT
COPY dir:774c748cac67d918432726696917d770e1c557a90a62f56899a68f5b5861f304 in /opt/java/openjdk 
# Wed, 06 Mar 2024 13:16:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 13:16:16 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 06 Mar 2024 13:16:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 13:16:16 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 13:16:22 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 06 Mar 2024 13:16:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 13:16:22 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 06 Mar 2024 13:16:40 GMT
RUN boot
# Wed, 06 Mar 2024 13:16:41 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb60af30bdfa4757501b10b3144c73b97f2ae7d85ebcf327f64d9b6e809c371`  
		Last Modified: Wed, 06 Mar 2024 13:33:53 GMT  
		Size: 142.0 MB (142008469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5971418c1ba428a167619448264200b43f606754e06ad98691b9c071739707`  
		Last Modified: Wed, 06 Mar 2024 13:33:44 GMT  
		Size: 3.3 MB (3322153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b88a91ad022e2d7564bc3a569342d3ae45e602584768775a7d4886a0504f4a`  
		Last Modified: Wed, 06 Mar 2024 13:33:47 GMT  
		Size: 58.8 MB (58820381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
