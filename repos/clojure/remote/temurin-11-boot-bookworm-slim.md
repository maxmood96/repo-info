## `clojure:temurin-11-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:3bcc5474afa91f554ae8b40e703881c6e65660fd3c2c28d4482de790ed4c61c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6c9544385498a0f4ee8fe3ba19871ea2234665b0adc514c2996ce7bc7468cb22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236721042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd1c4d098213d31ac6f79e2378bb7a1824641b114b4524b0a7ae556f14b83309`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:17:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 10:55:23 GMT
COPY dir:daac410d49a992b5ee309816020a7ba772f8c0edbe3557815c30b5c2d8f8820a in /opt/java/openjdk 
# Tue, 16 Apr 2024 10:55:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 10:55:25 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 16 Apr 2024 10:55:25 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 16 Apr 2024 10:55:25 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 10:55:32 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 16 Apr 2024 10:55:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Apr 2024 10:55:32 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 16 Apr 2024 10:55:51 GMT
RUN boot
# Tue, 16 Apr 2024 10:55:52 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b29a7abb3181bc51167c420779ff7be5838089d0b942bb6201d9e1826f471b`  
		Last Modified: Tue, 16 Apr 2024 11:17:05 GMT  
		Size: 145.3 MB (145270987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e49fc59166d0141c31b69ce20c50892d9767e7e22180d1fa6a57f8769cc566c`  
		Last Modified: Tue, 16 Apr 2024 11:16:54 GMT  
		Size: 3.5 MB (3498210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ece74a09f430dadd5249b98c18bd559aaeafec997e5d1a41ac69ff5b9b2b06a`  
		Last Modified: Tue, 16 Apr 2024 11:16:57 GMT  
		Size: 58.8 MB (58820487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8033f5294ed233cfd005e622537bd009cb16f105c0987b84ce4db50c0c7000d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233311144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3482f5953a25beff5cfe32f21426606444223a6fca53dbdfeacd0eab0b0ed1`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:38:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 06:33:11 GMT
COPY dir:337eb37873e2fe424b3d62c18ff2640cf50898156a884981e9e10924759441c3 in /opt/java/openjdk 
# Tue, 16 Apr 2024 06:33:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 06:33:15 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 16 Apr 2024 06:33:15 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 16 Apr 2024 06:33:15 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 06:33:20 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 16 Apr 2024 06:33:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Apr 2024 06:33:20 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 16 Apr 2024 06:33:38 GMT
RUN boot
# Tue, 16 Apr 2024 06:33:38 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf40e293c383aa322b6672363da730a85aaf0687fcd3e1c421634beaf9fd7e0`  
		Last Modified: Tue, 16 Apr 2024 06:52:31 GMT  
		Size: 142.0 MB (142006379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08e76fac1f4ccee2ed5edecc79b01ceccf0a838e24e5b601ad6f58544a609f6`  
		Last Modified: Tue, 16 Apr 2024 06:52:22 GMT  
		Size: 3.3 MB (3322180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fcf36069b2a6a5c9e80f0529bda7b0ba02bb5d6688464cb7d47506fb99beafe`  
		Last Modified: Tue, 16 Apr 2024 06:52:24 GMT  
		Size: 58.8 MB (58820428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
