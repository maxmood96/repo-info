## `clojure:temurin-17-boot-bookworm`

```console
$ docker pull clojure@sha256:5d0807c9c297e74c9fb4b80423de3a2d51037841523fdaf6469b12400f9ff843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:add3cc78a3986fbfe8cf395efe44122affb90fb0aff139285ae6b036ed2fd0f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258783360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb48d7dfb8f4e901d985a8c9e5fe06e848acfab18df5381b7bae6fc201aad3d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:50:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 14:19:11 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Wed, 17 Jan 2024 14:19:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 14:19:13 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 17 Jan 2024 14:19:13 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 17 Jan 2024 14:19:13 GMT
WORKDIR /tmp
# Wed, 17 Jan 2024 14:19:20 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 17 Jan 2024 14:19:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jan 2024 14:19:20 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 17 Jan 2024 14:19:37 GMT
RUN boot
# Wed, 17 Jan 2024 14:19:38 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 17 Jan 2024 14:19:38 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jan 2024 14:19:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fb2be7fbd1da06270fc5c7003947acda7b897a595db4365d8679d8f9d6fb93`  
		Last Modified: Wed, 17 Jan 2024 14:56:30 GMT  
		Size: 144.9 MB (144873969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c370fa70f9e35505b117f32ac7fb2c981889ff78554cc69b5b81853c41badbd`  
		Last Modified: Wed, 17 Jan 2024 14:56:19 GMT  
		Size: 5.5 MB (5527091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed75fc4dcd8eb31ea8a8511ec571f7d45582ca6d3dfe7ab53d31caefee87a5dc`  
		Last Modified: Wed, 17 Jan 2024 14:56:21 GMT  
		Size: 58.8 MB (58820411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a35eacf8d083ef70e920512bc67054bd2d8421b13f316c016d9bae638275181`  
		Last Modified: Wed, 17 Jan 2024 14:56:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7b4341c2d32dd9837beca6613fc4c407ef597a4930ec7c6fa0dcc1fde3d72134
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257444007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47ffef6ccb0fc1ea66437858cfd407c4af616654924797598572a4e3b5ce02f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:57:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:28:11 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:28:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:28:14 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 17 Jan 2024 09:28:14 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 17 Jan 2024 09:28:14 GMT
WORKDIR /tmp
# Wed, 17 Jan 2024 09:28:20 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 17 Jan 2024 09:28:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jan 2024 09:28:20 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 17 Jan 2024 09:28:36 GMT
RUN boot
# Wed, 17 Jan 2024 09:28:36 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 17 Jan 2024 09:28:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jan 2024 09:28:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fdb9f64e633ba52485f6a7bcf54cf49d0e8c8410496a91e1b792abfebdb576a`  
		Last Modified: Wed, 17 Jan 2024 09:41:53 GMT  
		Size: 143.7 MB (143681767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52def539cdb57c94487412d83e9f7faf4b30ce9f31d602c50f5a0fa1e563546c`  
		Last Modified: Wed, 17 Jan 2024 09:41:44 GMT  
		Size: 5.3 MB (5349277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee31fc0a4b438d323d65a2b1a2e3c2940d700d779951754c717aac634c3743b1`  
		Last Modified: Wed, 17 Jan 2024 09:41:47 GMT  
		Size: 58.8 MB (58820315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0717150d76cf516e9f2b5e95cbcc951b058a952be26e2677d16e5ccf9c9ea12`  
		Last Modified: Wed, 17 Jan 2024 09:41:44 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
