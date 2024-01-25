## `clojure:temurin-11-boot-bookworm`

```console
$ docker pull clojure@sha256:e953f2666613408780e1c6e1cd91510c041c2de19513df7720d0252d44ea1cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ccd81e147f59f2947a52efa81db20f12480ab8332caaae4699e18d2a7d8af1f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259179893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6048c12e36b88a839cca0289aa52244645c804ae9bb94f4da8c4737d74accc7e`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:50:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:08:57 GMT
COPY dir:e1ce96bca1c423a1c79b84eacb7ae69429353a37485cc24af4161ce4b9d3ee2a in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:08:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:08:58 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:08:58 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:08:58 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:09:05 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:09:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:09:05 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:09:23 GMT
RUN boot
# Wed, 24 Jan 2024 22:09:24 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb609733abdc20b4793d9c8bf11ee18e8754538a4c9ae52c203b68523b414a72`  
		Last Modified: Wed, 24 Jan 2024 22:36:48 GMT  
		Size: 145.3 MB (145270942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bc533c03beb5bb08c6e173c0263903abe354b71f15a83a633a3c0c61d5fa4a`  
		Last Modified: Wed, 24 Jan 2024 22:36:37 GMT  
		Size: 5.5 MB (5527003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040221669621db5335d932a5826e1d20a3ae54a40c47d7db346328eab28d6827`  
		Last Modified: Wed, 24 Jan 2024 22:36:39 GMT  
		Size: 58.8 MB (58820458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:14f89f44920b4f11a60b8ff87df13b458b9a522358a5a213fda03b59870fe0ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255768352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18099949cdee374b007018522b1d8099d179d4674b6019b0c6f672ba1369d616`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:57:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:14:18 GMT
COPY dir:454699b64b949edd3264b234e72a891ace37d538f2726c5ec754e17e6fb3fb19 in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:14:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:14:21 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:14:21 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:14:21 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:14:27 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:14:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:14:27 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:14:42 GMT
RUN boot
# Wed, 24 Jan 2024 22:14:43 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec5047588aad160e7dc5c6e44a35baeeed650fc3f5e788618cd10cc64259a62`  
		Last Modified: Wed, 24 Jan 2024 22:36:40 GMT  
		Size: 142.0 MB (142006514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484f8265c768de70032a64bc12dea3030d49709863c6e910fedd85ad55d66277`  
		Last Modified: Wed, 24 Jan 2024 22:36:32 GMT  
		Size: 5.3 MB (5349334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200d921ad00a3380a6974ecbd3c901d26682b6bc629becd970c90a2392cc333d`  
		Last Modified: Wed, 24 Jan 2024 22:36:34 GMT  
		Size: 58.8 MB (58820257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
